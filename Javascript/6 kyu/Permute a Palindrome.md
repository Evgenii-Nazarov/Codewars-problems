```javascript
function permuteAPalindrome (input) { 
let c = {};
  for ( let i = 0; i < input.length; i++) {
    if ( !c[input[i]] ) c[input[i]] = 1;
    else c[input[i]] ++;
  }
    let count = 0;
  for ( let key in c) {
   if ( c[key] % 2 === 0 ) delete c[key];
    else count ++;
    if ( count > 1 ) return false;
  }
return true;
}
```