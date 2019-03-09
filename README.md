# 多人 VR 教学式场景

在这个选题中，你需要实现一个完整的多人在线 VR 教学式场景。该环境可以是一个博物馆、校园、室内等任意环境， 用户拥有自己的虚拟形象，可以在这个环境中模拟真实世界中的操作，如行走、交流等。以你选择的环境为主题， 添加相应的功能。

这个网站具有以下特点:

- 模拟真实世界中的环境:远程旅游，不受时空限制;
- 多人可以选择化身进入同一个环境:社交因素的引入;
- 数字化的虚拟世界可以方便地进行用户行为的分析:化身在虚拟世界中的行为可以被记录下来进行分析，比如行走路线、速度等。
- 场景是教学式目的:如博物馆中，玩家可以漫游博物馆浏览文物学习知识。

## 1. 系统基本功能与流程

### 1.1 功能要求

#### 1.1.1 基本功能

- 支持多人加入同一个虚拟世界(采用 Web3D + WebSocket 构建)中:
    - 相互可见，并且行为共享;
    - 可以进行一定方式的交流;
    - 环境中可以有一些可交互性的实体，如可以打开的门。
- 维护虚拟世界的一致性:
    - 同一时刻各个化身能看到的场景应该是一致并且最新的。
- 系统部署在云服务器上，提供可以访问的公网地址。

#### 1.1.2 进阶功能

- 加入一些人工智能因素，增加一个由计算机控制的智能虚拟人(NPC)，比如导游、服务员。可以根据用户 化身的行为做简单的响应，比如介绍景点等。
- 在环境中的实体可以采用语义 Web 技术加入描述，甚至可以支持推理。

#### 1.1.3 附加说明

- 3D 建模和动画不是课程重点，不要求建模非常逼真，可以采用下载的模型。

### 1.2 使用流程

> 注:PJ 的具体界面设计和功能安排可自由发挥。除了这些页面外，你可以根据你的场景需要添加其他页面和 交互。

#### 1.2.1 登录注册页面

- 用户能够通过用户名和密码登录和注册。注册时需要完善用户名、密码等信息，并选择虚拟形象。
- 登录后进入多人 VR 环境。

#### 1.2.2 多人 VR 页面

- 提供一个多人在线的 VR 环境，参见之前的功能要求。 
- 根据你的场景，可选提供实时聊天等附加功能。

#### 1.2.3 用户后台页面

- 用户可以查看并修改自己的个人信息、虚拟形象等。
- 根据你的场景，可选提供历史行为查看和分析功能。

## 2. 技术实现

## 3. 建议

- 采用前后端分离架构。
- Web3D 展示建议使用 Three.js 。 多用户的位置同步、协同聊天等功能，建议使用 WebSocket(Socket.io)。

### 3.1 参考资料

- 开源多人 VR 环境 Vnet(Java + VRML)的介绍和源代码。
- 基于 WebGL 的 KataSpace (Sirikata) 参考文档。
- 基于 Three.js 和 WebSocket 的 3D 虚拟环境 demo。支持多人在线聊天，能够移动并互相看到其他用户的位置。

### 3.2  参考技术路线

![](./assests/img/1.png)

## 4. 评分细则 

### 4.1 分数组成

- 基本功能分:即完成系统基本内容与流程，满分 100 分。 
- 进阶任务分:包括但不限于更精致的设计、场景，更好的开发部署流程、设计模式等。最多 30 分。 
- 个人工作分:根据小组分工及个人完成工作量得分。每组组员该项分数总和 30 分，根据贡献比例分摊。

个人最终得分 = 基本功能分 + 进阶任务分 + 个人工作分，值域为 [0, 160]。 

### 4.2 评分点


|功能项 | 得分项 | 最高分数|
| ------ | ------ | ------ |
| 基本流程 |注册和登录页面| 5|
|（20分）| 多人 VR 页面 |10|
||用户后台页面 |5|
|VR 场景 |正确显示一个可交互的 3D 场景 |10|
|（50分） |支持多人加入同一个虚拟世界| 10|
||正确更新其他用户的位置、行为变化| 10|
||场景的创意、功能的完成度和交互的丰富程度 |10|
||多用户间的交流等交互功能 |10|
|工程能力| 文档 |5|
|（30分）| 系统架构 |10|
||代码风格| 5|
||项目完整度和易用性 |10|
|附加功能 |采用语义 Web 描述环境中的实体| 5|
|（40分）| 模型、动画、场景的美观程度 |10|
||简单响应用户化身行为的人工智能| 10|
||将服务器部署到公有云上 |10|
||使用 Docker 部署服务器 |5|
||其他合理的附加功能 |10|


### 4.3 评分点说明

1. 每一项的分数取决于该项功能的完成度。完成度和可用性越好，分数越高。 

2. 项目完整度和易用性评价标准:

- A. 最低要求为必须实现并完成规定的用户功能与操作。核心功能和技术都有实现，在应用逻辑和实际操 作便捷性上可以不做考虑。
- B. 基本要求为实现并完成规定的用户功能和操作，并设计合理便捷的操作流程，系统各部分衔接过度自 然，方便使用。
- C. 进阶要求为实现并完成规定的用户功能、操作和进阶加分项，形成一套完整的可发布的应用逻辑。 A、B、C 分别对应 0 - 3 分，4 - 6 分，7 - 10 分。

3. 附加功能必须在文档中明确写出，概述该功能并描述实现原理。 

4. 项目设计文档需要至少包含:
    - 项目组织以及其中每个文件的说明。
    - 关键功能实现的细节。
    - 服务器部署配置的详细介绍。

5. 团队分工文档需要至少包含: 
    - 团队成员、分工、具体完成工作，列出每个人的贡献比例。
    - 其他你们想说明的问题。 
    
## 5. 提交

1. 提交物包含以下三项:
    - 源代码:推荐使用 Git 进行协作，提交到 GitHub 等 Git 托管平台上。 
    - 文档:推荐使用 Markdown 编写项目文档，与源代码一同提交到 Git 托管平台上。 
    - 可供访问的公网地址，以及系统的操作说明(玩法)。

2. 提交物需要压缩打包提交到 FTP 上，文件名中请包含小队所有成员的姓名与学号。 

3. 友情提示:请尽早开工，本学期只有一个 Project，临时赶工很有可能完不成。