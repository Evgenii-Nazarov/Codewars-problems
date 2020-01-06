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