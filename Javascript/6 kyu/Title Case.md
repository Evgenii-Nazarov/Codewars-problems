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