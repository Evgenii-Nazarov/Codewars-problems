```javascript
function diamond(n){
if (!(n%2)||n<0) return null;
  let str = '',
      arr = [];
  for (let i = n; i >=1; i-=2) {
    str = ' '.repeat((n-i)/2) + '*'.repeat(i)+'\n';
    arr.push(str)
  }
  
  arr = arr.slice(1).reverse().concat(arr);
  return arr.join('');
}
```