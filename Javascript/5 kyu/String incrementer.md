```javascript
function incrementString (s) {
  const a = [];
  let count = 0;
  for (let i = s.length-1; i >= 0; i --){
    
    if (!Number.isNaN(+s[i])) {
        a.unshift(s[i];
        count++;
        }
  }

  let newNumber = String(+a.join('')+1);
  const letters = s.slice( 0,s.length-count);

  if ( newNumber.length >= a.length) {
    return(letters+newNumber);
  } else {
    let arr = newNumber.split('');
     while ( arr.length < a.length){
       arr.unshift('0')
     }
    newNumber = arr.join('');
    return( letters+newNumber);
  }

}
```