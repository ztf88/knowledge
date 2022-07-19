# Git

- [git tutuorial](https://www.atlassian.com/git/tutorials)

- [git cheat sheet](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet)

## Git config

常用git设置项

```bash
# check config
git config --list
# 取消
git config --global --unset https.proxy
## global config
git config --global user.name "john"
git config --global user.email "john@gmail.com"
## local config
cd git-project
git config user.name "john"
git config user.email "john@gmail.com"
## proxy
git config --global http.proxy http://127.0.0.1:8989
git config --global https.proxy https://127.0.0.1:8989
```

# Git version control

```bash
# 将文件加入版本控制，git会监测纳入版本控制的文件的改动，commit一次就是存档一次
git add filename
git commit -m "update message"
# 改动文件后，git status会显示那些staged文件改动了，重新添加存档
git add filename
git commit -m "update message again"
# 创建分支,并切换过去
git checkout -b new-branch
# 切换分支
git checkout master
# 合并分支（切近要保留的分支，merge其他develop分支）
git merge new-branch
git branch -d new-branch
# 若想保留develop分支的commit记录，使用rebase
git rebase new-branch
# 查看commit记录
git log
git log --graph --oneline -- decorate
# 撤销一次操作
git reset --hard
# 检出特定分支
git checkout 7ec0oa
# 撤销使用reset，revert
# unstaging file
git add readme.md
git reset readme.md
# removing local commit twice
git reset --hard HEAD~2
# a revert will create a new commit that inverses the changes specified. Git revert is a safer alternative to git reset in regards to losing work. 
git revert commit-id
```

## Git remote

```bash
git remote add <name> <url>
git remote add origin git...
git fetch <remote> <branch>
git pull <remote>
git pull --base <remote>
git push <remote> <branch>
```



## Use rebase

> `git rebase` 可以保留分支提交记录便于追溯debug，从远端拉取代码使用`git pull --rebase`

- 
- :x:`git merge develop`
- :heavy_check_mark:`git rebase develop`
- `git fetch`
- :x:`git pull` = `git fetch; git merge FETCH_HEAD`
- :heavy_check_mark:`git pull --rebase` = `git fetch; git rebase FETCH_HEAD`

