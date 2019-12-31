# solved-problems

#### Tortoise racing 6 kyu
```javascript
function race(v1, v2, g) {
  if (v1 >= v2) return null
  const time = [];
  let t =  g/ (v2-v1);
  const hours = Math.trunc(t);
  time.push( hours );
  const minutes = Math.trunc(t*60%60);
  console.log(t*60);
  time.push( minutes);
  const seconds = Math.trunc(t*3600%60);
  time.push( seconds );
  console.log(time);
  return(time);
}
```

#### Triple trouble 6 kyu
```javascript
function tripledouble(num1, num2) {
  const arr1 = String(num1).split(''),
        arr2 = String(num2).split('');
  let count = 0;
  let r = 0;
  arr1.forEach( (a,i) => {
 
    if (arr1[i] === arr1[i+1]) {
      count ++
    } else {
      count = 0;
      }
    if (count === 2) {
      let j = 0;
        while ( arr2.indexOf(arr1[i], j) >= 0) {
          let position = arr2.indexOf(arr1[i], j);
          if ( arr2[position] === arr2[position+1]) {
            r++;
            break;
          }
          j = position+1;

        }
      
    }

  })
  return r>0?1:0
}
```

#### Help the bookseller ! 6 kyu
```javascript
function stockList(listOfArt, listOfCat){
  if ( listOfArt == 0 ||  listOfCat == 0) return '';
  let obj = {};
  
  listOfCat.forEach( (letter) => {
    obj[letter] = 0;
  });
  
  listOfArt.forEach( (book) => {
    if ( listOfCat.indexOf(book[0]) >=0 ) {
        obj[book[0]] += +book.split(' ')[1];
      } 
  });
  
  
  const r = [];
  
  for ( let key in obj) {
    r.push( `(${key} : ${obj[key]})`  )
  }
  
  return(r.join(' - '));
}
```