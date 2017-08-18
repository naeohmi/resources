# Algorithm Practice:

## Reverse A String

### Version 1:
```
let reverseString = (str) => {
  let j = '';
  for (let i = str.length - 1; i >= 0; i--) {
      j += str[i];
  }
  return j;
};
reverseString("hello");
```

### Version 2:
```
let reverseString = (str) => {
  let arr = [];
  let lgth = str.length;
  for (let i = 0; i <= str.length; i++) {
      arr.push(str.charAt(lgth - i));
  }
  return arr.join('');
};
reverseString("hello");
```

### Version 3:
```
let reverseString = (str) => {
  return str.split("").reverse().join("");
};
reverseString("hello");
```


## Factorialize A Number:

### Version 1 (iterative):
```
let factorialize = (num) => {
  let counter = 1;
  for (let i = 1; i <= num; i++) {
    counter *= i;
  }
  return counter;
};
factorialize(5);
```

### Version 2 (recursive):
```
let factorialize = (num) => {
    if (num <= 1) {
        return num;
    } else {
        return num * factorialize(num - 1)
    }
};
factorialize(5);
```


## Check For Palindromes:

### Version 1:
```
let palindrome = (str) => {
    let str = str.replace(/[^a-zA-Z0-9]+/gi, '').toLowerCase();
    let reverseStr = '';
    for (let k in str) {
        reverseStr += str[(str.length - k) - 1];
    }
    return str === reverseStr ? true : false; 
};
palindrome("eye");
```

### Version 2:
```
let palindrome = (str) => {
    let str = str.replace(/[^a-zA-Z0-9]+/gi, '').toLowerCase();
    return str == str.split('').reverse().join('');
};
palindrome("eye");
```

## Find Longest Word:

```
let findLongestWord = (str) => {
    let arr = str.split(" ");
    let lgth = 0;
    for (let i in arr) {
        if (arr[i].length > lgth) {
            let lgth = arr[i].length;
        }
    }
    return lgth;
};
findLongestWord("The quick brown fox jumped over the lazy hen");
```