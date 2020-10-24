## 最快部署博客

你可能会想用阿里云申请一个域名，一台ECS服务器，然后备案。但是，这个流程很长。

我们还是用最快的方式，只需要你有Github账号。网上有很多教程，这里有一个[相对全面的教程](https://zhuanlan.zhihu.com/p/28321740)。

核心的步骤是：

1. 创建名为yourname.github.io的仓库
2. 构建vuepress站点，将dist目录内容推送到仓库

VuePress也提供了[Github部署说明](https://vuepress.vuejs.org/zh/guide/deploy.html#github-pages)。

需要适配的是git推送部分，尤其需要注意

```sh
# 生成静态文件
npm run docs:build

# 进入生成的文件夹
cd docs/.vuepress/dist

# 如果是发布到自定义域名
# echo 'www.example.com' > CNAME

git init
git add -A
git commit -m 'deploy'

# 如果发布到 https://<USERNAME>.github.io
# 重要
# 重要
# 重要
git push -f --set-upstream https://github.com/cecilpeng/cecilpeng.github.io.git master

# 如果发布到 https://<USERNAME>.github.io/<REPO>
# git push -f git@github.com:<USERNAME>/<REPO>.git master:gh-pages
```

然后，在package.json中增加一个新的脚本deploy

```json
{
  "scripts": {
    "docs:dev": "vuepress dev docs",
    "docs:build": "vuepress build docs",
    "deploy": "bash deploy.sh" // 对于windows用户，可以将deploy.sh转换为bat执行，或者使用node运行sh脚本
  },
  "devDependencies": {
    "vuepress": "^1.5.4"
  }
}
```

那么，我们以后就可以直接运行`npm run deploy`完成部署，在浏览器里访问`https://cecilpeng.github.io`。

