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

## O(n) a.k.a Linear
Something like a for loop.
The long the array, the longer the process will take.
eg. 

```js
const arr = [0,1,2,3,4]

for (let i = 0; i < arr.length; i++){
  console.log(arr[i])
}
```
*this loops through an array of 5 items, so it will run 5 times.

