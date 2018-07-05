#
将本地文件上传到git仓库
##
1\.使用命令mkdir 文件名新建文件到桌面

2\.使用cd 文件名 打开该文件

3\.使用git init把该文件夹变成Git可管理的仓库

4\.将想要上传的项目复制到该文件夹下

5\.使用git status查看当前文件夹

6\.使用git add .将该文件夹下的所有文件添加到仓库

7\.使用git commit -m把项目提交到仓库

8\.创建SSH KEY（由于本地Git仓库和Github仓库之间的传输是通过SSH加密的）命令为$ ssh-keygen -t rsa -C "fan.hui@zhongfl.com"回车几次，直到该命令结束，就会发现c盘下的administrator里面有.ssh文件夹，.ssh文件包含id_rsa和id_rsa.pub这两个文件 

9\.登录自己的git

10\.找到settings

11\.新建一个ssh key，使用id_rsa.pub里的内容成功新建一个shh key

12\.在git上创建一个仓库

13\.将创建好的仓库与本地仓库连接，使用 git remote add origin git@github.com:lanzhan/fh.git命令

14\.使用命令git push -u origin master将本地仓库的内容上传到自己的git仓库

15\.我使用该命令上传时报错
###
15.1\.错误信息：error: src refspec master does not match any.
error: failed to push some refs to 'https://github.com/lanzhan/fh.git'

15.2\.引起错误原因：目录中没有文件，空目录是不能提交上去的

15.3\.解决办法：$ touch README
git commit -m 'first commit'
git push origin master
##
16\.会跳出对话框请求登录git，输入用户名与密码可以上传到自己的git
