# Online Calculator

## Description
This project is a simple online calculator designed using HTML, CSS, and JavaScript. The calculator allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division. It features a clear button to reset the screen and parentheses for complex expressions.

## Design Steps
1. **HTML Structure**:
   - Create a basic HTML structure with a `<form>` to hold the calculator's display and buttons.
   - Use a table to layout the calculator buttons in a grid format.
   - Add input fields for each button with corresponding values and onclick events to handle user interactions.

2. **CSS Styling**:
   - Add styles to the table to enhance its visibility and layout.
   - Use border properties to define the appearance of the table and its cells.
   - Add spacing between table cells for a cleaner look.

3. **JavaScript Functionality**:
   - Implement functions to handle button clicks and perform calculations.
   - `addToScreen(value)`: Appends the clicked button's value to the screen.
   - `clearScreen()`: Clears the calculator screen.
   - `calculateFinalResult()`: Evaluates the expression on the screen and displays the result.

## Implementation
1. **HTML**:
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="stylesheet" href="style.css">
        <title>Calculator</title>
        <style>
            table {
                border: 2px double black;
                border-spacing: 10px;
            }
            tr {
                margin: 10px;
            }
        </style>
        <script>
            function addToScreen(value) {
                var screen = document.getElementById("screen");
                screen.value += value;
            }

            function clearScreen() {
                document.getElementById("screen").value = "";
            }

            function calculateFinalResult() {
                var screen = document.getElementById("screen");
                try {
                    screen.value = eval(screen.value);
                } catch (error) {
                    screen.value = "Error";
                }
            }
        </script>
    </head>
    <body>
        <div>
            <form name="calculator">
                <table>
                    <tr>
                        <th colspan="5"> <input type="textfield" id="screen" name="screen" value=""></th>
                    </tr>
                    <tr>
                        <td colspan="2"><input type="button" value="Clear" onclick="clearScreen()"></td>
                        <td> 
                            <input type="button" value="=" onclick="calculateFinalResult()">
                        </td>
                        <td> 
                            <input type="button" value="(" onclick="addToScreen('(')">
                        </td>
                        <td> 
                            <input type="button" value=")" onclick="addToScreen(')')">
                        </td>
                    </tr>
                    <tr>
                        <td> 
                            <input type="button" value="*" onclick="addToScreen('*')">
                        </td>
                        <td>
                            <input type="button" value="/" onclick="addToScreen('/')">
                        </td>
                        <td>
                            <input type="button" value="+" onclick="addToScreen('+')">
                        </td>
                        <td>
                            <input type="button" value="-" onclick="addToScreen('-')">
                        </td>
                        <td>
                            <input type="button" value="." onclick="addToScreen('.')">
                        </td>
                    </tr>
                    <tr>
                        <td> <input type="button" value="1" onclick="addToScreen('1')">
                        </td>
                        <td> <input type="button" value="2" onclick="addToScreen('2')">
                        </td>
                        <td> <input type="button" value="3" onclick="addToScreen('3')">
                        </td>
                        <td> <input type="button" value="4" onclick="addToScreen('4')">
                        </td>
                        <td> <input type="button" value="5" onclick="addToScreen('5')">
                        </td>
                    </tr>
                    <tr>
                        <td> 
                            <input type="button" value="6" onclick="addToScreen('6')">
                        </td>
                        <td>            
                            <input type="button" value="7" onclick="addToScreen('7')">
                        </td>
                        <td>            
                            <input type="button" value="8" onclick="addToScreen('8')">
                        </td>
                        <td>            
                            <input type="button" value="9" onclick="addToScreen('9')">
                        </td>
                        <td>
                            <input type="button" value="0" onclick="addToScreen('0')">
                        </td>
                    </tr>
                </table>
            </form>
        </div>
    </body>
    </html>
    ```

2. **CSS**:
    The CSS for this project is included directly within the `<style>` tags in the HTML file. It defines the appearance of the table and its cells.

3. **JavaScript**:
    The JavaScript functions are included within `<script>` tags in the HTML file. These functions manage the calculator's functionality, including handling button clicks and performing calculations.

## Requirements
To run this project, you need:
- A modern web browser (e.g., Chrome, Firefox, Safari).
- Basic knowledge of HTML, CSS, and JavaScript.
- A text editor or IDE for editing the code (e.g., VSCode, Sublime Text).

## How to Use
1. Open the `calculator.html` file in your web browser.
2. Use the calculator buttons to input numbers and operators.
3. Click the `=` button to calculate the result.
4. Click the `Clear` button to reset the calculator screen.

Feel free to customize the design and functionality according to your needs.
