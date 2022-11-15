Method: `concat`

1. **Parameter it accepts**: n (any) number of values (number, string, boolean, array, null, undefined, object and function etc).

2. **what it will return**: a single Array consisting of by all the values passed as parameters in the same order.

3. **Example**

```
    let numbers = [1, 2, 3];
    numbers.concat(4); //[1,2,3,4]
    let sentanceArray = 'A quick brown fox jumped over a lazy'.split(' ');
    sentanceArray.concat('dog').join(' '); //"A quick brown fox jumped over a lazy dog"
    let colors = ['red', 'green', 'blue'];
    colors.concat('black', 'red', 21, true); // ['red','green','blue','black', 'red', 21, true]
```

4. **Explanation**: concat accepts n number of values and returns one array with all the values in same order. It does not change the original array.

5. **Does it mutate the original array?**: No it does not mutate the original array

---

method: `flat`

1. **Parameter it accepts**: array

2. **what it will return**: all elements of the array, sans all internal brackets

3. **Example**

```
const arr1 = [0, 1, 2, [3, 4]];

console.log(arr1.flat());
// expected output: [0, 1, 2, 3, 4]

const arr2 = [0, 1, 2, [[[3, 4]]]];

console.log(arr2.flat(2));
// expected output: [0, 1, 2, [3, 4]]
```

4. **Explanation**: it copies all elements of the array, including all the elements of all sub arrays and pastes in a new array in order.

5. **Does it mutate the original array?**: no

---

method: `concat`

1. **Parameter it accepts**: 2 arrays

2. **what it will return**: 1 array

3. **Example**

```
const array1 = ['a', 'b', 'c'];
const array2 = ['d', 'e', 'f'];
const array3 = array1.concat(array2);

console.log(array3);
// expected output: Array ["a", "b", "c", "d", "e", "f"]
```

4. **Explanation**: merges 2 arrays into a single, new array.

5. **Does it mutate the original array?**: no

---

method: `push`

1. **Parameter it accepts**: one or more elements

2. **what it will return**: edited array

3. **Example**

```
const animals = ['pigs', 'goats', 'sheep'];
const count = animals.push('cows');
console.log(count);
// expected output: 4
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows"]

animals.push('chickens', 'cats', 'dogs');
console.log(animals);
// expected output: Array ["pigs", "goats", "sheep", "cows", "chickens", "cats", "dogs"]
```

4. **Explanation**: The push() method adds one or more elements to the end of an array and returns the new length of the array.

5. **Does it mutate the original array?**: yes

---

method: `pop`

1. **Parameter it accepts**: none

2. **what it will return**: element that is removed from the array

3. **Example**

```
const plants = ['broccoli', 'cauliflower', 'cabbage', 'kale', 'tomato'];
console.log(plants.pop());
// expected output: "tomato"
console.log(plants);
// expected output: Array ["broccoli", "cauliflower", "cabbage", "kale"]
plants.pop();
console.log(plants);
// expected output: Array ["broccoli", "cauliflower", "cabbage"]
```

4. **Explanation**: The pop() method removes the last element from an array and returns that value to the caller. If you call pop() on an empty array, it returns undefined.

5. **Does it mutate the original array?**: yes

---

method: `shift`

1. **Parameter it accepts**: nothing

2. **what it will return**: removes the first element from an array and returns that removed element.

3. **Example**

```
const array1 = [1, 2, 3];
const firstElement = array1.shift();

console.log(array1);
// expected output: Array [2, 3]

console.log(firstElement);
// expected output: 1
```

4. **Explanation**: removes the element at the zeroth index and shifts the values at consecutive indexes down, then returns the removed value. If the length property is 0, undefined is returned.

5. **Does it mutate the original array?**: yes

---

method: `unshift`

1. **Parameter it accepts**: nothing

2. **what it will return**: adds one or more elements to the beginning of an array and returns the new length of the array.

3. **Example**

```
const array1 = [1, 2, 3];
console.log(array1.unshift(4, 5));
// expected output: 5

console.log(array1);
// expected output: Array [4, 5, 1, 2, 3]
```

