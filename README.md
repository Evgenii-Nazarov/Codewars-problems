# solved-problems
#### Permute a Palindrome
```javascript
function permuteAPalindrome (input) { 
let c = {};
  for ( let i = 0; i < input.length; i++) {
    if ( !c[input[i]] ) c[input[i]] = 1;
    else c[input[i]] ++;
  }
    let count = 0;
  for ( let key in c) {
   if ( c[key] % 2 === 0 ) delete c[key];
    else count ++;
    if ( count > 1 ) return false;
  }
return true;
}
```
#### Most valuable character
```javascript
function solve(st) {
  let a = {}, max = 0, c = st[0];
  for ( let i = 0; i < st.length; i++) {
    let b = st.lastIndexOf(st[i]) - st.indexOf(st[i]);
    if ( b > max ) {
      max = b;
      c = st[i];
    } else if ( b === max && st[i] < c) {
      c = st[i];
    }
  }
 return c;
}
```

#### How many days are we represented in a foreign country?
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