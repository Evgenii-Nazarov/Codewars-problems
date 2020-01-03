# solved-problems

#### Buying a car 6 kyu
```javascript
function nbMonths(startPriceOld, startPriceNew, savingperMonth, percentLossByMonth){
  let s = 0, i =1;
  percentLossByMonth = percentLossByMonth * 0.01
  while (s + startPriceOld < startPriceNew) {
    startPriceOld -= startPriceOld * percentLossByMonth
    startPriceNew -= startPriceNew * percentLossByMonth
    s += savingperMonth

    if ( i % 2 ) percentLossByMonth += 0.005
    i++;
  }
  return( [ i-1 , Math.round(s + startPriceOld - startPriceNew) ]);
}
```

#### Divide and Conquer 7 kyu
```javascript
function divCon(x){

  let num = 0;

  for (i = 0;i<x.length;i++){
    if (typeof (x[i]) === 'number') {
      num +=x[i]
    } else 
    num += -x[i];
  }

return num;
}
```

#### Find the first non-consecutive number 8 kyu
```javascript
function firstNonConsecutive (arr) {

  for(i = 0; i < arr.length-1; i++){
    if ( arr[i]+1!==arr[i+1]) return arr[i+1]
  }
  return null
}
```