# DataStructures-Algorithms-javascript

## Big O 

### Things to remember:
- usually 3 case: 
  - best case = Ω (Omega)
  - average case = θ (theta)
  - worst case = O (Omicron), a.k.a Big O
* we only look at the worst case, Big O

- always reduce it, example:
If there is a linear for loop, O(n) and a contant, O(1) in the same algorythm. Don't write O(1n), reduce it to the worst (hightest) value, O(n)


![image](https://user-images.githubusercontent.com/91187363/222923608-1e39c183-6e27-460f-baff-ce36995b15e9.png)

### O(n) 
#### a.k.a Linear
Something like a for loop.
The longer the array, the longer the process will take.
eg. 

```js
const arr = [0,1,2,3,4]

for (let i = 0; i < arr.length; i++){
  console.log(arr[i])
}

// output: 0,1,2,3,4
```
*this loops through an array of 5 items, so it will run 5 times.




### O(n^2) 
#### a.k.a quadratic
Something like a nested for loop.
loops through the array .. and then for each item it loops through every item the array again!
eg. 

```js
const arr = [0,1,2,3,4]

for (let i = 0; i < arr.length; i++){
  for (let j = 0; j < arr.length; j++){
    console.log(arr[i][j])
  } 
}

// output: 00,01,02,03,04,10,11,12...43, 44
```
*this loops through an array of 5 items x 5 items, so it will run 25 times.


### O(n!) 
#### a.k.a n Factoria (terrible)
Something like a double nested for loop.
loops through the array .. and then for each item it loops through every item the array again!... and then again!

* This is rare unless you are trying to write bad code.


### O(1) 
#### a.k.a Constant (the fastest)
Something that will always take the same amount of time, regardless of how big the dataset gets.

```js
const arr = [0,1,2,3,4]

console.log(arr[3])

// output: 3
```

### O(log n)
#### a.k.a Logarithmic 
Some that as it loops through an array, it halves each loop, speeding up the loop much more than O(n) 
```js
No example yet
// output: 
```

### Multiple params:
if 2 different arrays are passed in and used, we can't use use n, example
```js
function loopingTest(a,b){
  
  for (let i = 0; i < a.length; i++){
    console.log(a[i])
  }

  for (let i = 0; i < b.length; i++){
    console.log(b[i])
  }

}

This is:
O (a * b)... i think

```
- O (2^n)


### No notes on:
- O (n log n)
- O (2^n)

## Js Functions:

array.pop() = O(1)

array.push() = O(1)

array.shift() = O(n)

array.unshift() = O(n)

*shift and unshift (add or remove from the start of and array) are linear because the array needs to be reindexed

## Space & Time:
### Space:
Memory

### Time:
How long it takes (how many times it will process)


## Classes for a dataset:
Reason for using classes on a dataset:
- the methods can be for insert, add, remove, edit, etc

## Pointers:
A pointer is referencing the object in memory,rather than just copying the value. Example:

#### non-pointer:
``` js

const thing1 = "hi"
const thing2 = thing1
thing1="bye"

console.log(thing1) 
// bye

console.log(thing2) 
// hi

```
* when thing2 was created it just copied the value, it didn't track any changes etc.

#### pointer:
``` js

const thing1 = {word:"hi"}
const thing2 = thing1
thing1.word="bye"

console.log(thing1.word) 
// bye

console.log(thing2.word) 
// bye

```
*when thing2 was created it just copied the value, it didn't track any changes etc.

## Garbage Collection

when removing pointers, it's possible to lose access to objects stored in memory but they'd still take up space.
JS has 'garbage collection' which clears up data like this that runs at intervals

## Array vs Linked List:
### Array:
*Memory:
```
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
```

*Memory with array in it, all together and indexed in order:
```
[ ] [ ] [0] [1] [2] [3] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [ ] [ ]
```

## Linked List:
*Memory with linked list in it, the items and not stored or indexed in any order. 
BUT there is a "head"(0) and a tail(4)*
- the head and tail are points and point to the reference memory spot, not to the value
- each item has a value and a "next" that points to the next item in the list
- node is the key word
```
[ ] [ ] [ ] [ ] [2] [ ] [ ] [ ]
[ ] [1] [ ] [ ] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [0] [ ] [ ] [ ] [ ]
[ ] [ ] [ ] [ ] [ ] [ ] [3] [ ]
```


the datastructure of a linked list:
```js
{head: {
        value: 0,
        next: {
              value: 1,
              next: {
                    value: 2,
                    next: {
                        value: 3,
                        next: null
                        }
                    }
              }
          }
  }
  ```
### Linked Lists functions:
- push (adding to the end)
  - make a new node (add a value and next:null)
  - change the tail pointer from the linked list to focus on the new node
  - the previous tails "next" value should now equal the new node
  *O(1)*

- pop (remove from end of list)
  - deleting the last element is O(1)
  - But to set the tail pointer, we must go through the list
  *O(n)*
  
- insert/ remove (add to or remove from the middle)
  - you need to count through the entire list
  *O(n)* for both value or index 

  


