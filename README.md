# solved-problems

#### Street Fighter 2 - Character Selection 6 kyu
```javascript
function streetFighterSelection(fighters, position, moves){
  const answer = [];
  
  const movesFn = (move) => {
    if (move === 'up') {
      position[0] = 0;
      answer.push(fighters[position[0]][position[1]])
    }
    
    if (move === 'down') {
      position[0] = 1;
      answer.push(fighters[position[0]][position[1]])
    }
  
    if (move === 'left') {
      position[1] =  position[1] === 0? 5: --position[1]
      answer.push(fighters[position[0]][position[1]])
    }
    
    if (move === 'right') {
      position[1] =  position[1] === 5? 0: ++position[1]
      answer.push(fighters[position[0]][position[1]])
    }
  
  }
  
  for (let i = 0; i <moves.length; i++) {


    movesFn(moves[i])

  }
return(answer);
}
```