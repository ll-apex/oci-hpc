# 简介

## 简介

高性能计算正在改变产品开发和研究，使客户能够更快地解决复杂问题。这意味着原型减少、加快测试速度并缩短上市时间。Oracle 提供的按需 HPC 基础设施基于先进的计算、存储、网络和软件技术，适用于任何 HPC 负载。您只需花费一小部分成本自行构建并避免容量利用率问题即可获得所有这些好处。

Oracle 提供了具有弹性和可扩展性的云基础设施来运行 HPC 应用。借助几乎无限的容量，工程师、研究人员和 HPC 系统所有者可以超越内部部署 HPC 基础设施的限制，进行创新。Oracle 提供了一套集成的服务，其中提供了在云中快速轻松地构建和管理 HPC 集群所需的一切，可以在各个行业垂直领域中运行计算密集型负载。这些负载涵盖传统 HPC 应用，例如基因组学、计算化学、财务风险建模、计算机辅助工程、地震成像和天气预测，以及新兴应用，例如机器学习、深度学习和自主驾驶。

借助 Oracle Cloud Infrastructure，企业可以在按使用付费或非计量付费模型上运行需要数百万 IOP、毫秒延迟和许多 GB/秒带宽的性能密集型 HPC 负载，从而在 3 年 TCO 上节省 32%。

这些上机操作实验指南提供了在 Oracle Cloud 上部署 Simcenter STAR-CCM+ 集群的分步过程，在计算节点之间建立低延迟网络。

估计研讨会时间：4 小时

### 关于高性能计算 (High Performance Computing，HPC)

HPC，或超级计算，就像日常计算，只有更强大。它是一种以非常高速的速度处理大量数据的方式，使用多台计算机和存储设备作为统一结构。HPC 能够探索和找到一些世界上最大的科学、工程和商业问题的答案。

集群网络是高性能计算 (High Performance Computing，HPC) 实例池，它们通过高带宽、超低延迟的网络连接在一起。集群中的每个节点都是位于与其他节点附近的物理裸金属机。节点之间的远程直接内存访问 (Remote Direct Memory Access，RDMA) 网络可提供与内部部署 HPC 集群相当的低延迟（以单位微秒为单位）。

在 OCI 区域内的 Oracle Cloud Infrastructure 上提供高性能计算。

OCI 中的 Oracle 市场映像和 BM.HPC2.36 中提供了高性能计算实例。

Oracle 市场映像中的高性能计算机架包括 HPC 集群节点、集群网络和 NFS 共享。

计算节点通过集群网络连接，通过该网络为计算节点提供基于 RDMA 的存储访问。

目前，每个计算节点支持一个 BM。它允许客户在保护硬件和网络的同时进行 root 访问，计算节点使用 BM.HPC2.36 进行虚拟化。

### 目标

在本练习中，您将：

*   启动 HPC 集群网络
*   访问集群
*   配置可视化
*   访问 VNC
*   安装 STAR-CCM+
*   运行 STAR-CCM+

### 前提条件

*   了解云和数据库术语有帮助
*   熟悉 Oracle Cloud Infrastructure (OCI) 有帮助
*   熟悉网络有帮助

## 关于此研讨会

*   在 Oracle Cloud Infrastructure 中启动高性能计算集群网络
*   使用堡垒的公共 IP 地址访问集群
*   使用 GPU 可视化节点为模拟创建和配置可视化工具
*   通过 SSH 隧道连接来访问 VNC
*   通过添加所有必需的库和二进制文件，在实例上安装 STAR-CCM+
*   运行 STAR-CCM+

请注意：您需要提供您自己的 STAR-CCM+ 许可证！

## 确认

*   **作者** - 高性能计算团队
*   **贡献者** - Chris Iwicki、Harrison Dvoor、Gloria Lee、Selene Song、Bre Mendonca、Samrat Khosla
*   **上次更新者/日期** - Samrat Khosla，2020 年 10 月