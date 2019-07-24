# learn_git
分享git 在epark

## git 操作指南

[git简易使用指南](https://www.bootcss.com/p/git-guide/)
## 平时遇到的问题？

#### 怎么修改 每次commit后的authorName?
`git config --global user.name 'yourName'`
`git config --global user.email 'yourEmail@xx.com'`

#### 本地仓库怎么关联远端仓库? (远端创建的仓库有readme.md 文件)?

`git pull origin master --allow--unrelated-histories`

#### 生产环境有个bug需要及时处理，怎么新建分支处理？

    1. `git checkout -b yyh`
    2. `修改bug`
    3. `合并分支`
    
#### 查看某段代码是谁的?

`git blame <fileName>`

#### 忽略某个文件的改动？
    
* 关闭 track 指定文件的改动，也就是 Git 将不会在记录这个文件的改动

    `git update-index --assume-unchanged path/to/file` 
* 恢复 track 指定文件的改动

    `git update-index --no-assume-unchanged path/to/file`

#### 存储当前的修改，但不用提交 commit？

    1. `git stash`  
    2. `git checkout master`
    3. `git checkout -b issue110`
    4. `回到当前分支`
    5. `git stash list` `git stash apply` `git stash drop`

#### git 彩蛋

    `git commit -m :dog:`
    
    `git commit -m :dog: test`
    

#### git 清除远端已经删除的分支

 * git branch -a 查看本地和远端所有分支 (git branch -r 查看远端分支) 发现远端分支还存在
 * git remote show origin 可以查看remote地址、远端分支和本地分支对应的关系
 * 使用 git remote prune origin 命令就删除了那些远端已经不存在的分支

  
#### 赵凯强教学  2019年6月13日

```
use "git checkout -- <file>..." to discard changes in working directory 本地撤回
use "git add <file>..." to update what will be committed 本地提交
git add -u 提交本地所有的更改到工作台
git status 查看本体工作状态 是否有改变
use "git reset HEAD <file>..." to unstage 从工作台撤回到本地
git commit -m "test" 从工作台提交到暂存区
git push origin master  从本地仓库提交到远端仓库
git branch -a 查看本地和远端的所有分支
git checkout -b zkq 创建一个叫做“feature_x”的分支，并切换过去
git push origin dev 把本地分支推送到远端
git reflog 查看所有的commit
git merge dev 本地dev合并到master ，先切到master低版本再合并

ios 的Xcode IDE有个文件不需要被git 监控 可以这样
git rm --cached <files>

```


