```javascript
var moveZeros = function (arr) {
let arr1 = [], arr0 = [];
  
  for( let i = 0; i < arr.length; i++){
    if ( arr[i] !== 0){
      arr1.push(arr[i])
    } else {
      arr0.push(arr[i])
    }
    
  }
  return( [...arr1,...arr0]);
}
```