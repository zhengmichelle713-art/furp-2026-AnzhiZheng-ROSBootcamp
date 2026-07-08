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


robot link 与 joint
1. link（连杆）：机器人身上硬的、不会变形的零件，一块硬壳、一个轮子、底座、雷达支架，相    当于人的胳膊、大腿
   - 差速小车
     base_link （车身底盘）、left_wheel（左轮子）、right_wheel（右轮子），每一样单独      都是一个 link
     连杆本身不能动，是固定硬块
2. joint（关节）：把两个连杆连在一起、能活动的连接部位，就是关节，相当于人的肩膀、膝盖
   关节规定两个连杆之间能怎么动
   - 差速小车
     left_wheel_joint: 连接车身 base_link 和左轮 left_wheel
     right_wheel_joint: 连接车身 base_link 和右轮 right_wheel
     只有这两个能动的关节专门用来驱动轮子转动
     差速小车的轮子关节是旋转关节：车身底盘和轮子中间的转轴，轮子能绕轴转圈
     
与差速运动学、ROS2 的关系
1. 在 URDF 机器人模型文件里，写清楚 link、joint 位置
   电脑能自动算出左右两个轮子相隔多远 L、轮子半径多大 r
   差速运动学计算也需要用到以上数据
2. ROS2 差速控制器（diff_drive_controller）依靠 joint 名称识别驱动轮
   eg.: 配置文件里写 left_wheel_names: ["left_wheel_joint"], 程序才知控制哪两个转轴
3. Gazebo 虚拟小车读取 joint，模拟轮子转动
   收到`/cmd_vel`速度指令，算出左右轮转速，直接控制这两个关节旋转，画面里的轮子就会       转，小车前进拐弯  


URDF 和 Xacro
URDF：机器人的身份证 + 组装说明书
1. 里面写清楚机器人所有零件 link、joint
2. 电脑 / Gazebo/ROS2 读这份文件，都这份文件，就能知道机器人长什么样、零件在哪、轮子多    大、两轮隔多远
3. 差速小车里靠 URDF 定义：车身、左轮、右轮，还有连接车身和轮子的旋转关节
URDF 的缺点：
纯原始 URDF 只能写固定文字，没有任何简化功能：
- 同样尺寸、同样形状要重复复制一大段代码
- 轮半径 r、轮距L 这种数字改一处、所有地方都得手动改，很容易改错
- 不能算数学公式、不能批量生成零件，写起来又长又麻烦
死板、代码重复

Xacro：URDF 的升级版简化工具，相当于给 URDF 加了“快捷功能”，后缀`.xacro`
       不会直接被 ROS/Gazebo 读取，使用时会自动把 xacro 翻译成标准 urdf
Xacro 的功能：
1. 定义变量
   把固定尺寸单独存起来，只改一处全局生效
   eg.:
   ```
   <xacro:property name="wheel_r" value="0.05"/>
   <xacro:property name="wheel_sep" value="0.3"/>
   ```
   后面写轮子尺寸直接`${wheel_r}`,改数值只改上面一行
3. 宏 Macro（模板）
   重复的零件做成模板，左右轮子只写一套代码，调用两次即可，无需复制粘贴
4. 简单数学计算
   可以做加减乘除，比如轮距一半`${wheel_sep / 2}`,不用手动算数字填进去
写说明书的便捷工具，支持变量、模板、计算，简化代码，最后自动转为 URDF 给机器人软件使用

二者关系
1. URDF：底层标准格式，所有机器人软件认识它，不能简化、没有变量
2. Xacro：预处理器工具，写代码使用它简化，运行前自动编译、展开成纯 URDF
3. 流程：写`.xacro`文件 → 程序自动转成标准 URDF → Gazebo/ROS2 控制器读取 URDF 模型

与差速运动学、ROS2 的关系
1. xacro 统一管理 `wheel_r`轮半径、`wheel_sep`轮距
2. 转化后的 URDF 会把轮子位置尺寸写死
3. diff_drive_controller、Gazebo 差速插件读取 URDF里的几何参数，带入差速运动学公式计    算轮速
4. 如果尺寸写错，小车前进、转弯、里程计全都不准，xacro只用改一个变量，修复很方便


robot_state_publisher
机器人状态播报器
ROS2 里一个专门读取机器人模型、然后不停广播所有零件位置的小程序
读模型 + 读轮子转角，计算轮子相对车身的位置，广播 TF

robot_state_publisher 运转需要：
1. URDF/Xacro 文件
   robot_state_publisher 启动第一件事：读取写好的小车 URDF/Xacro 文件，把整个机器人     结构装（长什么这样子、零件固定的安装距离）进去
