---
title: git常用指令
---

```
    合并分支 (将其他的分支的内容更新到当前分支) :
        git merge origin/master  //合并远程的master分支
        git merge 0.2.5  //合并本地的0.2.5分支
    清除缓存 (不小心上传了不需要的文件 想重新上传)
        git rm --cached -r .
        git add .
        git commit -m 'xxxx'
        git pull
        git push
    回退版本 (字面意思)
        git log  //查看提交历史及提交的commit_id
        git reset --hard HEAD^  //回退到上个版本
        git reset --hard HEAD~3  //回退到前3次提交之前，以此类推，回退到n次提交之前
        git reset --hard "commit_id"  //退到/进到 指定commit
```
