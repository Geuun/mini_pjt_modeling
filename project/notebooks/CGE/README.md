CGE's Jupyter Notebook Directory

# IEEE-CIS Fraud Detection Modeling 

<font size="5">[kaggle](https://www.kaggle.com/competitions/ieee-fraud-detection/overview/description)</font>

<font size="5">pipeline</font> <br>
분석 문제 정의 → 데이터 수집 → EDA&Data Preprocessing → feature engineering → Modeling(XGBoost,LightGBM), 둘 중 더 좋은 성능으로 -> undersampling vs non undersampling, Confusion matrix 비교 → GridSearchCV(최적의 하이퍼파라미터를 찾아줌)


### Data Preprocessing
- KNN 
    - PCA : Vxxxx 
- label encoding

 
### feature engineering
[AMEX-Data Preprocesing & Feature Engineering](https://www.kaggle.com/code/susnato/amex-data-preprocesing-feature-engineering)

1. Correlation -> 원핫인코딩(0,1)해서 별로 의미가 없을듯!, 사용할 때 절댓값으로 사용

    1. VIF(다중공선성 사용가능하지만 feature가 많으면 비추천!)


2. feature importance (차원축소를 하기위해 ML을 돌림)
    1. **LGBM**
    2. 👍🏻[모델이 학습하면서 feature 선택](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SequentialFeatureSelector.html)


### Modeling(train = 8:2로 진행, random states = 0xC0FFEE)
   - **XGBoost**, LGBM, Catboost 


**Evaluation**
- ROC curve
- TransactionID(PK) 
- isFraud (**Target, 사기 거래일 확률 예측**)
