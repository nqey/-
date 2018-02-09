# 抄自阮一峰大神[博客](http://www.ruanyifeng.com/blog/2015/12/git-cheat-sheet.html)
## 常用命令图
![常用命令](http://www.ruanyifeng.com/blogimg/asset/2015/bg2015120901.png)
## 专用名词
* Workspace：工作区
* Index / Stage：暂存区
* Repository：仓库区（或本地仓库）
* Remote：远程仓库
## 新建代码库
* git init
  > 在当前目录新建一个Git代码库
* git init [project-name]
  > 新建一个目录，将其初始化为Git代码库
* git clone [url]
  > 下载一个项目和它的整个代码历史
## 配置
* git config --list
  > 显示当前的Git配置
* git config -e [--global]
  > 编辑Git配置文件
* git config [--global] user.name "[name]"
* git config [--global] user.email "[email address]"
  > 设置提交代码时的用户信息
## 增加/删除文件
* git add [file1] [file2] ...
  > 添加指定文件到暂存区
* git add [dir]
  > 添加指定目录到暂存区，包括子目录
* git add .
  > 添加当前目录的所有文件到暂存区
* git add -p
  > 添加每个变化前，都会要求确认    
  > 对于同一个文件的多处变化，可以实现分次提交
* git rm [file1] [file2] ...
  > 删除工作区文件，并且将这次删除放入暂存区
* git rm --cached [file]
  > 停止追踪指定文件，但该文件会保留在工作区
* git mv [file-original] [file-renamed]
  > 改名文件，并且将这个改名放入暂存区
## 代码提交
