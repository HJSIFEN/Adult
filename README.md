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
   - Numerical Data + Categorical Data OneHotEncoding
   - MinMaxScaling & Categorical Data OneHotEncoding
   - StandardScaler & Categorical Data OneHotEncoding
 - Test & Estimation_


# Result

![image](https://user-images.githubusercontent.com/60573146/169687940-b225d599-a84c-43e3-822e-93fff5080c47.png)

gray :  Only Numerical Data Training <br>
blue : Numerical Data + Categorical Data OneHotEncoding <br>
red :  Numerical Data(MinMaxScaling) & Categorical Data OneHotEncoding <br>
Yellow : Numerical Data(StandardScaler) & Categorical Data OneHotEncoding <br>



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


Only up to 10%. For More Detail, please check jupyter notebook code!

#### 1. workClass <br>
 ![image](https://user-images.githubusercontent.com/60573146/169684982-89af5de0-26cd-4699-b664-89dc17f95825.png)
 - Privet 69%


#### 2. Education <br>
 ![image](https://user-images.githubusercontent.com/60573146/169685004-d6191a57-64b8-473a-a9b3-1ddd87293ab5.png)
 - HS-grad 32%
 - Some-colleage 22%
 - Bachelors 16%


#### 3. martial-status <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689633-2dab85f3-5ab9-4a11-98f8-7d771bafa218.png)
 - Married-civ-spouse 45%
 - Never-married 32%
 - Divorced 13%
 
 
#### 4. Occupation <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689595-be8c2016-2214-498c-8cf4-7f4f256eeae8.png)
 - Prof-specialty 12%
 - Craft-repair 12%
 - Exec-managerial 12%
 - Adm-clerical 11%
 - Sales 11%
 - Other-service 10%


#### 5. relationship <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689557-8587c16f-4495-4a46-b765-76a880c353cc.png)
 - Husband 40%
 - Not-in-familty 25%
 - Own-child 13%
 - Unmarried 10%
 
#### 6. race <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689538-9c0a702c-0414-4e2e-b115-9189bdd883e2.png)
 - WHITE 85%
 

#### 7. sex <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689501-b30a7921-504a-4169-80a4-1328d3f21401.png)
 - Male 66%
 - Female 33%
 
 
#### 8. native-county <br>
 ![image](https://user-images.githubusercontent.com/60573146/170689382-a9d5e838-39f9-4c3e-90ec-e7ffba126b1b.png)
 - US 89%

 
### 3. Feature Correlation <br>
![image](https://user-images.githubusercontent.com/60573146/170690317-8d0d5cb8-6245-4714-b186-459d9fe87eff.png)

No Corelation each Features

### 4. TEST ACC

<table>
 <th>
 <td>Decision Tree</td><td>Random Forest</td><td>LDA</td><td>KNN</td><td>SVN</td>
 </th>
 <tr>
 <td>Numerical Value</td><td>0.816</td><td>0.81</td><td>0.838</td><td>0.852</td><td>0.802</td>
 </tr>
 