4. **Explanation**: inserts the given values to the beginning of an array-like object. Array.prototype.push() has similar behavior to unshift(), but applied to the end of an array.

5. **Does it mutate the original array?**: yes

---

method: `indexOf`

1. **Parameter it accepts**: any element of the array

2. **what it will return**: the index of the element if it exists, or -1 if it doesn't

3. **Example**

```
const beasts = ['ant', 'bison', 'camel', 'duck', 'bison'];
console.log(beasts.indexOf('bison'));
// expected output: 1

// start from index 2
console.log(beasts.indexOf('bison', 2));
// expected output: 4

console.log(beasts.indexOf('giraffe'));
// expected output: -1
```

4. **Explanation**: returns the first index at which a given element can be found in the array, or -1 if it is not present.

5. **Does it mutate the original array?**: no

---

method: `lastIndexOf`

1. **Parameter it accepts**: any element

2. **what it will return**: index of last occurrence of the element, if it exists

3. **Example**

```
const animals = ['Dodo', 'Tiger', 'Penguin', 'Dodo'];
console.log(animals.lastIndexOf('Dodo'));
// expected output: 3

console.log(animals.lastIndexOf('Tiger'));
// expected output: 1
```

4. **Explanation**: returns the last index at which a given element can be found in the array, or -1 if it is not present. The array is searched backwards, starting at fromIndex.

5. **Does it mutate the original array?**: no

---

method: `includes`

1. **Parameter it accepts**: an array

2. **what it will return**: a boolean

3. **Example**

```
const array1 = [1, 2, 3];
console.log(array1.includes(2));
// expected output: true

const pets = ['cat', 'dog', 'bat'];

console.log(pets.includes('cat'));
// expected output: true

console.log(pets.includes('at'));
// expected output: false
```

4. **Explanation**: determines whether an array includes a certain value among its entries, returning `true` or `false` as appropriate.

5. **Does it mutate the original array?**: no

---

method: `reverse`

1. **Parameter it accepts**: an array

2. **what it will return**: the edited (reversed) array

3. **Example**

```
const array1 = ['one', 'two', 'three'];
console.log('array1:', array1);
// expected output: "array1:" Array ["one", "two", "three"]

const reversed = array1.reverse();
console.log('reversed:', reversed);
// expected output: "reversed:" Array ["three", "two", "one"]

// Careful: reverse is destructive -- it changes the original array.
console.log('array1:', array1);
// expected output: "array1:" Array ["three", "two", "one"]
```

4. **Explanation**: reverses an array in place and returns the reference to the same array, the first array element now becoming the last, and the last array element becoming the first. In other words, elements order in the array will be turned towards the direction opposite to that previously stated.

5. **Does it mutate the original array?**:

---

method: `splice`

1. **Parameter it accepts**: starting index,number of elements to be deleted, elements to add to the array (if not specified, splice will only delete elements)

2. **what it will return**: An array containing the deleted elements.If no elements are removed, an empty array is returned.

3. **Example**

