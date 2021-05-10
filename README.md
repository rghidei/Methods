## Array Methods:


## 1. IndexOf/lastIndexOf Methods:

## Syntax:
arr.indexOf(searchElement, fromIndex);

## Defintion:
-looks for item starting from index from, and returns the index where it was found, otherwise -1.
-returns the first index at which a given element can be found in the array, or -1 if it is not present.

## Time Complexity:

## Extra Information:
-arr.lastIndexOf(searchElement, fromIndex);
// same, but looks for from right to left.

## Example 1:
var numbers = [1, 2, 3, 2, 1];
console.log(numbers.IndexOf(1, 1));
//found at index 4
console.log(numbers.IndexOf(1, 0));
//found at index 0
console.log(numbers.IndexOf(1, 5));
//not found, therefore -1 is returned

## Example 2:
let array = [1, 0, false];
console.log(array.indexOf(0));
//found at index 1
console.log(array.indexOf(false));
//found at index 2
console.log(array.indexOf(null));
//element not found, therefore -1 is returned instead

## Example 3:
const animals = ['Dodo', 'Tiger', 'Penguin', 'Tiger', 'Dodo'];
console.log(animals.indexOf('Tiger', 2));
//found at index 3
console.log(animals.indexOf('Dodo'));
//found at index 0
console.log(animals.lastIndexOf('Dodo'));
// found at index 3
console.log(animals.lastIndexOf('bear'));
//element not found, therefore -1 is returned


## 2. Includes Method:

## Syntax:
arr.includes(searchElement, fromIndex);

## Defintion:
-determines whether an array includes a certain value among its entries, returning true or false as appropriate.

## Time Complexity:

## Extra Information:
-a difference of includes is that it correctly handles NaN, unlike indexOf/lastIndexOf.

## Example 1:
let array = [1, 2, 3];
console.log(array.includes(2));
//returns true
console.log(array.includes(3));
//returns true
console.log(array.includes(4));
//returns false

## Example 2:
const pets = ['cat', 'dog', 'bat'];
console.log(pets.includes('cat'));
// expected output: true
console.log(pets.includes('at'));
// expected output: false

## Example 3:
const arr = [NaN];
console.log(arr.indexOf(NaN));
// -1 (should be 0, but === equality doesn't work for NaN)
console.log(arr.includes(NaN));
// expected output: true


## 3. Sort Method:

## Syntax:
arr.sort((firstEl, secondEl) => firstEl - secondEl);
arr.sort()
## Defintion:
-Sorts the array in-place, changing its element order.
-It also returns the sorted array, but the returned value is usually ignored, as arr itself is modified.
## Time Complexity:
-The time and space complexity of the sort cannot be guaranteed as it depends on the implementation.
## Does It Affect The Original Array Or Not?
-Yes.
## Extra Information:

## Example 1:
let array = [3, 1, 4, 2];
console.log(array.sort());
// expected output: [1, 2, 3, 4]

## Example 2:
let arr = [ 1, 2, 15 ];
console.log(arr.sort());
// expected output: [1, 2, 15]

## Example 3:
let fruits = ['apple', 'pineapple', 'pear', 'banana']
console.log(array2.sort((wordA, wordB) => wordB.length - wordA.length))
// expected output: ['pineapple', 'banana', 'apple', 'pear']


## 4. Every Method:
## Syntax:
every((element, index, array) => { ... } )
## Defintion:
-Tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

## Time Complexity:
## Example 1:
let array = [2, 3, 4, 5]
console.log(array.every(num => num > 2))
// expected output: false

## Example 2:
let array = [6, 7, 8, 9]
console.log(array.every(num => num > 5))
// expected output: true

## Example 3:
const array1 = [1, 30, 39, 29, 10, 13];
console.log(array.every(num => num < 40))
// expected output: true


## 5. Filter Method:

## Syntax:
filter((element, index, array) => { ... } )
## Defintion:
-Creates a new array with all elements that pass the test implemented by the provided function. If no elements pass the test, an empty array will be returned.

## Time Complexity:

## Example 1:
let array = [1, 2, 3]
console.log(array.filter(num => num > 1))
// expected output: [2, 3]

