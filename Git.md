
分支相关命令
==============
本地
------
* 1\.创建分支git branch new_master(创建了一个新分支，名字叫做new_master)

>此时可以使用 git branch语句查看所在的分支

>> ![1](http://chuantu.biz/t6/339/1530870739x-1376440096.png)

* 2\.切换分支git checkout new_master

> * a\.当前分支为master，可使用该语句切换分支到new_master,此时再使用git branch 语句可看到所在分支变为new_master

>> ![1](http://chuantu.biz/t6/339/1530870841x-1376440096.png)

> * b\.接下来我们使用该分支上传一些文件到仓库里，使用 git add fan.txt 将文件fan添加到仓库，使用git commit -m "new fan complete."语句提交

>> ![1](http://chuantu.biz/t6/339/1530870355x-1376440096.png)

> * c\.如下图所示，我们返回到上级目录下，切换分支查看我们的fan.txt会找不到，再切回new_master查看可以进去，证明一个分支里建的项目另一分支是没有的

>> ![1](http://chuantu.biz/t6/339/1530870185x-1376440096.png)

* 3\.合并分支git merge new_master

> 使用该命令将两个分支合并到一起，此时使用分支master查看fan.txt也可以查看了

* 4\.删除分支git branch -d

> ![1](http://chuantu.biz/t6/339/1530870430x-1376440096.png)


远程
-----
* 1\.查看远程所有分支 git branch -rll

* 2\.拉取远程分支，并创建本地分支

> * a\.git checkout -b user origin/master在本地新建分支名为user,并切换到该分支下

> * b\.git fetch origin master:user1在本地新建分支名为user1，但并不切换到分之下，可以手动切换

>> ![1](http://chuantu.biz/t6/339/1530867612x-1376440096.png)

* 3\.git fetch相关命令的使用：该命令相当于从远程获取最新版本到本地，但是不会自动合并

> * a\.git fetch origin master 从远程的origin的分支master上下载最新版到本地分支master上

>> ![1](http://chuantu.biz/t6/339/1530871199x-1376440096.png)

> * b\.git log -p master..origin/master比较远程分支和本地分支的差别

>> ![1](http://chuantu.biz/t6/339/1530871236x-1376440096.png)

> * c\.get merge origin/master手动进行合并

* 4\.git pull origin master 从远程获取最新版本到本地并且直接合并，相当于fetch和merge两个过程

> ![1](http://chuantu.biz/t6/339/1530868070x-1376440096.png)

* 5\.git push origin master 将本地的master分支推送到远程master上，如果本地master分支不存在，则会新建一个

>如图所示 使用git push origin master 报错

>>错误信息： failed to push some refs to 'https://github.com/lanzhan/fh.git'

>>解决方法：将 git push origin master命令  改为git push -f origin master

>> ![1](http://chuantu.biz/t6/339/1530868206x-1376440096.png)

* 6\.git push origin : master与git push origin --delete master作用相同，都是删除指定的远程分支，等同于推送一个空的本地分支到远程分支

> ![1](http://chuantu.biz/t6/339/1530868568x-1376440096.png)

* 7\. git push origin 将当前分支推送到主机的对应分支

> ![1](http://chuantu.biz/t6/339/1530868508x-1376440096.png)

> 如果当前分支只有一个追踪分支，那么主机名都可以省略。直接写 git push

> ![1](http://chuantu.biz/t6/339/1530868462x-1376440096.png)

* 8\. git push -all origin会将本地所有的分支都推送到主机origin上，没有的远程分支会被创建

> ![1](http://chuantu.biz/t6/339/1530868415x-1376440096.png)

* 9\.git push origin HEAD将当前分支推送到origin上，没有的话会被创建

> ![1](http://chuantu.biz/t6/339/1530868364x-1376440096.png)

* 10\.git push origin HEAD : master将当前主机推送到origin的master分支上

> ![1](http://chuantu.biz/t6/339/1530868312x-1376440096.png)

* 11\.git remote的相关操作，查看及新建

> ![1](http://chuantu.biz/t6/339/1530868774x-1376440096.png)

> ![1](http://chuantu.biz/t6/339/1530868809x-1376440096.png)

> ![1](http://chuantu.biz/t6/339/1530868871x-1376440096.png)

查看日志命令
======
* 1\.列出历史提交记录 git log

> ![1](http://chuantu.biz/t6/339/1530869681x-1376440096.png)

* 2\.使用git show aa6875命令列出aa6875开头的操作

> ![1](http://chuantu.biz/t6/339/1530869357x-1376440096.png)

* 3\.使用git diff 5bdde0..aa6875可查看两次更改的不同

> ![1](http://chuantu.biz/t6/339/1530869520x-1376440096.png)

* 4\.使用git difftool可查看到第一次与最后一次比较的全部更改

> ![1](http://chuantu.biz/t6/339/1530869606x-1376440096.png)

* 5\.查看历史记录的简洁的版本 git log --oneline

> ![a](http://chuantu.biz/t6/339/1530869473x-1376440096.png)

* 6\.查看历史中什么时候出现了分支、合并 git log --oneline --graph

> ![a](http://chuantu.biz/t6/339/1530869728x-1376440096.png)

查看信息
======
* 1\.git show master查看master分支

> ![a](http://chuantu.biz/t6/339/1530869431x-1376440096.png)

* 2\.git show HEAD^查看HEAD的上一级信息

> ![a](http://chuantu.biz/t6/339/1530869202x-1376440096.png)

* 3\.git tag V3 aa6875 用V3来代替复杂的名称(以aa6875为例)

* 4\.git show  V3 查看V3

> ![a](http://chuantu.biz/t6/339/1530869128x-1376440096.png)

* 6\.git cat-file -t ...查看对象（....）类型

* 7\.git cat-file commit ...... 查看一个commit类型的对象

> ![a](http://chuantu.biz/t6/339/1530869835x-1376440096.png)

合并冲突及解决办法
=======
* 1\.新建分支test2

* 2\.进入该分支

* 3\.编辑文件之前建好的test.txt文件

> ![a](http://chuantu.biz/t6/339/1530867181x-1404817659.png )

* 4\.提交

> ![a](http://chuantu.biz/t6/339/1530867249x-1376440096.png )

* 5\.切换回master分支 

> ![a](http://chuantu.biz/t6/339/1530867308x-1376440096.png)

* 6\.再次提交master

* 7\.使用merge合并test2

* 8\.报错了

> ![a](http://chuantu.biz/t6/339/1530867326x-1376440096.png)

* 9\.查看状态，显示test.TXT错误

* 10\.vim编辑该文档

* 11\.编辑完保存退出

> ![a](http://chuantu.biz/t6/339/1530867347x-1376440096.png)

* 12\.再次提交，成功

> ![a](http://chuantu.biz/t6/339/1530867367x-1376440096.png)
