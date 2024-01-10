## Questions

1. Ques: Find the Largest Number?
```javascript
let numbers = [1,3,5,6];
let largestNum = Math.max(...numbers);
console.log(largestNum)
**using reduce**
let numbers = [1,3,5,6];
let largestNum = numbers.reduce((a,b) => {
    return Math.max(a,b);
})
console.log(largestNum);

let numbers = [1,3,5,6];
numbers.sort((a,b) => {
    return b - a;
})
let largestNum = numbers[0];
console.log(largestNum);