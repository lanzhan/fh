
分支相关命令
==============

*1\.创建分支git branch

*2\.切换分支git checkout

*3\.合并分支git merge

*4\.创建新分支并立即切换到该分支下git checkout -b

*5\.删除分支git branch -d

Git常用命令
============

#
config

##
*1\.设置用户名：git config --global user.name"你的用户名"

*2\.设置email：git config --global user.email"你的邮箱"

*3\.配置编辑器：git config --global core.editor(后面跟想要设置的编辑器名字，不加显示当前编辑器）

*4\.配置比较工具：git config --global merge.tool(和编辑器同理)

*5\.列出该处找到的所有配置：git config --list

*6\.添加一个配置项：git config --add site.name fanhui

*7\.删除一个配置项：git config --local -unset site.name 

#
add

##
*1\.添加该目录及其子目录下的txt文件： git add documentation/*.txt

*2\.添加脚本：git add git-*.sh
