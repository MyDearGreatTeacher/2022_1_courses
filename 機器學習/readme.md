## Google Meet 

https://meet.google.com/wdf-tvom-sbo

## 報告內容:機器學習演算法分析與應用報告
- 機器學習MACHINE LEARNING 
- 機器學習類型與常見演算法
- 機器學習開發環境
- 機器學習演算法實戰與應用
  - 監督式機器學習演算法(1)回歸演算法
  - 監督式機器學習演算法(2)分類演算法
  - 監督式機器學習演算法(3)決策樹演算法
  - 非監督式機器學習演算法:叢集演算法
# 參考書scikit-learn
- [scikit-learn 新手的晉級：實作各種機器學習解決方案 (Mastering Machine Learning with scikit-learn, 2/e)Gavin Hackeling](https://www.tenlong.com.tw/products/9789864344840)
- [打下最紮實的AI基礎：從scikit-learn一步一腳印](https://www.books.com.tw/products/0010816766?sloc=main)
- [scikit-learn Cookbook - Second Edition(2017)](https://www.packtpub.com/product/scikit-learn-cookbook-second-edition/9781787286382) [GITHUB](https://github.com/packtpublishing/scikit-learn-cookbook-second-edition)


# 機器學習演算法實戰與應用
## 監督式機器學習演算法(1)回歸演算法
- [回歸演算法Regression analysis](https://en.wikipedia.org/wiki/Regression_analysis)
- [Least Squares Method最小平方法](https://en.wikipedia.org/wiki/Least_squares)
- 線性回歸演算法
- [小小練習: matplotlib.pyplot!](機器學習類型: https://matplotlib.org/3.5.0/api/_as_gen/matplotlib.pyplot.html)
- [小專案1:pizza定價模型](https://github.com/PacktPublishing/Mastering-Machine-Learning-with-scikit-learn-Second-Edition/tree/master/chapter02)
  - 關鍵程式碼1: from sklearn.linear_model import LinearRegression  選擇你要使用的模型
  - 關鍵程式碼2: model = LinearRegression()
  - 關鍵程式碼3: model.fit(X, y) 建立模型
  - 關鍵程式碼4:test_pizza = np.array([[200]]) 建立要預測的資料
    - predicted_price = model.predict(test_pizza)[0]  進行預測
- 小專案:波士頓房價預測模型
## 監督式機器學習演算法(2)分類演算法
- 分類演算法
- [k-nearest neighbors algorithm (k-NN) ](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)
- 分類演算法效能評估指標
- 小專案:Pima印地安人糖尿病預測模型
## 監督式機器學習演算法(3)決策樹演算法
- 決策樹演算法
- 決策樹演算法
- 精進決策樹演算法 == >
- 小專案:鐵達尼號倖存者預測模型
## 非監督式機器學習演算法:叢集演算法
- 叢集演算法
- 叢集演算法實戰範例
- 叢集演算法效能評估指標:silhouette coefficient(輪廓係數)
