## Questions

1. Ques: Find the Largest Number?
```javascript
let numbers = [1,3,5,6];
let largestNum = Math.max(...numbers);
console.log(largestNum)
//using reduce
let numbers = [1,3,5,6];
let largestNum = numbers.reduce((a,b) => {
    return Math.max(a,b);
})
console.log(largestNum);
//using sort
let numbers = [1,3,5,6];
numbers.sort((a,b) => {
    return b - a;
})
let largestNum = numbers[0];
console.log(largestNum);

2. Ques: Find the sum of all elements?
let array = [3, 6, 7, 9]; 

function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

console.log(sumArray(array));