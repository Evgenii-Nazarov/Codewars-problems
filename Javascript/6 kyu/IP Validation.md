```javascript
function isValidIP(str) {
  const r = str.split('.');
  console.log(r);
  if (r.length !== 4) return false;
  const a = r.filter( a=> {
    if ( String(+a) != a || Number.isNaN(+a) || a > 255 || a < 0 || ( a[0] == 0 && a.length > 1) ) 
      return true
  });
  if (a.length !== 0) return false;
  return true
  }
```