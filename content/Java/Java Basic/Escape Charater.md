---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - java
Creation Date: 
Last Date: 
References: 
description: Java Intro Page
---

## Abstract
---
- In Java, an escape character is a character preceded by a backslash (`\`) that has a special meaning to the compiler. 
- Escape characters are used to represent certain special characters within string literals and character literals.

## Common Escape Characters
---
### Single Quote (`\'`)
- Used to represent a single quote character.

```java
char singleQuote = '\'';
System.out.println("Single quote: " + singleQuote);
//Output: Single quote: '
```

### Double Quote (`\"`)
- Used to represent a double quote character.

```java
String doubleQuote = "He said, \"Hello, World!\"";
System.out.println(doubleQuote);
//Output: He said, "Hello, World!"
```

### Backslash (`\\`)
- Used to represent a backslash character.

```java
String backslash = "This is a backslash: \\";
System.out.println(backslash);
//Output: This is a backslash: \
```

### New Line (`\n`)
- Used to represent a new line character.

```java
String newLine = "First line.\nSecond line.";
System.out.println(newLine);
//Output: 
//First line.
//Second line.
```

### Carriage Return (`\r`)
- Used to represent a carriage return character.

```java
String carriageReturn = "First line.\rSecond line.";
System.out.println(carriageReturn);
//Output: Second line.
```

### Tab (`\t`)
- Used to represent a tab character.

```java
String tab = "Column1\tColumn2";
System.out.println(tab);
//Output: Column1    Column2
```

### Backspace (`\b`)
- Used to represent a backspace character.

```java
String backspace = "Hello\bWorld";
System.out.println(backspace);
//Output: HellWorld
```