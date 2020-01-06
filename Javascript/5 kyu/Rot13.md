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