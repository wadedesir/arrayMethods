# Array Methods

### map: 
remaps array values to something new based on a pattern.

### MDN:
The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

ie:
[1, 2, 3].map(x => x+1) returns [2, 3, 4]
[a, b, c].map(x => x+ 'X') returns [aX, bX, cX]
[1, 2, 3].map(x => x * 2) returns [2, 4, 6]

### reduce:
takes in an array and returns a new value.

arguments are: 
.reduce(accumulator, curArrVal, index, srcArr)

accumulator argument is starts as the arrays initial value specified after the {},

ie:
[a, b, c].reduce( acc, val => {
 acc += val
}, ''")   returns "abc"

[1, 2, 3, 4].reduce()

### filter:
filters items in an array by a specific criteria. 

ie:
[2, 3, 4, 7, 8, 9].filter( x => x > 4) returns: [7, 8, 9]

[2, 3, 4, 7, 8, 9].filter( x => x < 4) returns: [2, 3]

[2, 3, 4, 7, 8, 9].filter( x => x < 7) returns: [2, 3, 4]

### forEach():
iterates through every value in an array and sets it to a variable that is usable withing the function

ie:
[a, b, c].forEach( val, index => {
 console.log(val)
}) returns "a" "b" "c" in console

### sort():
The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

## The time and space complexity of the sort cannot be guaranteed as it depends on the implementation.

ie:
[2, 1, 3].sort((a, b) => a - b) returns [1, 2, 3]

### Slice:
takes part of an array and returns a new array

ie:
[1, 2, 3, 4].slice(1) returns [2, 3, 4]
[1, 2, 3, 4].slice(2) returns [3, 4]
[a, b, c].slice(1) returns [b, c]

### pop:
removes last element from an array and returns it as a value

[1, 2, 3, 4].pop() returns 4 and the array is set to [1, 2, 3]
[1, 2, 3].pop() returns 3 and the array is set to [1, 2]
[a, b, c].pop() returns c and the array is set to [a, b]

### shift():
The shift() method removes the first element from an array and returns that removed element. This method changes the length of the array.

ie:
[1, 2, 3].shift() returns 1 and the array is set to [2, 3]
['test', 1, 2, 3].shift() returns test and the array is set to [1, 2, 3]
[a, b, c].shift() returns a and the array is set to [b, c]


### push():
Adds an item to the end of an array.

Ie:
[1, 2 , 3].push(a) returns [1, 2, 3, a]
[1, 2 , 3].push('test') returns [1, 2, 3, 'test]
[1, 2 , 3].push(4) returns [1, 2, 3, 4]

### unshift():
Adds an item to the start of an array

Ie:
[a, b, c].unshift(1) returns [1, a, b, c]
[a, b, c].unshift(2) returns [2, a, b, c]
[a, b, c].unshift('ll') returns [ll, a, b, c]

### includes():
Checks to see if value exists within the array.

Ie:
[a, b, c].includes(b) returns true
[a, b, c].includes(d) returns false

### indexOf():
Returns the index of an item within the array.

Ie:
[a, b, c].indexOf(b) returns 1
[a, b, c, d, e].indexOf(e) returns 4
[a, b, c].indexOf(z) returns null

### every():
The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

Ie:
[1, 2, 3].every( num => num < 4) returns true

[a, b, c].every( letr => typeOf(letr) == String) returns true

[1, 2, 3].every( num => num > 1) returns false

### charAt():
Returns the index of the given character in the string

“Good morning”
