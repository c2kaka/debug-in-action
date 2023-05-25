# 如何通过 vscode 调试 NestJS 项目

## 配置 launch.json

### 1.nest-cli + vscode debugger

- 使用 nest-cli 的 nest start --debug
- 用 vscode 的 debug 选项卡启动项目

```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "attach",
      "name": "Attach",
      "skipFiles": ["<node_internals>/**"],
      "port": 9229
    }
  ]
}
```

### 2. 只使用 vscode debugger

- 用 vscode 的 debug 选项卡启动项目

```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "debug nest",
      "runtimeExecutable": "nest",
      "args": ["start", "--watch"],
      "skipFiles": ["<node_internals>/**"],
      "console": "integratedTerminal"
    }
  ]
}
```
