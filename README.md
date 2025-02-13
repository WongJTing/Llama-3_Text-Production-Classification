# Llama-3 基於產品分類的公司簡介分析

本專案展示了如何使用 Llama-3 模型根據公司的主要產品重點對公司簡介進行分類。整個流程包括數據轉換、模型訓練和模型使用三個主要步驟。此外，還提供了一個詳細的 PPT 教學，指導如何建立 Hugging Face 並使用訓練好的模型。

## 目錄

- [專案介紹](#專案介紹)
- [先決條件](#先決條件)
- [使用指南](#使用指南)
  - [步驟 1：將 Excel 轉換為 JSON](#步驟-1將-excel-轉換為-json)
  - [步驟 2：訓練模型](#步驟-2訓練模型)
  - [步驟 3：使用模型](#步驟-3使用模型)
- [附加資源](#附加資源)
- [範例工作流程](#範例工作流程)


## 專案介紹
在當前快速變化的商業環境中，尋找合適的供應商或客戶已成為一項重大挑戰，精準行銷對企業的成功變得愈發重要。傳統依賴人脈的方式既耗時，且效果無法保證，難以找到最合適的合作夥伴，甚至可能導致商機流失和公司利潤的損失。本專案開發了一個基於大型語言模型（Llama-3）的推薦與精準行銷系統，旨在加速並優化供應鏈中潛在上下游關係的識別，從而減少商機流失，降低公司損失風險，並促進整體產業的發展。

## 先決條件
1. Google 帳戶：用於訪問 Google Colab。
2. GitHub 帳戶：用於克隆專案和提交代碼。
3. 必要的 Python 知識：了解基本的 Python 編程和 Jupyter Notebook 操作。

## 使用指南
### 步驟 1：將 Excel 轉換為 JSON
使用 xlsx2json.ipynb notebook 來預處理你的數據。
 - 輸入：包含公司簡介信息的 Excel 文件。
 - 輸出：用於訓練的 JSON 文件。

如何運行：
1. 打開 xlsx2json.ipynb 在 Google Colab 上：
2. 按照 notebook 中的指示上傳你的 Excel 文件並生成 JSON 文件。

---

### 步驟 2：訓練模型
使用 ftmodel.ipynb notebook 來微調 Llama-3 模型。
 - 輸入：步驟 1 生成的 JSON 文件。
 - 輸出：儲存在 Hugging Face 上的訓練模型。

如何運行：
1. 打開 ftmodel.ipynb 在 Google Colab 上：
2. 更新配置（例如訓練參數、數據集路徑和 Hugging Face 認證信息）。
3. 運行 notebook 以訓練模型並將其保存到 Hugging Face。

---

### 步驟 3：使用模型
使用 model_use.ipynb notebook 來加載訓練好的模型並進行預測。
 - 輸入：公司簡介文本。
 - 輸出：預測的產品分類。

如何運行：
1. 打開 model_use.ipynb 在 Google Colab 上：
2. 在指定的單元格中輸入公司簡介文本。
3. 運行 notebook 以查看分類結果。

## 附加資源
為了更詳細地了解如何設置 Hugging Face 以及如何使用模型，請參考我們準備的 PPT 教學：
- 設置 Hugging Face 帳戶和倉庫。
- 每個 notebook 的詳細工作流程。
- 自訂和改進模型的技巧。

## 範例工作流程
以下是一個完整流程的範例：
1. 準備包含公司數據的 Excel 文件
2. 使用 xlsx2json.ipynb 將其轉換為 data.json。
3. 在 ftmodel.ipynb 中使用 data.json 訓練模型。
4. 使用 model_use.ipynb 對新的公司簡介進行分類。
