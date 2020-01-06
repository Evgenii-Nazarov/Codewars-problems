```javascript
function songDecoder(song){
  const wub = song.split('WUB'),
        newWub = [];
  for (let i = 0; i < wub.length; i++) {
    if ( wub[i] !== '') {
      newWub.push( wub[i] );
    }
  }
  return newWub.join(' ')
}
```