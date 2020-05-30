# 基于HUGO的博客平台搭建

## 下载HUGO
 [点击下载HUGO](https://github.com/gohugoio/hugo/releases)
将HUGO 添加到path,并 ``` hugo version  ``` 测试hugo是否安装好.

 ##  设置位置
    hugo new site xxx.github.io-creator 

## 进入目录
    cd  xxx.github.io-creator 

## 创建心得仓库
    git init

##  下载主题链接
    git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke 

## 将主题追加到config.toml
    echo 'theme = "ananke"' >> config.toml 

##  进入config.toml
``` 
baseURL = "http://example.org/"  
languageCode = "zh-Hans" 
title = "Jumpawaltz"
theme = "ananke"  
```
## 建立.gitifnore 文件
    /public/  不提交public以外的文件

## 编辑你的第一篇博客了
     hugo new posts/my-first-post.md 

```
title: "开博大吉"
date: 2020-05-30T19:15:13+08:00
draft: false  //是否为草稿.false不是
```

## 生成静态页面
    hugo server -D 

## 打开GitHub 
创建 xxx.github.io 的仓库

点击settings

找到GitHubPages选择 masterbranch    

## 提交到GitHub 
    git add .
    git commit -v 
    git push

# 最后你已经有了你的第一博客啦!