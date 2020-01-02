# solved-problems

#### Remove exclamation marks 8 kyu
```java
class Solution {
    static String removeExclamationMarks(String s) {
        int ind = 0 ;
        while ( s.indexOf('!') != -1) {
          ind = s.indexOf('!');
          s = s.substring(0, ind) + s.substring(ind + 1);
        }
    return s;
    }
}

```

#### Get the mean of an array 8 kyu
```java
public class School{

 	public static int getAverage(int[] marks){
		int score = 0;
    for ( int i = 0; i < marks.length; i++ ) {
      score += marks[i];
    }
    score = score / marks.length;
    
    return score;
	}

}
```

#### Transportation on vacation 8 kyu
```java
public class Kata {
  public static int rentalCarCost(int d) {
    int result;
    if (d< 3) {
      result = d*40;
    } else if (d< 7) {
        result = d*40-20;
      } else {
          result = d*40-50;
        }
    return result;
  }
}

```