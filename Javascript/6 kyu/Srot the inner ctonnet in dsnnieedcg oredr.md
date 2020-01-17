```javascript
function sortTheInnerContent(words){
 return words.split(' ').map((el) => {
    if (el.length === 1) return el;
    else {
    let st = el.split('');
    let a = st.slice(1,st.length-1).sort().reverse().join('');
    let newEl = st[0] + a + st[st.length-1];
    return newEl
    }
  }).join(' ')
}
```