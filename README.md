# git_study
git study 小改常commit pull request
## git init
- 创建一个版本
## 创建一个版本
- git add code.txt  把文件的修改添加到暂存区，可多次进行add再commit一个版本号,add 后可以跟多个文件或者路径。
- git commit -m '描述信息'  把暂存区的修改内容创建版本记录，只会用暂存区的内容。
  - 报错：进入.git里面的config 文件夹添加三行。
         - [user]
         - name = xxx
         - email= xxx
- git log ：查看创建的信息。
git 不同版本并不是复制了原先的版本，而是在旧版本的基础上新版本记录更改了什么。也就是新版本只记录进行更改的地方。
## 版本的回退
- git reset --hard HEAD~1
- git reset --hard 版本号，
- git reflog 查看创建记录：
  - HEAD 指针指向最新的版本，可用上尖括号代表上一个版本，也可以用~1表示前一个用~100表示前100个版本。
## 工作区和暂存区
- 工作区：创建git的地方
- 版本库: .git就是版本库
- git status 查看当前git 的状态
## 管理修改
- git checkout -- code.txt 撤销工作区的修改
- git reset HEAD code.txt  git checkout -- code.txt 修改完添加到暂存区的先用第一个命令撤回然后用第二个命令撤回
- 对于
## git 分支
- 查看分支
  - git branch
- 创建分支
  - git branch name
- 切换分支
  - git checkout name
- 创建+切换
  - git checkout -b name
- 合并某分支到当前分支
  - git merge name
- 删除分支
  - git branch -d name
- 合并冲突 master commit 和dev commit 同时提交版本，再合并会报错合并冲突
  - 进入文件，手动解决，然后git add git commit 
## github 使用
- 创建项目
  - new ----name --- public --- readme ---add.gitignore
  - 生成ssh 秘钥
  - git clone git@github.com:youyuebingchen/hj18.git
  - 报错sign_and _send pukkey使用 eval "$(ssh-agent -s)";  ssh-add   再克隆
- 创建分支，在本地写代码commit
  - git branch dev
- 推送分支,将本地的commit代码推送到github
  - git push origin smart
- 将本地分支跟踪服务器分支
  - git branch --set-upsetream-to=origin/远程分支  本地分支
- 从远程分支拉取
  - git pull origion master
- 工作中使用git
  - 项目经理搭建项目框架
  - 搭建完成后，项目经理把箱门框架代码放到服务器
  - 普通员工在自己的电脑上生成ssh 公钥，然后把公钥交给项目经理，项目经理把他添加到服务器上。
  - 项目经理会给每个组员的项目代码的地址，组员把diamante下载到自己的电脑上。
  - 创建本地的分支dev,在dev分支中进行每天的开发
  - 每个组员开发完后，需要将代码发布远程的dev分支上。不要每次都提交。
  
  
  
