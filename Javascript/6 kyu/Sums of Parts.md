```javascript
function partsSums(ls) {
if (ls.length === 0) return [0];
  let ans = [ ls.reduce((a,b) => a + b) ];
  
   for (let i = 1; i < ls.length; i++) {
      ans.push( ans[i-1] - ls[i-1]);
    }
  ans.push(0);
  return( ans);
}
```