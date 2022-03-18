---
title: 用Hexo和GitHub仓库搭建一个基础的个人博客
date: 2022-3-1 10:22:00
categories: 
- 教程
tags: 
- Hexo
- 博客
- GitHub
---



# 第一步 安装软件
## Node.js
1. 检查版本：
```
node -v
npm -v
```
2. 切换国内镜像源：
```
npm install -g cnpm --registry=https://registry.npm.taobao.org
```
3. 检查镜像源：
```
cnpm
```
4. 安装hexo：
```
cnpm install -g hexo-cli
```
5. 检查hexo：
```
hexo -v
```

---

# 第二步 建立博客
1. 创建一个目录作为博客根目录，进入该目录下
2. 用hexo生成博客：
```
hexo init
```
3. 生成博客：
```
hexo g
```
4. 启动博客：
```
hexo s
```
5. 访问：
```
localhost:4000
```
6. 新建文章：
```
hexo n "file_name"
```

---

# 第三步 将博客部署到Github
1. 在GitHub上新建一个仓库，命名一定为：`username.github.io`
2. 进入博客根目录
3. 安装插件：
```
npm isntall hexo-deployer-git --save
```
4. 修改_config.yml（deploy中）：
```
type: git
repo: repository address
branch: master
```
5. 部署到远端：
```
hexo d
```

---

# 至此我们完成了最基础的hexo博客搭建

# 将博客源文件上传至GitHub实现远程同步管理
1. 将根目录以及主题根目录（如`themes/next`）下的隐藏文件`.git`删除，否则主题文件无法上传
2. 上传本地博客项目
```
git init
git remote add origin 仓库地址
git checkout -b hexo
git add .
git commit -m ""
git push -u origin hexo
```

# 其他设备上clone远端GitHub分支文件到本地
```
git clone -b hexo 仓库地址
```

# 本地环境搭建及调试运行
```
npm install hexo --no-optional
hexo clean && hexo g && hexo s
```

# 同步项目文件到GitHub
```
git add .
git commit -m ""
// 先拉原来 GitHub 分支上的源文件到本地，进行合并
// 分支名后面的“--allow-unrelated-histories”是为了弹出“fatal: refusing to merge unrelated histories.”的错误
git pull origin hexo --allow-unrelated-histories
// 比较解决前后版本冲突后，push 源文件到 GitHub 的分支
git push origin hexo
```
