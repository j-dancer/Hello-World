# Git 常用命令
`在 Git 中，所有的命令都是以git开头，例如，git init其作用就是初始一个 Git 仓库`

## 1、命令介绍：
---
- **`git status` 查看仓库的状态**
- **`git init` 初始化 Git 仓库**
- **`git add` 将文件添加到 Git 仓库临时缓冲区**
- **`git commit` add后将文件提交到 Git 仓库**
- **`git log` 打印 Git 仓库提交日志**
- **`git branch` 查看 Git 仓库的分支情况**
- **`git branch a` 创建了一个名为a的分支**
- **`git checkout a` 切换到a分支**
- **`git merge a` 切换到master分支，然后输入git merge a命令，将a分支合并到master分支**
<font color=LightCoral>Tips:  
在合并分支的时候，要考虑到两个分支是否有冲突，如果有冲突，则不能直接合并，需要先解决冲突；反之，则可以直接合并。</font>
- **`git git branch -d` 删除分支（git git branch -d a 表示删除a分支）**
- **`git tag` 在命令行窗口的光标处，输入git tag v1.0命令，为当前分支添加标签**

## 2、通过 Git 将代码提交到 GitHub
----
**提交代码需要先了解两个命令，也是我们在将来需要经常用到的两个命令，分别为push和pull.**
- `push`:该单词直译过来就是“推”的意思，如果我们本地的代码有了更新，为了保持本地与远程的代码同步，我们就需要把本地的代码推到远程的仓库，代码示例:
```html
git push origin master
```
- `pull`:该单词直译过来就是“拉”的意思，如果我们远程仓库的代码有了更新，同样为了保持本地与远程的代码同步，我们就需要把远程的代码拉到本地，代码示例:
```html
git pull origin master
```
<font color=LightCoral>**`Tips`：在我们向远程仓库提交代码的时候，一定要先进行pull操作，再进行push操作，防止本地仓库与远程仓库不同步导致冲突的问题**</font>

## 3、多人协作的工作模式通常如下：
---------
- （1）首先将远程仓库克隆为本地仓库
git clone git@github.com:xxx/LearnGit.git
- （2）在本地创建和远程分支对应的分支
git checkout -b <本地分支名> origin/<远程分支名>
本地和远程分支的名称最好一致；
- （3）在本地分支完成任务后，可以试图用git push <远程主机名> <本地分支名>推送自己的修改；
- （2）如果推送失败，则表明远程分支比本地更新，需要先用git pull试图合并；
- （3）如果pull失败并提示“no tracking information”，则说明本地分支和远程分支的链接关系没有创建，用命令git branch --set-upstream-to=<远程主机名>/<远程分支名>  <本地分支名>创建链接；
- （4）如果合并有冲突，则解决冲突，并在本地提交（add => commit）；
- （5）没有冲突或者解决掉冲突后，再用git push <远程主机名> <本地分支名>推送就能成功。

## 4、新建项目并提交文章
**`创建一个新仓库
- git clone git@gitlab:xxx/project.git
- cd project
- touch README.md
- git add README.md
- git commit -m "add README"
- git push -u origin master

**`推送现有文件夹
- cd existing_folder
- git init
- git remote add origin git@gitlab:xxx/project.git
- git add .
- git commit -m "Initial commit"
- git push -u origin master

**`推送现有的 Git 仓库
- cd existing_repo
- git remote rename origin old-origin
- git remote add origin git@gitlab:xxx/project.git
- git push -u origin --all
- git push -u origin --tags
