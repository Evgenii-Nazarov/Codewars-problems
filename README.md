#### Find Nearest square number 8 kyu
```java 
public class CodeWarsMath {
  public static int nearestSq(final int n){
   double m = n;
   double sqrt =  Math.round( Math.sqrt(m) );
   int a = (int) sqrt;
   return a * a;
  }
}
```