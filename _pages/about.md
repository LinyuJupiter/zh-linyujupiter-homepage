---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

刘芳新，广东河源人，2025年毕业于中山大学智能工程学院智能科学与技术专业，后进入香港中文大学工程学院信息工程系就读硕士学位。

喜欢编程，现有自己基于Python开发的已上线软件两款(隐私限制，不方便展示)，用户过百，全部前后端开发与运维工作由我一人完成。[这里](http://134.175.123.166)是我自己搭建的网站主页，[这里](http://134.175.123.166:3003)是我的博客网站，欢迎访问。

曾加入[高陈强](https://gaocq.github.io/index.html)教授的课题组协助参与部分科研任务，方向为计算机视觉，主要参与教室场景下行为检测任务。发表有SCI四区论文一篇。

后跟随[沈颖](https://sysu-hcp.net/faculty/442.html)副教授研究大语言模型领域，完成本科毕业论文《大模型RAG的加速算法与精确度提升方法研究》。

现工作于腾讯金融科技，任测试开发岗位，从事基于大模型等人工智能技术提升研发效率的工作。

<span class='anchor' id='news'></span>
# 🔥 新闻

- *2025.04*: &nbsp;🎉🎉 发表的论文《Dual-branch vision transformer for low-resolution action recognition》被SCI期刊《Multimedia Tools and Applications》接收。

- *2024.07*: &nbsp;🎉🎉 加入腾讯金融科技，任测试开发岗位，从事基于大模型等人工智能技术提升研发效率的工作。

- *2024.06*: &nbsp;🎉🎉 参加"挑战杯"中国大学生创业计划竞赛，与团队成员一起获得河北省二等奖。

- *2024.02*: &nbsp;🎉🎉 与两名同专业同学一起参加国际大学生数学建模竞赛(MCM/ICM)，担任论文手。获得S奖。

- *2024.01*: &nbsp;🎉🎉 在寒假实习(风华高科)期间，搭建的智能文档助手应用与智能物料机器人应用得到领导高度赞誉，目前该项目已经申报总公司的项目论证。

- *2023.08*: &nbsp;🎉🎉 在暑期实习期间，独立设计开发的软件小白自装(宜春版)上线。

- *2023.05*: &nbsp;🎉🎉 软件三七自动识别(在线版)上线，吸引了大批用户资源。目前该软件已和本地版结合，并不断保持更新维护。

- *2023.03*: &nbsp;🎉🎉 自研开发的软件三七自动识别(本地版)上线，用户体验反馈良好。

- *2022.07*: &nbsp;🎉🎉 在计算机类（深圳）的大类排名前三分之一（大类共900人），以第一志愿进入智能工程学院智能科学与技术专业继续进修本科学业。

- *2021.07*: &nbsp;🎉🎉 在河源中学高考理科排名44名，以全省4900名左右的成绩被中山大学计算机类（深圳）录取。

<span class='anchor' id='projects'></span>
# 💬 项目

## screenshot2code——基于GLM-4的将网页截图转换成HTML代码的工具

*2023.12 - 2024.01* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/screenshot2code)

- 使用设计图片的形式写出前端页面代码可以节省前端工程师的大量时间，本项目旨在使用国产大模型识别屏幕截图中的网页样式，并生成页面代码
- 探索国产大模型在视觉识别与代码生成方面的能力，确定选择智谱的GLM-4模型的技术方案
- 基于FastAPI搭建后端接口，在后端程序中设计提示词让视觉大模型识别屏幕截图，由文本大模型生成HTML+tailwind代码，最后使用cogview-3生图模型生成网页插图
- 使用PyQT设计前端界面，使用websocket与后端进行通信，实现用户友好型操作界面，能实时显示生成效果
- 使用Inno Setup制作安装包，编写详细的项目开发文档与使用说明文档，布置站点发布文档

## 重点专项教室行为数据集构建 
*2023.10 - 2024.06* - 核心组员
- 本项目旨在构建高质量大型数据集，填补行为识别领域对密集场景数据集的空缺，并探究教室密集场景下行为识别问题；
- 寻找数据源，制定标注方案，组织项目团队，形成项目计划
- 从互联网批量下载教室场景视频；人工筛选出具有合适的视角的视频，切分视频片段；
- 将筛选后的视频交给团队进行标注，组织验收团队，对标注完成的数据进行标签检查。

## 低分辨率场景行为识别 
*2023.09 - 2024.06* - 核心组员
- 围绕基于YoLov5的目标检测模块、基于slowfast的行为分类模块，初步确定技术方案；
- 预处理AVA超大型数据集，使用OpenCV批量提取并分类视频帧，整理有效标签。使用AVA数据集训练slowfast官方提供的预训练模型，多次更换配置训练不同结构的模型，并建立项目demo展示成果；
- 预处理Kinetics-400超大型数据集，使用FFmpeg批量裁剪与缩放视频，提取有效视频标签，完成slowfast网络所需数据集的格式配置，使用处理后的数据集在多张显卡上分布式训练slowfast，获取预训练模型；
- 参考slowfast网络，提出一个具有双重分支的网络，用来分离时空特征。在主分支中，使用较低的帧速率提取空间信息。而在辅分支中，使用较高的帧速率来提取时间信息。这两个分支的信息通过交叉注意力实现双向融合；
- 提出的新网络结构在公开数据集上获得75.2\%的F1分数，而在新提出的教室场景行为识别数据集上获得83.41\%的准确率，超越了baseline模型，推理成本仅增加13.41\%。

## 基于 Raft 的容错的分布式键值存储系统
*2023.11 - 2024.01* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/Distributed-Raft)
- 基于 MIT 6.824 分布式课程中的项目框架，利用 Go 语言实现容错的分布式键值（key-value）存储系统；
- 查阅 Raft-Extended 论文，完成 Raft Leader 选举和心跳、日志复制与一致性、快照机制与日志压缩等功能；
- 分别设计客户端和服务端，完善增删查改等功能，实现数据库和 Raft 算法的结合；
- 设计容错方案，完成节点断网、RPC 丢包、网络分区等故障测试；
- 完成高并发测试，系统可实现在规定时间内处理大量的并发请求。

## 基于卷积神经网络的苹果树叶片病害检测
*2023.10 - 2023.11* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/Identify-the-category-of-foliar-diseases-in-apple-trees)
- 对数据集标签进行 one-hot 编码，将多分类任务转化为多标签分类任务；
- 分别采用 LeNet 和 VIT 模型架构设计并训练神经网络模型，对比分析 CrossEntropyLoss 与 ArcFaceLoss 在解决细
粒度分类问题上的性能差异，最终训练出的 LeNet 模型于测试集上准确率达 89.5%。

