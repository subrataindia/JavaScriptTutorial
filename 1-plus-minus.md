~~~javaScript
'use strict';

process.stdin.resume();
process.stdin.setEncoding('utf-8');

let inputString = '';
let currentLine = 0;

process.stdin.on('data', function(inputStdin) {
    inputString += inputStdin;
});

process.stdin.on('end', function() {
    inputString = inputString.split('\n');

    main();
});

function readLine() {
    return inputString[currentLine++];
}

/*
 * Complete the 'plusMinus' function below.
 *
 * The function accepts INTEGER_ARRAY arr as parameter.
 */

function plusMinus(arr) {
    // Write your code here
    let plus = 0;
    let minus = 0;
    let zero = 0;
    arr.forEach((item) => {
        (item > 0) ? plus++ : (item < 0) ? minus++ : zero++
    });
    console.log((plus/(plus+minus+zero)).toFixed(6))
    console.log((minus/(plus+minus+zero)).toFixed(6))
    console.log((zero/(plus+minus+zero)).toFixed(6))
}

function main() {
    const n = parseInt(readLine().trim(), 10);

    const arr = readLine().replace(/\s+$/g, '').split(' ').map(arrTemp => parseInt(arrTemp, 10));

    plusMinus(arr);
}
~~~
