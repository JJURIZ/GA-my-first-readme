## Vanilla JavaScript Tic Tac Toe

Below is a description of my code for a vanilla JS version of Tic Tac Toe. 
In this version each click alternates between X's and O's. 

## How to Play
The two easiest methods to play this version of Tic Tac Toe are listed below.
### Method One
1. `Fork` and `Clone` the repository [here](https://github.com/JJURIZ/tic-tac-toe).
2. Once cloned, open the `tic-tac-toe` folder in VS Code or an editor of your choice. 
3. If using [LiveServer](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) click "Go Live"
	at the bottom right of the editor. Otherwise open the index.html in your favorite browser. 
4. Play to your heart's content.

### Method Two
1. Go to [Codepen.io](http://www.codepen.io). 
2. Create a new Pen.
3. Open the Tic-Tac-Toe repository [here](https://github.com/JJURIZ/tic-tac-toe).
4. Open the index.html file and copy the contents into the HTML form in codepen.
5. Repeat this step for the CSS and JavaScript files. 

## Technologies Used
### HTML
The Game Board
```html
<body>
  <div class="main_container">
  <h1>Tic-Tac-Toe</h1>
    <div class="box_container" id="board">
      <div class="box" id="box0"></div>
      <div class="box" id="box1"></div>
      <div class="box" id="box2"></div>
      <div class="box" id="box3"></div>
      <div class="box" id="box4"></div>
      <div class="box" id="box5"></div>
      <div class="box" id="box6"></div>
      <div class="box" id="box7"></div>
      <div class="box" id="box8"></div>
    </div>
    <button id="reset-button">Reset</button>
    </div>
```
### CSS
Container Style
```css
.box_container {
  display: grid;
  grid-template-columns: 150px 150px 150px;
  grid-template-rows: 150px 150px 150px;
  max-width: 450px;
  position: absolute;
  top: 5rem;
  }
```
### JavaScript
Winner Check Script
```javascript
function checkForWin() {
    let winner = null;
    if (turnNumber >= 5) {
    winningArray.forEach(function(combo, index) {
        if (board[combo[0]] && board[combo[0]] === board[combo[1]] && board[combo[0]] === board[combo[2]])
            winner = board[combo[0]];
    });
    if (winner !== null) {
        changeStatus();
    } else  if (turnNumber === 9) {
        return alert("It's a tie!")
    } else {
        return null;
    }
}
};
```
## JavaScript Game Elements
| Variables | Description |
| ----------- | ----------- |
| `turn` | Holds the current player's symbol (X or O) |
| `turnNumber` | Tracks the number of clicks on the baord. At 9 clicks if no winner is declared the game is a draw/tie |
| `box0 - box8` | Clickable game elements which display the user's symbol |
| `turnNumber` | Using querySelector grabs the box elements from the board |
| `resetButton` | Using querySelector grabs tthe reset button |
| `winningArray` | Nested array containing all possible winning combinations |
| `emptyBoard` | Contains empty array representing the indexes of the board |
| Functions | Description |
| ----------- | ----------- |
| `changeStatus()` | Controls whether game is active |
| `checkForWin()` | Checks to see if a winner has been reached |
| `handleClick()` | Handles actions taken when a player clicks on the game board |
| `resetGame()` | Resets the game so player can clear the board and play again |
| Event Listeners | Description |
| ----------- | ----------- |
| `box0 - box8` | Listens for player clicks on the specified box within the game board. Takes `handleClick` as a callback function |
| `resetButton` | Listens for clicks to the reset button. Takes `resetGame` as a callback function |


## Of Note 
The current version (as of October 26th, 2020) contains no option to play against the computer. 
Registering a player's move in one square immediately advances to the next player. 
There is no way to "take back" your play. Once a mark is made in a box it is final.



