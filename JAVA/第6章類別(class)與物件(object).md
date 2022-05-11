# 第6章類別(class)與物件(object)

```java
public class Ccar {
	public double gas, tbo;              //宣告最多載油量, 平均耗油量
	public double max_dist = 0;          //加滿油可行駛最長距離
	
	public void maxDist() {              //計算可行駛最長距離
	    max_dist = gas * tbo;
	}
	 
	public double dist(double oil) {     //一般加油可行駛距離
	    return oil * tbo;
	}
}

```



```java

public class BuildObject {
	public static void main(String[] args) {
	    Ccar car1;                         //宣告car1物件
		car1 = new Ccar();                 //建立car1物件
		car1.gas = 40;                     //設定car1物件的屬性值
		car1.tbo = 13.6;
		car1.maxDist();                    //呼叫car1物件的方法
		double distance = car1.dist(20);   //呼叫car1物件的方法,並取得傳回值
		System.out.println("car1汽車資訊：");
		System.out.println("最大載油量：" + car1.gas + " L");
		System.out.println("平均耗油量：" + car1.tbo + " km/L");
		System.out.println("加滿油可行駛 " + car1.max_dist + " km");
		System.out.println("加油20L可行駛 " + distance + " km");
			    
		Ccar car2 = new Ccar();            //宣告並建立car2物件
		car2.gas = 60;                     //設定car2物件的屬性值
		car2.tbo = 9.5;
	}
}
```

## 物件導向程式設計(object-oriented programming)
- 類別(class)與物件(object)
- 物件導向程式設計三大特徵:
  - 封裝(Encapsulation)
    - private (私有)  protected (保護) public (公開)
  - 繼承
  - 多形

```java

class Ccar {                      //汽車類別
    private double gas, tbo;       //宣告最多載油量, 平均耗油量
    private double max_dist;       //加滿油可行駛最長距離

    private void maxDist() {       //計算可行駛最長距離
       max_dist = gas * tbo;
    }

    public void setValue(double g, double t) { //傳入資料
       gas = g;
       tbo = t;
       maxDist();
    }

    public double getDist() {      //傳出資料
       return max_dist;
    }
 }

public class Encapsulate {       //主類別
    public static void main(String[] args) { //主程式
       Ccar car1;                            //宣告car1物件
       car1 = new Ccar();                    //建立car1物件
       double g1 = 40, t1 = 13.6;
       car1.setValue(g1, t1);                //設定car1物件的屬性值
       double distance1 = car1.getDist();    //取得car1物件的方法傳回值
       System.out.println("car1加滿油可行駛 " + distance1 + " km");
       Ccar car2 = new Ccar();               //宣告並建立car2物件
       car2.setValue(60, 9.5);               //設定car1物件的屬性值
       System.out.println("car2加滿油可行駛 " + car2.getDist() + " km");
    }
}
```

## 6.3 方法多載

```
「多載」是指同一個類別內，有兩個以上相同名稱的方法，但是因為各個方法所要傳入的引數個數不同，
或者是引數的資料型別不同，則這些方法將被視為不同，且各有各自的內容。
```

```java
class Cavg {
    public double getAvg(int num1, int num2) {
       return (num1+num2)/2;
    }
    public double getAvg(double num1, double num2) {
       return (num1+num2)/2;
    }
    public double getAvg(int[] vArray) {
       int n = vArray[0];
       for(int i=1; i<vArray.length; i++){
          n += vArray[i];
       }
       double avg = (double)n/vArray.length;
       return avg;
    }
}

public class Overload {                          //主類別
    public static void main(String[] args) {     //主程式
	   Cavg num = new Cavg();
	   int n1 = 20, n2 = 30;
	   System.out.println(n1 + " 和 " + n2 + "平均值為 " + num.getAvg(n1, n2));
	   int[] ary = {12,23,31,45,56};
	   System.out.println("{12,23,31,45,56}平均值為 " + num.getAvg(ary));
	}
}
```
