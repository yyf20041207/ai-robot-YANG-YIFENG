## Week8docker-ros2-desktop-vnc <br>
打开 Windows docker 网站进行下载 <br>
在c盘中把ProgramData里面的dockers文件删了 <br>
在管理员命令中把docker的地址放入进行下载 <br>
重启电脑后在管理员命令中放入docker run -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m ghcr.io/tiryoh/ros2-desktop-vnc:humble <br>
下载完后进入http://127.0.0.1:6080/. <br>
打开Terminator输入ros2 run turtlesim turtlesim_node <br>
![这是效果图](屏幕截图 2026-04-22 131218.png)
