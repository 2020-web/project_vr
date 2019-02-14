# 多人 VR 环境

在这个选题中，你需要实现一个完整的多人在线 VR 环境。该环境可以是一个旅游场景、校园、室内等任意环境， 用户拥有自己的虚拟形象，可以在这个环境中模拟真实世界中的操作，如行走、交流等。以你选择的环境为主题， 添加相应的功能，如景点介绍(旅游场景)、基于 LBS 的聊天(校园)、游戏(室内)等。

这个网站具有以下特点:

- 模拟真实世界中的环境:远程旅游，不受时空限制;
- 多人可以选择化身进入同一个环境:社交因素的引入;
- 数字化的虚拟世界可以方便地进行用户行为的分析:化身在虚拟世界中的行为可以被记录下来进行分析，比如行走路线、速度等。

## 系统基本功能与流程

### 功能要求

#### 基本功能

- 支持多人加入同一个虚拟世界(采用 Web3D + WebSocket 构建)中:
    - 相互可见，并且行为共享;
    - 可以进行一定方式的交流;
    - 环境中可以有一些可交互性的实体，如可以打开的门。
- 维护虚拟世界的一致性:
    - 同一时刻各个化身能看到的场景应该是一致并且最新的。
- 系统部署在云服务器上，提供可以访问的公网地址。

#### 进阶功能

- 加入一些人工智能因素，增加一个由计算机控制的智能虚拟人(NPC)，比如导游、服务员。可以根据用户 化身的行为做简单的响应，比如介绍景点等。
- 在环境中的实体可以采用语义 Web 技术加入描述，甚至可以支持推理。