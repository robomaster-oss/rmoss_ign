![](rmoss_bg.png)
RoboMasterOSS是一个面向RoboMaster的开源软件栈项目，目的是为RoboMaster机器人软件开发提供了一个快速的，灵活的开发工具，支持算法原型研究和robomaster比赛应用开发。

> [RoboMaster竞赛](https://www.robomaster.com/)，全称为`全国大学生机器人大赛RoboMaster机甲大师赛` 。
>
> - 全国大学生机器人[RoboMaster](https://www.robomaster.com/)大赛，是一个涉及“机器视觉”、“嵌入式系统设计”、“机械控制”、“人机交互”等众多机器人相关技术学科的机器人比赛。
> - 在RoboMaster 2019赛季中，参赛队伍需自主研发不同种类和功能的机器人，在指定的比赛场地内进行战术对抗，通过操控机器人发射弹丸攻击敌方机器人和基地。每局比赛7分钟，比赛结束时，基地剩余血量高的一方获得比赛胜利。
>
> 更多详情参考官网：[www.robomaster.com](https://www.robomaster.com/)

# rmoss_ign

rmoss_ign是RoboMaster OSS中的基础项目，为RoboMaster提供Ignition Gazebo仿真支持，主要提供Ignition插件，相关机器人模型资源等。

## 1.主要模块

|            模块             |                           功能说明                           |
| :-------------------------: | :----------------------------------------------------------: |
|     `rmoss_ign_plugins`     |        RoboMaster相关Ignition Gazebo Simulator插件。         |
|      `rmoss_ign_base`       |   RoboMaster基本机器人Ignition-ROS通信（仿真MCU部分功能）    |
|     `rmoss_ign_referee`     |                  RoboMaster裁判系统（TODO）                  |
|    `rmoss_ign_resources`    | RoboMaster相关核心SDF模型资源，官方机器人模型和核心场地模型。 |
| `rmoss_ign_extra_resources` |                 RoboMaster相关额外模型资源。                 |

* `rmoss_ign_resources` 和`rmoss_ign_extra_resources`主要包含资源文件，体积较大，单独成库。

## 2.使用说明

* 目前仅支持`ROS2 foxy` & `Ignition Dome` 版本
* 环境依赖：
  *  [rmoss_interfaces](https://github.com/robomaster-oss/rmoss_interfaces) : ROS2 interfaces (.msg, .srv, .action) used in the RoboMaster OSS Projects

环境配置

```bash
#cd ros2 workspaces src
git clone https://github.com/robomaster-oss/rmoss_interfaces.git
git clone https://github.com/robomaster-oss/rmoss_ign.git
# 资源仓库比较大，可视情况使用。
#git clone https://github.com/robomaster-oss/rmoss_ign_resources.git --depth=1
#git clone https://github.com/robomaster-oss/rmoss_ign_extra_resources.git --depth=1
#cd ros2 workspaces
colcon build
```

* 相关功能包使用详见相应package的README.md

## 3.RMOSS Ign架构

![](rmoss_ign_arch.png)

* RMOSS Ign项目将遵循该架构进行开发。

## 4.维护者及开源许可证

Maintainer : Zhenpeng Ge,  zhenpeng.ge@qq.com

rmoss_ign is provided under MIT License.

