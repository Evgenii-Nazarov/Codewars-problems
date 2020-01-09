```javascript
function vowelBack(s){
  let ans = '';
  const vowels = 'aiu', 
        expection = 'code';
  for ( let i = 0; i < s.length; i ++) {
    
    if ( vowels.indexOf(s[i]) !== -1) {
      let charCode = s[i].charCodeAt(0) - 5
      if ( charCode < 97) charCode += 26
      let newLetter = String.fromCharCode(charCode);
      ans += expection.indexOf(newLetter) !== -1? s[i]:newLetter;
    }   

    else if ( s[i] === 'c' ) {
      ans += 'b'
    }
    
    else if ( s[i] === 'o' ) {
      ans += 'n'
    }
    
    else if ( s[i] === 'd' ) {
      ans += 'a'
    }
    
    else if ( s[i] === 'e' ) {
      ans += 'a'
    }
      
    else {
      let charCode = s[i].charCodeAt(0) + 9
      if ( charCode >122) charCode -= 26
      let newLetter = String.fromCharCode(charCode);
      ans += expection.indexOf(newLetter) !== -1? s[i]:newLetter;
      
    }
    
    
  }
  
  return(ans);
}
```