### 通过ssh方式上传代码
- 首先要初始化一个.git仓储


- 查看是否已经有了ssh秘钥
	+ `cd ~/.ssh`如果没有秘钥就不会有此文件夹
	+ C盘用户里面`C:\Users\hasee\.ssh`里面的`id_rsa.pub`就是公钥
- 生成ssh秘钥的过程:
	+ `ssh-keygen -t rsa -C '邮箱'`按3个回车,密码为空
	+ 把.ssh文件下的.pub文件复制添加到GitHub是指的秘钥里去


###  上传之前,先`pull`,防止文件冲突,先`pull`到本地,解决冲突,然后在`push`

### pull 和 push的简写:
- 在push时,加上-u参数,name在下一次push时,只需要写上`git push`就可以上传代码了.
	+`git remote add origin git@github.com:newMrc/text.git`相当于设置`origin = git@github.com:newMrc/text.git`

	+`git push origin -u master`会把当前分支与远程的指定分支进行关联

	+ 在push和pull是就可以直接写`git push`和`git pull`了
**注意:**这个这些只能在添加了关联的才能简写,否则不能简写pull和push