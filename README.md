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
######################################################################
import React, { useState } from 'react';

function App() {
  const [msg, setMsg] = useState('');

  const login = (e) => {
    e.preventDefault();
    const user = e.target.user.value;
    const pass = e.target.pass.value;

    if (user === 'admin' && pass === '1234') setMsg('Success!');
    else setMsg('Failed!');
  };

  return (
    <div style={{ textAlign: 'center', marginTop: '100px' }}>
     <h2>Welcome App</h2>
      <form onSubmit={login}>
        <input name="user" placeholder="User" /><br /><br />
        <input name="pass" type="password" placeholder="Pass" /><br /><br />
        <button>Login</button>
      </form>
      <p>{msg}</p>v
    </div>
  );
}

export default App;
###########################################################################
import React, { useState } from 'react';

function App() {
  const [name, setName] = useState('');
  const [show, setShow] = useState(false);

  const handleSubmit = (e) => {
    e.preventDefault();
    if (name) setShow(true);
  };

  return (
    <div style={{ textAlign: 'center', marginTop: '80px' }}>
      <h2>Hello App</h2>
      {show ? <h3>Hello, {name}!</h3> : (
        <form onSubmit={handleSubmit}>
          <input value={name} onChange={(e) => setName(e.target.value)} placeholder="Enter name" />
          <br /><br />
          <button type="submit">Greet</button>
        </form>
      )}
    </div>
  );
}

export default App;
############################################################################################################
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Simple Form</title>
</head>
<body>

<h2>Contact Form</h2>

<form id="myForm">
  <input type="text" id="name" placeholder="Name" required><br><br>
  <input type="email" id="email" placeholder="Email" required><br><br>
  <button type="submit">Submit</button>
</form>

<script>
  document.getElementById('myForm').addEventListener('submit', function(e) {
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();

    if (!name || !email) {
      alert("Please fill in all fields.");
      e.preventDefault();
    } else {
      alert("Form submitted!");
    }
  });
</script>

</body>
</html>
#############################################################################################################
