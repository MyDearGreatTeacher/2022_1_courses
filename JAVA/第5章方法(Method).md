#
```
5.2 方法
5.3 傳值呼叫與參考呼叫
5.4 方法間傳遞陣列引數
5.5 方法多載
5.6 遞迴
```

## 5.2 方法(Method)
```
Java 中所使用的方法相當於 C 的函式。
不同處在可重複呼叫還可代表屬於該類別的特有行為，而函式則沒此特性。
```
```
使用時機
寫程式常碰到某個敘述區段需在程式不同地方重複執行。
每次都要再重寫該敘述區段，程式會冗長
會增加除錯和維護時的困難。
```
## 5.2.1 如何定義方法
```
Java 是屬物件導向程式語言，不允許方法以單獨型式存在，必須包含在某個物件之下，成為物件的方法之一。
方法就是物件專屬的函式，所代表該物件的特殊行為。
方法在定義時是由方法標頭及程式區段兩部份所構成

語法： 
```
```java
public class Math {
	static void mul(int x, int y) {
		System.out.print(x + " * " + y + " = " + (x * y));
	}
	void div(int x, int y) {
		System.out.print(x + " / " + y + " = " + (x / y));
	}
}
```

```java
public class Method1 {
	public static void main(String[] args) {
		factorial(6);
		factorial(9);
	}

	static void factorial(int x) {
		int i = x, j = 1;
		while(i > 0)
			j *= i--;
		System.out.println(x + "! = " + j);
	}
}
```

```java
public class Method2 {
	public static void main(String[] args) {
		int n1 = 6, n2 = 9;
		int fac1, fac2;
		fac1 = factorial(n1);
		System.out.println(n1 + "! = " + fac1);
		fac2 = factorial(n2);
		System.out.println(n2 + "! = " + fac2);
	}

	static int factorial(int x) {
		int i = x, fac = 1;
		while(i > 0)
			fac *= i--;
		return fac;
	}
}
```





## 5.3 傳值呼叫(call by value)與參考呼叫(call by reference)

- 傳值呼叫(call by value) == > 把數值傳給
- 參考呼叫(call by reference)
- call by address(記憶體位址)
```java
public class CallByVal {
	public static void main(String[] args) {
		int a = 10, b = 15;
		System.out.println(" 傳值呼叫前\ta=" + a + "\tb=" + b );
		byVal(a, b);
		System.out.println(" 傳值呼叫後\ta=" + a + "\tb=" + b );
	}

	static void byVal(int x, int y) {
		int t; //以變數t作為暫存區，將引數互換
		t = x;
		x = y;
		y = t;
		System.out.println(" 傳值呼叫中\tx=" + x + "\ty=" + y );
	}
}
```
```java
class Obj {
	int a, b;

	Obj() {
		a = 10;
		b = 15;
	}
}

public class CallByRef {
	public static void main(String[] args) {
		Obj obj = new Obj();
		System.out.println(" 參考呼叫前\t a = " + obj.a + "\tb = " + obj.b);
		byRef(obj);
		System.out.println(" 參考呼叫後\t a = " + obj.a + "\tb = " + obj.b);
	}

	static void byRef(Obj p) {
		int t;
		t = p.a;
		p.a = p.b;
		p.b = t;
	}
}
```

## 5.4 方法間傳遞陣列引數
```java
public class MyClass {
	void sub(int x, int y) {
		System.out.print(" 呼叫MyClass類別的sub方法-->");
		System.out.println(x + " - " + y + " = " + (x - y));
	}

	public static void main(String[] args) {
		int a = 25;
		MyClass c1 = new MyClass(); // 建立屬於MyClass類別的物件c1
		c1.sub(a - 5, 3); // 呼叫物件c1的sub方法
		MyCal c2 = new MyCal(); // 建立屬於MyCal類別的物件c2
		c2.sub(a + 3, 5); // 呼叫物件c2的sub方法
	}
}

class MyCal {
	void sub(int x, int y) {
		System.out.print(" 呼叫MyCal  類別的sub方法-->");
		System.out.println(x + " - " + y + " = " + (x - y));
	}
}
```

```java

```

```java

```

```java
public class bubbleSort {
	public static void main(String[] args) {
		int i;
		int[] myArray = new int[] {69,91,12,56,23,78};
		System.out.print("排序前->");
		for(i = 0; i < myArray.length; i ++)
			System.out.print("  " + myArray[i]);
		System.out.println();
		bSort(myArray);
		System.out.print("排序後->");
		for(i = 0; i < myArray.length; i ++)
			System.out.print("  " + myArray[i]);
	}
	
	static void bSort(int[] vArray) {
		int tmp, i, j;
		for(i = vArray.length - 2; i >= 0; i --) {
			for(j = 0; j <= i; j ++) {
				if(vArray[j] > vArray[j + 1]) {
					tmp = vArray[j];
					vArray[j] = vArray[j + 1];
					vArray[j + 1] = tmp;
				}
			}
		}
	}
}

```
## 5.4.2 取得命令列的資料
```
main 方法中虛引數 args 屬字串陣列型別變數。
Args 可用來取得由命令列輸入的資料。
若連續輸入資料
資料間必須使用一個空白來加以區隔
由命令列輸入的第一個資料會放在args[0]，
第二個輸入的資料會放在args[1]，以此類推。

```

```java
public class Score {
	public static void main(String[] args) {
		for (int i = 0; i < args.length; i++)
			System.out.println(" 座號 " + (i + 1) + " 同學成績：" + args[i]);
	}
}
```


## 5.5 方法多載(overloading)

```java
public class AddNum {
	public static void main(String[] args) {
		int total1, x=17, y=28;
		double total2, i=3.8, j=22.7, k=15.1;
		total1 = add(x, y);
		total2 = add(i, j, k);
		System.out.printf("%d%n",total1);
		System.out.printf("%f%n",total2);
	}
	static int add(int a, int b) {
		return a + b; // 傳回兩個整數相加的結果
	}
	static double add(double a, double b, double c) {
		return a + b + c; // 傳回三個倍精確度相加的結果
	}
}
```

```java
public class AddNums {
	public static void main(String[] args) {
		System.out.printf("%d%n", add());
		System.out.printf("%d%n", add(2, 4));
		System.out.printf("%d%n", add(1, 3, 5));
		System.out.printf("%d%n", add(2, 4, 6, 8));
	}
	static int add(int... a) {
		int sum = 0;
		for (int i : a)
			sum += i;
		return sum; // 傳回陣列a元素相加的結果
	}
}
```


```java
public class OverLoading {
	static int max(int x, int y) {
		if (x > y)
			return x;
		else
			return y;
	}

	static double max(double[] vArray) {
		double n = vArray[0];
		for (int i = 1; i < vArray.length - 1; i++) {
			if (vArray[i] > n)
				n = vArray[i];
		}
		return n;
	}

	public static void main(String[] args) {
		int a = 26, b = 37;
		System.out.println(a + "和" + b + "最大的數值為" + max(a, b));
		double f[] = new double[] { 2.1, 5.3, 7.2, 4.8 };
		System.out.println("陣列元素 [2.1,5.3,7.2,4.8] 中最大的數值為" +	max(f));
	}
}
```

## 5.6 遞迴

```java
public class Recursive {
	static int f (int n) {
		if (n == 1)
			return n;
		else
			return n + f(n - 1);
	}

	public static void main(String[] args) {
		System.out.println("10 + 9 + ... + 2 + 1 = " + f(10));
		System.out.println("100 + 99 + ... + 2 + 1 = " + f(100));
	}
}
```
