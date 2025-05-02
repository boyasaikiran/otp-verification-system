<!DOCTYPE html>
<html>
<head>
  <title>Simple Scientific Calculator</title>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjs/10.6.4/math.min.js"></script>
</head>
<body>
  <h2>Scientific Calculator</h2>
  <input type="text" id="display" readonly><br><br>

  <button onclick="append('sin(')">sin</button>
  <button onclick="append('cos(')">cos</button>
  <button onclick="append('tan(')">tan</button>
  <button onclick="append('sqrt(')">√</button><br>

  <button onclick="append('7')">7</button>
  <button onclick="append('8')">8</button>
  <button onclick="append('9')">9</button>
  <button onclick="append('/')">/</button><br>

  <button onclick="append('4')">4</button>
  <button onclick="append('5')">5</button>
  <button onclick="append('6')">6</button>  
  <button onclick="append('*')">*</button><br>

  <button onclick="append('1')">1</button>
  <button onclick="append('2')">2</button>
  <button onclick="append('3')">3</button>
  <button onclick="append('-')">-</button><br>

  <button onclick="append('0')">0</button>
  <button onclick="append('.')">.</button>
  <button onclick="calculate()">=</button>
  <button onclick="append('+')">+</button><br>

  <button onclick="append('pi')">π</button>
  <button onclick="append('e')">e</button>
  <button onclick="append('log(')">log</button>
  <button onclick="append('^')">^</button><br>

  <button onclick="clearDisplay()">C</button>
  <button onclick="backspace()">⌫</button>

  <script>
    function append(val) {
      document.getElementById("display").value += val;
    }

    function clearDisplay() {
      document.getElementById("display").value = '';
    }

    function backspace() {
      const disp = document.getElementById("display");
      disp.value = disp.value.slice(0, -1);
    }

    function calculate() {
      try {
        const result = math.evaluate(document.getElementById("display").value);
        document.getElementById("display").value = result;
      } catch {
        alert("Invalid Expression");
      }
    }
  </script>
</body>
</html>
