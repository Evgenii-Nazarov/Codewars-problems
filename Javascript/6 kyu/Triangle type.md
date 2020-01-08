```javascript
function triangleType(a, b, c){
  let arr = [a,b,c].sort((a,b) => b - a);
  if (arr[1] + arr[2] <= arr[0]) return 0
  
  const l = Math.pow(arr[1],2) + Math.pow(arr[2],2);
  const cSqr = Math.pow(arr[0],2);
  
  return cSqr < l ?  1 : cSqr > l ? 3 : 2
}
```