2. /joint_states 话题（各个活动 joint 实时转动角度）
   不管是 Gazebo 虚拟小车，还是真实实体小车，都会不停发送消息 `/joint_states`,里面写     了“现在左、右轮分别一共转了多少圈”
   
robot_state_publisher 完整的工作流程：
1. 开机读取 xacro 模型，记住车身、轮子的固定尺寸
2. 时刻监听`/joint_states`，获取做右轮字当前转了多少角度
3. 根据模型尺寸 + 轮子转动角度，自动计算：轮子相对于车身底座（base_link）的事实坐标
4. 持续向外广播 TF 坐标变换（一套位置对照表）
5. RViz 可视化窗口、激光雷达、导航程序接受这份坐标表，才能正常工作

和里程计 odom 的区别：
odom：获取整台小车在整个房间的那个位置、车头朝哪边
robot_state_publisher: 只关心小车自己身上零件相互的位置（轮子相对于车身在哪、雷达相对于车头在哪）


RViz
机器人的监控显示屏
机器人所有看不见的数据、小车长什么样、在哪、障碍物在哪，在这个窗口礼券都能画出来
robot_state_publisher、tf、/odom、激光雷达数据，最后都送到 RViz 上可视化

RViz 可以看到差速小车
1. 小车实体模型
   车身、左右两个轮子完整显示，发`/cmd_vel`让小车前进转弯。RViz 里轮子会跟着同步转动
   原理：robot_state_publisher 算好轮子相对车身的位置，RViz 接收 TF 画出来
2. 小车的全局位置（odom 坐标）
   窗口里有个网格地面，能看见小车在网格上跑动、拐弯，对应里程计算出来的 x、y、车头角度
3. 激光雷达扫描的障碍物
   小车前方会飘出一堆彩色小点，小点就是墙、桌子、凳子。机器人靠这些点避障、导航，人在      RViz 能一眼看清周围环境
4. 坐标坐标系（TF）
   屏幕会出现小箭头：
   - base_link: 小车车身中心
   - odom：房间原点
     能只管看懂各个零件、传感器的相对位置，排查程序坐标错乱问题

和 Gazebo 的区别：
Gazebo: 虚拟训练场，小车真的在里面跑、会撞墙、有物理摩擦力，是仿真运行环境
RViz：观察窗口，只负责画图展示数据，不能控制小车运动，小车不会在 RViz 碰撞，纯可视化工具

整套运行流程：
1. 写好小车 xacro 模型
2. 启动 robot_state_publisher 读取模型广播零件坐标 TF
3. 打开 Gazebo，虚拟小车接收`/cms_vel`前进转弯，发布轮子弯角
4. 打开 RViz，订阅 TF、里程计、雷达数据
5. RViz 窗口实施画出会动的小车、地面位置、周围障碍物，人直观监控机器人状态


静态 TF 与动态 TF
TF：两个零件之间的位置对照表，告诉电脑 A 零件相对于 B 零件在哪、朝那边

静态 TF（固定不动的坐标系）
静态：
两个东西装在一起，永远不会变位置、不会转角度，从开机到关机距离、角度完全不变
在小车中：
1. 激光雷达固定拧在小车车头，雷达和车身底座`base_link`相对位置永远不变
2. 摄像头卡在车顶，不会晃、不会转
3. 地图原点`map`和里程计原点`odom`（建图没漂移时固定）
`static_transform_publisher`发布静态 TF
开机只发一次，之后电脑会一直记住这个固定位置，不用每秒反复刷新
特点：
- 位置永久固定，不会随小车走动、轮子转动改变
- 只启动时发送一次，占用电脑资源很小
- 雷达、摄像头、支架这类固定外设都依赖于此

动态 TF（会不停变化的坐标关系）
动态：
两个东西相对位置 / 角度时时刻刻在变，小车一动，这个对照表就要一秒刷新好多次
举例：
1. 车身 ↔ 轮子（robot_state_publisher 发的动态 TF）
   车身`base_link`和左轮`left_wheel`、右轮`right_wheel`
   小车一前进，轮子不停旋转，轮子相对于车身的角度一直在变
   `robot_state_publisher`每一小段时间就重新算一遍轮子角度，不停刷新 TF
2. 房间原点 odom ↔ 车身 base_link（里程计 odom 发的动态 TF）
   小车在地面乱跑，车身在房间里的坐标一直在变，`/odom`里程计不停更新`odom`到             `base_link`的变换
机器人自身零件（轮子、关节）发布`robot_state_publisher`
小车全局地面位置发布差速控制器 / Gazebo 仿真插件（输出 odom TF）
特点：
- 相对位置 / 角度一直在变，几十毫秒刷新一次
- 程序全程持续不断广播，实时同步最新位置
- 能动的关节、走动的车身，都是动态 TF


