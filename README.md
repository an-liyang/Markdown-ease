# Markdown-
 
 Git 学习

## 介绍
 - Git 是和 SVN 一样的版本控制系统 
  + 相同点
   * 历史记录
   * 多人协作
  + svn 是集中式版本控制
  + Git 是分布是版本控制系统

  - 关于名字： Git ：
   + angular 有角的

### Ubuntu Linux学习

---

## git使用
1. git -- version 就可以检测git版本。 看IP ；ipconfig ifconfig是Linux系统  exit退出环境；快速打开指定目录 shift+鼠标右键
2. + 命令台：pwd 打印当前路径 cls清除 ls清单 ls +指定目录 ls -a 找到目录隐藏的文件  cp复制 cd~回到上级目录和cd ../
   + mv mkdir clear rm touch cat  del 
3. 常用工具类 ：date format格式化 shutdown设置关机   ping ipconfig等等 winver电脑版本信息
4. GUI程序
  + feiq
### 文件系统性命令
1. pwd路径；ls清单 ls +指定目录 `ls -a` 找到目录隐藏的文件 `../`返回上一级 `cd`更换切换目录。如果想切换盘符直接输入D:文件路径
2. cd ~直接切换磁盘 cp 复制 到从一个文件复制到其他文件夹内 ` mv dir1 /a.txt dir2 /b.txt`
3. cls清除 clear 清屏 touch新建一个文件 cat 查看指定的文本文件
### less命令
+ less 加文件进入文编辑less中，shift+G到最后 g移动到开始 q退出

### vi命令

#### 插入模式
vi a.txt新建一个文本
通过  `i`表示insert输入 进入编辑模式；
esc退出编辑模式；
`w`保存 从编辑模式进入命令系统 `wq`保存并退出 `:q!`强制退出；

yy 当前行 p粘贴 d删除

---

#### git
查看是不是get环境 git--version
+ git commit -m 暂存区提交 m为描述信息
+ git init 建一个空的文件
+ git add 添加
+ git status 
+ git log 版本
+ git diff 查看暂存和工作树有什么区别
 - 配置git git config --golbal user .name 
 - 配置git git config --golbal user .email 邮箱
+ gitk表示打开图形界面查看

---

## Git_Toturial

### git命令大全

1. git init # 初始化本地git仓库（创建新仓库）

2. git config --global user.name "xxx" # 配置用户名

3. git config --global user.email "xxx@xxx.com" # 配置邮件

4. git config --global color.ui true # git status等命令自动着色

5. git config --global color.status auto

6. git config --global color.diff auto

7. git config --global color.branch auto

8. git config --global color.interactive auto

9. git config --global --unset http.proxy # remove proxy configuration on git

10. git clone git+ssh://git@192.168.53.168/VT.git # clone远程仓库

11. git status # 查看当前版本状态（是否修改）

12. git add xyz # 添加xyz文件至index

13. git add . # 增加当前子目录下所有更改过的文件至index

14. git commit -m 'xxx' # 提交

15. git commit --amend -m 'xxx' # 合并上一次提交（用于反复修改）

16. git commit -am 'xxx' # 将add和commit合为一步

17. git rm xxx # 删除index中的文件

git rm -r * # 递归删除

git log # 显示提交日志

git log -1 # 显示1行日志 -n为n行

git log -5

git log --stat # 显示提交日志及相关变动文件

git log -p -m

git show dfb02e6e4f2f7b573337763e5c0013802e392818 # 显示某个提交的详细内容

git show dfb02 # 可只用commitid的前几位

git show HEAD # 显示HEAD提交日志

git show HEAD^ # 显示HEAD的父（上一个版本）的提交日志 ^^为上两个版本 ^5为上5个版本

git tag # 显示已存在的tag

git tag -a v2.0 -m 'xxx' # 增加v2.0的tag

git show v2.0 # 显示v2.0的日志及详细内容

git log v2.0 # 显示v2.0的日志

git diff # 显示所有未添加至index的变更

git diff --cached # 显示所有已添加index但还未commit的变更

git diff HEAD^ # 比较与上一个版本的差异

git diff HEAD -- ./lib # 比较与HEAD版本lib目录的差异

git diff origin/master..master # 比较远程分支master上有本地分支master上没有的

git diff origin/master..master --stat # 只显示差异的文件，不显示具体内容

git remote add origin git+ssh://git@192.168.53.168/VT.git # 增加远程定义（用于push/pull/fetch）

git branch # 显示本地分支

git branch --contains 50089 # 显示包含提交50089的分支

git branch -a # 显示所有分支

git branch -r # 显示所有原创分支

git branch --merged # 显示所有已合并到当前分支的分支

git branch --no-merged # 显示所有未合并到当前分支的分支

git branch -m master master_copy # 本地分支改名

git checkout -b master_copy # 从当前分支创建新分支master_copy并检出

git checkout -b master master_copy # 上面的完整版

git checkout features/performance # 检出已存在的features/performance分支

git checkout --track hotfixes/BJVEP933 # 检出远程分支hotfixes/BJVEP933并创建本地跟踪分支

git checkout v2.0 # 检出版本v2.0

git checkout -b devel origin/develop # 从远程分支develop创建新本地分支devel并检出

git checkout -- README # 检出head版本的README文件（可用于修改错误回退）

git merge origin/master # 合并远程master分支至当前分支

git cherry-pick ff44785404a8e # 合并提交ff44785404a8e的修改

git push origin master # 将当前分支push到远程master分支

git push origin :hotfixes/BJVEP933 # 删除远程仓库的hotfixes/BJVEP933分支

git push --tags # 把所有tag推送到远程仓库

git fetch # 获取所有远程分支（不更新本地分支，另需merge）

git fetch --prune # 获取所有原创分支并清除服务器上已删掉的分支

git pull origin master # 获取远程分支master并merge到当前分支

git mv README README2 # 重命名文件README为README2

git reset --hard HEAD # 将当前版本重置为HEAD（通常用于merge失败回退）

git rebase

git branch -d hotfixes/BJVEP933 # 删除分支hotfixes/BJVEP933（本分支修改已合并到其他分支）

git branch -D hotfixes/BJVEP933 # 强制删除分支hotfixes/BJVEP933

git ls-files # 列出git index包含的文件

git show-branch # 图示当前分支历史

git show-branch --all # 图示所有分支历史

git whatchanged # 显示提交历史对应的文件修改

git revert dfb02e6e4f2f7b573337763e5c0013802e392818 # 撤销提交dfb02e6e4f2f7b573337763e5c0013802e392818

git ls-tree HEAD # 内部命令：显示某个git对象

git rev-parse v2.0 # 内部命令：显示某个ref对于的SHA1 HASH

git reflog # 显示所有提交，包括孤立节点

git show HEAD@{5}

git show master@{yesterday} # 显示master分支昨天的状态

git log --pretty=format:'%h %s' --graph # 图示提交日志

git show HEAD~3

git show -s --pretty=raw 2be7fcb476

git stash # 暂存当前修改，将所有至为HEAD状态

git stash list # 查看所有暂存

git stash show -p stash@{0} # 参考第一次暂存

git stash apply stash@{0} # 应用第一次暂存

git grep "delete from" # 文件中搜索文本“delete from” git grep -e '#define' --and -e SORT_DIRENT git gc git fsck 
