---
Author:
  - JiaJun Liu
Author Profile:
  - https://www.linkedin.com/in/jiajun-liu-775252244/
tags:
  - dsa
---

## Understanding Algorithms in Daily Life
---
- Algorithms are not just mathematical concepts but are also embedded in basic logic that we use daily.

**Examples of Algorithms in Everyday Activities:**
1. **Looking Up a Dictionary:**
   - **Process**: Open the dictionary halfway, compare the first letter on the page, and continue halving the section until the word is found.
   - **Algorithm**: This process is known as the Binary Search algorithm, where the dictionary acts as a sorted "array."
  
2. **Organizing Playing Cards:**
   - **Process**: Divide cards into "ordered" and "unordered" sections, then insert each card from the unordered section into its correct position in the ordered section.
   - **Algorithm**: This is the Insertion Sort algorithm, commonly used for small datasets.

3. **Making Change:**
   - **Process**: Start with the largest denomination and subtract until the exact change is given.
   - **Algorithm**: This is a Greedy Algorithm, where the best choice is made at each step to reach an optimal solution.

## Definition of an algorithm
---
- **Algorithm:** A set of instructions to solve a specific problem within a finite amount of time
  - **Characteristics:**
    1. **Clearly Defined:** Input and output are unambiguous.
    2. **Feasibility:** Can be completed within a finite number of steps, time, and memory.
    3. **Definitive Steps:** Each step has a clear meaning, and the output is consistent under the same conditions.

## Definition of a data structure
---
- **Data Structure:** A method of organizing and storing data in a computer.
  - Design Goals:
    1. **Minimize Space:** Reduce memory usage.
    2. **Optimize Operations:** Make data operations (access, addition, deletion, updating) as fast as possible.
    3. **Concise Representation:** Provide a logical structure for efficient algorithm execution.
  - **Trade-offs:** Improving one aspect often requires compromising another.
      - **Examples:**
        - **Linked Lists vs. Arrays:** Easier addition/deletion but slower data access.
        - **Graphs vs. Linked Lists:** Richer logical information but higher memory usage.

## Relationship between Data Structures and Algorithms
---
Data structures and algorithms are closely related and integrated, particularly in the following aspects:

1. **Foundation of Algorithms**: Data structures provide the necessary storage and methods for manipulating data in algorithms.
2. **Stage for Data Structures**: Algorithms apply data structures to solve specific problems; data structures alone only store data.
3. **Efficiency Variance**: Different data structures can be used to implement algorithms, but their execution efficiency can vary greatly. Choosing the right data structure is crucial.

**Comparing Data Structures and Algorithms to Building Blocks**
| **Data Structures and Algorithms** | **Building Blocks** |
| ---------------------------------- | ------------------- |
| Input data                         | Unassembled blocks  |
| Data structure                     | Organization of blocks, including shape, size, connections, etc. |
| Algorithm                          | Steps to assemble the blocks into the desired shape |
| Output data                        | Completed block model |

**Note**: Data structures and algorithms are independent of programming languages, allowing implementations in various languages.