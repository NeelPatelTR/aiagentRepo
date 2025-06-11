# Python Command-Line Calculator Project

## 1. Project Overview & User Requirement
The goal of this project is to create a simple, yet robust, command-line calculator using Python. The application should be able to perform basic arithmetic operations. The primary requirement is to build a tool that is both functional for calculations and resilient to common user errors, providing a smooth user experience.

The calculator will run in a loop, continuously prompting the user for input and performing calculations until the user decides to exit.

---

## 2. Input and Output

### Input
- The user will input a mathematical expression in a single line.
- The format should be: `[number] [operator] [number]`.
- **Supported Operators:**
  - `+` (Addition)
  - `-` (Subtraction)
  - `*` (Multiplication)
  - `/` (Division)
- The program should also accept a command to terminate the application (e.g., `exit` or `quit`).

**Example Inputs:**
```
5 + 10
12.5 * 2
100 / 4
exit
```

### Output
- The program will print the result of the calculation, clearly labeled.
- If the user provides invalid input or attempts an invalid operation, the program will print a clear, user-friendly error message.

**Example Outputs:**
```
Result: 15.0
Result: 25.0
Result: 25.0
Error: Invalid input. Please use the format: [number] [operator] [number]
Error: Cannot divide by zero.
Thank you for using the calculator. Goodbye!
```

---

## 3. Handling Edge Cases
A robust calculator must anticipate and manage potential errors gracefully. The following edge cases must be handled:

| Edge Case           | How to Handle                                                                 |
|---------------------|-------------------------------------------------------------------------------|
| Division by Zero    | If the user tries to divide by 0 (e.g., 10 / 0), display: `Error: Cannot divide by zero.` |
| Invalid Operator    | If the user enters an unsupported operator (e.g., 5 ^ 2), display: `Error: Invalid operator. Supported operators are +, -, *, /.` |
| Incorrect Format    | If the input does not match the `[number] [operator] [number]` format (e.g., 5+5, ten + five, 5 +), display a generic invalid input error. |
| Non-Numeric Input   | If `[number]` parts of the input are not valid numbers, display an error indicating that valid numbers are required. |
| Empty Input         | If the user hits Enter without typing anything, the program should re-prompt for input without crashing. |

---

## 4. Test Cases
To ensure the calculator is working correctly, the following test cases should be passed:

| #  | Input      | Expected Output                                      | Test Case Description                |
|----|------------|-----------------------------------------------------|--------------------------------------|
| 1  | 10 + 5     | Result: 15.0                                        | Basic Addition                       |
| 2  | 20 - 4     | Result: 16.0                                        | Basic Subtraction                    |
| 3  | 7 * 6      | Result: 42.0                                        | Basic Multiplication                 |
| 4  | 100 / 4    | Result: 25.0                                        | Basic Division                       |
| 5  | 3.5 + 1.5  | Result: 5.0                                         | Floating Point Addition              |
| 6  | 10 / 0     | Error: Cannot divide by zero.                       | Edge Case: Division by Zero          |
| 7  | 5 % 2      | Error: Invalid operator. Supported operators are +, -, *, /. | Edge Case: Invalid Operator          |
| 8  | five + 5   | Error: Invalid input. Please use the format: [number] [operator] [number] | Edge Case: Non-numeric Input         |
| 9  | 5+5        | Error: Invalid input. Please use the format: [number] [operator] [number] | Edge Case: Incorrect Format          |
| 10 | exit       | Thank you for using the calculator. Goodbye!         | Program Termination                  |

---

## 5. Making it User-Friendly
To ensure a good user experience, the following features should be implemented:

- **Clear Welcome Message and Instructions:**
  - When the program starts, it should display a welcome message and simple instructions on how to use it, including the input format and how to exit.
  - *Example:* `Welcome to the Python Calculator! Enter calculations as 'number operator number' (e.g., 5 * 3). Type 'exit' to quit.`

- **Continuous Operation:**
  - The calculator should operate in a loop, allowing the user to perform multiple calculations without restarting the script.

- **Informative Error Messages:**
  - Instead of crashing or showing a Python traceback, the program must catch exceptions and provide friendly messages that guide the user on how to correct their input.

- **Graceful Exit:**
  - The user should have a clear and simple way to exit the application (e.g., by typing `exit` or `quit`). The program should print a goodbye message upon exiting.
