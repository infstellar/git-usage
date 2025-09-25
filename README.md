## 完成以下操作:
1. 切换到no-conflict-dev分支，使用rebase同步main分支的更改，然后push到remote;
2. 切换到dev分支，使用rebase同步main分支的更改，然后解决冲突并push到remote;
3. 切换到main分支，merge dev分支。

## 提示：
- 使用git rebase main同步main分支到当前分支，同时不产生分叉;
- 使用git push -f推送rebase后的分支到远程分支。注意，只有当前分支仅有你在编辑时可以使用push -f；严禁在main/master分支使用push -f !
- 你可以使用vscode编辑器/命令行或其他GUI程序解决冲突。解决冲突后，main的内容应该在第一行，dev的内容在第二行。
- 你可以在main分支运行git merge dev或者在Github页面开一个Pull Request(推荐！)

## 常用命令:

|命令|描述|
|--------|--------|
|git checkout xxx|切换分支|
| git remote add origin https://xxx.git | 添加远程仓库url|
|git remote set-url origin https://xxx.git | 切换远程仓库url|
|git fetch | 更新远程仓库的metadata，不会修改文件|
|git pull | 同步远程仓库到本地|
|git push | 推送本地到远程|
|git push -f | 强制覆盖远程仓库在当前分支的内容。慎用！|
|git push --set-upstream origin new-branch |当你在本地创建了一个分支但是远程没有的时候使用，会push内容并在远程创建这个分支。|
|git branch new-branch | 从当前分支创建一个新的分支|
|git branch -D xxx | 删掉本地分支|
|git rebase main | 变基到main分支（把当前分支与main分支变动的提交追加到main分支的最后，然后作为当前分支。详细原理推荐搜索了解。）|
|git rebase --continue | 继续变基，解决冲突后使用。|
