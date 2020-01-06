```javascript
function daysRepresented(trips){
  let r = [];
  trips.forEach( a =>{
   for (let i = a[0]; i <= a[1]; i++) {
     r.push(i);
   }
  })

  return r.filter( (x,i) => r.indexOf(x) === i).length;
}
```