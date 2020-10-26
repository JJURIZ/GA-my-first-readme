# GA - My First Readme

Reviewing how to write a Readme.

```javascript
const handleWin = (letter) => {
  gameIsLive = false;
  if (letter === "x") {
    statusDiv.innerHTML = `${letterToSymbol(letter)} has won!`;
  } else {
    statusDiv.innerHTML = `<span>${letterToSymbol(letter)} has won!</span>`;
  }
};
```

```css
.grid {
background-color: salmon;
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-template-rows: repeat(3, 1fr);
	gap: 15px;
	margin-top: 50px;
	
}
```

```html
<div class="grid">
	<div class="box" id="box-1"></div>
	<div class="box" id="box-2"></div>
	<div class="box" id="box-3"></div>
	<div class="box" id="box-4"></div>
	<div class="box" id="box-5"></div>
	<div class="box" id="box-6"></div>
	<div class="box" id="box-7"></div>
	<div class="box" id="box-8"></div>
	<div class="box" id="box-9"></div>
</div>
```
 
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

| Variables | Description |
| ----------- | ----------- |
| `turn` | Holds the current player's symbol (X or O) |
| `turnNumber` | Tracks the number of clicks on the baord. At 9 clicks if no winner is declared the game is a draw/tie |
| `box0 - box8` | Holds the current player's symbol (X or O) |
| `turnNumber` | Using querySelector grabs the box elements from the board |
| `resetButton` | Using querySelector grabs tthe reset button |
| `winningArray` | Nested array containing all possible winning combinations |
| `emptyBoard` | Contains empty array representing the indexes of the board |




