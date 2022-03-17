---
title: 用Hexo和GitHub仓库搭建一个基础的个人博客
categories: 
- Hexo基础博客创建
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