# solved-problems

#### Take a Number And Sum Its Digits Raised To The Consecutive Powers And ....¡Eureka!!
```javascript
function sumDigPow(a, b) {
  const r = [];
  for ( let i = a; i <= b; i++) {
    let c = String(i).split(''), sum = 0;
    for ( let j = 0; j < c.length; j ++) {
      sum += Math.pow (c[j], j+1);
    }
    if ( sum === i) r.push(i);
  }
return(r);
}
```

#### Detect Pangram
```javascript
function isPangram(string){
let a = 'qwertyuiopasdfghjklzxcvbnm';
  for ( let i = 0; i < a.length; i ++) {
    let c = string.indexOf(a[i]);
    let b = string.indexOf( a[i].toUpperCase() );
    if (  c === -1 && b === -1 ) return false;
  }
  return true;
}
```

#### Bouncing Balls
```javascript
function bouncingBall(h,  b,  w) {
if ( h <= 0 || b <= 0 || b >= 1 || w >= h) return -1;
  let r = 1;
  h = h * ( b) ;
  while (h > w) {
    h = h * ( b);
    r+=2;
  }

  return(r)
}
```