## 基于 YoLov8 与 Tesser act-OCR 的车流量分析系统
*2023.06 - 2023.07* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/Traffic-Flow-Analysis-System)
- 使用开源数据集训练车型识别与车辆识别的 YoLo 神经网络模型，并在多个道路监控视频上进行测试；
- 训练 Tesseract-OCR 文字识别模型，实现手写文字识别实验，并将模型应用至车牌文字识别；
- 使用 Python 设计车流量计数算法，通过 BoT-SORT 算法实现目标追踪，并通过区域判定的方式判断车流量；
- 采用 tkinter 库设计项目 UI 界面，添加简易交互控件与信息显示控件，利于项目拓展应用。

## 基于 simulink 的小车自动寻路与控制仿真
*2023.06 - 2023.07* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/Fundamentals-of-autopilot-project)
- 在系统生成的随机 2D 地图上，使用 A*算法实现起点至终点的可行路径规划；
- 设计缩放与插值策略，在加速路径规划的基础上，通过贝塞尔曲线插值法与 De Casteljau 算法对生成的可行路径
进行优化，采用分段平滑化的方式平滑路径并处理碰撞问题；
- 利用 MATLAB 软件编程对 LQR 参数进行求解，计算小车参数对应的 ABQR 矩阵，建立 LQR 控制器的 k 值表；
- 设计 PID 控制器实现小车横向控制，设计 LQR 控制器结合小车横向速度与路径曲率，实现小车纵向控制；
- 利用 simulink 进行小车路径跟踪仿真，建立控制器仿真模型，成功使小车一次性无碰撞到达终点；
- 在竞速中获得 MATLAB 组前 3 名（总 35 人）。

