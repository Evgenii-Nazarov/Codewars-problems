```javascript
function solution(string) {
  let s = '';
  const arr = [];
  for (let i = 0; i < string.length; i++) {
    if (string[i].toLowerCase() === string[i]) {
      s +=string[i]
    } else {
      arr.push(s);
      s = string[i];
    }
  }
  arr.push(s)
    return (arr.join(' '))
}
```