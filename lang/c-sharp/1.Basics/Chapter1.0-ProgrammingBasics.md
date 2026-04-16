# Chapter 1.0 - Programming Basics

## 1. The Entry Point
Every C# program must have a Main method.  
This is where the execution of your application starts.  
Without it, the program won't know where to begin.
## 2. Sequential Execution
C# code executes sequentially from top to bottom.
## 3. Case Sensitivity  
C# is a case-sensitive programming language, which means uppercase and lowercase code are treated differently.
## 4. Code Blocks and Braces
C# code should be written within a pair of curly braces, known as a code block.  
Each code block belongs to the statement preceding it.  
Every opening brace `{` must have a matching closing brace `}`.
## 5. Statement Endings
Every standalone instruction (statement) in C# must end with a semicolon.  
It tells the compiler that one instruction has finished and the next is about to begin.
## 6. Whitespace and Indentation
C# is whitespace-insensitive.  
This means extra spaces, tabs, or new lines are ignored by the compiler.  
However, we use indentation to make the code readable for humans.
## 7. Naming Conventions
PascalCase: Used for Classes and Methods (e.g., MyProgram, CalculateTotal).  
camelCase: Used for Variables (e.g., userName, itemCount).
## 8. Comments
Use comments to explain your logic.  
They are ignored by the compiler.  
Single-line: Use // for brief notes.  
Multi-line: Use /* ... */ for longer explanations.
## 9. Namespaces
C# uses Namespaces to organize code into logical containers.  Think of a namespace as a "folder" that holds related classes to prevent naming conflicts.
## 10.  Reserved Keywords
Keywords are special words predefined by C# (e.g., `class`, `void`, `using`).  
You cannot use these as identifiers (names for variables or methods) because they have a specific meaning to the compiler.
## 11. Strongly Typed System
In C#, every variable must have a declared type.   
This ensures that the data stored in a variable matches what the program expects, preventing many common errors during compilation.
## 12. Statements vs. Expressions
A Statement is a complete instruction that performs an action (ends with a `;`).  
An Expression is a fragment of code that produces a value (e.g., `10 + 20`).
## 13. Identifier Naming Rules
When naming your variables, methods, or classes:  
Must start with a letter or an underscore `_`.  
Cannot start with a number.  
Cannot contain spaces or special symbols (except `_`).  
Cannot be a Reserved Keyword.  
## 14. Literals
Literals are fixed values written directly in the source code.  
`123` (Integer literal)  
`3.14` (Double literal)  
`"Archotech"` (String literal)  
`'A'` (Character literal)  
## 15. The Compilation Flow
C# does not run directly on hardware.  
It is compiled into Intermediate Language (IL).  
When you run the program, the Common Language Runtime (CLR) translates the IL into machine code.  
This is why C# is called Managed Code.
## 16. Using Directives
The `using` keyword is used to include namespaces.  
For example, `using System;` allows you to use the `Console` class without typing `System.Console` every time.

## Example Code:
```
// 9. NAMESPACES & 16. USING DIRECTIVES
using System; 

namespace ArchotechDev.Basics 
{
    // 7. NAMING CONVENTIONS (PascalCase) & 10. RESERVED KEYWORDS (class)
    class ProgrammingRules 
    {
        // 1. THE ENTRY POINT
        static void Main(string[] args) 
        {
            // 2. SEQUENTIAL EXECUTION
            // Line A must happen before Line B
            string status = "Learning"; // Line A
            Console.WriteLine(status);  // Line B

            // 3. CASE SENSITIVITY
            int age = 25;
            int Age = 30; // Different from 'age'

            // 4. CODE BLOCKS AND BRACES
            // The braces { } belong to the 'if' statement preceding it.
            if (true) 
            {
                // 6. WHITESPACE AND INDENTATION
                // The spaces before 'Console' are for human readability.
                Console.WriteLine("Inside a block"); 
            }

            // 5. STATEMENT ENDINGS (Semicolons)
            // 11. STRONGLY TYPED SYSTEM (must declare 'int')
            int score = 100; 

            // 8. COMMENTS
            // Single-line: setting a value
            /* Multi-line:
               The following section calculates 
               the final result. */

            // 12. STATEMENTS VS. EXPRESSIONS
            // "10 + 20" is an expression.
            // "int sum = 10 + 20;" is a statement.
            int sum = 10 + 20;

            // 13. IDENTIFIER NAMING RULES
            int _validName = 1;  // Starts with underscore
            int value2 = 2;      // Contains number
            // int 2value;       // INVALID: starts with number

            // 14. LITERALS
            int myInt = 123;            // Integer literal
            double myDouble = 3.14;     // Double literal
            string myString = "Hi";     // String literal
            char myChar = 'A';          // Character literal

            // 15. COMPILATION FLOW (Conceptual)
            // This C# source code -> Compiled to IL -> Executed by CLR
            Console.WriteLine("Managed code running on CLR.");
        }
    }
}

```