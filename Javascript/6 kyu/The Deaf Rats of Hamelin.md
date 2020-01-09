```javascript
var countDeafRats = function(town) {
  let i = 0, mice = '~O', count = 0;
  town = town.replace(/\s+/g, '');  

  while (i < town.length) {
 
    if ( town[i] === 'P') {
      mice = 'O~'
      i++;
      continue;
    }
    if ( town[i] + town[i+1] !== mice ) {
      count++;
      console.log( town[i] + town[i+1] );
    }
    
    i+=2;
  }
  
  return(count);
}
```