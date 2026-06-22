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
节点，话题，服务，动作，参数的相关概念及作用为

<img width="784" height="1030" alt="image" src="https://github.com/user-attachments/assets/6e2341ac-a737-48b8-9b00-2dbb05dcd843" />
<img width="1010" height="921" alt="image" src="https://github.com/user-attachments/assets/8e970268-5185-4146-8a84-65b560a61b5b" />
<img width="1030" height="1194" alt="image" src="https://github.com/user-attachments/assets/cb414804-8674-4056-a493-671617ace546" />
<img width="1028" height="1247" alt="image" src="https://github.com/user-attachments/assets/269ce257-db82-4e9b-abdd-36417adfa411" />
<img width="1122" height="1128" alt="image" src="https://github.com/user-attachments/assets/f0375ee7-587c-4f3e-b117-328820ccd1f8" />
<img width="623" height="1209" alt="image" src="https://github.com/user-attachments/assets/e7deed3e-8e01-4c84-a3df-1f6a9a644194" />
<img width="1315" height="1178" alt="image" src="https://github.com/user-attachments/assets/959f668d-74ec-427c-b4dc-f1918b2cdb3f" />


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


ros2 查看节点信息、动作列表、动作类型、动作信息、接口显示，以及发送操作目标、查看此目标的反馈

<img width="2286" height="1188" alt="屏幕截图 2026-06-14 115941" src="https://github.com/user-attachments/assets/88b32bad-10ce-4d97-9d0b-ded2c0144aec" />


查看参数列表、获取参数、在参数集中更改参数值、参数转储、参数加载以及节点启动时加载参数文件

<img width="1910" height="1050" alt="image" src="https://github.com/user-attachments/assets/02415852-2402-4068-9a5f-f6c8e196175a" />
<img width="912" height="756" alt="image" src="https://github.com/user-attachments/assets/6e06699a-2bba-46a2-aa20-4c12551734eb" />


用 rqt_console 查看日志，并进行相关设置

<img width="1198" height="1195" alt="image" src="https://github.com/user-attachments/assets/16c42aae-c00c-43e7-b385-a8b3ddae87e8" />
<img width="2296" height="820" alt="image" src="https://github.com/user-attachments/assets/18c86706-301e-4789-babd-efcc365e694c" />
<img width="2292" height="822" alt="image" src="https://github.com/user-attachments/assets/c8ec29ff-d111-4ec7-98b4-a8bb9cc56c35" />


launch 文件

<img width="781" height="810" alt="image" src="https://github.com/user-attachments/assets/3f17b6e9-71be-4ae6-8a0a-df5d971990e5" />
<img width="1364" height="850" alt="image" src="https://github.com/user-attachments/assets/9279dda0-195e-4456-a201-94d521310e30" />


ros2 bag

<img width="771" height="1188" alt="image" src="https://github.com/user-attachments/assets/8e09012e-7955-4466-89fa-9145acec55b2" />
<img width="2290" height="1248" alt="image" src="https://github.com/user-attachments/assets/9314a812-981f-42f3-b550-8783cc0b548e" />


用 colcon 构建软件包

<img width="1228" height="1232" alt="image" src="https://github.com/user-attachments/assets/9d11ccf8-f628-43f0-b887-6c7f625cd5e8" />
<img width="1852" height="1219" alt="image" src="https://github.com/user-attachments/assets/d8ae6dd0-67d2-4c14-8895-86e0b34d1895" />
<img width="1723" height="1229" alt="image" src="https://github.com/user-attachments/assets/aa5b0b17-3121-4932-9d64-320cac9b1a58" />


安装 colcon -- 创建工作区 -- 添加一些 source -- 构建工作区

<img width="2292" height="1206" alt="image" src="https://github.com/user-attachments/assets/281b3502-b4f4-42cc-950e-6a1b55478b6e" />

运行测试

<img width="2294" height="1204" alt="image" src="https://github.com/user-attachments/assets/655d7fec-af45-4670-aa6b-c2db6902e9da" />
<img width="2290" height="1248" alt="image" src="https://github.com/user-attachments/assets/1cf4c163-22d3-42b2-97d5-d431985201cc" />
<img width="2294" height="700" alt="image" src="https://github.com/user-attachments/assets/41360dd8-3800-4235-af9e-c554222e20f3" />

环境来源 -- 试用演示版

<img width="1536" height="486" alt="image" src="https://github.com/user-attachments/assets/21a244d6-3b5d-4504-b3f7-170f6c92fc9a" />

设置 colcon_cd

