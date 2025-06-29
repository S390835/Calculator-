# Calculator-
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Calculator</title>
  </head>
<body>
  
     <div class="calculator">
  <div class="display" id="display"></div>
       
      

  <div class="buttons">
    <button class="kgf"onclick="clearDisplay()">C</button>
    <button class="rrr"onclick="appendValue('()')">()</button>
    <button class="rrr"onclick="appendValue('%')">%</button>
    <button class="rrr"onclick="appendValue('/')">÷</button>
    
    <button onclick="appendValue('7')">7</button>
    <button onclick="appendValue('8')">8</button>
    <button onclick="appendValue('9')">9</button>
    <button class="rrr"onclick="appendValue('*')">×</button>
    
    <button onclick="appendValue('4')">4</button>
    <button onclick="appendValue('5')">5</button>
    <button onclick="appendValue('6')">6</button>
    <button class="rrr"onclick="appendValue('-')">−</button>
    
    <button onclick="appendValue('1')">1</button>
    <button onclick="appendValue('2')">2</button>
    <button onclick="appendValue('3')">3</button>
    <button class="rrr"onclick="appendValue('+')">+</button>
    
    <button class="rrr"onclick="toggleSign()">+/-</button>
    <button onclick="appendValue('0')">0</button>
    <button class="rrr"onclick="appendValue('.')">.</button>
    <button class="equal" onclick="calculate()">=</button>
  </div>
</div>
  <style>
  .kgf {
    color:red;
  }
  .rrr {
    color: green;
  }
  .calculator {
  width: 300px;
  margin: 30px auto;
  padding: 20px;
  background: #f2f2f2;
  border-radius: 20px;
  box-shadow: 0 0 15px #aaa;
}

.display {
  background: white;
  padding: 20px;
  font-size: 28px;
  text-align: right;
  border-radius: 10px;
  margin-bottom: 10px;
  min-height: 40px;
  border: 1px solid #ccc;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 20px;
  border: none;
  border-radius: 50%;
  background: white;
  color: black;
  box-shadow: 0 2px 5px rgba(0,0,0,0.2);
  transition: 0.2s;
}

button:hover {
  background: #e6e6e6;
}

.equal {
  background: green;
  color: white;
  border-radius: 50%;
}
  button:hover {
    background: #00ff00;
  }
  </style>
  <script>
  let display = document.getElementById('display');

function appendValue(value) {
  display.innerText += value;
}

function clearDisplay() {
  display.innerText = "";
}

function calculate() {
  try {
    display.innerText = eval(display.innerText);
  } catch {
    display.innerText = "Error";
  }
}

function toggleSign() {
  if (display.innerText.startsWith("-")) {
    display.innerText = display.innerText.slice(1);
  } else {
    display.innerText = "-" + display.innerText;
  }
}
  </script>
  
</body>
</html>
