learn git 2019-6-19
#参考自 廖雪峰 Git教程
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

Version3.0
git status
#掌握仓库当前状态 那些文件修改了还没提交
#一次失败记录
"""
第一次：
修改readme.txt 文件后 直接git add 并且commit了
使用git status 查看git中文件的状态时 没有显示文件的修改情况
第二次：
修改readme.txt文件后 不加add 也不commit 
直接输入 $git status 
出现了两个文件的前后对比，新增了三条记录，显示+号
如果删除，应该是显示-号，暂时没有尝试
第三次：
想知道add但是不commit 进行比较是怎样的情况
对readme.txt进行修改并且add之后
$git status
显示readme.txt文件modified
$git diff readme.txt
没有出现文件比对

所以commit之后 文件状态已经修改 $git status 无法查看文件修改情况
而add之后 $git status可以知道文件本身状态 diff命令比对文件内容在add之后就无法做到了

"""


version4.0 

"""
$git reset --hard HEAD^
#--hard参数暂时属于黑盒状态，字面意思猜测可能是回退的状态判断 回退程度？
HEAD 表示当前状态，也就是最新提交的版本
HEAD^ 表示上一个版本
HEAD^^ 表示上上个版本
Head～100 表示往上100个版本
"""

Version5.0

#时光穿梭
$git reset --hard commit_id
$git reflog 记录了每一次命令 可以在里面查看commit_id

#git push origin master 推送最新修改
