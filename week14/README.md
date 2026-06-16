# Week 14 单人项目：ROS2 小乌龟迷宫探索

## 项目简介
本项目基于 ROS2 的 TurtleSim 仿真环境，实现了小乌龟在迷宫环境中的移动控制与探索。通过键盘或网络控制方式，实现小乌龟在地图中的前进、转向和路径探索，并完成目标点到达任务。

## 项目目标
- 熟悉 ROS2 节点通信机制
- 学习 Topic 消息发布与订阅
- 掌握 TurtleSim 仿真环境使用方法
- 实现小乌龟移动控制
- 完成迷宫探索实验

## 开发环境
- Ubuntu 22.04
- ROS2 Humble
- Docker
- Python 3

## 项目结构

```text
turtle_maze_project/
├── src/
│   ├── turtle_controller.py
│   ├── maze_navigation.py
│   └── launch/
├── screenshots/
├── README.md
└── report.pdf
```

## 操作过程总结

### 1. 环境搭建
启动 Docker 容器并配置 ROS2 开发环境。

```bash
docker start ros2_container
docker exec -it ros2_container bash
```

### 2. 启动 TurtleSim

```bash
ros2 run turtlesim turtlesim_node
```

成功启动后出现小乌龟仿真窗口。

### 3. 编写控制节点

创建 Python 节点，通过发布 `/turtle1/cmd_vel` 控制小乌龟运动。

主要功能：
- 前进
- 后退
- 左转
- 右转
- 自动寻路

### 4. 运行控制程序

```bash
ros2 run my_package turtle_controller
```

### 5. 迷宫探索测试

通过控制算法让小乌龟在迷宫环境中移动：

1. 获取当前位置
2. 判断障碍方向
3. 规划下一步路径
4. 持续移动直至到达终点

### 6. 项目结果

成功完成：

- ROS2 节点创建
- Topic 通信
- 小乌龟运动控制
- 迷宫路径探索
- 仿真测试验证

## 遇到的问题

| 问题 | 解决方法 |
|--------|--------|
| 节点无法启动 | 检查 ROS2 环境变量 |
| 无法控制小乌龟 | 检查 Topic 名称 |
| Docker 网络异常 | 重启容器并重新连接 |
| 运动方向错误 | 调整角速度参数 |

## 实验收获

通过本项目掌握了：

- ROS2 基础开发流程
- Docker 运行机器人项目
- 发布/订阅通信机制
- 仿真机器人控制方法
- 机器人路径规划基础思想

## 项目完成效果

成功实现 ROS2 小乌龟迷宫探索与运动控制，为后续移动机器人开发奠定基础。
