## [恩師上課超連結](https://github.com/MyDearGreatTeacher/2022_1_courses)

## youtube視訊

- JAVA物件導向程式開發
  - [使用super0525](https://youtu.be/FKRUzSzGjTA)
  - [使用FINAL0525](https://youtu.be/HAWU-v5I1KI)
  - [使用static]
  - [抽象類別(abstract class)與抽象方法(abstract method)](https://youtu.be/D7tsHcjlXJI)


## 開發環境1:Online Java Compiler IDE

- [JDoodle](https://www.jdoodle.com/online-java-compiler/)

## 開發環境2: Java Development Kit (JDK) 我們要用的
- [How to Install Java JDK on Windows 10 ( with JAVA_HOME )](https://www.youtube.com/watch?v=IJ-PJbvJBGs&ab_channel=ProgrammingKnowledge)
- [How to Install Java JDK on Windows 11 ( with JAVA_HOME )](https://www.youtube.com/watch?v=VTzzmqNwGzM&ab_channel=ProgrammingKnowledge)
- Java Development Kit (JDK) 我們要用的
  - [下載點](https://www.java.com/en/download/help/develop.html)
  - C:\Program Files\Java\jdk-17.0.2\bin
  - cd C:\Program Files\Java\jdk-17.0.2\bin
  - 正確安裝後要設定
    - 1.設定環境變數: 把C:\Program Files\Java\jdk-17.0.2\bin加入到PATH
    - 2.在user的使用者環境變數新增 JAVA_HOME  <== 填入  C:\Program Files\Java\jdk-17.0.2
- Java Runtime Environment (JRE) 只能執行| 不能編譯
  - C:\Program Files (x86)\Java\jre1.8.0_321\bin
    - 沒有javac
    - java
```
C:\Program Files (x86)\Java\jre1.8.0_321\bin>java -version
java version "1.8.0_321"
Java(TM) SE Runtime Environment (build 1.8.0_321-b07)
Java HotSpot(TM) Client VM (build 25.321-b07, mixed mode, sharing)
```
## 程式開發
- 1.使用notepad++ 開發程式 ==> Hi2.java
- 2.編譯  javac Hi2.java  ==> 產生Hi2.class
- 3.執行檔案  java Hi2


## JAVA與中文

- [Java 與 Unicode](https://ithelp.ithome.com.tw/articles/10082051)

```
d:\A999E168>javac -encoding utf-8 Hi.java

d:\A999E168>java Hi
請輸入姓名：tseng
Hi! tseng, 歡迎來到Java世界！
```
## 教科書

- Java SE 12基礎必修課(適用Java 12~10，涵蓋OCJP與MTA Java國際認證)
- http://books.gotop.com.tw/download/AEL022500

```
第1章 Java概述
第2章 資料型別與運算子
第3章 控制敘述
第4章 陣列
第5章 方法
第6章 物件與類別
第7章 繼承、介面與多型
第8章 例外處理
第9章 集合與泛型
第10章 多執行緒
第11章 Swing視窗應用程式
第12章 Swing 元件(一)
第13章 Swing 元件(二)
第14章 I/O 常用類別
第15章 JDBC 資料庫程式設計
第16章 Lambda運算式
附錄A MTA 98-388 Introduction to Programming Using Java國際認證模擬試題
```

## 成績計算

- 期中平時(20%)
- 期中考(30%)
- 期末平時(20%)
- 期末考(30%)
