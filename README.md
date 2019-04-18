# learn_git
分享git 在epark

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
    
    `git commit -m :dog: tes`
    

## Which Emoji to Use? ❓

Commit Type | Emoji
----------  | -----
Initial Commit | [🎉 Party Popper](http://emojipedia.org/party-popper/)
Version Tag | [🔖 Bookmark](http://emojipedia.org/bookmark/)
New Feature | [✨ Sparkles](http://emojipedia.org/sparkles/)
Bugfix | [🐛 Bug](http://emojipedia.org/bug/)
Security Fix | [🔒 Lock](https://emojipedia.org/lock/)
Metadata | [📇 Card Index](http://emojipedia.org/card-index/)
Refactoring | [♻️ Black Universal Recycling Symbol](http://emojipedia.org/black-universal-recycling-symbol/)
Documentation | [📚 Books](http://emojipedia.org/books/)
Internationalization | [🌐 Globe With Meridians](http://emojipedia.org/globe-with-meridians/)
Accessibility | [♿ Wheelchair](https://emojipedia.org/wheelchair-symbol/)
Performance | [🐎 Horse](http://emojipedia.org/horse/)
Cosmetic | [🎨 Artist Palette](http://emojipedia.org/artist-palette/)
Tooling | [🔧 Wrench](http://emojipedia.org/wrench/)
Tests | [🚨 Police Cars Revolving