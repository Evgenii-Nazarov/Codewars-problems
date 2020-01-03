# solved-problems

#### Thinkful - Logic Drills: Traffic light 8 kyu
```java
public class TrafficLights {

  public static String updateLight(String current) {
    String answer;
    if (current == "red") answer = "green";
    else if (current == "green") answer = "yellow";
    else answer = "red";
    return answer;
  }
}

```

#### Get Nth Even Number 8 kyu
```java
public class Num {
  public static int nthEven(int n) {
    return n * 2 - 2;
  }
}
```

#### Volume of a Cuboid 8 kyu
```java
public class Kata {

  public static double getVolumeOfCuboid(final double length, final double width, final double height) {
    return length*width*height ;
  }
  
}

```

#### Twice as old 8 kyu
```java
public class TwiceAsOld{

  public static int TwiceAsOld(int dadYears, int sonYears){
    int diff = dadYears - sonYears, i = 0, ans;
    
    while ( diff != i * 2) {
      diff ++;
      i++;
    }
    ans = i-sonYears;
    return ans < 0 ? - ans: ans;
  }

}

```