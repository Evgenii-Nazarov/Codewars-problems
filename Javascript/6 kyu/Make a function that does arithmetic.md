```javascript
function arithmetic(a, b, operator){
  const o = {
    add:  a+b,
    subtract: a-b,
    multiply: a*b,
    divide: a/b,
  }
  return o[operator];
}
```