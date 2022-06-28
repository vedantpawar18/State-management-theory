

components of the React tic tac toe are:
1.Square
2.Board (consisting of 3x3 Square Components)
3.Game (parent of Board)
The idea is that whenever a square Component is clicked the clicked event will pass up to the Board and further up to the Game Component. The Game Component will handle this onClick event.
handleClick(i) is a function inside Board Component.