<img width="932" height="164" alt="image" src="https://github.com/user-attachments/assets/afd8a2cd-e362-4d3a-b367-62985eb45846" />

通过命令构建好的目录

<img width="722" height="896" alt="image" src="https://github.com/user-attachments/assets/7ab0b0e8-7f3d-4257-af7e-448309d7e74e" />


创建工作区
source ROS2 环境 -- 创建新目录 -- 克隆示例仓库 -- 解决依赖关系 -- 使用 colcon 构建工作区 -- 获取叠加层 -- 修改叠加层

<img width="1330" height="1214" alt="image" src="https://github.com/user-attachments/assets/f7f4aa1a-fd07-4db4-8ec1-b62a108e72db" />
<img width="1747" height="1181" alt="image" src="https://github.com/user-attachments/assets/5adfc550-ed15-4388-a300-5070f783c222" />
<img width="975" height="1183" alt="image" src="https://github.com/user-attachments/assets/24b90b71-b28e-41d9-bd9d-36711a0205b4" />
<img width="2276" height="1248" alt="image" src="https://github.com/user-attachments/assets/22cda03c-39ca-4164-baea-d5ed17637cac" />
<img width="896" height="746" alt="屏幕截图 2026-06-15 173858" src="https://github.com/user-attachments/assets/077df088-638f-443a-943c-05594eade0e7" />


创建软件包
<img width="1320" height="1148" alt="image" src="https://github.com/user-attachments/assets/187c5e7a-e23c-4e37-b2bc-3c9efad4fb15" />
<img width="1521" height="1158" alt="image" src="https://github.com/user-attachments/assets/ad79d98d-98c9-4e3c-aec8-2996e2178f19" />
<img width="1213" height="1132" alt="image" src="https://github.com/user-attachments/assets/d6238d92-12a1-45d9-8c41-26dbae83c883" />
<img width="928" height="1234" alt="image" src="https://github.com/user-attachments/assets/5dd40e62-4a8d-4ef0-9650-8e1395456415" />
<img width="1399" height="1196" alt="image" src="https://github.com/user-attachments/assets/2a586e84-4108-4f3c-9c21-7b6d841b68d0" />
<img width="1738" height="1226" alt="image" src="https://github.com/user-attachments/assets/e77ca031-f87c-4a31-b1d1-d870bfe9001b" />
第二个终端的运行路径有错 应该在`~/ros2_ws`下运行
<img width="747" height="489" alt="image" src="https://github.com/user-attachments/assets/3525a29e-8ee4-4725-b020-77e338be0ef0" />
<img width="1808" height="752" alt="image" src="https://github.com/user-attachments/assets/3b235e2b-d582-4d14-b770-295367a23397" />


用 Python 编写一个 publisher 和 subscriber 程序
<img width="1322" height="1167" alt="image" src="https://github.com/user-attachments/assets/93f42657-dbfc-4d59-a880-21897d910681" />
<img width="1312" height="1204" alt="image" src="https://github.com/user-attachments/assets/0bd4b1df-76c1-4e7f-a4c1-8d312df6d576" />
<img width="874" height="1186" alt="image" src="https://github.com/user-attachments/assets/4207c7b0-9fe2-45d3-b9e5-b3224b776c1f" />
<img width="1257" height="1131" alt="image" src="https://github.com/user-attachments/assets/3d725a6c-2e6e-44c9-8505-2e162772a674" />
<img width="1197" height="1210" alt="image" src="https://github.com/user-attachments/assets/a973e86d-7355-43fa-b7e1-37be255d9f2d" />
<img width="2292" height="1256" alt="image" src="https://github.com/user-attachments/assets/a72be21f-fc27-4c26-a625-9c13ac0ee050" />
<img width="2294" height="1252" alt="image" src="https://github.com/user-attachments/assets/ba1a76a2-cd67-41fe-97fa-02b744e1bc12" />


用 Python 编写一个 service 和 client 程序

<img width="1850" height="1154" alt="image" src="https://github.com/user-attachments/assets/c06ca2e6-2c01-4b7e-9b2b-ecc1115b8b4c" />
<img width="741" height="1123" alt="image" src="https://github.com/user-attachments/assets/93005778-ed6b-4381-aca8-6d75a6b3664e" />
<img width="1034" height="1164" alt="image" src="https://github.com/user-attachments/assets/a4ea104d-855a-4bad-ae25-e8b603814aa5" />
<img width="920" height="1215" alt="image" src="https://github.com/user-attachments/assets/6c3b6ff7-029f-4b82-a40f-9a9f3257ae15" />
<img width="1641" height="807" alt="屏幕截图 2026-06-19 124258" src="https://github.com/user-attachments/assets/ee8943ba-62b7-4daf-82a6-3da664e8c5d1" />
<img width="1641" height="807" alt="屏幕截图 2026-06-19 124258" src="https://github.com/user-attachments/assets/2d69c639-fafe-4e4e-9e0d-604df76e3b22" />



