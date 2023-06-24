# 激光雷达密封环境的地图的构建与对比

## 1. 激光雷达构建环境地图
- 1. 激光雷达接收器连接电脑上
  


- 2. 检查是否正常被连接：
```
ls /dev/ttyUSB*
```

![image](image/1.png)
- 3. 启动ROS雷达驱动：
```
roslaunch tianbot_mini lidar.launch
```

![image](/image/2.png)
- 4. 若采样率 >=4k ,方为正常，若不大于等于4k：ctrl c 关闭驱动 ，重启即可
  
  第一次为3k
  
![image](https://github.com/STLIFE97/robot-ws/blob/main/image/2.png)

  第二次为5k（可以使用）
  
![image](https://github.com/STLIFE97/robot-ws/blob/main/image/3.png)

- 5. 新建终端，输入: rviz 打开可视化工具查看

   ![image](https://github.com/STLIFE97/robot-ws/blob/main/image/4.png)
 
- 6. 打开左下角 add ，在by topic 添加一个话题；选中：/tianbot_mini   /scan  LaserScan
 
 
- 7. 出现报错，在Global Options里的Fixed Frame里添加 tianbot_mini/laser 即可

  ![image](https://github.com/STLIFE97/robot-ws/blob/main/image/6.png)
- 8. 在LaserScan 列表的Size参数里，设置0.05使可视化更清晰
 
    ![image](https://github.com/STLIFE97/robot-ws/blob/main/image/7.png)

- 9. 查看现实与扫描地图对比

  1）门后
  
    ![image](https://github.com/STLIFE97/robot-ws/blob/main/image/8.1.png)![image](https://github.com/STLIFE97/robot-ws/blob/main/image/8.2.png)
  
  2）四周包围

  
    ![image](https://github.com/STLIFE97/robot-ws/blob/main/image/9.1.png)![image](https://github.com/STLIFE97/robot-ws/blob/main/image/9.2.png)
