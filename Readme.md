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

17. Ques: How do you find the length of the longest substring without repeating characters?
```javascript
var lengthOfLongestSubstring = function(s) {
    let count = 0;
    let i = 0;
    let j = 0;
    let n = s.length;
    let set = new Set();
    while (i < n && j < n) {
        let char = s.charAt(j);
        if(!set.has(char)) {
            set.add(char);
            j++;
            count = Math.max (count, j - i);
        } else {
            set.delete(s.charAt(i));
            i++;
        }
    }
    return count;
};

let result = lengthOfLongestSubstring('abcabcbb')
console.log(result);
```

18. Ques: How do you check if a given string is a palindrome?
```javascript
const mapOfString = str => {
 const map ={};
 str.split("").forEach(i => map[i] = map[i] ? map[i] + 1: 1);
 return map;
} 
const checkPalindrome = (string1, string2) => {
   const mapObject1 = mapOfString(string1);
   const mapObject2 = mapOfString(string2)
   if(mapObject1.length !== mapObject2.length){
       return false;
   }
   for(let i in mapObject1){
       if(mapObject1[i] !== mapObject2[i]){
           return false;
       }
   }
   return true;
}
console.log(checkPalindrome("ffsss","sfsf"));
```

19. Ques: How do you reverse a given string in place?
```javascript
"helloWorld".split("").reverse().join("");
```
20. How do you print duplicate characters from a string?
```javascript
const mapOfString = str => {
    const map ={};
    str.split("").forEach(i => map[i] = map[i] ? map[i] + 1: 1);
    return map;
   } 
   const duplicateString = str => {
    const arr =[];
    const obj = mapOfString(str)
    for(let j in obj){
        if(obj[j] > 1){
            arr.push(j)
        }
    }
    return arr.join("")
   }
   console.log(duplicateString("wefdwd"));
```

21. Ques: How do you find all the permutations of a string?
```javascript
let findPermutations = (string) => {
    if (!string || typeof string !== "string"){
      return "Please enter a string"
    } else if (string.length < 2 ){
      return string
    }
  
    let permutationsArray = [] 
     
    for (let i = 0; i < string.length; i++){
      let char = string[i]
  
      let remainingChars = string.slice(0, i) + string.slice(i + 1, string.length)
  
      for (let permutation of findPermutations(remainingChars)){
        permutationsArray.push(char + permutation) }
    }
    return permutationsArray
  }
```

22. Ques: How do you print duplicate characters from a string?
```javascript
function printDuplicateCharacters(str) {
    const charCount = new Map();

    // Count occurrences of each character in the string
    for (let char of str) {
        charCount.set(char, (charCount.get(char) || 0) + 1);
    }

    // Print duplicate characters
    charCount.forEach((count, char) => {
        if (count > 1) {
            console.log(`Character '${char}' appears ${count} times.`);
        }
    });
}

// Example usage
let inputString = "programming";
printDuplicateCharacters(inputString);
```
23. Ques: How can a given string be reversed using recursion?
```javascript
function reverseString(str) {
    // Base case: if the string has one or zero characters, it's already reversed
    if (str.length <= 1) {
        return str;
    }

    // Recursive case: reverse the substring excluding the first character,
    // then append the first character to the end
    return reverseString(str.slice(1)) + str[0];
}

// Example usage
let originalString = "hello";
let reversedString = reverseString(originalString);
console.log(reversedString);
```