# Week 2
差速驱动运动学：
定义：两个独立驱动轮的小车，它的左右轮分开转，靠两轮转速不一样来拐弯，这套计算轮子速度、车子走多块、往哪拐的算法，就叫差速运动学
- 轮子粗细半径 r ：决定轮子转一圈走的距离
- 两轮中间间距 L ：左右轮子隔开的宽度

正向运动学（轮子转多快 → 整车怎么走）：
轮子里有计数装置能读出左轮右轮各自的速度
- 车子往前的平均速度 = （左轮速度 + 右轮速度）÷ 2
- 车子拐弯转动快慢 = （右轮速度 - 左轮速度）÷ 两轮间距 L
  1. 两轮一样快：只直走，不拐弯
  2. 一轮快一轮慢：走弧线拐弯
  3. 一轮往前、一轮往后：原地转圈

逆向运动学（想要车子怎么走 → 算出左右该多快）：
车子以 v 速度往前走，每秒拐弯 ω 
右轮速度 = 整车前进速度 + （L × 拐弯速度）÷ 2
左轮速度 = 整车前进速度 -（L × 拐弯速度）÷ 2

里程计算位置：
持续记录轮子转速，一点点累加，算出车子现在的坐标、车头朝向，让机器人知道自己在哪

缺点：
只能前进后退、转弯，不能横着平移；地面打滑时计算出来的位置会不准

差速运动学在 ROS2 中的运用：
ROS2 是机器人统一管理程序的工具，差速运动学是它控制两轮小车的核心计算，全程自动算，不用人手算
- 接受走路指令（上层下发）
  遥控、自动导航程序会发统一消息`/cmd_vel`，只写车子前进速度、车头拐弯速度，不直接控制   左右轮子
- 内部自动运行【逆向运动学】
  ROS2 自带差速控制器，拿到前进 + 拐弯指令，自动套公式算出左右两轮目标转速，把转速命令    发给电机，控制轮子转动  
- 读取轮子反馈，运行【正向运动学】
  电极上的计数器实时传回左右轮真实转速，ROS2 再用正向公式算出整车实时前进、拐弯速度
- 积分算出位置，向外分发数据
  不断累加运动距离和转向角度，得到机器人当前坐标、朝向，产出两份关键信息：
  1. `/odom`里程话题：记录机器人位置，给导航、建图软件用
  2. TF 坐标变换：告诉雷达、摄像头机器人现在面朝哪个方向
- 两种使用场景
  1. 电脑仿真：Gazebo（电脑上的虚拟仿真软件，可以造出来假两轮差速小车，包含全套真实小车      的所有部件） 虚拟小车，内置差速插件，不用实物，提前测试行走逻辑
  2. 真实实体小车：搭配 ros2_control 硬件控制器直接操控真是电机，自主导航、避障
 
Summary：
导航 / 遥控器发整车行走指令 → ROS2 算逆运动学控制轮子 → 读取轮子转速正运动学 → 计算自身位置给导航地图使用，循环工作


`/cmd_vel`
cmd = command 命令、指令
vel = velocity 速度
/cmd_vel = 发给机器人的【速度指令通道】
它是 ROS2 里固定的一条信息通道，所有小车程序都统一走这个通道发走路命令
作为中间桥梁，上层导航 / 遥控器 ↔ 底层差速轮子驱动

其中的内容：
消息类型是 Twist，包含 linear、angular
1. linear.x: 向前 / 向后走的速度（往前正数，往后负数）
   linear.y、linear.z 差速小车永远是 0，它不能横着走、上下飞
2. angular.z: 转弯旋转速度（往右转正数，往左转负数）
   angular.x、angular.y 也永远是 0，小车不会上下歪头
For example：
- 只前进不拐弯：linear.x = 0.2, angular.z = 0
- 原地右转不往前走：linear.x = 0, angular.z = 0.5

和差速运动学的关联：
人、遥控、导航软件只需要发`/cmd_vel`，只说整车怎么走（前进、转弯），不用管左右轮子转多快
不管是真是小车的控制器，还是 Gazebo 虚拟小车插件，收到`/cmd_vel`之后，会自动运行差速逆运动学公式，换算出左轮、右轮各自该转多快，再控制轮子


