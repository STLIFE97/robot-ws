# 小车开箱使用与基本配置。

## 1. 小车组件介绍
- 1. 小车主体

  ![image](https://github.com/RichardMJT/robot-ws/assets/51042944/bc64fe06-7ccb-4ce8-ab6d-ab2530c6cb7e)

- 2.  ROS2GO U 盘系统


  ![image](https://github.com/RichardMJT/robot-ws/assets/51042944/033f1909-62ac-4f48-b3df-8b9e70d939f8)
  
```
内置完整ROS开发环境，无需配置，可直接插入电脑使用。
```
```
设备要求：
  1.计算机支持UEFI
```
- 3. 接收天线
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








