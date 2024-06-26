# Milestone 1: Input Handling Implementation
### Grammar Rules
The grammar for the language supported by the parser is as follows:
* **Operators**: Addition (+), Subtraction (-), Multiplication (*), Division (/)
    * Valid Expressions:
        * `3 * (4 - 2)`
        * `x / 2`
    * Invalid Expressions:
        * `2 +`
        * `3 ** 2`
* **Functions**: Trigonometric functions (sin, cos, tan), Square root (sqrt)
    * Valid Expressions:
        * `sin(pi/6)`
        * `cos(0) * 2`
    * Invalid Expressions:
        * `sqrt(-1)`
        * `tan(x) +`
* **Variables**: Single-letter variables (x, y, z)
    * Valid Expressions:
        * `x + y`
        * `2 * z`
    * Invalid Expressions:
        * `x y`
        * `xy`
* **Parentheses**: Open and close parentheses for grouping expressions
    * Valid Expressions:
        * `(x + 2) * 3`
        * `sqrt(4) * (y - 1)`
    * Invalid Expressions:
        * `2 + (3 * 4`
        * `sqrt(2 + )`

### Input Handling Implementation
* **Prompt User Input**: A function or method prompts the user to enter an arithmetic expression.
* **Tokenization**: The input string is tokenized by identifying numbers, operators, functions, variables, and parentheses based on the grammar rules.
* **Regular Expressions**: Regular expressions and string manipulation techniques are used to extract tokens efficiently.
* **Error Handling**: Edge cases and error scenarios, such as invalid characters or mismatched parentheses, are handled to prevent crashes and ensure robustness.
* **Token Storage**: Tokens are stored in a data structure like a list or a queue to facilitate parsing and further processing in subsequent milestones.

### Usage
To run the input handling implementation:
1. Execute the provided code in a Python environment.
2. Enter an arithmetic expression when prompted.
3. The tokenizer will tokenize the input expression and display the tokens.

# Milestone 2: Lexical Analysis (Tokenization)
### Tokenization Process
The tokenization process implemented in this milestone includes the following steps:
* **Prompt User Input**: A function or method prompts the user to enter an arithmetic expression.
* **Tokenization Logic**: The input string is tokenized by identifying numbers, operators, functions, variables, and parentheses based on the grammar rules.
* **Regular Expressions**: Regular expressions and string manipulation techniques are used to match input patterns and generate tokens accordingly.
* **Whitespace and Comment Handling**: Whitespace and comments in the input string are removed to ensure that only relevant characters contribute to tokenization.
* **Error Handling**: Error handling is implemented to detect invalid characters, mismatched parentheses, and other potential issues during tokenization. Error messages are displayed to guide users in correcting input errors.

### Usage
To run the tokenization process:
* Execute the provided code in a Python environment.
* Enter an arithmetic expression when prompted.
* The tokenizer will tokenize the input expression and display the tokens.

### Error Handling
The tokenizer implements error handling to detect and report the following issues:
* Invalid characters in the input expression.
* Mismatched parentheses (closing brackets without corresponding opening brackets, and vice versa).

# Milestone 3: Parsing Algorithm
### Steps
1. **Choose a Parsing Algorithm**: Select an appropriate parsing algorithm based on the complexity of the grammar. Common parsing algorithms include recursive descent, LL(1), and LR(1).
2. **Implement the Parsing Algorithm**: Develop the parsing algorithm using object-oriented design principles. Define classes to represent the grammar rules, parse tree nodes, and other relevant components.
3. **Parse Input Tokens**: Develop methods for parsing input tokens generated by the tokenizer. Implement recursive descent parsing or another suitable technique to analyze the tokens and construct a parse tree.
4. **Construct Parse Tree or Generate Parse Results**: Use the parsing algorithm to construct a parse tree representing the input expression's syntactic structure. Alternatively, generate parse results directly from the input tokens.

### Sample Inputs and Results:
1. Input: `2 + 3 * 4`
   * Expected Result: `14`
2. Input: `sqrt(16) / 2`
   * Expected Result: `2.0`
3. Input: `2 + (3 * 4)`
   * Expected Result: Error: 1 open bracket(s) '(' without corresponding closing bracket ')'
4. Input: `10 / 0`
   * Expected Result: Error: Division by zero
5. Input: `sin(0) + cos(pi/2)`
   * Expected Result: `1.0`
6. Input: `tan(pi/4)`
   * Expected Result: `1.0`
7. Input: `2 * sqrt(9)`
   * Expected Result: `6.0`
