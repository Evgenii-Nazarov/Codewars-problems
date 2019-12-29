# solved-problems

#### Text align justify 4 kyu
```javascript
var justify = function(str, len) {
  let arr = str.split(' ');
  let resultTotal = '';
  console.log(arr);
  while (arr.length > 0) {
      let newStr = arr[0];
      let i = 1;
    while ( (newStr +' '+ arr[i]).length < len) {
       if (arr[i] === undefined) {
        resultTotal +=newStr;
        console.log(resultTotal);
         return resultTotal
        break;
      }
      newStr +=' '+ arr[i] ;
      i++;
     
    }
    let newArr = newStr.split(' ')
    let numberOfNeededSpaces = len - newArr.join('').length;
    console.log( numberOfNeededSpaces);
    newArr = newArr.map( (x,i) => {
      x+= ' '.repeat( Math.ceil(numberOfNeededSpaces/ ( newArr.length-(i+1) ) ));
      numberOfNeededSpaces -=Math.ceil(numberOfNeededSpaces/ ( newArr.length-(i+1) ) );

      return x
    });  
    result=newArr.join('')+'\n'
    console.log(result);
    console.log(result.length);
    resultTotal +=result
    arr.splice(0,i)

  }
}
```