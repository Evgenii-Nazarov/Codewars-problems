```javascript
function boredom (staff) {
  const score = {
    accounts : 1,
    finance : 2,
    canteen : 10,
    regulation : 3,
    trading : 6,
    change : 6,
    IS : 8,
    retail : 5,
    cleaning : 4,
    'pissing about' : 25,
  }
  let r = 0;
  let arr = Object.values(staff);
  arr.forEach ( a => {
    r+= score[a];
  })
  return r <= 80? 'kill me now': r >= 100? 'party time!!': 'i can handle this';
  
}
```