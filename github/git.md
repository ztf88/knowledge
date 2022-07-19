# Git

## Use rebase

> `git rebase` 可以保留分支提交记录便于追溯debug，从远端拉取代码使用`git pull --rebase`

- 
- :x:`git merge develop`
- :heavy_check_mark:`git rebase develop`
- `git fetch`
- :x:`git pull` = `git fetch; git merge FETCH_HEAD`
- :heavy_check_mark:`git pull --rebase` = `git fetch; git rebase FETCH_HEAD`

