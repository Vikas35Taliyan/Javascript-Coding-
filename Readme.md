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
```

2. Ques: Find the sum of all elements?
```javascript
let array = [3, 6, 7, 9]; 

function sumArray(arr) {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
}

console.log(sumArray(array));

//using forEach
let array = [3, 6, 7, 9]; 
function sumArray(arr) {
    let sum = 0;
    arr.forEach(num => sum += num);
    return sum;
}

console.log(sumArray(array));

//using reduce
const myArr = [2,5,8,4];
function sumArr(arr) {
    return arr.reduce((acc, curr) => acc + curr, 0);
}
console.log(sumArr(myArr));
```

3. Ques: Remove the duplicate and return unique values
```javascript
let arr = [1, 4, 6, 4, 3, 5, 6]; 

function unique(arr) {
    let items = {};
    arr.forEach((item) => {
        if (!items[item]) {
            items[item] = item;
        }
    });
    return Object.values(items);
}

console.log(unique(arr));

//using Set
let arr = [1, 4, 6, 4, 3, 5, 6]; 

function unique(arr) {
    return Array.from(new Set(arr));
}

console.log(unique(arr));

//using filter
let arr = [1, 4, 6, 4, 3, 5, 6]; 

function unique(arr) {
    return arr.filter((item, index) => arr.indexOf(item) === index);
}

console.log(unique(arr));
```

4. Quest: 1 to 10 Even or odd
```javascript
