```javascript
function getLengthOfMissingArray(arr) {
  if (arr === null || arr.length === 0 || arr.some((a) => a === null || a.length === 0) ) return 0
  const newArr = arr.sort( (a,b) => a.length - b.length)
  for ( let i = 0; i < newArr.length-1; i++ ) {  
    if (newArr[i].length + 1 !== newArr[i+1].length) {
      return newArr[i].length + 1
    }
  }
}
```