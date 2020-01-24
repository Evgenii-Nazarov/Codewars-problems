```javascript
function numericals(s){
  let obj = {}, ans = [];
  
  for (let i = 0; i < s.length; i++) {
    if ( obj[s[i]] === undefined) {
      obj[s[i]] = 1;
    } else {
      obj[s[i]]++;
    }
    ans.push(obj[s[i]])
  }

 return ans.join('');
}
```