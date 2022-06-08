# 期中平時成績:JAVA多執行緒開發報告
```
執行緒簡介
JAVA執行緒
執行緒的生命週期
建立執行緒
建立執行緒1
建立執行緒2
```
## 執行緒
## JAVA執行緒
## 執行緒的生命週期
## 如何建立執行緒
## 建立執行緒1
```java

public class Rate1 {
	public static void main(String[] args) {
		Thread tortoise = new Thread() {
			public void run() {
				for(int i = 1; i <= 20; i ++) {
					System.out.println("烏龜共跑 " + i + " 公里");
				}
				System.out.println("烏龜抵達終點！");
			}
		};
		Thread rabbit = new Thread() {
			public void run() {
				for(int i = 4; i <= 20; i += 4) {
					if(Math.random() > 0.2) { 
						System.out.println("兔子休息");
						i -= 4;  //使兔子停止
					} else {
						System.out.println("兔子共跑 " + i + " 公里");
					}
				}
				System.out.println("兔子抵達終點！");
			}
		};
		rabbit.start();
		tortoise.start();
	}
}
```
## 建立執行緒2
```java

class MyThread2 implements Runnable {
	int m; 				// m為執行的次數
	MyThread2(int a) { 		// MyThread類別的建構式
		m = a;
	}
	public void run() { 	// 覆寫run方法
		for (int i = 1; i <= m; i++) {
			System.out.println(Thread.currentThread().getName() + " = " + i);
		}
	}
}

public class RunnableThread {
	public static void main(String[] args) {
		//建立Runnable物件obR1，並傳入引數20
		MyThread2 obR1 = new MyThread2(20);
		//建立Runnable物件obR2，並傳入引數25
		MyThread2 obR2 = new MyThread2(25);
		//建立Thread物件obT1，並傳入obR1和執行緒名稱
		Thread obT1 = new Thread(obR1, "執行緒1");
		//建立Thread物件obT2，並傳入obR2和執行緒名稱
		Thread obT2 = new Thread(obR2, "執行緒2");
		obT1.start(); // 啟動obT1執行緒
		obT2.start(); // 啟動obT2執行緒
	}
}
```