## C++实现双人中国象棋游戏 
*2022.11 - 2023.01* - 个人项目 [<img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub" width="20"/>](https://github.com/LinyuJupiter/Two-Player-Chinese-Chess-Game)
- 设计程序底层架构，包括棋子基类与棋盘基类、棋子状态 vector 等，在棋子基类之上实现 14 种棋子派生类，通
过仿 vector 类储存棋子存活状态，使用移前推演和移后验证双重检查策略，确保棋子行动逻辑符合规则；
- 通过 IO 流与自定义文件格式，实现游戏进度保存与加载，并添加检测机制，防止残局不合理情况出现；
- 基于 QT designer 设计 UI 界面，添加自定义控件，用 Visual Studio 自制安装包，成果获班级第 1 名（总 47 人）。

<span class='anchor' id='honors-and-awards'></span>
# 🎖 荣誉与奖项
- *2024.07* "挑战杯"中国大学生创业计划竞赛河北省二等奖
- *2024.02* 国际大学生数学建模竞赛(MCM/ICM)。 
- *2023.03* 智能工程学院首届"智数杯"数据分析赛三等奖。 

<span class='anchor' id='educations'></span>
# 📖 教育经历
- *2025.09 - 至今*, 硕士：香港中文大学, 工程学院，信息工程系, 香港。
- *2021.09 - 2025.06*, 本科：中山大学, 智能工程学院, 智能科学与技术专业, 深圳。
- *2018.09 - 2021.06*, 高中：河源中学, 河源。

<span class='anchor' id='publications'></span>
# 📝 发表作品 

- *2025.04* [Chen, R., Gao, C., Tan, Z., Liu, F., Yu, J., & Li, X. (2025). Dual-branch vision transformer for low-resolution action recognition. Multimedia Tools and Applications, 1-20.](https://link.springer.com/article/10.1007/s11042-025-20827-w)

- *2024.06* 计算机软件著作权——CellMaster 教学系统

<span class='anchor' id='internships'></span>
# 💻 实习经历

## *2024.07 - 至今*, [腾讯科技（深圳）有限公司](https://www.tencent.com/zh-cn/index.html), 测试开发, 深圳
- 负责开发自动化测试用例生成工具，该工具旨在根据调用日志等信息，由基于大模型的Agent工作流生成对应测试场景的场景测试用例代码。
- 设计日志解析方案，编写算法从庞杂的接口调用日志提取有效接口信息。
- 使用基于匹配算法与混元大模型的多路匹配方案，追溯各个接口请求体参数来源。
- 基于混元大模型与向量索引服务，使用Few-shot-Cot方法设计提示词，提供接口信息与少量代码模版，让大模型输出测试用例代码。
- 解析数据库表记录，使用多路匹配方案追溯数据库字段来源，从而实现测试流程的结果检查。
- 完成系统整体设计，拆分任务并搭建解耦出来的各个模块，串联全部流程并最终实现完整系统。


## *2024.01 - 2024.02*, [广东风华高新科技股份有限公司](https://www.china-fenghua.com/), 人工智能工程师, 肇庆。
- 编写智能订单报表管理程序，批量高速处理公司订单入库问题；
- 基于chatGLM-6b、qwen-7b等开源大模型，使用公司文档进行风华人工智能文档大模型开发、训练与部署；
- 对公司物料数据库进行整理，使用embedding模型与reranker模型等技术建立物料知识库，并结合大模型开发出智能物料信息客服应用；
- 开发公司采购物资平台的后端接口并完成数据库对接工作。

## *2023.07 - 2023.08*, 广东万师达智能科技有限公司, 软件开发实习生, 河源。
- 深入装修行业智慧平台项目，基于 Python、MySQL，独立开发客户公司的一站式平台软件；
- 基于客户需求匹配技术方案，搭建 anaconda 虚拟环境，设计软件底层架构，可实现聊天、选购等模块功能；
- 搭建 MySQL 数据库，实现前后端交互，前端设计图形化界面，后台通过 SQL 语句封装，完成接口的设计编写；
- 使用 tkinter 库，按照要求设计软件 UI 界面与交互逻辑，利用 ttkbootstrap 库美化界面并使其适配多分辨率窗口；
- 采用 Inno Setup 制作安装包，并撰写项目文档与使用说明。