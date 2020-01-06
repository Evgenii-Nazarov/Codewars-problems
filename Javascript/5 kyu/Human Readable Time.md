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