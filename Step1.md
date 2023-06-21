# 小车开箱使用与基本配置。

## 1. 小车组件介绍
- 1. 小车主体

  ![image](https://github.com/RichardMJT/robot-ws/assets/51042944/bc64fe06-7ccb-4ce8-ab6d-ab2530c6cb7e)
  ```
  TIANBOT迷你机器人配备360°激光雷达传感器，集成差速运动控制系统，只需3步即可实现SLAM建图导航功能，从开机到建图导航仅需数秒钟，快速帮您使用ROS机器人操作系统控制与构建智能机器人，同时可通过预置接口，连接扩展模块，轻松拓展更加丰富的应用场景。
  ```
  ```
  指示灯说明：
  1. 系统状态指示灯
     黄灯闪烁：热点模式启动30S内需要连接到TBMINI-XXX热点
     绿色常亮：已有客户端正常连接到TBMINI-XXX热点
     白灯常亮：进入遥控控制模式，可以在网页端进行遥控控制
  2. 雷达状态指示灯
     红灯常亮，蓝灯常亮，已正常配对连接
     红灯闪烁，此时雷达未连接成功，需检查线路以及接收器是否连接正常
  3. 电量指示灯
     在一格时指示灯闪烁，电量过低，处于该状态时，请立即充电，系统在此电量时，将无法保证正常工作
  ```
- 2.  ROS2GO U 盘系统


  ![image](https://github.com/RichardMJT/robot-ws/assets/51042944/033f1909-62ac-4f48-b3df-8b9e70d939f8)
  
```
U盘中预装有基于Ubuntu的深度定制的Ubuntu18.04+ ROS Melodic，内置完整ROS开发环境，无需配置，可直接插入电脑使用。
```
```
设备要求：
  1.计算机支持UEFI
```
- 3. 接收天线
     
     ![image](https://github.com/RichardMJT/robot-ws/assets/51042944/11634332-9b4a-4c3f-af30-8ee6968e558c)

```
TODO
```

## 2 链接启动
- 1. ROS2GO U 盘系统启动

系统盘中已经预置了ROS2以及所需要的驱动，用户只需要将其提供的U盘插入电脑即可使用，具体步骤如下：
```
1. 将ROS2GO插入电脑的USB端口（USB端口协议需要为3.0）
2. 进入BIOS，启动项选择"TIANBOT ROS2GO"（各品牌按键不同，具体参考https://zhuanlan.zhihu.com/p/358043625）
3. 之后选择保存并重启，进入系统
```
进入 ROS2GO 系统后界面
```
TODO picture
```
- 2. 小车链接

进入系统后将小车与电脑进行连接，具体步骤如下：
```
1. 长按小车上的电源键3秒，在出现“滴”的一声后小车开启，机关雷达开始转动，系统灯黄灯闪烁，设备进入热点模式（首次使用）
2. 热点模式持续30秒，迷你机器人会创建TBMINI-XXXX热点，该热点未加密，使用电脑连接该热点，系统状态指示灯变为绿色。
```
连接小车成功后界面：
```
TODO picture
```

- 3. 初始化测试

电脑连接小车后，依次执行一下命令，完成系统的初始化

1. 打开终端输入以下命令：运行迷你机器人驱动
```
roslaunch tianbot_mini bringup.launch
```
2. 打开新终端输入以下命令：运行雷达驱动
```
roslaunch tianbot_mini lidar.launch
```
3. 打开新终端输入以下命令：运行SLAM
```
roslaunch tianbot_mini slam.launch
```
4. 打开新终端输入以下命令：运行键盘遥控
```
roslaunch tianbot_mini teleop.launch
```
```








