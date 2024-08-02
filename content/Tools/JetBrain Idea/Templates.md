---
Author:
  - Liu JiaJun
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags: 
  - ide
Creation Date: 
Last Date: 
References: 
description: Tools -> Idea -> Template
---

## JetBrains IntelliJ IDEA Templates
---
JetBrains IntelliJ IDEA provides a rich set of templates to improve development efficiency. These templates can include various code snippets, file templates, and custom live templates. Below are some common types of templates:

### 1. Live Templates
Live Templates help quickly insert frequently used code snippets. Here are some examples:

- **psvm**: Generates `public static void main(String[] args)` method.
- **sout**: Generates `System.out.println()`.
- **soutv**: Generates `System.out.println("var = " + var)`, outputting the variable value.
- **fori**: Generates a common for loop.

### 2. File Templates
These templates are used to create new files, usually containing basic file structures.

- **Java Class**: Creates a new Java class file.
- **Java Interface**: Creates a new Java interface file.
- **HTML File**: Creates a new HTML file.
- **JUnit Test Class**: Creates a new JUnit test class.

### 3. Custom Templates
Users can create custom templates according to their needs. Below are the steps to create and use custom templates:

#### Creating Live Templates
1. Go to `File -> Settings -> Editor -> Live Templates`.
2. Click the `+` button and select `Template Group` to create a new template group.
3. Select the newly created group, click the `+` button, and select `Live Template` to add a template.
4. Define the template abbreviation and template text, then specify the context.

#### Creating File Templates
1. Go to `File -> Settings -> Editor -> File and Code Templates`.
2. In the `Files` tab, click the `+` button to add a new file template.
3. Specify the file name and template content.

#### Example Code
Below are some examples of custom Live Templates:

##### Singleton Pattern
```java
public class $ClassName$ {
    private static final $ClassName$ INSTANCE = new $ClassName$();
    
    private $ClassName$() {}
    
    public static $ClassName$ getInstance() {
        return INSTANCE;
    }
}
```
##### Logging 
```java
private static final Logger logger = LoggerFactory.getLogger($ClassName$.class);
```
These templates can be quickly inserted using shortcuts, thus improving coding efficiency. If you have specific template requirements, feel free to describe them, and I can help you create specific templates.

