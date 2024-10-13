---
title: git 用法
date: 2024-10-13T00:18:35.626Z
---



### 1. git init 
初始化git仓库

### 2. 新建readme
git add README.md

### 3. 提交更改
git commit -m "第一次更新"

### 4. 增加要上传的git 仓库

git remote add xxxxxx.project

### 5. 上传到git 仓库
git push -u origin master


### 6. 举个例子
echo "# git-test" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/xxxx/git-test.git
git push -u origin main


### 6.2 远程 clone
…or push an existing repository from the command line
git remote add origin https://github.com/datafu/git-test.git
git branch -M main
git push -u origin main

## 2. 协同开发常见流程


### 2.1  克隆项目
git clone https://github.com/xxx/project.git

### 2.2 创建分支
git checkout -b feature/you-feature


### 2.3 定期提交分支
git add  . 
git commit -m "添加新功能"

### 2.4 同步远程仓库
git push xxxx  feature/your-feature
