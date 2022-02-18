# VS Code Only Web

## run

```sh
yarn
yarn watch
yarn watch-web
```

运行`scripts\code-web.bat` 或 `scripts\code-web.sh`

## debug

- 代码变动`Ctrl+Shift+B`编译
- vscode中运行调试选择`VS Code Server (Web,Chrome)`
- 点击运行（F5）

## 修改

- 移除右下角通知
- 移除左下角错误警告
- 移除account按钮
- 移除setting按钮
- 移除source control
- 移除debug
- 移除extension
- 移除terminal
- 移除内建语言支持js,css等
- 移除dockercompose（extensions修改yaml的package.json）

- `build\lib\builtInExtensions.js`删除内建扩展

## 问题

- 如何打包自己部署？引用？
- 后台服务可能没有清理干净
- 只是删除功能，依赖还不清晰

- <https://github.com/microsoft/vscode/issues/136361>
- <https://github.com/microsoft/vscode/pull/139725>

## 备注

- npm-run-all用于并行运行多个任务
- bat启动web版，内建扩展加载：bat > @vscode/test-web > extensions.js(scanBuiltinExtensions)
