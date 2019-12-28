# solved-problems

#### Title Case 6 kyu
```javascript
function titleCase(title, minorWords) {
console.log(title, minorWords);
const tilteArr = title.toLowerCase().split(' '),
finalArr = [];
if (title === '' || minorWords === '') return ''
if (minorWords === undefined) {
  for( let i = 0; i < tilteArr.length; i++){
   const arr = tilteArr[i].toLowerCase().split('')
         
         arr[0] = arr[0].toUpperCase()
         console.log(arr);

         finalArr.push(arr.join(''));
  }
  return finalArr.join(' ')
}

   const minorWordsArr = minorWords.toLowerCase().split(' ');
    
  for( let i = 0; i < tilteArr.length; i++){
    let wordFromMinorWords = minorWordsArr.find((word)=> word === tilteArr[i])
 
    if(wordFromMinorWords){
      if (i === 0) {
        const arr = wordFromMinorWords.toLowerCase().split('')
        arr[0] = wordFromMinorWords[0].toUpperCase()
        wordFromMinorWords = arr.join('')
        finalArr.push(wordFromMinorWords);
      } else {
        finalArr.push(wordFromMinorWords.toLowerCase())
      }
    } else {
         const arr = tilteArr[i].toLowerCase().split('')
         
         arr[0] = arr[0].toUpperCase()
         console.log(arr);

         finalArr.push(arr.join(''));
    }
  }
  return(finalArr.join(' '));
}
}
```

#### Mexican Wave 6 kyu
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