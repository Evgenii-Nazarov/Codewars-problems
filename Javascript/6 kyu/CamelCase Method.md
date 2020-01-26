```javascript
String.prototype.camelCase=function(){
  if (this.length === 0) return '';
  let arr = this.split(' ').filter(Boolean).map((el) => {
       return el[0].toUpperCase()+el.slice(1)
        });
       return(arr.join(''))
}
```