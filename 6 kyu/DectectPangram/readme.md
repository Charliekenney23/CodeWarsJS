## Instructions
```
A pangram is a sentence that contains every single letter of the alphabet at least once. For example, the sentence "The quick brown fox jumps over the lazy dog" is a pangram, because it uses the letters A-Z at least once (case is irrelevant).

Given a string, detect whether or not it is a pangram. Return True if it is, False if not. Ignore numbers and punctuation.
```

## Sample Tests
```js
var string = "The quick brown fox jumps over the lazy dog."
Test.assertEquals(isPangram(string), true)
var string = "This is not a pangram."
Test.assertEquals(isPangram(string), false)
```
## Solution
```js
function isPangram(s){
  return "ABCDEFGHIJKLMNOPQRSTUVWXYZ".split('').
        every(c => s.toUpperCase().includes(c));
}
```
## Submission Tests
```
Time: 310ms Passed: 11 Failed: 0
Test Results:
Test Passed: Value == true
 Some tests in random order:
 Log
Is 'abcdefghijklmopqrstuvwxyz ' a pangram ?
Test Passed: Value == false
 Log
Is 'aaaaaaaaaaaaaaaaaaaaaaaaaa' a pangram ?
Test Passed: Value == false
 Log
Is 'Detect Pangram' a pangram ?
Test Passed: Value == false
 Log
Is 'A pangram is a sentence that contains every single letter of the alphabet at least once.' a pangram ?
Test Passed: Value == false
 Log
Is 'Cwm fjord bank glyphs vext quiz' a pangram ?
Test Passed: Value == true
 Log
Is 'This isn't a pangram!' a pangram ?
Test Passed: Value == false
 Log
Is 'Pack my box with five dozen liquor jugs.' a pangram ?
Test Passed: Value == true
 Log
Is 'How quickly daft jumping zebras vex.' a pangram ?
Test Passed: Value == true
 Log
Is 'AbCdEfGhIjKlM zYxWvUtSrQpOn' a pangram ?
Test Passed: Value == true
 Log
Is 'ABCD45EFGH,IJK,LMNOPQR56STUVW3XYZ' a pangram ?
Test Passed: Value == true
Completed in 5ms
You have passed all of the tests! :)
```
