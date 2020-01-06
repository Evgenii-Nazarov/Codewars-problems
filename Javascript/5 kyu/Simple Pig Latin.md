```javascript
function pigIt(str){
 str = str.split(' ').map( function (a) {
   if ( a !== '!' || a !== '?') {
    a = a.split('');
    a.push(a[0],"ay");
    a.splice(0,1);
    a= a.join('')
    return a
  }}).join(' ');
  if (str[str.length-3] == '!' || str[str.length-3] =='?') {
   str = str.substr(0,str.length-2)
  }
  return (str)
}
```