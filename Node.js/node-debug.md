# 调试 Node.js

## 1. 使用 node-inspector

```bash
node --inspect-brk index.js
```

## 2. 使用 VSCode

launch.json:

```json
{
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Node.js",
      "type": "node",
      "request": "launch",
      "program": "${workspaceFolder}/index.js",
      "cwd": "${workspaceFolder}",
      "runtimeExecutable": "node",
      "runtimeArgs": ["--inspect-brk"],
      "port": 9229
    }
  ]
}
```
