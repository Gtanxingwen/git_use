>git merge

```
  // 当前分支master,把dev分支merge到master
  git merge dev
```

>git rebase
```
  ## branch dev
  git rebase master
  git checkout master
  ## 用于将master上的HEAD移动到最新的commit
  git merge dev
  ## rebase 对比 merge，优势在于合并后的结果很清晰，只有一条线
```

>get cherry-pick
```
  // 提交单个commit到另外一个分支
  // 比如当前在dev分支，找到一个commit '4db0729d'
  // 切换到master分支
  git cherry-pick 4db0729d
  git add -A (--all的缩写)
  git commit -m 'xxx'
  git push
```
>git stash
>git stash pop
>git reset
```
  // 但是 reset 的本质并不是删除了 commit，
  // 而是重新设置了 HEAD 和它指向的 branch
  // 回退到上一版
  git reset --hard HEAD^
  // 回退到倒数第二版
  git reset --hard HEAD^^
  // 回退到指定版本(commit id为3628164的版本)
  git reset --hard 3628164
```
>git reflog
