## 期末平時成績:JAVA例外處理開發報告
```
例外
例外處理
Java常用的內建例外類別
自行拋出例外
自定例外類別
```

## 例外處理
```java
public class ExceptionDemo {
	public static void main(String[] args) {
	   int[] myarray = new int[10];
	   try {
	       myarray[10] = 250;
	   }
	   catch(ArrayIndexOutOfBoundsException e) {
	       System.out.println("例外內容：" + e.toString());
	       System.out.println("也就是：超出陣列索引範圍");
	   }
	   System.out.println("程式最後一行執行完畢");
   }
}
```

## 多個catch敘述
```java
public class MultiException1 {
	public static void main(String[] args) {
		int[] myarray = new int[10];
		try {
		    int test = 120 / 0;
		    myarray[10] = 120;
		    int n = Integer.parseInt("你好嗎");  //字串無法轉換成整數
		}
		catch (ArrayIndexOutOfBoundsException e) {
		    System.out.println("例外內容1：" + e.toString());
		    System.out.println("也就是：超出陣列索引範圍的例外發生");
		}
		catch(ArithmeticException e) {
		    System.out.println("例外內容2：" + e.toString());
		    System.out.println("也就是：數學運算錯誤，如除數為0!");
		}
		catch(Exception e) {
		    System.out.println("例外內容3：" + e.toString());
		    System.out.println("例外發生!");
		}
		System.out.println("程式正確執行完畢!!");
	}
}
```
