## Instructions
```
Description

Your job is to create a simple password validation function, as seen on many websites.
The rules for a valid password are as follows:

There needs to be at least 1 uppercase letter.
There needs to be at least 1 lowercase letter.
There needs to be at least 1 number.
The password needs to be at least 8 characters long.
You are permitted to use any methods to validate the password.

Examples:

password("Abcd1234"); ===> true

password("Abcd123"); ===> false

password("abcd1234"); ===> false

password("AbcdefGhijKlmnopQRsTuvwxyZ1234567890"); ===> true

password("ABCD1234"); ===> false

password("Ab1!@#$%^&*()-_+={}[]|\:;?/>.<,"); ===> true;

password("!@#$%^&*()-_+={}[]|\:;?/>.<,"); ===> false;
Extra info

You will only be passed strings.
The string can contain any standard keyboard character.
Accepted strings can be any length, as long as they are 8 characters or more.
```

## Sample Tests
```js
Test.assertEquals(password("Abcd1234"), true);
Test.assertEquals(password("Abcd123"), false);
Test.assertEquals(password("abcd1234"), false);
Test.assertEquals(password("AbcdefGhijKlmnopQRsTuvwxyZ1234567890"), true);
Test.assertEquals(password("ABCD1234"), false);
Test.assertEquals(password("Ab1!@#$%^&*()-_+={}[]|\:;?/>.<,"), true);
Test.assertEquals(password("!@#$%^&*()-_+={}[]|\:;?/>.<,"), false);
```

## Solution
```js
const password = s => /^(?=.*[A-Z])(?=.*[a-z])(?=.*\d).{8,}$/.test(s);
```

## Submission Tests
```
Time: 353ms Passed: 157 Failed: 0
Test Results:
 Password validator
 Basic tests (7 of 7 Assertions)
Completed in 7ms
 Random tests
 Random tests too short (50 of 50 Assertions)
Completed in 5ms
 Random tests
 Random tests shorter strings (50 of 50 Assertions)
Completed in 4ms
 Random tests
 Random tests longer strings (50 of 50 Assertions)
Completed in 19ms
You have passed all of the tests! :)
```
