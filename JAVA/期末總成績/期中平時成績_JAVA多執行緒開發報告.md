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


```
