## 期末平時成績:JAVA例外處理開發報告
```
例外
例外處理1
例外處理2
例外處理3
例外處理4
```

## 例外處理1:try… catch… 
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

## 例外處理2:try… catch…catch… catch…  多個catch敘述
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
### 例外處理3:try… catch… finally…
```java
public class FinallyDemo {
	public static void main(String[] args) {
	    int[] myarray = new int[10];
	    try {
	        myarray[20] = 120;
	   	}
	    catch (ArrayIndexOutOfBoundsException e) {
	        System.out.println("例外內容：" + e.toString());
	        System.out.println("也就是：超出陣列索引範圍");
	    }
	    finally {     //finally敘述區塊一定會執行
	        System.out.println("執行finally 程式區塊完成");
	    }
	    System.out.println("程式正確執行完畢!!");
	}
}
```

### 例外處理4:方法的例外處理
```java
public class ExceptionMethod {
	static int[] data = new int[10];
	    public static void init() {
	    data[10] = 250;
	}
	
	public static void main(String[] args) {
	    try {
	        init();
	    }
	    catch (ArrayIndexOutOfBoundsException e) {
	        System.out.println("例外內容：" + e.toString());
	        System.out.println("也就是：超出陣列索引範圍");
	    }
	}
}
```
