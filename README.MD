# Array Methods

### 0(n) map: 
remaps array values to something new based on a pattern.

### MDN:
The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.

ie:
[1, 2, 3].map(x => x+1) returns [2, 3, 4]
[a, b, c].map(x => x+ 'X') returns [aX, bX, cX]
[1, 2, 3].map(x => x * 2) returns [2, 4, 6]

### 0(n) reduce:
takes in an array and returns a new value.

arguments are: 
.reduce(accumulator, curArrVal, index, srcArr)

accumulator argument is starts as the arrays initial value specified after the {},

ie:
[a, b, c].reduce( acc, val => {
 acc += val
}, ''")   returns "abc"

[1, 2, 3, 4].reduce()

### 0(n) filter:
filters items in an array by a specific criteria. 

ie:
[2, 3, 4, 7, 8, 9].filter( x => x > 4) returns: [7, 8, 9]

[2, 3, 4, 7, 8, 9].filter( x => x < 4) returns: [2, 3]

[2, 3, 4, 7, 8, 9].filter( x => x < 7) returns: [2, 3, 4]

### 0(n) forEach():
iterates through every value in an array and sets it to a variable that is usable withing the function

ie:
[a, b, c].forEach( val, index => {
 console.log(val)
}) returns "a" "b" "c" in console

###  0(n log(n)) sort():
The sort() method sorts the elements of an array in place and returns the sorted array. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.


ie:
[2, 1, 3].sort((a, b) => a - b) returns [1, 2, 3]

### O(n) Slice:
takes part of an array and returns a new array

ie:
[1, 2, 3, 4].slice(1) returns [2, 3, 4]
[1, 2, 3, 4].slice(2) returns [3, 4]
[a, b, c].slice(1) returns [b, c]

###  0(1) pop:
removes last element from an array and returns it as a value

[1, 2, 3, 4].pop() returns 4 and the array is set to [1, 2, 3]
[1, 2, 3].pop() returns 3 and the array is set to [1, 2]
[a, b, c].pop() returns c and the array is set to [a, b]

###  0(n) shift():
The shift() method removes the first element from an array and returns that removed element. This method changes the length of the array.

ie:
[1, 2, 3].shift() returns 1 and the array is set to [2, 3]
['test', 1, 2, 3].shift() returns test and the array is set to [1, 2, 3]
[a, b, c].shift() returns a and the array is set to [b, c]


### 0(1) push():
Adds an item to the end of an array.

Ie:
[1, 2 , 3].push(a) returns [1, 2, 3, a]
[1, 2 , 3].push('test') returns [1, 2, 3, 'test]
[1, 2 , 3].push(4) returns [1, 2, 3, 4]

### 0(n) unshift():
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

### 0(n) indexOf():
Returns the index of an item within the array.

Ie:
[a, b, c].indexOf(b) returns 1
[a, b, c, d, e].indexOf(e) returns 4
[a, b, c].indexOf(z) returns null

### 0(n) every():
The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

Ie:
[1, 2, 3].every( num => num < 4) returns true

[a, b, c].every( letr => typeOf(letr) == String) returns true

[1, 2, 3].every( num => num > 1) returns false

### charAt():
Returns the character at the given index in the string

ie:
“Good morning”.charAt(2) returns 'o'
“Good morning”.charAt(3) returns 'd'
“Good morning”.charAt(5) returns 'm'


### charCodeAt():
Returns the character code at the given index in the string

ie:
“Good morning”.charAt(2) returns 79
“Good morning”.charAt(2) returns 68
“Good morning”.charAt(2) returns 77


### 0(n) concat():
concatenates characters to the end of a string

ie:
"test".concat('o') returns "testo'
"test".concat('s') returns "tests'
"test".concat(' aye') returns "test aye'

### includes():
checks to see if string includes specific character

ie:
"test".includes(t) returns true
"lol".includes(l) returns true
"test".includes(l) returns false

### 0(n) indexOf():
returns the index of character in a string

ie:
"test".indexOf(t) returns 0
"stop".indexOf(p) returns 3
"index".indexOf(d) returns 2

### match():
The match() method retrieves the result of matching a string against a regular expression.

ie:

### repeat():
The repeat() method constructs and returns a new string which contains the specified number of copies of the string on which it was called, concatenated together.

ie:
"test".repeat(3) returns "test test test"

"hi".repeat(4) returns "hi hi hi hi"

"21".repeat(3) returns "21 21 21"

### replace():
replaces specified substring with new characters

ie:
"Hi test".replace(test, wade) returns 'Hi wade'

"a b c d z".replace(z, e) returns 'a b c d e'

"wassup".replace(wassup, hi) returns 'Hi'

### search():
The search() method executes a search for a match between a regular expression and this String object.

### 0(n) slice():
The slice() method extracts a section of a string and returns it as a new string, without modifying the original string.

ie:
"ayo".slice(1) returns "yo"

"hi friend".slice(2) returns 'friend'

"hahaha".slice(4) returns 'ha'

### split():
The split() method divides a String into an ordered list of substrings, puts these substrings into an array, and returns the array.  The division is done by searching for a pattern; where the pattern is provided as the first parameter in the method's call.  

ie:
"hi friend".split(' ') returns [hi, friend]

'a,b,c'.split(',') returns [a, b, c]

'wow'.split('') returns [w, o, w]

### substr():
The substr() method returns a portion of the string, starting at the specified index and extending for a given number of characters afterwards.

ie:
"test".substr(1, 2) returns 'es'

"friend".substr(1, 4) returns 'rien'

"lalala".substr(0, 2) returns 'la'

### toLowerCase():
Sets all letters of a string to lowercase letters

ie:
'Hi Friend'.toLowerCase() returns 'hi friend'

'HAHAHA'.toLowerCase() returns 'hahaha'

'WOW'.toLowerCase() returns 'wow'

### toUpperCase():
Sets all letters of a sring to uppercase letters

ie:
'lalala'.toUpperCase() returns 'LALALA'

'surprise'.toUpperCase() returns 'SURPRISE'

'hello'.toUppercase() returns 'HELLO'


### trim():
removes whitespace from the start and end of a string

ie:
'test '.trim() returns 'test'
' trim '.trim() returns 'trim'
' a b c '.trim() returns 'a b c'
