```javascript
function dataReverse(data) {
  let arr = [], str = ''
  for ( let i = 0; i < data.length; i += 8) {
    arr.push(data.slice(i, i+8))
  }
  arr.reverse().forEach((a) => {
    a.forEach( (b) => str+= b)
  });
  return(str.split('').map(a => +a));
}
```