## Example 2:
let array = ['bubbles', 'candy', 'hugs']
console.log(array.filter(word => word.length < 4))
// expected output: ['hugs']

## Example 3:
let users = [
  {id: 1, name: "John"},
  {id: 2, name: "Pete"},
  {id: 3, name: "Mary"}
];
let someUsers = users.filter(item => item.id < 3)
console.log(someUsers)
//expected output: [
  {id: 1, name: "John"},
  {id: 2, name: "Pete"}
]


## 6. Reduce Method:

## Syntax:
arr.reduce(function(accumulator, item, index, array) {
  ...
}, [initial]);
## Defintion:
-Used to execute a function on every member of an array until it results in a single output value. It receives the function to be executed and the initial value of the accumulator as arguments. The accumulator serves as a holder for the value returned in the last execution of the callback.

## Time Complexity:
## Example 1:
let string = "Fran"
let result = [...string].reduce((char, rev) => rev + char, "")
console.log(result)
// expected output: 'narF
'
## Example 2:
let arr = [1, 2, 3];
console.log(arr.reduce((sum, current) => sum + current, 0));
console.log(6)
Background:
(0, cur) => 0 + cur, 0
(0, 1) => 0 + 1, 1
(1, 2) => 1 + 2, 3
(3, 3) => 3 + 3, 6

## Example 3:
let arr = [1, 2, 3, 4, 5];
console.log(arr.reduce((sum, current) => sum + current));
// expected output: 15


## 7. Map Method:

## Syntax:
map((element, index, array) => { ... } )

## Defintion:
-It calls the function for each element of the array and returns  a new array of the updated elements.
## Time Complexity:

## Does It Affect The Original Array Or Not?
-No.

## Example 1:
let array = [1, 2, 3]
console.log(array.map(ele => 3 + ele))
// expected output: [4, 5, 6]

## Example 2:
const array1 = [1, 4, 9, 16];
console.log(array1.map(x => x * 2));
// expected output: [2, 8, 18, 32]

## Example 3:
let array = ["Bilbo", "Gandalf", "Nazgul"]
console.log(array.map(item => item.length));
// expected output: [5, 7, 6]


## 8. forEach Method:

## Syntax:
forEach((currentValue, index, array) => { ... } )

## Defintion:
-Executes a provided function once for each array element.

## Time Complexity:

## Example 1:
let array = ['pumpkin', 'pop', 'pie']
let words = array.forEach(word => {
  console.log(word)
})
//expected outputs: 'pumpkin', 'pop', and 'pie'

## Example 2:
let movie = ['sky', 'high']
let result = array.forEach((word, index, array) => {
console.log(`${word} is at index ${index} in ${array}`)
})
// expected output: 'sky is at index 0 in movie'
// expected output: 'high is at index 1 in movie'

## Example 3:
let array = [1, 2, 3]
let result = array.forEach(num => console.log(num * 2))
// expected output: 2
// expected output: 4
// expected output: 6


## 9. Slice Method:

## Syntax:
-arr.slice([start], [end])

## Defintion:
-returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified.

## Does It Affect The Original Array?
No.
## Extra Information:
-We can also call it without arguments: arr.slice() creates a copy of arr. That’s often used to obtain a copy for further transformations that should not affect the original array.

## Example 1:
let array = ['bye', 'hug', 'pie', 'fly', 'lip']
console.log(array.slice(1, -1))
// expected output: ['hug', 'pie', 'fly']

## Example 2:
let array = ['bye', 'hug', 'pie', 'fly', 'lip']
console.log(array.slice(2))
// expected output: ['pie', 'fly', 'lip']

## Example 3:
const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
console.log(animals.slice(3, 4))
// expected output: ['duck']


## 10. Pop Method:

## Syntax:
arr.pop()

## Defintion:
-removes the last element from an array and returns that element. This method changes the length of the array

## Time Complexity:

## Example 1:
const array = ['naruto', 'sakura', 'susake', 'ino', 'pervy sage']
let remove = array.pop()
console.log(array)
// expected output: ['naruto', 'sakura', 'susake', 'ino']

## Example 2:
const array = ['naruto', 'sakura', 'susake', 'ino']
let remove = array.pop()
console.log(array)
// expected output: ['naruto', 'sakura', 'susake']