TF tree 设计
<img width="1685" height="1279" alt="19ca959b8fdbe96cd24017d4968b228c" src="https://github.com/user-attachments/assets/d58f0d1d-66ce-4543-ad35-066798ef596f" />


base_footprint 车身投影坐标系（小车贴地面的中心点）
作用：导航避障、路径规划专用，导航算法只认地面这个点，不会考虑车身高度
与 base_link 的区别：base_link 一般在车身中心，离地有高度

laser_link 激光雷达坐标系（雷达自己的原点）
作用：雷达扫出来的障碍物坐标，均以 laser_link 为基准，程序会自动换算到 base_link、map

imu_link 惯性传感器坐标系（陀螺仪 / 加速度计原点）
作用：IMU 输出车身倾斜、旋转角速度，所有数据以 imu_link 为原点，用来辅助修正里程计漂移



MuJoCo 仿真环境
仿真节点功能
   - 加载机器人模型
   - 接收`/cmd_vel`速度指令（Twist 消息，线速度 x、角速度 z）驱动底盘
   - 输出传感器数据：`/scan`激光雷达、`/odom`里程计
   - 发布 TF 树：`map(无，SLAM生成) ← odom(里程计坐标系) ← base_link(机器人底盘中心)      ← lidar_link(激光雷达安装位置)`
   - 发布仿真时钟`/clock`，仿真时间核心

ROS工具包相关命令：  
- `teleop_twist_keyboard`: 键盘遥控，持续发布`/cmd_vel`控制机器人漫游建图
- `nav2-map-server`:	提供`map_saver_cli`，保存建图结果为 pgm 栅格图 + yaml 地图配     置文件
- `tf2_tools`: `view_frames`可视化 TF 坐标系树，排查坐标变换断层问题
- `use_sim_time:=true`:
   SLAM、RViz、所有依赖传感器时序的节点必须开启仿真时间，否则
   1. 激光雷达数据、TF 变换时间戳不匹配
   2. SLAM 无法匹配激光扫描，地图完全不更新、飘移严重
   3. RViz 操作：Global Options 勾选`Use Sim Time`，Fixed Frame 固定设为`map`           （SLAM输出全局坐标系）。
- `ros2 run tf2_tools view_frames`：生成 pdf 坐标系树，快速判断是否存在变换断层
- `ros2 topic list`：查看所有话题，确认 /scan、/odom、/clock、/map 存在
- `ros2 topic echo /scan`：打印激光雷达原始数据，验证雷达正常输出
- `ros2 topic echo /odom`：查看里程计位姿、速度是否随机器人运动变化
- `ros2 topic echo /clock`：验证仿真时钟正常发布（无输出则 sim_time 失效）
- `ros2 pkg list | grep xxx`：检查功能包是否正确安装、编译成功

SLAM 工作流程:
1. 订阅`/scan`激光雷达数据、`/odom`里程计、读取 TF 底盘 - 激光变换；
2. 扫描匹配：激光点云和历史地图匹配，修正里程计漂移；
3. 回环检测：机器人回到历史区域时校正全局位姿，消除长时间累积漂移；
4. 实时生成`/map`占据栅格地图 OccupancyGrid；
5. 输出`map → odom`坐标变换，建立全局世界坐标系

作业
1. 修改后的 SLAM Toolbox 参数文件
   <img width="726" height="572" alt="屏幕截图 2026-06-28 202230" src="https://github.com/user-attachments/assets/14944e08-7924-46d8-8442-b5384dcca41b" />
2. 建图运行截图
   <img width="2298" height="1300" alt="屏幕截图 2026-07-01 141730" src="https://github.com/user-attachments/assets/4869ef3e-672e-4f31-9b06-ed768f596969" />
3. 保存的地图文件（`.pgm` 与 `.yaml`）
   <img width="671" height="440" alt="image" src="https://github.com/user-attachments/assets/57341e98-3920-4d2b-be62-c5b5a4a855d8" />
   <img width="730" height="197" alt="image" src="https://github.com/user-attachments/assets/3a541dfc-58a9-4441-b1ad-41069450f9e3" />
