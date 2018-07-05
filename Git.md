
分支相关命令
==============
* 1\.创建分支git branch

* 2\.切换分支git checkout

* 3\.合并分支git merge

* 4\.创建新分支并立即切换到该分支下git checkout -b

* 5\.删除分支git branch -d

查看日志命令
======
* 1\.列出历史提交记录 git log
* 2\.查看历史记录的简洁的版本 git log --oneline
* 3\.查看历史中什么时候出现了分支、合并 git log --oneline --graph

查看信息
======
* 1\.git show master查看master分支
* 2\.git show HEAD^查看HEAD的上一级信息
* 3\.git tag V3 .....用V3来代替复杂的名称(....)
* 4\.git show  V3 查看V3
* 5\.git branch test V3 建一个test的分支
* 6\.git cat-file -t ...查看对象（....）类型
* 7\.git cat-file commit ...... 查看一个commit类型的对象

Git常用命令
============
#
config
##
* 1\.设置用户名：git config --global user.name"你的用户名"

* 2\.设置email：git config --global user.email"你的邮箱"

* 3\.配置编辑器：git config --global core.editor(后面跟想要设置的编辑器名字，不加显示当前编辑器）

* 4\.配置比较工具：git config --global merge.tool(和编辑器同理)

* 5\.列出该处找到的所有配置：git config --list

* 6\.添加一个配置项：git config --add site.name fanhui

* 7\.删除一个配置项：git config --local -unset site.name 

#
add
##
* 1\.添加该目录及其子目录下的txt文件： git add documentation/*.txt

* 2\.添加脚本：git add git-*.sh
