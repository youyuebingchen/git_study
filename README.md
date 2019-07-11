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
## github 使用
- 创建项目
