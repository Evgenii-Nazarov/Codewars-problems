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