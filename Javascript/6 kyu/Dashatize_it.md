```javascript
function dashatize(num) {
if ( Number.isNaN(num) )return 'NaN';
  let ans = '', arr = [];
  num = num < 0? -num: num;
  let str = String(num);
  for ( let i = 0; i < str.length; i++ ) {

   if ( str[i] % 2 === 0 ) {
     ans+=str[i]
   }
   else {
     arr.push(ans , str[i]);
     ans = '';
   }
  }
  arr.push(ans );
  return arr.filter(Boolean).join('-');
}
```