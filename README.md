# Zaplag Compiler

## Overview
Zaplag Compiler is a Java-based compiler for the custom programming language Zaplag. It supports lexical analysis, parsing, semantic analysis, and code generation. This compiler translates Zaplag source code into executable output while enforcing the language's syntax and semantics.

## Features
- **Lexical Analysis**: Tokenizes the input source code based on Zaplag's syntax rules.
- **Symbol Table Management**: Stores and retrieves variable types, scopes, and values.
- **Regular Expression Processing**: Constructs an **NFA** from a given regular expression and converts it into a **DFA** for pattern recognition.
- **Error Handling**: Provides detailed error messages for syntax and semantic violations.

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/zaplag-compiler.git
   cd zaplag-compiler
   ```
2. Ensure you have Java (JDK 11 or later) installed.
3. Compile the project using:
   ```sh
   javac -d bin src/*.java
   ```
4. Run the compiler:
   ```sh
   java -cp bin Processor sample.zaplag
   ```

## Usage
1. Write Zaplag code in a `.zaplag` file.
2. Run the compiler with the file as input.
3. The compiler will perform lexical analysis, generate an NFA/DFA for variable recognition, and display tokens and a symbol table.

## Example
### Sample Zaplag Code
```zaplag
mint x = 10;
bubble y = x + 5;
womp y;
```
### Compilation Output
```
🔹 Tokenized Output:
Token [KEYWORD, mint, Line 1]
Token [IDENTIFIER, x, Line 1]
Token [OPERATOR, =, Line 1]
Token [INTEGER, 10, Line 1]
...

🔹 Symbol Table:
+--------------+---------+---------+--------+
| Identifier  | Type    | Scope   | Value  |
+--------------+---------+---------+--------+
| x          | mint    | sabka   | 10     |
| y          | bubble  | sabka   | 15     |
+--------------+---------+---------+--------+

🔹 NFA Construction for variable names:
State 0 -- a -> 1
State 1 -- b -> 2
...

🔹 DFA Construction:
DFA State 0 -> [a -> 1] [b -> 2] ...
```

## Supported Syntax
Zaplag follows specific syntax rules including:
- **Data Types**: `mint`, `bubble`, `drink`, `cherry`
- **Operators**: `+`, `-`, `*`, `/`, `%`, `^`
- **Control Structures**: `?` (conditional), `womp` (print)
- **Comments**: `# single-line`, `#* multi-line *#`
- **String and Character Handling**


## Contribution
We welcome contributions! To contribute:
1. Fork the repository.
2. Create a new branch.
3. Commit changes and push to your fork.
4. Open a pull request.

## License
This project is licensed under the MIT License.

