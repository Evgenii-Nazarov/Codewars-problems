```javascript
function mazeRunner(maze, directions) {
console.log(maze, directions);
  let point = [];
  maze.forEach( (arr,i) => {
    if (arr.indexOf(2) !== -1) point = [i,arr.indexOf(2)]
  });
  
  function move (direction) {
    if (direction === 'N') {
      point[0]--; 
    }
    
    if (direction === 'S') {
      point[0]++; 
    }
    
    if (direction === 'W') {
      point[1]--; 
    }
    
    if (direction === 'E') {
      point[1]++; 
    }
  }
  
    for ( let i = 0; i < directions.length; i++) {
      move(directions[i]);
      if (maze[point[0]] === undefined) return 'Dead';
      const currentPosition = maze[point[0]][point[1]];
      if (currentPosition === 1 || currentPosition === undefined) return 'Dead';
      else if (currentPosition === 3) return 'Finish'
    }
    
  return 'Lost'
}
```