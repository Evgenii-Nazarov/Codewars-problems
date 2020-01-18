```javascript
function solve(s) {
  const v = 'aeiou';
  let current = 0,
      max = 0;
  for (let i = 0; i < s.length; i ++) {
    if (v.indexOf(s[i]) === -1 ) {
      current += s[i].charCodeAt(0) - 96
    } else {
      if (current > max) {
        max = current;
        current = 0;
      } else {
        current = 0;
      }
    }
    if (current > max) {
        max = current;
      } 
  }
  return(max);
};
```