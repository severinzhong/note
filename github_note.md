# github使用
---
## 建立一个分支
1. 在github上使用new repository建立一个名`rep_name`文件夹
2. 建立一个同名rep文件夹`mkdir rep_name`，并在文件夹中使用`git init`建立git
3. 在该文件夹下使用`git remote add origin git@github.com:user_name/rep_name.git`来连接github

## 文件操作
>本地文件是你的工作区
添加文件（文件修改加入暂存区）

    git add filename

修改文件之后提交（把暂存区的内容一起提交到分支）

    git commit -m "change reason"

查看文件区别

    git diff HEAD -- filename

查看git状态

    git status

将文件在工作区的修改撤销（最近一次add commit 的状态）

    git checkout -- filename

将文件暂存区的修改撤销(重新放回工作区)

    git reset HEAD file

将已经删除的文件从git中移除

    git rm filename

## 上传和克隆

上传本地内容到github

    git push -u origin master %first time
    git push origin master %normal condition
    git push origin branch_name

克隆一个github上的项目

    git clone git@github.com:user_name/rep_name.git

查看远程库的信息

    git remote % -v 查看更多


## 分支管理

创建分支并切换

    git checkout -b newbranch
    %equal
    git branch newbranch
    git checkout newbranch

查看当前分支

    git branch

合并分支

    git merge newbranch

删除分支

    git branch -d newbranch

## 标签

制作新标签(没有commit ID 会打在最新的commit上)

    git tag tag_name (commit id)
    git tag -a tag_name -m "tag information" %带说明的标签

查看标签信息

    git show tag_name

删除标签

    git tag -d tag_name %删除本地
    git push origin :refs/tags/tag_name  %删除远程

test for git
 


---
参考 [廖雪峰git教程](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)