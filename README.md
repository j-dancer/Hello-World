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
<font color=LightCoral>一般情况下，我们在`push`操作之前都会先进行`pull`操作，这样不容易造成冲突。`</font>