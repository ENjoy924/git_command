# git_command
git 常用命令大全

1 清除本地未提交的修改\n
git checkout . && git clean -xdf\n
2 远程覆盖本地
git fetch --all &&  git reset --hard origin/master && git pull
3 添加文件
git add . 和git add * 
git add . 会忽视ignore git add * 不会
4 提交文件
git commit -a 
git commit -a -m '信息'
5 
