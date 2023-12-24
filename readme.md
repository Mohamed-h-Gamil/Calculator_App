# Scientific Calculator

This project is a Java-based scientific calculator. It's built using Apache Ant, a Java library and command-line tool that helps in driving processes described in build files as targets and extension points dependent upon each other. The calculator is designed to provide a user-friendly interface that allows users to perform a wide range of mathematical operations.

## Code Overview

The main class `calculator_app` extends `javax.swing.JFrame`, indicating that this is a Swing-based GUI application. Swing is a part of Java Foundation Classes (JFC) that is used to create window-based applications. It is built on the top of AWT (Abstract Windowing Toolkit) API and entirely written in java. This makes it platform-independent and lightweight.

The class contains several private variables to keep track of the current number (`num`), the current text (`txt`), and a draft string (`draft`). These variables are used to manage the state of the calculator and to store intermediate results of calculations.

The calculator also uses a `HashMap` to map characters to integers (`opr`). This is likely used to represent the precedence of different operators in mathematical expressions. For example, in the constructor of the class, the character '=' is mapped to the integer 0, which might indicate that '=' is considered an operator with the lowest precedence.

In addition, the class uses two `Stack` objects, `operations` and `operands`. These are stacks of stacks of characters and doubles, respectively. These data structures are likely used to parse and evaluate the mathematical expressions entered by the user. The `operations` stack probably stores the operators in the current expression, while the `operands` stack stores the numerical operands.

The class also contains several boolean flags and integer counters, such as `empty_flag`, `opr_flag`, `end_flag`, `func_flag`, `end_bracket`, `decimal_flag`, `bracket_flag`, and `func_count`. These are used to manage the state of the calculator and to track various aspects of the parsing and evaluation process. 
- `num`: This variable is used to store the current number that the user has input or the result of a calculation. It's a double-precision floating-point number, which allows it to hold very large (or small) numbers with a high degree of precision.

- `txt`: This is a `String` variable that holds the current text displayed on the calculator's screen. It could be a number, an expression, or a message to the user.

- `draft`: This `String` variable is used to store a draft of the current expression. It's used when the user is in the middle of typing an expression and hasn't yet hit the equals button to calculate the result.

- `opr`: This is a `HashMap` that maps `Character` keys to `Integer` values. It's used to represent the precedence of different operators in mathematical expressions. For example, the character '=' might be mapped to the integer 0, indicating that '=' is considered an operator with the lowest precedence.

- `operations`: This is a `Stack` of `Stack<Character>` objects. It's used to store the operators in the current expression. The use of a stack of stacks allows the calculator to handle nested expressions correctly.

- `operands`: This is a `Stack` of `Stack<Double>` objects. It's used to store the numerical operands in the current expression. Like `operations`, the use of a stack of stacks allows the calculator to handle nested expressions.

- `empty_flag`: This boolean flag is used to indicate whether the current expression is empty. It's likely set to `true` when the calculator is cleared or after a calculation is completed.

- `opr_flag`: This boolean flag is used to indicate whether the last character entered was an operator. This could be used to prevent the user from entering two operators in a row.

- `end_flag`: This boolean flag is used to indicate whether the current operation is complete. It's likely set to `true` after the user hits the equals button and the result is calculated.

- `func_flag`: This boolean flag is used to indicate whether a function is being used. It's likely set to `true` when the user starts typing a function name.

- `end_bracket`: This boolean flag is used to indicate whether a closing bracket is expected. It's likely set to `true` when the user types an opening bracket and set to `false` when they type a closing bracket.

The constructor `calculator_app()` initializes the `opr` HashMap and sets up the GUI. This involves creating the buttons for the calculator and setting up the layout of the GUI.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or above
- Apache Ant

### Installation

1. Clone the repository to your local machine.
2. Open the project in your preferred Java IDE.
3. Build and run the project using Apache Ant.

## Usage

After running the application, you will see a user-friendly interface. You can perform calculations by clicking the buttons on the calculator. The calculator supports a wide range of mathematical operations, from basic arithmetic to complex scientific calculations. It also supports functions like sine, cosine, and tangent, as well as logarithmic and exponential functions.

## Contributing

Contributions are welcome. Please open an issue first to discuss what you would like to change. Please make sure to update tests as appropriate. We value all our contributors and aim to make the contributing process as smooth as possible.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details. The MIT License is a permissive license that is short and to the point. It lets people do anything they want with your code as long as they provide attribution back to you and don’t hold you liable.

## Acknowledgements

- Java Swing library for providing the GUI components.
- Java Math library for providing the mathematical functions.
- Apache Ant for providing the build tool.

We would like to express our gratitude to the developers of these libraries and tools for making this project possible. Their hard work and dedication have greatly simplified the process of developing this scientific calculator.

## Future Work

We plan to continue improving and expanding the functionality of this scientific calculator. Future updates may include additional mathematical functions, improved error handling, and enhanced user interface. We welcome feedback and suggestions from users to help guide these improvements.