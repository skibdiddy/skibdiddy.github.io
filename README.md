# skibdiddy.github.io
skib diddy

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Skib diddy toilet</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="calculator">
        <input type="text" id="result" disabled>
        <div class="buttons">
            <button onclick="clearResult()">C</button>
            <button onclick="appendToResult('7')">7</button>
            <button onclick="appendToResult('8')">8</button>
            <button onclick="appendToResult('9')">9</button>
            <button onclick="appendToResult('/')">/</button>
            <button onclick="appendToResult('4')">4</button>
            <button onclick="appendToResult('5')">5</button>
            <button onclick="appendToResult('6')">6</button>
            <button onclick="appendToResult('*')">*</button>
            <button onclick="appendToResult('1')">1</button>
            <button onclick="appendToResult('2')">2</button>
            <button onclick="appendToResult('3')">3</button>
            <button onclick="appendToResult('-')">-</button>
            <button onclick="appendToResult('0')">0</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendToResult('+')">+</button>
        </div>
    </div>
    <script src="script.js"></script>
</body>
</html>


function appendToResult(value) {
    document.getElementById('result').value += value;
}

function clearResult() {
    document.getElementById('result').value = '';
}

function calculateResult() {
    try {
        const result = eval(document.getElementById('result').value);
        document.getElementById('result').value = result;
    } catch (error) {
        document.getElementById('result').value = 'Error';
    }
}


body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #f4f4f4;
}

.calculator {
    border: 1px solid #ccc;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    background-color: white;
}

#result {
    width: 100%;
    height: 40px;
    text-align: right;
    font-size: 24px;
    margin-bottom: 10px;
    padding: 5px;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

button {
    height: 40px;
    font-size: 18px;
    cursor: pointer;
}
