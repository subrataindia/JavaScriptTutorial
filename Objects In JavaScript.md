# JavaScript Objects
## Use of Objects
Objects are used to store keyed collections of various data and more complex entities.

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
Now you will definitely say that the first approach is better because it is taking less lines to write the code as compared to the second approach. But the actual fact is, the second approach is more efficient then first. Let us try to print the name of players to understand this.
```
// First Approach
console.log(playerOneName);
console.log(playerTwoName);

//Second Approach
function printPlayerName(player){
  console.log(player.name);
}
printPlayerName(playerOne)
printPlayerName(playerTwo)
```
In first approach you have to remember correct variable names of all players. But not in second approach. Let us consider the example of a Book Library where we have thousands of books to understand it better.
```
// Object Constructor
// Note : Arrow functions cannot be used as constructors. They cannot be called with the new keyword. Doing that throws an error indicating that the function is not a constructor.
function Books(title, author, pages){
  this.title = title; // Optional
  this.author = author; // Optional
  this.pages = pages; // Optional
  return {title, author, pages}
}

const book1 = new Books("book1","Subrat Dash","295 Pages");
const book2 = new Books("book2","Ramesh Jena","155 Pages");

console.log(book1.title);
console.log(book2.title);
```
In the above approach we have created an Object constructor. Property values can be accessed using the dot notation. We can also include a function with in Object constructor. THis can be a simple function or an arrow function. In the below example we are adding an arrow function 'info' to display book details.
```
function Books(title, author, pages){
  info = () => (title + " By "+ author+", "+pages+", not read yet")
  return {title, author, pages, info }
}

const book1 = new Books("book1","Subrat Dash","295 Pages");
const book2 = new Books("book2","Ramesh Jena","155 Pages");

console.log(book1.info());
console.log(book2.info());

console.log(book1.title);
console.log(book2.title);
```

