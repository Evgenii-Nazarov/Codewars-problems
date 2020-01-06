```javascript
function wave(str){
  const mexicanArr = [];
  for ( let i = 0; i < str.length; i++) {
    const charCode = str[i].charCodeAt(0)
    if ( str[i].toLowerCase() === str[i].toUpperCase()) {
      console.log(str[i]+ ' 1');
    } else {
      let changedArr = str.split('');
      const char = changedArr[i];
      if ( char === char.toLowerCase() ) {
        changedArr[i]= changedArr[i].toUpperCase()
        console.log(char + ' '+changedArr );
      } else {
        changedArr[i]= changedArr[i].toLowerCase()
        console.log('22');
      }
      const changedStr = changedArr.join('')
      mexicanArr.push(changedStr)
    }
  }
  return(mexicanArr);
}
```