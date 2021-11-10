# git_command
git 常用命令大全

1 清除本地未提交的修改

git checkout . && git clean -xdf

2 远程覆盖本地

git fetch --all &&  git reset --hard origin/master && git pull

3 添加文件

git add . 和git add * 

git add . 会忽视ignore git add * 不会

4 提交文件

git commit -a 

git commit -a -m '信息'

5 将本地文件回退到上一个版本

git reset --hard HEAD^  

6 将本地文件回退到上3个版本

git reset --hard HEAD~3  

7 将本地文件恢复到某个版本号

git reset --hard '版本号'

8 查看命令以及提交版本号

git reflog

9 从暂存区恢复readme.txt文件

git checkout -- readme.txt

10 从本地仓库恢复readme.txt文件

git reset HEAD readme.txt

11 将本地库关联到远程库

git remote add origin git@github.com:michaelliao/learn-git.git

12 第一次推送master分支的所有内容

git push -u origin master

13 以后每次推送
git push origin master


