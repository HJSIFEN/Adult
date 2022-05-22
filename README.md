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
 - Experiment
   - Just Training
   - OneHotEncoding
   - MinMaxScaling & OneHotEncoding
   - StandardScaler & OneHotEncoding
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
 ![image](https://user-images.githubusercontent.com/60573146/169684908-a41c28cb-04e8-4218-a34a-f955b0c761f5.png)

### 2. Categorical Attiribute 
 ![image](https://user-images.githubusercontent.com/60573146/169684982-89af5de0-26cd-4699-b664-89dc17f95825.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685004-d6191a57-64b8-473a-a9b3-1ddd87293ab5.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685010-b3d955fd-87b4-4325-8b15-3e94fd64ac75.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685018-3c3616af-2a2e-499f-8187-712094bbc953.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685058-808f89bf-3d0d-46e9-ad5a-c28cad97b8c6.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685036-1fb28765-b985-4288-8e1e-622017d76487.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685070-ea4a6b40-35a5-4aa8-bfea-06e88b7fdee6.png)
 ![image](https://user-images.githubusercontent.com/60573146/169685081-aad41ccc-e34a-48cd-8988-2484c001efa1.png)





