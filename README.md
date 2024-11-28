# LineBotFAQ
# DSM 1128: 鐵達尼號生存預測

## 專案介紹
本專案針對 Kaggle 提供的鐵達尼號資料集，透過探索性數據分析 (EDA) 和機器學習模型進行生存預測。本專案適合作為機器學習入門練習，涵蓋數據預處理、特徵工程以及模型建立。

關鍵字: 
- **探索性數據分析 (Exploratory Data Analysis)**
- **特徵工程 (Feature Engineering)**
- **隨機森林 (Random Forest)**

## 資料集簡介
資料集來源：[Kaggle Titanic Dataset](https://www.kaggle.com/c/titanic/data)
- **`train.csv`**: 包含乘客的特徵與生存結果，作為訓練集。
- **`test.csv`**: 包含乘客的特徵，但不含生存結果，用於測試模型。
- **`gender_submission.csv`**: 提供樣本提交格式。

目標：預測乘客是否生存 (`Survived`，1=生存，0=死亡)。

---

## 功能與流程

### 1. 資料蒐集與初步檢視
- 讀取資料 (`pandas`) 並顯示資料的結構。
- 定義函數觀察欄位型態及缺失值，確定需處理的特徵與補值策略。

### 2. 資料預處理
#### 缺失值處理
- 欄位如 `Age`, `Cabin`, `Embarked`, `Fare` 存在缺失值，採用適當的填補策略。

#### 基礎統計分析
- 利用 `describe()` 函數檢視數值型欄位的統計量，協助辨識資料尺度差異及是否存在離群值。

### 3. 探索性數據分析 (EDA)
#### 生還比例
- 計算生還者與遇難者比例，並可視化結果 (圓餅圖)。
  
#### 特徵相關性
- 計算數值型欄位與 `Survived` 的相關係數，篩選影響生存預測的重要特徵。

#### 分類欄位分析
- 分析性別、票務艙等與生存率的關係，繪製長條圖和統計表。

### 4. 特徵工程與模型建立
（未展示，但可延伸）
- 利用所選特徵建立隨機森林模型，進行分類預測。

---

## 技術堆疊
- **語言與工具**: Python, Jupyter Notebook
- **資料處理**: `pandas`, `numpy`
- **可視化**: `matplotlib`, `seaborn`
- **機器學習**: (擴展) `sklearn` (Random Forest)

## 使用方法
1. 安裝必要的 Python 套件：
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn

