#1\.先在官网上下载git
#2\.配置本地连接
#3\.可以使用命令mkdir 文件名新建文件到桌面
4.使用cd 文件名 打开该文件
5.使用git init把该文件夹变成Git可管理的仓库
6.将想要上传的项目复制到该文件夹下
7.使用git status查看当前文件夹
8.使用git add .将该文件夹下的所有文件添加到仓库
9.使用git commit -m把项目提交到仓库
10.创建SSH KEY（由于本地Git仓库和Github仓库之间的传输是通过SSH加密的）命令为$ ssh-keygen -t rsa -C "fan.hui@zhongfl.com"回车几次，直到该命令结束，就会发现c盘下的administrator里面有.ssh文件夹，.ssh文件包含id_rsa和id_rsa.pub这两个文件 
11.登录自己的git
12.找到settings
13.新建一个ssh key，使用id_rsa.pub里的内容成功新建一个shh key
14.在git上创建一个仓库
15.将创建好的仓库与本地仓库连接，使用 git remote add origin git@github.com:lanzhan/fh.git命令
16.使用命令git push -u origin master将本地仓库的内容上传到自己的git仓库
17.我使用该命令上传时报错
17.1错误信息：error: src refspec master does not match any.
error: failed to push some refs to 'https://github.com/lanzhan/fh.git'
17.2引起错误原因：目录中没有文件，空目录是不能提交上去的
17.3解决办法：$ touch README
git commit -m 'first commit'
git push origin master
18.会跳出对话框请求登录git，输入用户名与密码可以上传到自己的git
