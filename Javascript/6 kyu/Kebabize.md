```javascript
function kebabize(str) {
  str = str.replace(/[0-9]/g,'');
  let arr = str.split('');
  for (let i = 0; i < arr.length; i++) {
    if (i === 0 && arr[i].toUpperCase() === arr[i] ) {
      arr[i] = arr[i].toLowerCase()
    } else if (arr[i].toUpperCase() === arr[i]) {
      arr[i] = '-' + arr[i].toLowerCase()
     }
  }
  
  
  return(arr.join(''));
}
```