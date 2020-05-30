# GitHub的使用技巧
## 首先让git和GitHub建立连接
```
 ssh-keygen -t rsa -b 4096 -c 邮箱地址
```
## 返回密匙和公钥 粘贴到GitHub 填入
测试配对成功 ```  ssh -t git@github.com ```
## 就可上传和下载了
```
git remote add origin git@xxxx
git push -u origin master
```
## 如何上传其他分支
```
git push origin x:x

git checkout x
git push =u orifin x
```

## 下载别人代码
```
git clone git# xxxx[目标路径]

git clone git@xxx.git yyy
将文件下载到yyy目录里记得 cd yyy

git clon git@xxx.git .
使用当前目录容纳代码和.git,最好时空目录
```

## 上传到两个远程仓库
```
git remote add repo2 git@xxx
git push -u repo2 master
```

## git pull 冲突了怎么办呢
* 发现冲突
使用```git status -sh``` 查看哪些文件冲突 
* 解决冲突 依次打开文件,搜索===== 删除不用的代码,直到没有冲突
 

## git 高级操作
使用bash alias 简化命令
```
touch ~/.bashrc
echo 'alias ga="git add"'>> ~/.bashrc
echo 'alias gc="git commit -v"'>> ~/.bashrc
echo 'alias gl="git pull"'>> ~/.bashrc
echo 'alias gp="git push"'>> ~/.bashrc
echo 'alias gco="git checkout"'>> ~/.bashrc
echo 'alias gst="git status -sb"'>> ~/.bashrc
然后重启命令行,运行```cource ~/.bashrc```
```
## 好看的glog
在~/.bashrc 的最后一行添加
```
alias glog="git log --graph --
pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s
%Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
-- | less"
```
## 美化历史命令
```
git rebase -i xxx
```

## git 隐藏文件
```
git stash //隐藏文件
git stash pop  //显示隐藏文件
```