# Siemens STAR-CCM+の紹介

## 概要

Simcenter STAR-CCM+は、製品および設計のシミュレーションのための完全な多機能ソリューションです。このランブックでは、Simcenter STAR-CCM+クラスタをOracle Cloudにデプロイし、コンピュート・ノード間の低レイテンシ・ネットワーキングを実現するプロセスについて説明します。Simcenter STAR-CCM+をOracle Cloudで実行することは非常に簡単です。このガイドに従って、すべてのヒントとコツを確認してください。

注意: Simcenter STAR-CCM+のライセンスが必要です。

![](images/simulation.png " ")

## アーキテクチャ

このランブックのアーキテクチャは次のとおりです。接続先の小さいマシン(要塞)が1つあります。計算ノードは、RDMA RoCE v2ネットワーキングにリンクされた個別のプライベート・ネットワーク上にあります。要塞には、SSHを介して鍵を持つすべてのユーザー(有効にする場合はVNC)からアクセスできます。コンピュート・ノードには、ネットワーク内の要塞を介してのみアクセスできます。これは、2つのサブネット、1つのパブリックおよび1つのプライベートがある1つのVirtual Cloud Networkで実現されます。

### **ベースライン・インフラストラクチャ**

クラスタNetworksは、次のリージョンでサポートされています。いずれの場合も、ベースライン参照アーキテクチャを使用し、必要に応じて調整して特定の要件を満たすことをお薦めします。

*   箇条書きVCN
*   Public Subnet、Security List、Route Table
*   プライベート・サブネット、セキュリティ・リスト、ルート表
*   インターネット・ゲートウェイ
*   NAT Gateway
*   計算ノード
*   パブリック・サブネットの要塞ホスト
*   プライベート・サブネットのHPCコンピュート・ノード

![](images/architecture.png " ")

前述のベースライン・インフラストラクチャでは、次の仕様が提供されます。

*   ネットワーク
    *   コンバージドEthernet (ROCE)経由の1 x 100Gビット/秒RDMA v2
    *   1.5μs以下のレイテンシ
*   HPCコンピュート・ノード(BM.HPC2.36)
    *   ノード当たり6.4TBのローカルNVME SSDストレージ
    *   36コア/ノード
    *   384 GBメモリー/ノード

### **オプションのインフラストラクチャ**

### ストレージ

HPCシェイプに付属のNVME SSDストレージの上で、Oracleの最高パフォーマンスSLAで保証されたボリューム当たり32k IOPSでブロック・ボリュームをアタッチすることもできます。このソリューションを使用してインフラストラクチャを起動する場合、nfs-shareはデフォルトで/mntのNVME SSDストレージにインストールされます。パフォーマンス要件に応じて、NVME SSDストレージまたはブロック・ストレージのいずれかに独自のパラレル・ファイル・システムをインストールすることもできます。

### ビジュアライザ・ノード

要件に応じて、GPU VMやBMマシンなどのビジュアライザ・ノードを作成できます。このビジュアライザ・ノードは要塞ホストにすることも、別々にすることもできます。ワークロードのセキュリティ要件に応じて、ビジュアライザ・ノードをプライベート・サブネットまたはパブリック・サブネットに配置できます。

## 確認

*   **作成者** - High Performance Computeチーム
*   **貢献者** - Chris Iwicki、Harrison Dvoor、Gloria Lee、Selene Song、Bre Mendonca、Samrat Khosla
*   **最終更新者/日付** - Samrat Khosla、2020年10月