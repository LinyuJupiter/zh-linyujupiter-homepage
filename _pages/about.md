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

中山大学智能工程学院智能科学与技术专业大三学生，现跟随高陈强教授的课题组协助参与部分科研任务，目前主要方向为计算机视觉方面，参与教室场景下智能行为检测任务。

<span class='anchor' id='news'></span>
# 🔥 新闻
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 
- *2022.02*: &nbsp;🎉🎉 Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ornare aliquet ipsum, ac tempus justo dapibus sit amet. 

<span class='anchor' id='projects'></span>
# 💬 项目

## 重点专项教室行为数据集构建 
*2023.10 - 至今* - 核心组员
- 构建高质量大型数据集，探究教室密集场景下行为识别问题；
- 使用 Python 于 YouTube、优酷等平台爬取大量教室场景视频，并通过 FFmpeg 将视频裁剪至多个 2s 小片段；
- 利用倍赛 BasicFinder 系统验收标注后数据集，参与视频行为时间定位工作，提取各行为持续的关键时间点；
- 研究进行至论证单个视频裁剪的合理性阶段，下阶段将在 SOTA 模型上测试效果并与其他传统数据集作比较。

## 教室场景下的交互行为识别 
*2023.09 - 至今* - 核心组员
- 围绕基于 YoLov5 的目标检测模块、基于 slowfast 的行为分类模块，初步确定技术方案；
- 基于 Linux 系统，构建并调试项目代码，解决漏洞并不断优化，配置服务器环境；
- 预处理 AVA 超大型数据集，使用 OpenCV 批量提取并分类视频帧，整理有效标签并用 Python 转换标签格式；
- 训练 slowfast 官方提供的预训练模型，多次更换配置训练不同结构的模型，并建立项目 demo 展示成果；
- 预处理 Kinetics-400 超大型数据集，使用 FFmpeg 批量裁剪与缩放视频，提取有效视频标签，完成 slowfast 网络
所需数据集的格式配置，使用处理后的数据集在多张显卡上分布式训练 slowfast，获取预训练模型；
- 目前处于调整网络超参数以提高精度阶段，下一步预计在新数据集上训练新预训练模型。

## 基于 Raft 的容错的分布式键值存储系统 
*2023.11 - 2024.01* - 个人项目
- 基于 MIT 6.824 分布式课程中的项目框架，利用 Go 语言实现容错的分布式键值（key-value）存储系统；
- 查阅 Raft-Extended 论文，完成 Raft Leader 选举和心跳、日志复制与一致性、快照机制与日志压缩等功能；
- 分别设计客户端和服务端，完善增删查改等功能，实现数据库和 Raft 算法的结合；
- 设计容错方案，完成节点断网、RPC 丢包、网络分区等故障测试；
- 完成高并发测试，系统可实现在规定时间内处理大量的并发请求。

## 基于卷积神经网络的苹果树叶片病害检测 
*2023.10 - 2023.11* - 个人项目
- 对数据集标签进行 one-hot 编码，将多分类任务转化为多标签分类任务；
- 分别采用 LeNet 和 VIT 模型架构设计并训练神经网络模型，对比分析 CrossEntropyLoss 与 ArcFaceLoss 在解决细
粒度分类问题上的性能差异，最终训练出的 LeNet 模型于测试集上准确率达 89.5%。

## 基于 YoLov8 与 Tesser act-OCR 的车流量分析系统 
*2023.06 - 2023.07* - 个人项目
- 使用开源数据集训练车型识别与车辆识别的 YoLo 神经网络模型，并在多个道路监控视频上进行测试；
- 训练 Tesseract-OCR 文字识别模型，实现手写文字识别实验，并将模型应用至车牌文字识别；
- 使用 Python 设计车流量计数算法，通过 BoT-SORT 算法实现目标追踪，并通过区域判定的方式判断车流量；
- 采用 tkinter 库设计项目 UI 界面，添加简易交互控件与信息显示控件，利于项目拓展应用。

## 基于 simulink 的小车自动寻路与控制仿真 
*2023.06 - 2023.07* - 个人项目
- 在系统生成的随机 2D 地图上，使用 A*算法实现起点至终点的可行路径规划；
- 设计缩放与插值策略，在加速路径规划的基础上，通过贝塞尔曲线插值法与 De Casteljau 算法对生成的可行路径
进行优化，采用分段平滑化的方式平滑路径并处理碰撞问题；
- 利用 MATLAB 软件编程对 LQR 参数进行求解，计算小车参数对应的 ABQR 矩阵，建立 LQR 控制器的 k 值表；
- 设计 PID 控制器实现小车横向控制，设计 LQR 控制器结合小车横向速度与路径曲率，实现小车纵向控制；
- 利用 simulink 进行小车路径跟踪仿真，建立控制器仿真模型，成功使小车一次性无碰撞到达终点；
- 在竞速中获得 MATLAB 组前 3 名（总 35 人）。

## C++实现双人中国象棋游戏 
*2022.11 - 2023.01* - 个人项目
- 设计程序底层架构，包括棋子基类与棋盘基类、棋子状态 vector 等，在棋子基类之上实现 14 种棋子派生类，通
过仿 vector 类储存棋子存活状态，使用移前推演和移后验证双重检查策略，确保棋子行动逻辑符合规则；
- 通过 IO 流与自定义文件格式，实现游戏进度保存与加载，并添加检测机制，防止残局不合理情况出现；
- 基于 QT designer 设计 UI 界面，添加自定义控件，用 Visual Studio 自制安装包，成果获班级第 1 名（总 47 人）。

<span class='anchor' id='honors-and-awards'></span>
# 🎖 荣誉与奖项
- *2024.02* 国际大学生数学建模竞赛(MCM/ICM)。 
- *2023.03* 智能工程学院首届“智数杯”数据分析赛三等奖。 

<span class='anchor' id='educations'></span>
# 📖 教育经历
- *2021.09 - 2025.06 (至今)*, 中山大学深圳校区, 智能工程学院, 智能科学与技术专业, 深圳。
- *2018.09 - 2021.06*, 河源中学, 河源。

<span class='anchor' id='publications'></span>
# 📝 发表作品 
- 暂无。

<span class='anchor' id='internships'></span>
# 💻 实习经历
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