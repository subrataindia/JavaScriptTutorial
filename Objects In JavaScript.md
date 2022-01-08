# JavaScript Objects
## Are Objects Useful ?
Suppose we want to create a tic tac toe game. Let us create the variables of the game :
```
const playerOneName = "Subrat";
const playerOneMarker = "X";
const playerTwoName = "Ramesh";
const playerTwoMarker = "Y";
```
Now have a look at the Object approach of creating variables :
```
const playerOne = {
  name : "Subrat",
  marker : "X"
}

const playerTwo = {
  name = "Ramesh",
  marker = "O"
}
```
Now you will definitely say that the first approach is better because it is taking less lines to write the code as compared to the second approach. But the second approach is more efficient then first. Let us try to print the name of players to understand this.
```
// First Approach
console.log(playerOneName);
console.log(playerTwoName);

//Second Approach
function printPlayerName(player){
  console.log(player.name);
}
```
