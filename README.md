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

14创建并切换分支

git checkout -b 名称

git switch -c 名称

15查看当前分支

git branch

15切换分支

git checkout 名称

git switch 名称

16 将分支合并到当前分支

git merge 名称

17 删除分支

git branch -d 名称

18 查看远程库的信息

git remote

19显示简短log

git log --graph --pretty=oneline --abbrev-commit

20 提交远程

git push origin(远程) master(远程分支)

21 从远程拉取

git pull


21 清除缓存区信息

git rm -r --cached

# docker command
1 查看docker镜像

docker images

2 启动resitory为python tag为3.6的镜像，并且运行命令/bin/bash

docker run python:3.6 /bin/bash  

docker run -itd python:3.6 /bin/bash   #加-it是交互模式，-d是后台运行

docker run -itd --name p python:3.6 /bin/bash  #--name 给容器起别名

docker run -itd -P python:3.6 python app.py   #-P添加web映射端口

docker run -itd -p 5000:8888 python:3.6 python app.py #-p添加对应映射端口

3 查看docker目前正在运行的容器

docker ps  # 加-a是所有历史记录

docker ps -a

4 停止容器

docker stop 别名

5 拉取镜像

docker pull 镜像名

6 进入容易的交互模式

docker exec -it 容器名 /bin/bash

7 导出容器

docker export 容器名 > tmp.tar

8 导入容器

cat tmp.tar | docker import - python:3.6

9 删除镜像

docker rmi python:3.6

10 删除所有容器的运行记录

docker container prune

11 查看容器映射端口

docker port 容器名

12 查看容器得运行日志

docker logs -f 容器

13 将当前容器保存为一个镜像

docker commit -a '' -m '' id python:3.6  #-a 作者 -m 说明 id:container的id python:3.6 respyity和tag






