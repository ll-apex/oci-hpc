# 工作坊簡介

## 您將在本研討會中學習的內容

在本研討會中，您將瞭解如何在 Oracle Cloud Infrastructure 上的 GPU 虛擬機器上執行深偽造的應用系統 [Faceswap](https://faceswap.dev/) 。我們將涵蓋佈建的所有步驟，以及準備執行處理以使用 GPU 核心來執行 Python 命令檔 (Faceswap GAN) 以擷取臉孔、訓練 GAN 及在影片中轉換交換臉孔。

估計工作坊時間：120 分鐘 (除 GAN 培訓時間外)

## 什麼是深層假

Deepfake 是「深度學習」和「假」的複合詞，代表 AI 產生的媒體，其中現有圖片或影片中的某個人被別人取代，或使用其他外部功能修改 (例如年齡、髮型、膚色、語音等)。操控影片和影像的行為已久，但運用機器學習和 AI 製作具有高度欺騙潛力的媒體是新的。裸眼幾乎不可能分辨真實與假的媒體。

## 深層假如何運作？

深湖是以人工神經網路為基礎，可辨識資料中的模式 (例如臉孔、聲音) (人員的照片或影片)。大量資料會輸入神經網路，這些網路經過訓練可辨識樣式並偽造。神經網路是一種由人類大腦激發的演算法。神經元會接收並傳送訊號給其他神經元，通過它們在軸子和樹枝上的同步，目標就是合約肌肉。當信號從 A 移到 B 時，可能會被神經元層傳遞。同樣地，神經網路演算法會接收輸入資料，透過一組配備不同加權的數學運算 (矩陣乘法) 處理資料，這些加權會在訓練期間調整，最後再產生輸出。

為了及時執行 100 億個參數的矩陣乘法，需要足夠的運算能力。更快地同時執行所有作業，而非在其他作業之後執行。CPU 會在執行緒數量少的另一個之後執行一個程序，而 GPU 則有助於同時使用大量的執行緒來進行平行運算。可同時處理多個運算，讓 GPU 成為訓練神經網路演算法的最佳選擇。用於深度湖泊的神經網路稱為 GAN (一般的逆向網路)，其中兩個機器學習模型彼此互相競爭。第一個模型稱為讀取真實資料並產生假資料的產生器。第二種稱為鑑別器的模型負責偵測假資料。產生器會產生假資料，直到鑑別器無法再偵測它們為止。產生器可以使用更多的訓練資料，產生可信賴的深層偽造更容易。

## 什麼是 Faceswap？

[Faceswap](https://faceswap.dev/) 是目前已知和最廣泛用於產生深層湖的平台。它是一個以 Tensorflow、Keras 和 Python 為基礎的開放原始碼平台，可以在 Windows、macOS 和 Linux 上執行。一個活躍的社群已經形成了，它可以交換 Github 與其它討論區的資訊，並分享腳本以及提出問題的建議解決方案。

您可以使用 Oracle Free Tier (包含 Always Free Offering 和 30 天免費試用版) 來執行深層假的工作負載。在 Always Free Tier 中，VM.Standard.E2.1。Micro 可加以使用，並且在 30 天試用版中測試所有可用的 VM 和 BM 執行處理。若要測試 GPU 方案，可以將 Oracle 雲端帳戶升級為 PAYG。

## **確認**

*   **建立者 / 日期** - Maria Patelkou，HPC Solution Architect，Oracle Proposal to Production Program，2021 年 3 月
*   **上次更新者 / 日期** - Maria Patelkou，HPC Solution Architect，Oracle Proposal to Production Program，2021 年 3 月