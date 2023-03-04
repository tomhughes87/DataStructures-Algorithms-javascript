# DataStructures-Algorithms-javascript

## Big O 

### Things to remember:
- usually 3 case: 
  - best case = Ω (Omega)
  - average case = θ (theta)
  - worst case = O (Omicron), a.k.a Big O
* we only look at the worst case, Big O

- always reduce is, example:
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
#### a.k.a constant (the fastest)
Something that will always take the same amount of time, regardless of how big the dataset gets.

```js
const arr = [0,1,2,3,4]

console.log(arr[3])

// output: 3
```



