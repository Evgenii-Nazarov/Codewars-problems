```javascript
function catMouse(x, j){
const m = x.indexOf('m');
const C = x.indexOf('C');
const D = x.indexOf('D');
if (D === -1 || C === -1 || m === -1) return "boring without all three"
if ( C > m && (C < D || D < m) && (C - m) <= j ) return "Caught!"
if ( C < m && (C > D || D > m) && (m - C) <= j ) return "Caught!"

if ( C > m && (C > D || D > m) && (C - m) <= j ) return 'Protected!'
if ( C < m && (C < D || D < m) && (m - C) <= j ) return 'Protected!'

return "Escaped!"
}
```