4. 参数选择、遇到的问题和解决方法
   - 参数选择
     base_frame: "base_link"
     odom_frame: "odom"
     map_frame: "map"
     TF 树固定链路：`map → odom → base_link → lidar_link`
     
     scan_topic: "/scan"           Mujoco 仿真发布激光话题固定名称
     min_laser_range: 0.1          过滤雷达自身近处盲区，0.1 米内无效点会干扰匹配
     max_laser_range: 12.0         迷宫房间最大宽度远小于 12m，完整保留全部墙体数                                       据；太小会丢失远处墙壁，匹配约束变少，漂移加重
                        
     
     resolution: 0.05              代表每一格栅格 = 5 厘米 = 0.05 米
                                   0.05 是平衡精度和内存的最优值：更小（0.025）地                                      图文件巨大、卡顿；更大（0.1）墙体模糊，匹配不准                                      漂移
     
     mode: "mapping"               在线实时建图模式，刷图专用
     
     loop_closure_enable: true     走完闭环路线后自动修正里程计累积漂移，把跑偏的                                       地图拉回原位；关闭则漂移只会越来越严重
     
     loop_search_max_dist: 5.0     机器人在 5 米范围内搜索曾经走过的区域做回环匹                                        配；迷宫尺寸不大，5 米能保证频繁触发校正；数值                                       太大计算卡顿，太小很难找到闭环
     
     scan_matcher_type: "PLICP"    针对激光雷达优化的 ICP 匹配算法，比传统 ICP 抗                                      噪声更强，仿真激光抖动环境下匹配更稳，减少漂移
     minimum_travel_distance: 0.1  小车至少前进 0.1 米才执行一次地图更新
     minimum_travel_rotation: 0.1  小车至少旋转 0.1 弧度才更新地图
     
     map_update_interval: 1.0      每 1 秒全局刷新一次栅格地图，平衡流畅度与计算压力
     transform_timeout: 0.2        SLAM 等待 TF 坐标变换的最长时间 0.2 秒；仿真传感                                    器数据存在微小延迟，给 0.2 秒容错，不会因为时间差                                    丢失变换导致匹配失败
   - 遇到的问题
   - 解决方法


# Week 3
作业
<img width="448" height="145" alt="image" src="https://github.com/user-attachments/assets/1849502f-c6f9-4ef3-a2da-3963fd3f580b" />
<img width="2305" height="1241" alt="屏幕截图 2026-07-05 191727" src="https://github.com/user-attachments/assets/1fe57a67-92d9-4964-8629-76b8e0406dba" />
<img width="2298" height="1199" alt="屏幕截图 2026-07-05 194157" src="https://github.com/user-attachments/assets/082a8fd8-4ba0-4e46-83cc-99b5263c514c" />
<img width="2199" height="483" alt="屏幕截图 2026-07-05 201211" src="https://github.com/user-attachments/assets/f14c7b78-a16d-4c1d-9ba3-24cc57a0e529" />
<img width="2289" height="1101" alt="屏幕截图 2026-07-05 201325" src="https://github.com/user-attachments/assets/014414c5-67b7-45e2-804f-79ce76195d9d" />
<img width="2290" height="1252" alt="屏幕截图 2026-07-05 200559" src="https://github.com/user-attachments/assets/63785d45-17c3-4848-9ff0-eace87b7667a" />
<img width="1605" height="595" alt="image" src="https://github.com/user-attachments/assets/de27aa7b-0204-478f-936e-4836d67c68ec" />
第二次尝试
<img width="2287" height="1247" alt="屏幕截图 2026-07-06 140204" src="https://github.com/user-attachments/assets/15f609a3-f976-418c-b3bd-406deeb2d3a4" />
<img width="1898" height="983" alt="image" src="https://github.com/user-attachments/assets/4ca12515-64df-4af8-87da-f19d4b699433" />
录制的rosbag
<img width="1591" height="619" alt="屏幕截图 2026-07-06 205258" src="https://github.com/user-attachments/assets/9920acbe-244d-4de1-ab0f-d5893a149eaa" />
<img width="1789" height="999" alt="屏幕截图 2026-07-06 205345" src="https://github.com/user-attachments/assets/e715e498-9ec9-41e5-a0dd-8aa9f9d6a702" />
打分的新节点
<img width="851" height="746" alt="image" src="https://github.com/user-attachments/assets/8c8bd3f1-5925-4e56-a68a-c10e0ae39eae" />
<img width="2212" height="482" alt="image" src="https://github.com/user-attachments/assets/2d44d948-944d-4dc5-9b43-0932a9249ede" />
只做可视化的新节点
<img width="1368" height="1086" alt="image" src="https://github.com/user-attachments/assets/8c512b33-43bc-4348-b570-5771a5ca267a" />
<img width="844" height="934" alt="image" src="https://github.com/user-attachments/assets/0a828f3d-431a-4c0c-8b1b-1df75ba62cc0" />
<img width="2282" height="1264" alt="image" src="https://github.com/user-attachments/assets/f93016a4-75e0-439a-887d-b25b4a6ddf6a" />
