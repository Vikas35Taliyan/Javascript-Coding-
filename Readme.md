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
for(let i = 1; i <= 10; i += 2) {
    console.log(i);
}
//
for(let i = 1; i <= 10; i++) {
    if(i % 2 === 0){
        console.log(i);
    }
}

//1 to 10 odd
for(let i = 1; i <= 10; i++) {
    if(i % 2 === 1){
        console.log(i);
    }
}
//1 to 100
for(let x = 1; x <= 100; x++) {
    if(x % 2 != 0){
        console.log(x);
    }
}
//both
const arr = [2, 5, 7, 3, 9]; 

const evenNumbers = [];
const oddNumbers = [];

for (let i = 0; i < arr.length; i++) {
  if (arr[i] % 2 === 0) {
    evenNumbers.push(arr[i]);
  } else {
    oddNumbers.push(arr[i]);
  }
}

console.log("Even numbers:", evenNumbers);
console.log("Odd numbers:", oddNumbers);

//using forof
const number = [1,2,3,4,5,6,7];
for (let num of number) {
    if (num % 2 === 0) {
        console.log(`${num} is even`);
    } else {
        console.log(`${num} is odd`)
    }
}
```
5. Ques: Print the Numbers
```javascript
const arr = [2, 5, 7, 3, 9];

for(let i = 0; i < arr.length; i++) {
    console.log(arr[i]);
}
```

6. Ques: Factorial of a number?
```javascript
function factorial (num) {
    let result = 1;
    for(let i = 2; i <= num; i++){
        result *= i;
    }
    return result;
}
console.log(factorial(5));

//using the recursion
function factorial (num) {
    if(num === 0) {
        return 1;
    } else {
        return num * factorial (num -1);
    }
}
console.log(factorial(5));
```
7. Ques: Check Number is prime or not?
```javascript
function isPrime(num) {
if(num < 2)
return false;
for(let i = 2; i < num; i++){
    if(num % i === 0)
    return false;
}
return true;
}
console.log(isPrime(8));

//prime from 0 to 100
function isPrime(num) { 
    if (num <= 1) return false;
    if (num <= 3) return true;

    if (num % 2 === 0 || num % 3 === 0) return false;

    for (let i = 5; i * i <= num; i += 6) {
        if (num % i === 0 || num % (i + 2) === 0) {
            return false;
        }
    }

    return true;
}

function find(start, end) {
    const primes = [];
    for (let i = start; i <= end; i++) {
        if (isPrime(i)) {
            primes.push(i);
        }
    }
    return primes;
}

const primeNum = find(1, 100);
console.log(primeNum);
```
8. Ques: Generate random int b/w the two given numbers?
```javascript
function getRandomNum (min, max) {
    return Math.floor(Math.random() * (max -min + 1)) + min;
}
console.log(getRandomNum (1, 10));
```

9. Ques: Find the square root?
```javascript
let num = 24;
let squareRoot = Math.sqrt(num);
console.log(squareRoot);

//using the exponent operator
let num = 24;
let squareRoot = num ** 0.5;
console.log(squareRoot);
```
10. Ques: Swapping the two numbers?
```javascript
let a = 10;
let b = 20;
let temp = a;
a = b;
b = temp;
console.log(a, b);

//using destructuring
let a = 10;
let b = 20;
[a, b ] = [b = a];
console.log(a, b);
```

11. Ques: Check number is integer?
```javascript
function isInt (num) {
    return num % 1 === 0;
}
console.log(isInt(4));
```
12. Ques: Sum of natural numbers?
```javascript
function sumOfNaturalNumbers(n) { 
    return (n * (n + 1)) / 2;
}
const n = 10;
const sum = sumOfNaturalNumbers(n);
console.log(`The sum of natural numbers from 1 to ${n} is: ${sum}`);
```

13. Ques: calculate the Age?
```javascript
function calculateAge(birthdate) { 
    const birthdateDate = new Date(birthdate);
    const currentDate = new Date();

    const years = currentDate.getFullYear() - birthdateDate.getFullYear();
    const months = currentDate.getMonth() - birthdateDate.getMonth();
    const days = currentDate.getDate() - birthdateDate.getDate();

    if (months < 0 || (months === 0 && days < 0)) {
        years--;
    }

    return years;
}

// Replace 'YYYY-MM-DD' with the person's birthdate in 'YYYY-MM-DD' format.
const birthdate = '1990-01-15'; // Example birthdate

const age = calculateAge(birthdate);
console.log(`The person's age is ${age} years.`);
```
14. Ques: Convert Decimal to Binary?
```javascript
function decimalToBinary(decimal) { 
    return decimal.toString(2);
}

const decimalNumber = 42; // Replace with your decimal number
const binaryNumber = decimalToBinary(decimalNumber);
console.log(`Binary representation of ${decimalNumber} is: ${binaryNumber}`);
```
15. Ques: How to find the maximum occurring character in given String?
```javascript

const getMaxChar = (string) => {
    const map = {};
    string.split("").forEach(char => {
        map[char] = map[char] ? map[char] + 1 : 1;
    });
    max = 1;
    char = string[0]
    for(let k in map){
        if(map[k] > max) {
            max = map[k];
            char = k
        }
    }
    return char;
}
console.log(getMaxChar("hello world"));
```

16. Ques: How do you remove a given character from String? 
```javascript
const removeChar = (string, char) => {
    return string.split("").filter(i => i !== char).join("")
}
console.log(removeChar("hello world",'h'));
```

17. Ques: 
