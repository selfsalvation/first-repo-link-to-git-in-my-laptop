git diff
此命令比较的是工作目录(Working tree)和暂存区域快照(index)之间的差异
也就是修改之后还没有暂存起来的变化内容。

命令git checkout -- readme.txt意思就是，把readme.txt文件在工作区的修改全部撤销，这里有两种情况：

一种是readme.txt自修改后还没有被放到暂存区，现在，撤销修改就回到和版本库一模一样的状态；

一种是readme.txt已经添加到暂存区后，又作了修改，现在，撤销修改就回到添加到暂存区后的状态。

总之，就是让这个文件回到最近一次git commit或git add时的状态。

Git同样告诉我们，用命令git reset HEAD <file>可以把暂存区的修改撤销掉（unstage），重新放回工作区：


git diff :比较工作区与暂存区
git checkout ：回复工作区到最新的commit或者add
git reset HEAD file ：撤销暂存区到工作区

删除版本库中的文件：git rm 文件名
		git commit

或
	rm 文件名
	git add 文件名
	git commit

rm 文件名
取消删除
git checkout -- 文件名

一个ssh可以验证一个电脑的身份
为什么GitHub需要SSH Key呢？因为GitHub需要识别出你推送的提交确实是你推送的，而不是别人冒充的，而Git支持SSH协议，所以，GitHub只要知道了你的公钥，就可以确认只有你自己才能推送。

当然，GitHub允许你添加多个Key。假定你有若干电脑，你一会儿在公司提交，一会儿在家里提交，只要把每台电脑的Key都添加到GitHub，就可以在每台电脑上往GitHub推送了。

