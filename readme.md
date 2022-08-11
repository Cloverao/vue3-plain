**pnpm-workspace.yaml：**定义工作空间的根目录，可以设置排除目录

pakages: //声明说有的包都在 packages 目录下面

shamefully-hoist=true//禁止依赖提升

-w workspace-root

-rf node_modules//删除 node_modules 目录
touch ts.config.js

node_modules 里面 vue 里面内容很少，把所有公共的模块放到.pnpm 目录下面
怎么引用.pnpm 里面的某个模块？
解决：使用.npmrc 配置 shamefully-hoist = true，把幽灵依赖重新安装到 node_modules 下面
minimist:命令行解析工具

```
     "buildOptions": {
    "name": "VueReactivity",
    "formats": [
    "global",//在全局中使用
      "cjs",//只在node中使用
      "esm-bundler"
    ]
  }
```

- 命令行初始化 typescript 配置文件

```
    pnpm tsc --init
```
