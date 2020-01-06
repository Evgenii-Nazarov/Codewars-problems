```javascript
function validSolution(board){
  const validRow = '123456789';
  
  //проверяем ряды
  
  for (let i = 0; i < board.length; i++){
    let testRow= [...board[i]];
    if ( testRow.sort( (a,b) => a-b).join('') !== validRow ) return false;
    // тут я узнал, что переменные хранят ссылки на массивы так же, как и в java...и что переприсваивать нужно каждый подмассив...
  }

  //проверяем столбы

  for (let i = 0; i < board.length; i++){
    let testColumn = []; 
    for (let j = 0; j < board.length; j++) {//хотя тут правильней было бы j< board[i].length, но так как у нас квадрат, то не важно
      testColumn.push( board[j][i] )
    }
   if ( testColumn.sort( (a,b) => a-b).join('') !== validRow ) return false;  
  }

  //проверяем ячейки 3 х 3
  
  for (let i = 0; i < board.length; i+=3) {
    let testCell = [];
    for (let j = 0; j < board.length; j++){
      testCell.push(board[j][i],board[j][i+1],board[j][i+2])
      if (testCell.length === 9) { //ставим ограничение на 9 значений, так как при 9 значениях получаем наш квадрат.
        if ( testCell.sort((a,b)=>a-b).join('') !== validRow ) return false;
        testCell = []; //обнуляем квадрат и начинаем заполнять уже новым квадратом
      }
    }
  }
  return true
}
```