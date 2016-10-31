## 全局初始配置账号和邮箱
```
git config --global user.name xxx
git config --global user.email xxx@xx.xx 
git config --list 查看所有配置
```
## cd 命令
mkdir 创建目录
## 初始化git
```
git init
```
## 初始化文件
```
echo hello > 1.txt
```
- 一个>代表清空并写入 两个>>代表追加
## 删除文件rm
## 查看状态
```
git status
```
## 将文件加入到暂存区中
```
git add file
git add . 
git add -A
```
## 提交commit
```
git commit -m "对于修改内容的描述"
```
## vi控制台
如果进入了编辑模式可以通过i键进入插入模式
- i表示编辑
- 退出esc+ :wq
## 查看版本库信息
```
git log --oneline
```
## 比较代码差异
- 比较工作区和暂存区
```
git diff
```
- 比较工作区和版本库的区别
```
git diff master
```
- 比较暂存区和版本库的区别
```
git diff --cached
```
## 从暂存区删除本次的add
```
git reset HEAD file
```
> 取消本次的add
## 从缓存区 从历史区将代码覆盖掉工作区
```
git checkout file
```
## 回到过去
```
git reset --hard commit_id/^^^^^/HEAD~4
```
## 查看未来的版本
```
git reflog
```
## 查看所有分支
```
git branch
```
## 创建分支
```
git branch xx
```
## 切换分支
```
git checkout xx
```
## 创建并切换
```
git checkout -b xx
```
## 删除分支
```
git branch -d xx
```
## 合并分支
```
git merge xx
```
## 在gitHub上部署静态页
需要将特定的内容推送到gitHub上的gh-pages分支上
- 创建一个gh-pages的分支
```
git checkout -b gh-pages
```
- 将代码commit 到这个分支上
```
git add .
git commit -m ""
```
- 连接远程仓库和本地仓库
```
git remote add origin 地址
```
- 将代码推送到远程仓库上
```
git push origin gh-pages
```
## 合并分支产生冲突
- 在主干的某个版本上进行分支开发，在分支上开发1.txt这个文件(drag)，在主干上也开发1.txt(limit),此时回到主干上合并时，会产生冲突，需要我们手动解决
## 从工作区中提交到历史区
```
git commit -a -m ""
```
> 第一次不能这样写
## 解决冲突
去掉 >>> ===<<<保留需要的内容再提交
## 合并
git rebase 变基
git cherry-pick 精选
## 显示结构
```
git log --graph --oneline --decorate
```
## 创建忽略文件
将项目提交到gitHub上，需要在gitHub上创建一个空的仓库
## 添加远程仓库的连接
```
git remote add 地址名字 地址
```
## 查看配置的所有配置的地址
```
git remote -v
```
## 删除地址
```
git remote rm 地址名字
```
## upstream
```
-u 下次提交或者拉取代码可以直接git push 或者git pull
```

## fork
把别人的项目原封不动的拷贝一份放置到自己的仓库下，只能fork一次
