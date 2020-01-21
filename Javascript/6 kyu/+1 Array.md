```javascript
function upArray(arr){
  if (arr.length === 0) return null;
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > 9 || arr[i] < 0 || typeof(arr[i]) !== 'number') return null
  }

  for (let i = arr.length-1; i >=0; i--) {
    arr[i]++;
    if (arr[i] === 10) arr[i] = 0;
    else break;
  }
  if (arr[0] === 0) arr.unshift(1);
  return(arr);
}

```