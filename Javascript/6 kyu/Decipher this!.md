```javascript
function decipherThis(str) {
  let string = '0123456789';
 let arr = str.split(' ');
  arr = arr.map(el=> {
    let st = '';
    let i = 0;
    for ( i = 0; i < el.length; i++){
      
     if ( string.indexOf(el[i]) === -1){
        break;
      } else {
        st+=el[i];
      }
      
    }
    if (el.slice(i).length === 1){
        return String.fromCharCode(+st)+ el.slice(i,i+1)
      } else if (el.slice(i).length === 0) {
        return String.fromCharCode(+st)
      } else {
        return String.fromCharCode(+st)+el[el.length-1]+el.slice(i+1,-1)+el.slice(i,i+1)
      }


  });
  return(arr.join(' '));
};
```