# 如何搭建最简单的 vuepress 站点

## 依赖环境

1. [Node](https://nodejs.org/en/)，如果你需要版本管理，可以通过[nvm](https://github.com/nvm-sh/nvm)、[nvm-windows](https://github.com/coreybutler/nvm-windows)引导安装node。这里有[nvm教程](https://zhuanlan.zhihu.com/p/47977487)、[nvm-windows教程](https://www.jianshu.com/p/d0e0935b150a)
2. 如果你不喜欢npm，可以安装[yarn](https://classic.yarnpkg.com/zh-Hans/)，安装体验更好

## 创建项目

新建一个blog目录，按照下面的目录结构创建文件。

```
├─docs                  // 基础目录
| ├─.vuepress           // vuepress配置目录
| | └─config.js         // 基本配置
| └─README.md           // 主页内容
└─package.json          // 项目配置
```

::: tip 提示
/开头表示当前目录下的绝对路径
:::

/docs/.vuepress/config.js

```js
module.exports = {
  title: '网站的标题，头部导航' // 如果不配置，无法返回主页
}
```

/package.json

```json
{
  "scripts": {
    "docs:dev": "vuepress dev docs",  // 调试
    "docs:build": "vuepress build docs" // 构建
  },
  "devDependencies": {
    "vuepress": "^1.5.4"
  }
}
```

/README.md

```
Hello VuePress
```

创建之后，运行`npm run docs:dev`，浏览器访问`http://localhost:8080`就可以看到`Hello VuePress`
