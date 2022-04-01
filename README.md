# mumbling-codewars

## Problem 
Description:
This time no story, no theory. The examples below show you how to write function accum:

Examples:
accum("abcd") -> "A-Bb-Ccc-Dddd"
accum("RqaEzty") -> "R-Qq-Aaa-Eeee-Zzzzz-Tttttt-Yyyyyyy"
accum("cwAt") -> "C-Ww-Aaa-Tttt"

## Solution
```javascript 
const accum = (s) => {
  var char = s.split('');
  var words = [];
  for(let i = 0; i < char.length; i++) {
    words.push(char[i].toUpperCase() + Array(i + 1).join(char[i].toLowerCase()))
  }
  return words.join('-')
}
```
