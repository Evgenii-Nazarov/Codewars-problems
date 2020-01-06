```javascript
function formatDuration (s) {
const a = {}, b = [];
let str = '';
if ( s === 0 ) return 'now'  

a.year=( Math.floor(s/31536000) );
s -= a.year*31536000;
 
a.day=(  Math.floor( s/ 86400 ) )
s -= a.day*86400;

a.hour=(  Math.floor( s/ 3600 ) )
s -= a.hour*3600;
  
a.minute=(  Math.floor( s/ 60 ) )
s -= a.minute*60;

a.second= (s)
  
for ( let key in a) {
  if ( a[key] === 0) {
    delete a[key]
  }
}

for ( let key in a) {
  b.push ( a[key] > 1? `${a[key]} ${key+'s'}`: `${a[key]} ${key}`);
}  

if (b.length > 1) {
  return( b.slice( 0, b.length-1).join(', ') + ' and ' + b[b.length-1]  );
} else return (b.join());

}
```