# Week 0
这周是准备阶段，主要复习了之前是如何把 VMware Workstation 虚拟机安装到电脑上的，回顾了将 Ubuntu 22.04 安装到虚拟机的相关操作。同时学习 Linux 终端基础知识，以及本周建议尝试的 Linux 的命令。另外，通过阅读提供的资料，成功将 ROS2 安装到了 Linux 系统上，并初步练习了 turtlesim 的基础操作。

通过本周的学习，我了解到终端是用来输入命令、操作系统，代替图形鼠标操作的文字交互窗口。 Shell 是终端里的命令解释器，在 Ubuntu 系统中，默认的命令解释器是 Bash。

打开终端的快捷键是 `Ctrl + Alt + T`，关闭终端可以使用 `Ctrl + D`。打开终端后，第一行通常是：
```
az@az-virtual-machine:~$
```
其中：
- `az` 是用户名
- `@` 是分隔符
- `az-virtual-machine` 是主机名
- `:` 是分隔符
- `~` 代表当前所在的用户主目录
- `$` 是普通用户的命令提示符


对于Linux常用命令的学习与尝试，我附图在下面

<img width="1608" height="1217" alt="image" src="https://github.com/user-attachments/assets/73192c63-6231-4b5d-8a50-964d0b3c832b" />
<img width="1773" height="1180" alt="image" src="https://github.com/user-attachments/assets/ebb2a8a3-215f-447f-a56e-a50133252f38" />
<img width="1584" height="1095" alt="image" src="https://github.com/user-attachments/assets/b2efcb50-4229-4a58-a9e3-e899f433209e" />
<img width="1587" height="390" alt="image" src="https://github.com/user-attachments/assets/713267e3-e1cc-4385-a414-d6e6eac5fe17" />
<img width="1448" height="950" alt="image" src="https://github.com/user-attachments/assets/a44a840d-33d2-4ca0-9a77-d4ba6fa46d10" />


对于 ROS 2 smoke test

<img width="2292" height="1242" alt="image" src="https://github.com/user-attachments/assets/6312df02-15b4-47e7-a1f8-84d1108ef63c" />
<img width="1754" height="1074" alt="image" src="https://github.com/user-attachments/assets/63d6d546-2f8a-4968-9035-ba4ec9ad7e97" />
<img width="1490" height="752" alt="image" src="https://github.com/user-attachments/assets/0f0bf2c8-bf37-41d6-8125-2453962ba7ec" />


然后是turtlesim的使用

<img width="1598" height="1090" alt="image" src="https://github.com/user-attachments/assets/e7890e4c-c0cd-48ee-92f6-ca2a21369e0e" />


下一步我将学习 node，topic，service，action的相关概念，创建 ROS 2 工作空间和 Python 包，尝试写发布者和订阅者节点，建立 launch 文件，录制 rosbag，并用 rqt_graph 命令查看节点的连接关系。




# Week 1
节点，话题，服务，动作的相关概念及作用为

<img width="784" height="1030" alt="image" src="https://github.com/user-attachments/assets/6e2341ac-a737-48b8-9b00-2dbb05dcd843" />


以turtlesim为例，展示 ros 2 的节点列表

<img width="1580" height="541" alt="屏幕截图 2026-06-11 172118" src="https://github.com/user-attachments/assets/fa8da80d-ee73-4b82-bf97-8ad2ae46d337" />


用 rqt_graph 展示 ros2 主题列表

<img width="2190" height="928" alt="image" src="https://github.com/user-attachments/assets/624d4c43-83d6-4952-a3a0-906a26923440" />


查看主题发布的数据

<img width="2066" height="1252" alt="image" src="https://github.com/user-attachments/assets/6e0a77d3-5276-4b31-a7d8-5de828d28800" />
<img width="1332" height="652" alt="image" src="https://github.com/user-attachments/assets/2f05b6b4-f0c8-4c1b-82dc-3034c37d3187" />


查看主题的详细信息：
-发布者和订阅者的节点名称和命名空间
-主题类型
Qos 配置文件

<img width="711" height="1130" alt="image" src="https://github.com/user-attachments/assets/5f4d0201-d760-48ec-9c5c-565e9efbd568" />


ros2 接口显示

<img width="782" height="328" alt="image" src="https://github.com/user-attachments/assets/0856c6f6-ecc0-4a7b-944e-8c46704a1e29" />

由此了解消息期望的数据结构，这说明 /turtlesim 节点期望收到一个包含两个向量的消息，linear 这两个向量各有三个元素。


ros2 主题发布

<img width="2292" height="1242" alt="屏幕截图 2026-06-12 150654" src="https://github.com/user-attachments/assets/b355ebfc-218f-418a-b1fb-26d8654b283f" />
<img width="2290" height="1250" alt="image" src="https://github.com/user-attachments/assets/d2f92100-4b38-4cbc-a37d-3508799aa19d" />

不提供任何命令行选项，`ros2 topic pub`以1 Hz 的频率稳定地发布命令（画圆圈）--只想主题发布一次数据（而非持续发布）`$ ros2 topic pub --once -w 2 /turtle1/cmd_vel geometry_msgs/msg/Twist "{linear: {x: 2.0, y: 0.0, z: 0.0}, angular: {x: 0.0, y: 0.0, z: 1.8}}"}` [在 pub 后添加 --once - w 2]（--once 是可选参数，代表“发布一条消息然后退出”；- w 2 也是可选参数，代表“等待两个匹配的订阅”，其中，2 代表同时订阅的 turtlesim 和 echo 两个主题）

运行`$ ros2 topic echo /turtle1/pose`命令后，/turtlesim 节点也向 pose 发布数据到新的 echo 节点订阅的 pose 主题。


ros2 服务列表显示、类型显示、服务查找及服务调用（先使 turtle 运动，再清除其绘制的所有线条；通过调用`/sqawn`并设置参数来生成一个新的 turtle）

<img width="2289" height="1249" alt="屏幕截图 2026-06-12 184326" src="https://github.com/user-attachments/assets/56b291f1-087a-4b1b-8ecf-54663365ff00" />

