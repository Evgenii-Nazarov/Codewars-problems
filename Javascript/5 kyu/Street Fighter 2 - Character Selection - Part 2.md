```javascript
function superStreetFighterSelection(fighters, position, moves){
  const answer = [];
  
  const movesFn = (move) => {
    
    if (move === 'up') {
      
      if (position[0] === 0) {
         answer.push(fighters[position[0]][position[1]])
      } else {
          if ( fighters[ position[0] - 1 ][ position[1] ] !== '' ) {
            position[0] -= 1;
          }
        answer.push(fighters[position[0]][position[1]])
        }
       
      }
    
    if ( move === 'down' ) {
      if (position[0] === fighters.length-1 ) {
        answer.push( fighters[position[0]][position[1]] )
      } else {
          const newPosition = fighters[ position[0] + 1 ][ position[1] ]
          if ( newPosition !== '') {
            position[0] += 1;
          }
        answer.push( fighters[position[0]][position[1]] )
        }
       
    }
 
  
    if (move === 'left') {
      let newPosition = position[1]===0? fighters[ position[0] ].length-1: position[1] -1;
      console.log(newPosition);
      while (newPosition !== position[1]) {
        
        if (newPosition === 0) {
          if (fighters[ position[0] ][ newPosition ] !== '') {
            position[1] = newPosition;
            break;
          }
          newPosition = fighters[ position[0] ].length-1;
          continue;
        }
        
        if (fighters[ position[0] ][ newPosition ] !== '') {
          position[1] = newPosition;
          break;
        }
        
        newPosition -= 1;
      }
      
      
      
      answer.push(fighters[position[0]][position[1]])
    }
    
    if (move === 'right') {
      let newPosition = position[1]===fighters[ position[0] ].length-1? 0: position[1] +1;
      console.log(newPosition);
      while (newPosition !== position[1]) {
        
        if (newPosition === fighters[ position[0] ].length-1 ) {
          if (fighters[ position[0] ][ newPosition ] !== '') {
            position[1] = newPosition;
            break;
          }
          newPosition = 0;
          continue;
        }
        
        if (fighters[ position[0] ][ newPosition ] !== '') {
          position[1] = newPosition;
          break;
        }
        
       newPosition += 1;
     }
      
      
      
      
      answer.push(fighters[position[0]][position[1]])
    }
  
  }
  
  for (let i = 0; i <moves.length; i++) {
    

    movesFn(moves[i])
      
  }
return(answer);
  

}
function superStreetFighterSelection(fighters, position, moves){
  const answer = [];
  
  const movesFn = (move) => {
    
    if (move === 'up') {
      if (position[0] === 0) {
         answer.push(fighters[position[0]][position[1]])
      } else {
          if ( fighters[ position[0] - 1 ][ position[1] ] !== '' ) {
            position[0] -= 1;
          }
        answer.push(fighters[position[0]][position[1]])
        }
      }
    
    if ( move === 'down' ) {
      if (position[0] === fighters.length-1 ) {
        answer.push( fighters[position[0]][position[1]] )
      } else {
          const newPosition = fighters[ position[0] + 1 ][ position[1] ]
          if ( newPosition !== '') {
            position[0] += 1;
          }
        answer.push( fighters[position[0]][position[1]] )
        }
    }
 
  
    if (move === 'left') {
      let newPosition = position[1]===0? fighters[ position[0] ].length-1: position[1] -1;
      console.log(newPosition);
      while (newPosition !== position[1]) {
        if (newPosition === 0) {
          if (fighters[ position[0] ][ newPosition ] !== '') {
            position[1] = newPosition;
            break;
          }
          newPosition = fighters[ position[0] ].length-1;
          continue;
        }
        if (fighters[ position[0] ][ newPosition ] !== '') {
          position[1] = newPosition;
          break;
        }
        newPosition -= 1;
      }
      answer.push(fighters[position[0]][position[1]])
    }
    
    if (move === 'right') {
      let newPosition = position[1]===fighters[ position[0] ].length-1? 0: position[1] +1;
      console.log(newPosition);
      while (newPosition !== position[1]) {
        if (newPosition === fighters[ position[0] ].length-1 ) {
          if (fighters[ position[0] ][ newPosition ] !== '') {
            position[1] = newPosition;
            break;
          }
          newPosition = 0;
          continue;
        }
        if (fighters[ position[0] ][ newPosition ] !== '') {
          position[1] = newPosition;
          break;
        }
       newPosition += 1;
     }
      answer.push(fighters[position[0]][position[1]])
    }
  }
  
  for (let i = 0; i <moves.length; i++) {
    movesFn(moves[i])
      
  }
return(answer);
}
```