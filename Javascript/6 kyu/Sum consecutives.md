```javascript
function sumConsecutives(s) {
    const ans = [];
    let num = s[0];
    s.forEach((a,i) => {
      if (s[i] === s[i+1]) {
        num += s[i];
      } else {
          ans.push(num);
          num = s[i+1];
        }
    })
    return (ans);
}
```