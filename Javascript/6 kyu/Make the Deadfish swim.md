```javascript
function parse( data ){
  const ans = [];
  let n = 0;
  data.split('').forEach( (el) => {

    if ( el === 'i' ) {
      n++;
    }
    if ( el === 'd' ) {
      n--;
    }
    if ( el === 's' ) {
      n*=n;
    }
    if ( el === 'o' ) {
      ans.push(n);
    }
  });
  
  return ans;
}
```