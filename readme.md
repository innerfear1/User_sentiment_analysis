基于机器学习的餐饮服务评价情感倾向分析研究
---------------------------------------------------------------
### 环境依赖(基于win10平台)

    python           3.9
    scikit-learn     1.0.2
    PyYAML           6.0
    numpy            1.21.5
    jupyter          1.0.0
    jieba            0.42.1
    pandas           1.4.4
    matplotlib       3.5.2

### 部署步骤(基于conda Prompt)

    1. pip install numpy
    
    2. pip install jieba
    
    3. pip install pandas
    
    4. pip insatll matplotlib
    
### 目录结构描述

|-- readme.md
|-- ChineseStopWords.txt
|-- clean_data.xlsx
|-- font.ttf
|-- data
|    |-- data.xlsx
|    |-- test.xlsx
|    |-- 字段说明.xlsx
|-- train.xlsx
|-- Q1_and_clean.ipynb
|-- Q1
|    |-- acclaim.jpg
|    |-- Negativity.jpg
|    |-- 文件读取.jpg
|-- Q2.ipynb
|-- Q2
|    |-- Q2_data.xlsx
|    |-- 关系表.xlsx
|-- Q3.ipynb
|-- Q3
|    |-- document-distribution.xlsx
|    |-- document-lda-visualization-top.html
|    |-- group_acclaim_data.xlsx
|    |-- group_max_acclaim_data.xlsx
|    |-- lda-joblib.pkl
|    |-- LDA主题词分析.jpg
|    |-- max_sellerId_acclaim.jpg
|    |-- tf_idf_vectorizer.pkl
|    |-- top-topic-words.xlsx
|-- Q4.ipynb
|-- Q4
|    |-- document-distribution.xlsx
|    |-- document-lda-visualization-top.html
|    |-- group_max_Negativity_data.xlsx
|    |-- group_Negativity_data.xlsx
|    |-- lda-joblib.pkl
|    |-- LDA最差商家主题词分析.jpg
|    |-- max_sellerId_Negativity.jpg
|    |-- tf_idf_vectorizer.pkl
|    |-- top-topic-words.xlsx
|-- Q5.ipynb
|-- Q5
|    |-- clean_test.xlsx
|    |-- lr.model
|    |-- test.xlsx
|    |-- test_old.xlsx

### 使用方式

    1. 安装环境依赖库
    
    2. 基于jupyter依次运行Q1_and_clean.ipynb、Q2.ipynb、Q3.ipynb、Q4.ipynb、Q5.ipynb文件，
       对本地的data.xlsx进行数据预处理、商家分组分析、二分类模型训练。
    
    3. 将需要预测的文件放入Q5.ipynb的如下代码下：
       # -*- coding: utf-8 -*-
        '''
       Author : WangQiang
       Datetime : 2023/1/4 12:01
       User : inner
       Product : jupyter
       Project : 题目B：餐饮服务评价情感倾向分析
       File : Q5.ipynb
       '''
       
       import pickle
       import re
       pickle.dump(clf, open('./Q5/lr.model', 'wb'))
       data = pd.read_excel('./Q5/test.xlsx')
       
    4. 退出文件执行，使用结束。 
      
      



