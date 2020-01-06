```javascript
function meeting(s) {
    let arr = s.toUpperCase().split(';');
    arr = arr.map((name)=> {
      name = name.split(':');
      let oldName = name[0];
      name[0] = name[1];
      name[1] = oldName;
      return '(' + name.join(', ') + ')'
    });
    return(arr.sort().join(''))
}
```