```
//Remove 0 (zero) elements before index 2, and insert "drum"
const myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
const removed = myFish.splice(2, 0, 'drum');
// myFish is ["angel", "clown", "drum", "mandarin", "sturgeon"]
// removed is [], no elements removed
//Remove 0 (zero) elements before index 2, and insert "drum" and "guitar"
const myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
const removed = myFish.splice(2, 0, 'drum', 'guitar');
// myFish is ["angel", "clown", "drum", "guitar", "mandarin", "sturgeon"]
// removed is [], no elements removed
//Remove 1 element at index 3
const myFish = ['angel', 'clown', 'drum', 'mandarin', 'sturgeon'];
const removed = myFish.splice(3, 1);
// myFish is ["angel", "clown", "drum", "sturgeon"]
// removed is ["mandarin"]
//Remove 1 element at index 2, and insert "trumpet"
const myFish = ['angel', 'clown', 'drum', 'sturgeon'];
const removed = myFish.splice(2, 1, 'trumpet');
// myFish is ["angel", "clown", "trumpet", "sturgeon"]
// removed is ["drum"]
//Remove 2 elements from index 0, and insert "parrot", "anemone" and "blue"
const myFish = ['angel', 'clown', 'trumpet', 'sturgeon'];
const removed = myFish.splice(0, 2, 'parrot', 'anemone', 'blue');
// myFish is ["parrot", "anemone", "blue", "trumpet", "sturgeon"]
// removed is ["angel", "clown"]
//Remove 2 elements, starting from index 2
const myFish = ['parrot', 'anemone', 'blue', 'trumpet', 'sturgeon'];
const removed = myFish.splice(2, 2);
// myFish is ["parrot", "anemone", "sturgeon"]
// removed is ["blue", "trumpet"]
//Remove 1 element from index -2
const myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
const removed = myFish.splice(-2, 1);
// myFish is ["angel", "clown", "sturgeon"]
// removed is ["mandarin"]
//Remove all elements, starting from index 2
const myFish = ['angel', 'clown', 'mandarin', 'sturgeon'];
const removed = myFish.splice(2);
// myFish is ["angel", "clown"]
// removed is ["mandarin", "sturgeon"]
//Using splice() on sparse arrays
//The splice() method preserves the array's sparseness.
const arr = [1, , 3, 4, , 6];
console.log(arr.splice(1, 2)); // [empty, 3]
console.log(arr); // [1, 4, empty, 6]
```

4. **Explanation**:The splice() method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place

5. **Does it mutate the original array?**: yes

---

method: `slice`

1. **Parameter it accepts**: starting index, ending index

2. **what it will return**:

3. **Example** A new array containing the extracted elements.

```
// Using slice, create newCar from myCar.
const myHonda = { color: 'red', wheels: 4, engine: { cylinders: 4, size: 2.2 } };
const myCar = [myHonda, 2, 'cherry condition', 'purchased 1997'];
const newCar = myCar.slice(0, 2);
console.log('myCar =', myCar);
console.log('newCar =', newCar);
console.log('myCar[0].color =', myCar[0].color);
console.log('newCar[0].color =', newCar[0].color);
// Change the color of myHonda.
myHonda.color = 'purple';
console.log('The new color of my Honda is', myHonda.color);
console.log('myCar[0].color =', myCar[0].color);
console.log('newCar[0].color =', newCar[0].color);

//This script writes:

myCar = [
  { color: 'red', wheels: 4, engine: { cylinders: 4, size: 2.2 } },
  2,
  'cherry condition',
  'purchased 1997'
]
newCar = [ { color: 'red', wheels: 4, engine: { cylinders: 4, size: 2.2 } }, 2 ]
myCar[0].color = red
newCar[0].color = red
The new color of my Honda is purple
myCar[0].color = purple
newCar[0].color = purple
```

4. **Explanation**: returns a shallow copy of a portion of an array into a new array object selected from start to end (end not included) where start and end represent the index of items in that array. The original array will not be modified.

5. **Does it mutate the original array?**:
   no

---

method: `forEach`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: undefined

3. **Example**

```
const arraySparse = [1, 3, /* empty */, 7];
let numCallbackRuns = 0;

arraySparse.forEach((element) => {
  console.log({ element });
  numCallbackRuns++;
});

console.log({ numCallbackRuns });

// { element: 1 }
// { element: 3 }
// { element: 7 }
// { numCallbackRuns: 3 }
```

4. **Explanation**: executes a provided function once for each array element.

5. **Does it mutate the original array?**: no, but the callback function can.

---

method: `map`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: A new array with each element being the result of the callback function.

3. **Example**

```
const numbers = [1, 4, 9];
const roots = numbers.map((num) => Math.sqrt(num));

// roots is now     [1, 2, 3]
// numbers is still [1, 4, 9]
```

4. **Explanation**: THe `map()` method is an iterative method. It calls a provided callbackFn function once for each element in an array and constructs a new array from the results.

5. **Does it mutate the original array?**: no

---

method: `filter`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: a shallow copy of the elements that are selected by the filter callback function.

3. **Example**

```
function isBigEnough(value) {
  return value >= 10;
}
const filtered = [12, 5, 8, 130, 44].filter(isBigEnough);
// filtered is [12, 130, 44]
```

