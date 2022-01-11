# JavaScript Objects

## What is an Object ?
An object in JavaScript is a collection of related data (several variables) and/or functionality (functions). Variables are called properties and functions are called methods when they are inside objects.

## Defining an Object
An object in JavaScript can be defined and initialised like a variable.
~~~javascript
const objectName = {};
~~~
There are multiple ways to define objects but in most cases, it is best to use the __object literal__ syntax as follows:

~~~javascript
const myObject = {
  property: 'Value!',
  otherProperty: 77,
  "obnoxious property": function() {
    // do stuff!
 }
}
~~~

There are also 2 ways to get information out of an object: dot notation and bracket notation.

~~~javascript
// dot notation
myObject.property // 'Value!'

// bracket notation
myObject["obnoxious property"] // [Function]
~~~

## Use of Objects
Objects are used to store keyed collections of various data and more complex entities.

## Are Objects Useful ?
Suppose we want to create a tic tac toe game. Let us create the variables of the game :
~~~javascript
const playerOneName = "Subrat";
const playerOneMarker = "X";
const playerTwoName = "Ramesh";
const playerTwoMarker = "Y";
~~~
Now have a look at the Object approach of creating variables :
~~~javascript
// Created Object using object literal syntax (We've literally written out the object contents as we've come to create it.)
const playerOne = {
  name : "Subrat",
  marker : "X"
}

const playerTwo = {
  name = "Ramesh",
  marker = "O"
}
~~~
Now you will definitely say that the first approach is better because it is taking less lines to write the code as compared to the second approach. But the actual fact is, the second approach is more efficient then first. Let us try to print the name of players to understand this.
~~~javascript
// First Approach
console.log(playerOneName);
console.log(playerTwoName);

//Second Approach
function printPlayerName(player){
  console.log(player.name);
}
printPlayerName(playerOne)
printPlayerName(playerTwo)
~~~
In first approach you have to remember correct variable names of all players. But not in second approach. Let us consider the example of a Book Library where we have thousands of books to understand it better.
~~~javascript
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
~~~
In the above approach we have created an Object constructor. Property values can be accessed using the dot notation. We can also include a function with in Object constructor. THis can be a simple function or an arrow function. In the below example we are adding an arrow function 'info' to display book details.
~~~javascript
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
~~~