24. Ques: How do you check if a string contains only digits?
```javascript
function containsOnlyDigits(str) {
    // Use a regular expression to check if the string contains only digits
    return /^\d+$/.test(str);
}

// Example usage
let testString1 = "12345";
let testString2 = "abc123";
let testString3 = "  456  ";

console.log(containsOnlyDigits(testString1));  // Output: true
console.log(containsOnlyDigits(testString2));  // Output: false
console.log(containsOnlyDigits(testString3));  // Output: false
```
25. Ques: How do you count a number of vowels and consonants in a given string?
```javascript
function countVowelsAndConsonants(str) {
    // Convert the string to lowercase to handle both uppercase and lowercase vowels
    str = str.toLowerCase();

    // Define arrays of vowels and consonants
    const vowels = ['a', 'e', 'i', 'o', 'u'];
    const consonants = 'bcdfghjklmnpqrstvwxyz';

    // Initialize counters
    let vowelCount = 0;
    let consonantCount = 0;

    // Iterate through each character in the string
    for (let char of str) {
        if (vowels.includes(char)) {
            vowelCount++;
        } else if (consonants.includes(char)) {
            consonantCount++;
        }
    }

    // Return the counts
    return { vowels: vowelCount, consonants: consonantCount };
}

// Example usage
let testString = "Hello, World!";
let result = countVowelsAndConsonants(testString);
console.log(result);
```

26. Ques: How do you count the occurrence of a given character in a string?
```javascript
function countOccurrences(str, char) {
    return str.split(char).length - 1;
}

// Example usage:
let inputString = "hello, world";
let characterToCount = "l";
let result = countOccurrences(inputString, characterToCount);

console.log(`The character '${characterToCount}' occurs ${result} times in the string.`);
```

27. Ques: How do you print the first non-repeated character from a string?
```javascript
function firstNonRepeatedCharacter(str) {
    // Create an object to store character frequencies
    const charFrequency = {};

    // Iterate through the string to populate the character frequencies
    for (let char of str) {
        charFrequency[char] = (charFrequency[char] || 0) + 1;
    }

    // Iterate through the string again to find the first non-repeated character
    for (let char of str) {
        if (charFrequency[char] === 1) {
            return char;
        }
    }

    // If no non-repeated character is found, return null or any appropriate value
    return null;
}

// Example usage:
let inputString = "hello, world";
let result = firstNonRepeatedCharacter(inputString);

console.log(`The first non-repeated character is: ${result}`);
```

28. Ques: How do you reverse words in a given sentence without using any library method?
```javascript
function reverseWords(sentence) {
    // Split the sentence into an array of words
    const words = sentence.split(' ');

    // Reverse each word in the array
    const reversedWords = words.map(word => {
        // For each word, reverse its characters
        return word.split('').reverse().join('');
    });

    // Join the reversed words back into a sentence
    const reversedSentence = reversedWords.join(' ');

    return reversedSentence;
}

// Example usage:
let inputSentence = "Hello, world!";
let result = reverseWords(inputSentence);

console.log(`Original sentence: ${inputSentence}`);
console.log(`Reversed sentence: ${result}`);
```

29. Ques: How do you check if a given string is a palindrome?
```javascript
function isPalindrome(str) {
    // Remove non-alphanumeric characters and convert to lowercase
    const cleanedStr = str.replace(/[^A-Za-z0-9]/g, '').toLowerCase();

    // Compare characters from the start and end of the cleaned string
    for (let i = 0, j = cleanedStr.length - 1; i < j; i++, j--) {
        if (cleanedStr[i] !== cleanedStr[j]) {
            return false; // If characters do not match, it's not a palindrome
        }
    }

    return true; // If the loop completes without returning false, it's a palindrome
}

// Example usage:
let inputString = "A man, a plan, a canal, Panama";
let result = isPalindrome(inputString);

console.log(`Is "${inputString}" a palindrome? ${result}`);
```

30. Ques: How do you find the length of the longest substring without repeating characters?
```javascript
function lengthOfLongestSubstring(s) {
    let maxLength = 0;
    let start = 0;
    const charIndexMap = {};

    for (let end = 0; end < s.length; end++) {
        const currentChar = s[end];

        if (charIndexMap[currentChar] !== undefined && charIndexMap[currentChar] >= start) {
            start = charIndexMap[currentChar] + 1;
        }

        charIndexMap[currentChar] = end;
        const currentLength = end - start + 1;
        maxLength = Math.max(maxLength, currentLength);
    }

    return maxLength;
}

// Example usage:
let inputString = "abcabcbb";
let result = lengthOfLongestSubstring(inputString);

console.log(`Length of the longest substring without repeating characters: ${result}`);
```

