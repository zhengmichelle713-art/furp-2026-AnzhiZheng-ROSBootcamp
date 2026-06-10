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
