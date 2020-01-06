```javascript

function longest (str) {
  let startIndex = 0, maxSI = 0, endIndex = 0, maxEI = 0, len = 1, maxLen = 1, ans = '';
  for ( let i = 0; i < str.length-1; i ++) {
    if ( str[i+1].charCodeAt(0) >= str[i].charCodeAt(0) ) {
      endIndex ++;
      len++;
    } else {
        if ( len > maxLen) {
        maxLen = len;
        maxSI = startIndex;
        maxEI = endIndex;
        }
        startIndex = i+1;
        endIndex = i+1;
        len = 1;
      }
  }

  if ( len > maxLen) {
    maxLen = len;
    maxSI = startIndex;
    maxEI = endIndex;
  }
  for ( let i = maxSI; i <= maxEI; i++) {
    ans+=str[i]
  }
  return(ans)
}
```