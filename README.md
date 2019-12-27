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

#### Good vs Evil 6 kyu
```javascript
function goodVsEvil(good, evil){
const goodPower = [1,2,3,3,4,10], evilPower = [1,2,2,2,3,5,10];
const goodArmy = good.split(' '), evilArmy = evil.split(' ');
let goodForce = 0, evilForce = 0;

for ( let i = 0; i < goodArmy.length; i++) {
  goodForce += goodArmy[i] *goodPower[i];
}
for ( let i = 0; i < evilArmy.length; i++) {
  evilForce += evilArmy[i]*evilPower[i];
}
return goodForce === evilForce? 'Battle Result: No victor on this battle field': goodForce > evilForce?'Battle Result: Good triumphs over Evil':'Battle Result: Evil eradicates all trace of Good'
}
}
```

#### Rot13 5 kyu
```javascript
function rot13(message){
  let str = '';
  
  for ( let i = 0; i < message.length; i++){
    console.log(message[i].charCodeAt(0));
    const charIndex = message[i].charCodeAt(0);
    
    if (charIndex > 96 && charIndex < 123){
      
      let rottedCharIndex = charIndex + 13;
      if ( rottedCharIndex > 122) rottedCharIndex -= 26;
      str += String.fromCharCode(rottedCharIndex) ;
      
    } else if (charIndex > 64 && charIndex < 91){
        let rottedCharIndex = charIndex + 13;
        if ( rottedCharIndex > 90) rottedCharIndex -= 26;
        str += String.fromCharCode(rottedCharIndex) ;
      } else {
        str+=message[i]
      }
  }
  console.log(str);
  return str;
}
```