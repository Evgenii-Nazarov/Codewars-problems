# solved-problems

#### String incrementer 5 kyu
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

#### Human Readable Time 5 kyu
```javascript
function humanReadable (s) {
const a = [], b = [];
if ( s === 0 ) return '00:00:00';

a.push(  Math.floor( s/ 3600 ) );
s -= a[0]*3600;
  
a.push(  Math.floor( s/ 60 ) );
s -= a[1]*60;

a.push (s);
  
a.forEach(a=> {
  if (a<10) b.push(String('0'+a));
  else b.push(String(a))
} );

return(b.join(':'));

}
```

#### IP Validation 6 kyu
```javascript
function isValidIP(str) {
  const r = str.split('.');
  console.log(r);
  if (r.length !== 4) return false;
  const a = r.filter( a=> {
    if ( String(+a) != a || Number.isNaN(+a) || a > 255 || a < 0 || ( a[0] == 0 && a.length > 1) ) 
      return true
  });
  if (a.length !== 0) return false;
  return true
  }
```