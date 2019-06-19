learn git 2019-6-19

version1.0
#Git is a version control system.

#first step 
git init #初始化git仓库

"""
初始化完成之后会出现一个 .git的文件夹 说明成功生成一个空仓库
如果没有出现，可能是隐藏了
输入命令 ls -ah 显示隐藏文件夹
"""

version2.0
git add readme.txt #告诉git 把文件添加到仓库 
#执行完命令没有任何显示，说明成功；没有消息就是好消息，是unix的哲学

git commit -m  "修改说明"
#-m 后面是本次提交的说明 可以任意输入 但是最好有意义 这样方便从历史记录里找改动

#小思考
"""
Q：为什么Git添加文件需要add commit两步
A：因为commit一次可以提交很多文件
	eg:$git add file1.txt
	   $git add file2.txt file3.txt
	   $git commit -m "add three files at one time"

"""
