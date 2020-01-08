```javascript
function validPhoneNumber(p){
  const n = '0123456789';
  const f = p.split('').filter((a) => n.indexOf(a) !== -1 );
  const ans = `(${f[0]+f[1]+f[2]}) ${f[3]+f[4]+f[5]}-${f[6]+f[7]+f[8]+f[9]}`
  return p === ans? true: false
}
```