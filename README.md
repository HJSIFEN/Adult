# Adult Data Analysis
## 0. Contents
It is data analysis with
 - Descriptive Statistics (기술통계)
 - Univariate analysis (frequency table, histogram, boxplot, etc.) 단변량분석 (빈도테이블, 히스토그램, 박스플랏)
 - Model building, analysis, or predictions (모델개발, 분석, 예측)
  - Models
    - Decision Tree (결정트리)
    - RandomForest (랜덤포레스트)
    - LDA (Linear Discriminant Analysis, LDA)
    - KNN (K-Nearest Neighbor)
    - SVM (Support Vector Machine)
    - MLP (Multi layer Perceptron)
 - Training with several Experiments
   - Only Numerical Data Training
   - Categorical Data OneHotEncoding
   - MinMaxScaling & Categorical Data OneHotEncoding
   - StandardScaler & Categorical Data OneHotEncoding
 - Test & Estimation_


## 1. Dataset
<a href = https://archive.ics.uci.edu/ml/datasets/adult >Adult Dataset</a>

- Train_data <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684532-39c07e2c-0843-4244-9a10-d735faf5c418.png)
  - length : 32561
  - There is Null data in workCalss,  Opccuptation, native-country.

- Test Data <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684542-15a95979-27f1-40e6-abd2-3a1ad78b2786.png)
  - 16281
  - There is Null data in workClas, Opccuptation, native-country

## 2. Descriptive Statistic
Using Only train_data,,,
- Train_data <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684624-d72b33e3-6a13-47a5-bf71-0c9ca7b615bf.png)

- Numberical Attributes <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684668-6f2be880-069d-4dec-a1c1-01b12d7d5176.png)

- Categorical Attributes <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684680-a587affd-2a8e-43b1-ab64-a0f11584cd1d.png)

## 3. Histogram
### 1. Numberical Attribute
 #### 1. Age 
 ![image](https://user-images.githubusercontent.com/60573146/169685186-92b9bfb7-f073-4147-a9ee-5b3a1b6bd24c.png)
 - Mean : 38.5
 - std : 13.64
 - min : 17
 - max : 90
 - 25% : 28
 - 50% : 37
 - 75% : 48
 <br>
 
 #### 2. fnlwgt <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685194-0a8c2a93-f179-4551-89d3-e85c1e191cf0.png)<br>
 - Mean : 189778
 - std : 105550
 - min : 12285
 - max : 1484705
 - 25% : 117827
 - 50% : 178356
 - 75% : 237051
 <br>
 
 #### 3. Education-num <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685259-83779891-0f1c-4e4a-a592-fb373564cb3c.png) <br>
 - Mean : 10.08
 - std : 2.57
 - min : 1
 - max : 16
 - 25% : 9
 - 50% : 10
 - 75% : 12
<br>

 #### 4. Capital-Gain <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685248-4584ac20-5872-47ef-b5d4-99efbaa35b51.png)
 - Mean : 1077.65
 - std : 7385.29
 - min : 0
 - max : 99999
 - 25% : 0
 - 50% : 0
 - 75% : 0
 - It's not good distribution. Almost datas are at 0 and fews are at 99999
<br>

 #### 5. Capital-loss <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685268-3dac2389-c0b6-46a4-ac39-aab4a147457a.png)
 - Mean : 87.30
 - std : 402.96
 - min : 0
 - max : 4356
 - 25% : 0
 - 50% : 0
 - 75% : 0
 - It's not good distribution. Almost dataws are at 0 and fews are at 4356
<br>

#### 6. hours-per-week <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685278-d9bde248-14d8-4f44-bb0a-9f3fa0891f0a.png)
 - Mean : 40.44
 - std : 12.34
 - min : 1
 - max : 99
 - 25% : 40
 - 50% : 40
 - 75% : 45 (?)
 <br> 50% people work 40~45 hours per week. Min is one(?) and Max is 99(???????)

### 2. Categorical Attiribute 
 ![image](https://user-images.githubusercontent.com/60573146/169684982-89af5de0-26cd-4699-b664-89dc17f95825.png)
 
 빈도테이블
===============================================
workClass_freq_table
                   freq    r_freq     p_freq
Private           22696  0.697030  69.703019
Self-emp-not-inc   2541  0.078038   7.803814
Local-gov          2093  0.064279   6.427935
State-gov          1298  0.039864   3.986364
Self-emp-inc       1116  0.034274   3.427413
Federal-gov         960  0.029483   2.948312
Without-pay          14  0.000430   0.042996
Never-worked          7  0.000215   0.021498
===============================================
 
 ![image](https://user-images.githubusercontent.com/60573146/169685004-d6191a57-64b8-473a-a9b3-1ddd87293ab5.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685203-88ca9f37-241b-4a13-9c13-106ad43d9ba8.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685213-cc4d69ba-f2c9-445c-9ad4-184512e55c39.png)


 ![image](https://user-images.githubusercontent.com/60573146/169685010-b3d955fd-87b4-4325-8b15-3e94fd64ac75.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685018-3c3616af-2a2e-499f-8187-712094bbc953.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685058-808f89bf-3d0d-46e9-ad5a-c28cad97b8c6.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685036-1fb28765-b985-4288-8e1e-622017d76487.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685070-ea4a6b40-35a5-4aa8-bfea-06e88b7fdee6.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685081-aad41ccc-e34a-48cd-8988-2484c001efa1.png)





