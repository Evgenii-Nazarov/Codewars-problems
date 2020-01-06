```javascript
function solve(st) {
  let a = {}, max = 0, c = st[0];
  for ( let i = 0; i < st.length; i++) {
    let b = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
    if ( b > max ) {
      max = b;
      c = st[i];
    } else if ( b === max && st[i] < c) {
      c = st[i];
    }
  }
 return c;
}
```