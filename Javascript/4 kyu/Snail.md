```javascript
snail = function(a) {
if ( a[0].length === 0) return [];
  let b = [];
while (a.length > 1) {
  let c = a[a.length-1].reverse();
  b.push( a.shift() );
  a.pop();
 
  a.forEach ( a => {
    b.push( a.pop())
  });
 
  b.push(c);

  for ( let i = a.length-1; i >= 0; i --) {
    b.push(a[i].shift());
  }
}  
  if ( a[0] !== undefined) b.push(a[0]);
  
  return(b.join().split(',').map(a=>+a));
}
```