## Example 3:
const array = ['naruto', 'sakura']
let remove = array.pop()
console.log(array)
// expected output: ['naruto']

## 11. Push Method:

## Syntax:
arr.push(...items)

## Defintion:
-adds one or more elements to the end of an array and returns the new length of the array.

## Time Complexity:

## Example 1:
const array = ['pigs', 'goats', 'cows'];
let add = array.push('dogs')
console.log(array)
// expected output: ['pigs', 'goats', 'cows', 'dogs']

## Example 2:
const array = ['pigs', 'goats', 'cows', 'dogs'];
let add = array.push('chickens', 'ducks', 'horses')
console.log(array)
// expected output: ['pigs', 'goats', 'cows', 'dogs', 'chickens', 'ducks', 'horses']

## Example 3:
const array = ['pigs', 'goats', 'cows', 'dogs', 'chickens', 'ducks', 'horses'];
let add = array.push('cats', 'spiders')
console.log(array)
// expected output: ['pigs', 'goats', 'cows', 'dogs', 'chickens', 'ducks', 'horses', 'cats', 'spiders']


# 12. Shift Method:

## Syntax:
arr.shift()

## Defintion:
-removes the first element from an array and returns that removed element. This method changes the length of the array.

## Example 1:
let array = ['pink', 'blue', 'green', 'yellow', 'orange', 'lime']
let remove = array.shift()
console.log(array)
// expected output: ['blue', 'green', 'yellow', 'orange', 'lime']

## Example 2:
let array = ['blue', 'green', 'yellow', 'orange', 'lime']
let remove = array.shift()
console.log(array)
// expected output: ['green', 'yellow', 'orange', 'lime']

## Example 3:
let array = ['green', 'yellow', 'orange', 'lime']
let remove = array.shift()
console.log(array)
// expected output: ['yellow', 'orange', 'lime']


# 13. Unshift Method:
## Syntax:
arr.unshift()
## Defintion:
-adds one or more elements to the beginning of an array and returns the new length of the array.

## Time Complexity:

## Example 1:
const array1 = [6, 7, 8];
console.log(array1.unshift(4, 5));
// expected output: 5
console.log(array1);
// expected output: [4, 5, 6, 7, 8]

## Example 2:
const array1 = [4, 5, 6, 7, 8];
console.log(array1.unshift(2, 3));
// expected output: 7
console.log(array1);
// expected output: [2, 3, 4, 5, 6, 7, 8]

## Example 3:
const array1 = [2, 3, 4, 5, 6, 7, 8];
console.log(array1.unshift(1));
// expected output: 8
console.log(array1);
// expected output: [1, 2, 3, 4, 5, 6, 7, 8]




## String Methods:


## 14. CharAt Method:

## Syntax:
charAt(index)
## Defintion:
-returns the string character at a given index.

## Time Complexity:

## Example 1:
const str = 'Hello World';
console.log(str.charAt(0))
// expected output: 'H'
console.log(str.charAt(8))
// expected output: 'r'

## Example 1:
const str = 'Doritos';
console.log(str.charAt(4))
// expected output: 't'
console.log(str.charAt(6))
// expected output: 's'

## Example 3:
const sentence = 'The quick brown fox jumps over the lazy dog.';
console.log(str.charAt(0))
// expected output: 'T'
console.log(sentence.charAt(4))
// expected output: 'q'


## 15. CharCodeAt Method:

## Syntax:
charCodeAt(index)

## Defintion:
-returns the unicode of the character at a specified index in a string. This an UTF-16 cone integer between 0 and 65535.

## Time Complexity:

## Example 1:
const str = 'Hello World';
console.log(str.charCodeAt(0))
// expected output: 72
console.log(str.charCodeAt(5))
// expected output: 32

## Example 2:
const str = 'Doritos';
console.log(str.charCodeAt(0))
// expected output: 116
console.log(str.charCodeAt(5))
// expected output: 115

## Example 1:
const sentence = 'The quick brown fox jumps over the lazy dog.';
console.log(sentence.charCodeAt(4))
// expected output: 113
console.log(sentence.charCodeAt(16))
// expected output: 102
