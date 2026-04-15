## week6 ROS2 Kitti 数据集发布器 (Publishers) <br>
- 这是一个示例 ROS2 发布器应用程序，用于将 Kitti 数据集转换并发布为 ROS2 消息。 发布的消息主要包括 PointCloud2（点云）、Image（图像）、Imu（惯性测量单元）和 MarkerArray（标记阵列）。 <br>
- mkdir -p ~/ros2_ws/src <br>
- cd ~/ros2_ws/src <br>
- git clone https://github.com/ai-robot-class/ros2_kitti_publishers.git <br>
- Kitti 示例数据地址 https://drive.google.com/file/d/1lCOOkoUp1RRrFhUwRVNVwRWIclv-etBu/view?usp=drive_link <br>
- 数据保存路径 ~/ros2_ws/data <br>
week2
- ![这是效果图](作业1.png)
 ├── data<br>
│   └── 2011_09_26<br>
│       ├── 2011_09_26_drive_0001_sync<br>
│       │   ├── image_00<br>
│       │   │   ├── data<br>
│       │   │   │   ├── 0000000000.png<br>
│       │   │   │   ├── 0000000001.png<br>

- 终端运行<br>
d ~/ros2_ws<br>
colcon build --cmake-clean-cache<br>
source ./install/setup.bash<br>
ros2 run ros2_kitti_publishers kitti_publishers<br>
另一个终端运行<br>
ros2 daemon start<br>
rviz2<br>
week2
- ![这是效果图](作业2.png)
第三个终端运行
- rqt