4. **Explanation**: The filter() method creates a shallow copy of a portion of a given array, filtered down to just the elements from the given array that pass the test implemented by the provided function.

5. **Does it mutate the original array?**: no

---

method: `find`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: The first element in the array that satisfies the provided testing function. Otherwise, undefined is returned.

3. **Example**

```
const inventory = [
  { name: "apples", quantity: 2 },
  { name: "bananas", quantity: 0 },
  { name: "cherries", quantity: 5 },
];

const result = inventory.find(({ name }) => name === "cherries");

console.log(result); // { name: 'cherries', quantity: 5 }
```

4. **Explanation**: The find() method returns the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.

5. **Does it mutate the original array?**: no

---

method: `findIndex`

1. **Parameter it accepts**: callback function, index, array

2. **what it will return**: The index of the first element in the array that passes the test. Otherwise, -1.

3. **Example**

```
function isPrime(element) {
  if (element % 2 === 0 || element < 2) {
    return false;
  }
  for (let factor = 3; factor <= Math.sqrt(element); factor += 2) {
    if (element % factor === 0) {
      return false;
    }
  }
  return true;
}

console.log([4, 6, 8, 9, 12].findIndex(isPrime)); // -1, not found
console.log([4, 6, 7, 9, 12].findIndex(isPrime)); // 2 (array[2] is 7)
```

4. **Explanation**: The findIndex() method returns the index of the first element in an array that satisfies the provided testing function. If no elements satisfy the testing function, -1 is returned.

5. **Does it mutate the original array?**: no

---

method: `some`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: true if the callback function returns a truthy value for at least one element in the array. Otherwise, false.

3. **Example**

```
function isBiggerThan10(element, index, array) {
  return element > 10;
}

[2, 5, 8, 1, 4].some(isBiggerThan10);  // false
[12, 5, 8, 1, 4].some(isBiggerThan10); // true
```

4. **Explanation**: The some() method tests whether at least one element in the array passes the test implemented by the provided function. It returns true if, in the array, it finds an element for which the provided function returns true; otherwise it returns false. It doesn't modify the array.

5. **Does it mutate the original array?**:
   no

---

method: `every`

1. **Parameter it accepts**: callback function, element, index, array

2. **what it will return**: true if callbackFn returns a truthy value for every array element. Otherwise, false.

3. **Example**

```
function isBigEnough(element, index, array) {
  return element >= 10;
}
[12, 5, 8, 130, 44].every(isBigEnough);   // false
[12, 54, 18, 130, 44].every(isBigEnough); // true
```

4. **Explanation**: The every() method tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.

5. **Does it mutate the original array?**: no

---

method: `sort`

1. **Parameter it accepts**: compare function, 2 elements for comparison

2. **what it will return**: the array sorted in place.

3. **Example**

```
function compareFn(a, b) {
  if (a is less than b by some ordering criterion) {
    return -1;
  }
  if (a is greater than b by the ordering criterion) {
    return 1;
  }
  // a must be equal to b
  return 0;
}
```

4. **Explanation**: The sort() method sorts the elements of an array in place and returns the reference to the same array, now sorted. The default sort order is ascending, built upon converting the elements into strings, then comparing their sequences of UTF-16 code units values.

5. **Does it mutate the original array?**: Yes

---

method: `reduce`

1. **Parameter it accepts**: callback function, accumulator, current value, current index, array

2. **what it will return**: The value that results from running the "reducer" callback function to completion over the entire array.

3. **Example**

```
const array = [15, 16, 17, 18, 19];

function reducer(accumulator, currentValue, index) {
  const returns = accumulator + currentValue;
  console.log(
    `accumulator: ${accumulator}, currentValue: ${currentValue}, index: ${index}, returns: ${returns}`,
  );
  return returns;
}

array.reduce(reducer);
```

4. **Explanation**: The reduce() method executes a user-supplied "reducer" callback function on each element of the array, in order, passing in the return value from the calculation on the preceding element. The final result of running the reducer across all elements of the array is a single value.

5. **Does it mutate the original array?**: no

---