31. Ques: How to convert a byte array to String? 
```javascript
// Example byte array
const byteArray = new Uint8Array([72, 101, 108, 108, 111]); // Corresponds to ASCII values for "Hello"

// Convert byte array to string
const textDecoder = new TextDecoder('utf-8');
const resultString = textDecoder.decode(byteArray);

console.log(resultString); // Output: Hello
```

32. Ques: How to remove the duplicate character from String?
```javascript
// Example usage:
let inputString = "programming";
let result = removeDuplicates(inputString);

console.log(`Original string: ${inputString}`);
console.log(`String without duplicates: ${result}`);

// Function definition
function removeDuplicates(str) {
    let result = '';
    const charSet = new Set();

    for (let char of str) {
        if (!charSet.has(char)) {
            charSet.add(char);
            result += char;
        }
    }

    return result;
}
```
33. Ques: How to find the maximum occurring character in given String?
```javascript
function findMaxOccurringChar(str) {
    const charCount = {};

    // Count occurrences of each character
    for (let char of str) {
        charCount[char] = (charCount[char] || 0) + 1;
    }

    let maxChar = '';
    let maxCount = 0;

    // Find character with maximum count
    for (let char in charCount) {
        if (charCount[char] > maxCount) {
            maxChar = char;
            maxCount = charCount[char];
        }
    }

    return maxChar;
}

// Example usage:
let inputString = "programming";
let result = findMaxOccurringChar(inputString);

console.log(`Input string: ${inputString}`);
console.log(`Maximum occurring character: ${result}`);
```
34. Ques: How do you remove a given character from String?
```javascript
function removeCharacter(str, charToRemove) {
    let result = '';

    for (let char of str) {
        if (char !== charToRemove) {
            result += char;
        }
    }

    return result;
}

// Example usage:
let inputString = "character";
let charToRemove = "a";
let result = removeCharacter(inputString, charToRemove);

console.log(`Original string: ${inputString}`);
console.log(`String after removing '${charToRemove}': ${result}`);
```

35. Ques: How do you find the duplicate number on a given integer array?
```javascript
function findDuplicateNumber(arr) {
    const numSet = new Set();

    for (let num of arr) {
        if (numSet.has(num)) {
            return num; // Found the duplicate
        } else {
            numSet.add(num);
        }
    }

    return null; // No duplicate found
}

// Example usage:
let inputArray = [3, 1, 4, 2, 2];
let result = findDuplicateNumber(inputArray);

console.log(`Input array: ${inputArray}`);
console.log(`Duplicate number: ${result}`);
```
36. Ques: How do you find the largest and smallest number in an unsorted integer array?
```javascript
function findMinMax(arr) {
    if (arr.length === 0) {
        return { min: null, max: null };
    }

    let min = arr[0];
    let max = arr[0];

    for (let i = 1; i < arr.length; i++) {
        if (arr[i] < min) {
            min = arr[i];
        } else if (arr[i] > max) {
            max = arr[i];
        }
    }

    return { min, max };
}

// Example usage:
let inputArray = [3, 1, 4, 2, 8, 5];
let result = findMinMax(inputArray);

console.log(`Input array: ${inputArray}`);
console.log(`Smallest number: ${result.min}`);
console.log(`Largest number: ${result.max}`);
```
37. Ques: How do you find duplicate numbers in an array if it contains multiple duplicates?
```javascript
function findDuplicateNumbers(arr) {
    const numCount = {};
    const duplicates = [];

    for (let num of arr) {
        if (numCount[num] === undefined) {
            numCount[num] = 1;
        } else {
            numCount[num]++;
            if (numCount[num] === 2) {
                // This is the second occurrence, consider it a duplicate
                duplicates.push(num);
            }
        }
    }

    return duplicates;
}

// Example usage:
let inputArray = [3, 1, 4, 2, 2, 1, 3, 4, 5, 5];
let result = findDuplicateNumbers(inputArray);

console.log(`Input array: ${inputArray}`);
console.log(`Duplicate numbers: ${result}`);
```
38. 

