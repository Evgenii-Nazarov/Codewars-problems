# solved-problems

#### Count characters in your string 6 kyu
```javascript
function count (string) {  
  let obj = {};
  const arr = string.split('');
  arr.forEach((char)=> {
    if (obj[char]===undefined) obj[char] = 1;
    else obj[char] ++
  })
   return obj;
}
```

#### Two Sum 6 kyu
```javascript
function twoSum(numbers, target) {
  for (let i = 0; i < numbers.length; i++ ) {
    let neededNumber = target - numbers[i];
    if ( numbers.lastIndexOf(neededNumber) !== -1 ) return [i,numbers.lastIndexOf(neededNumber)]
  }
}
```

#### Checking Groups 6 kyu
```javascript
function groupCheck(s){
   console.log(s);
   s = s.split('');
   for ( let i = 0; i < s.length; i ++) {
     if ( s[i] === '(' && s[i+1] === ')') {
       s.splice(i,2);
       i = -1
     }
     if ( s[i] === '[' && s[i+1] === ']') {
       s.splice(i,2);
       i = -1
     }
     if ( s[i] === '{' && s[i+1] === '}') {
       s.splice(i,2);
       i = -1
     }
   }
   return s.length === 0? true:false
 }
```