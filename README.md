# calculator-javascript

## HTML:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <div class="display">
            <div class="name">B.ROSELINE<br>212221220046</div>
            <div id="result"></div>
        </div>
        <div class="buttons">
            <button onclick="clearDisplay()">AC</button>
            <button onclick="deleteLast()">DEL</button>
            <button onclick="appendOperator('/')">/</button>
            <button onclick="appendNumber(7)">7</button>
            <button onclick="appendNumber(8)">8</button>
            <button onclick="appendNumber(9)">9</button>
            <button onclick="appendOperator('*')">*</button>
            <button onclick="appendNumber(4)">4</button>
            <button onclick="appendNumber(5)">5</button>
            <button onclick="appendNumber(6)">6</button>
            <button onclick="appendOperator('-')">-</button>
            <button onclick="appendNumber(1)">1</button>
            <button onclick="appendNumber(2)">2</button>
            <button onclick="appendNumber(3)">3</button>
            <button onclick="appendOperator('+')">+</button>
            <button onclick="appendNumber(0)">0</button>
            <button onclick="appendOperator('%')">%</button>
            <button onclick="calculate()">=</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>
```
## CSS:
```
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background: linear-gradient(135deg, blue, pink);
    font-family: Arial, sans-serif;
}

.calculator {
    background: #f3e5f5;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
    display: grid;
    grid-template-rows: auto 1fr;
}

.display {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    padding: 10px;
    background: white;
    border-radius: 5px;
    margin-bottom: 10px;
    box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.1);
}

.display .name {
    align-self: center;
    text-align: center;
    font-size: 1.2em;
    color: #6200ea;
}

#result {
    font-size: 2em;
    color: #311b92;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

button {
    background: #9575cd;
    border: none;
    padding: 20px;
    font-size: 1.2em;
    border-radius: 5px;
    color: white;
    box-shadow: 0 4px #5e35b1;
    cursor: pointer;
    transition: all 0.2s;
}

button:active {
    box-shadow: 0 2px #5e35b1;
    transform: translateY(2px);
}

button:hover {
    background: #7e57c2;
}
```
## JAVASCRIPT:
```
function clearDisplay() {
    document.getElementById('result').innerText = '';
}

function deleteLast() {
    let result = document.getElementById('result').innerText;
    document.getElementById('result').innerText = result.slice(0, -1);
}

function appendNumber(number) {
    document.getElementById('result').innerText += number;
}

function appendOperator(operator) {
    document.getElementById('result').innerText += operator;
}

function calculate() {
    try {
        let result = eval(document.getElementById('result').innerText);
        document.getElementById('result').innerText = result;
    } catch (e) {
        document.getElementById('result').innerText = 'Error';
    }
}
```
## OUTPUT:
![image](https://github.com/Roselineb/calculator-javascript/assets/128909895/99689964-db18-4ed6-b2c8-469067f7294d)
![image](https://github.com/Roselineb/calculator-javascript/assets/128909895/fc2c62b8-9e3b-4c7c-b8fa-7854c290faa7)
![image](https://github.com/Roselineb/calculator-javascript/assets/128909895/56b33518-31a0-4999-a879-cb991807313b)



