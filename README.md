# solved-problems

#### Find the missing term in an Arithmetic Progression 6 kyu
```javascript
var findMissing = function (list) {  
  let difference = list[1]-list[0];
  let testMin = list[2] - list[1]
  if (testMin<0) {
    if ( testMin > difference) difference = list[2] - list[1]
  } else {
      if ( testMin < difference) difference = list[2] - list[1]
    }
  for ( let i = 0; i < list.length; i++) {
    if ( list[i] + difference !== list[i+1]) return list[i] + difference
  }
}
```

#### WeIrD StRiNg CaSe 6 kyu
```javascript
function toWeirdCase(string){
  const result = [];
  const strArr = string.toLowerCase().split(' ');
  strArr.forEach( (a)=>{
    let newWord = '';
    let wordArr = a.split('');
    wordArr.forEach( (a,i)=> {
     if (i%2) newWord += a
     else newWord += a.toUpperCase()
    })
    result.push(newWord)
  })
  return result.join(' ')
}
```