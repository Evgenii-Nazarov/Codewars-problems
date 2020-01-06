```javascript
function isPangram(string){
let a = 'qwertyuiopasdfghjklzxcvbnm';
  for ( let i = 0; i < a.length; i ++) {
    let c = string.indexOf(a[i]);
    let b = string.indexOf( a[i].toUpperCase() );
    if (  c === -1 && b === -1 ) return false;
  }
  return true;
}
```