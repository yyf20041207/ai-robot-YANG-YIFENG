## 容器如何与本地文件交互 <br>
使用 docker run -v 进行本地目录挂载 <br>
docker run命令首先在指定的镜像上创建一个可写的容器层，然后使用指定的命令启动。（来源 docker.com）使用参数-v允许你绑定一个本地目录。 <br>
 docker run -p 6080:80 --security-opt seccomp=unconfined --shm-size=512m  -v 当前目录$(pwd)/:/home/ws ghcr.io/tiryoh/ros2-desktop-vnc:humble <br>
![这是效果图](3.png) <br>
# 安装opencv <br>
pip install opencv-python opencv-contrib-python <br>
在命令行里输入 <br>
import cv2 <br>
import matplotlib.pyplot as plt <br>

img_basic = cv2.imread('cat.jpg', cv2.IMREAD_COLOR) <br>
plt.imshow(cv2.cvtColor(img_basic, cv2.COLOR_BGR2RGB)) <br>
plt.show() <br>

img_basic = cv2.cvtColor(img_basic, cv2.COLOR_BGR2GRAY) <br>
plt.imshow(cv2.cvtColor(img_basic, cv2.COLOR_GRAY2RGB)) <br>
plt.show() <br>
![这是效果图](1.png) <br>
![这是效果图](2.png) <br>