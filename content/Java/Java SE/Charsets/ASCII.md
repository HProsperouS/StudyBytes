---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - java se
Creation Date: 
Last Date: 
References: 
description: Charset - ASCII
---

## Abstract
---
- ASCII stands for the "American Standard Code for Information Interchange". It was designed in the early 60's, as a standard character set for computers and electronic devices. 
- ASCII is a 7-bit character set containing 128 characters, including numbers from 0-9, upper and lower case English letters from A to Z, and some special characters.
- The character sets used in modern computers, in HTML, and on the Internet, are all based on ASCII. 
  
## Example: ASCII Printable Characters 
---
| Char | Number | Description        |
|------|--------|--------------------|
| a    | 97     | Lowercase a        |
| b    | 98     | Lowercase b        |
| c    | 99     | Lowercase c        |
| d    | 100    | Lowercase d        |
| e    | 101    | Lowercase e        |
| f    | 102    | Lowercase f        |

## ACSII Use Cases
---
Understanding and using the ASCII encoding can be very useful when programming and solving algorithmic problems, such as on LeetCode. Here are some specific use cases:

### Conversion between characters and numbers
- The ASCII encoding makes it easy to convert characters and numbers to each other, which is very useful when working with strings and arrays of characters.

- Example 1: Determines whether the character is a number
```java
public boolean isDigit(char c) {
    return c >= '0' && c <= '9';
}
```

- Example 2: Convert character to number
```java
public int charToDigit(char c) {
    return c - '0';
}
```

- Example 3: Convert number to character
```java
public char digitToChar(int digit) {
    return (char) (digit + '0');
}
```

### Count the Frequency of Each Character
- Character frequency counting is a common task in string processing. It can be effectively achieved using ASCII codes.
- Example 4: Counting the occurrence of each character in a string
```java
public int[] countCharacters(String s) {
    int[] counts = new int[128]; // ASCII range is from 0 to 127
    for (char c : s.toCharArray()) {
        counts[c]++;
    }
    return counts;
}
```

## Reference
---
- [W3School](https://www.w3schools.com/charsets/ref_html_ascii.asp)