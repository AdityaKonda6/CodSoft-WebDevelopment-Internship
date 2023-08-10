#HTML CODE
**********************************************************************************************
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>Basic Calculator</title>
  </head>
  <!--Made By Aditya Konda (Task 3 Level 1) Hope it Helps You-->
  <body>
    <div class="calculator">
      <div class="boxer" id="boxer">Calculator</div>
      <div class="display" id="display">0</div>
      <button class="btn" id="clear">C</button>
      <button class="btn" id="backspace">←</button>
      <button class="btn" id="divide">/</button>
      <button class="btn" id="multiply">*</button>
      <button class="btn" id="7">7</button>
      <button class="btn" id="8">8</button>
      <button class="btn" id="9">9</button>
      <button class="btn" id="subtract">-</button>
      <button class="btn" id="6">6</button>
      <button class="btn" id="5">5</button>
      <button class="btn" id="4">4</button>
      <button class="btn" id="decimal">.</button>
      <button class="btn" id="1">1</button>
      <button class="btn" id="2">2</button>
      <button class="btn" id="3">3</button>
      <button class="btn" id="add">+</button>
      <button class="btn" id="0">0</button>
      <button class="btn" id="equals">=</button>

      <div class="display2" id="display2">
        Made By Aditya Konda For CodSoft Web Development Internship Level 1:-
        Task 3
      </div>
    </div>
    <script src="script.js"></script>
  </body>
</html>
********************************************************************************************
# CSS CODE

body {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  margin: 0;
  background-color: #f0f0f0;
  font-family: Arial, sans-serif;
}

.calculator {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 10px;
  max-width: 300px;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

.display {
  grid-column: 1 / -1;
  text-align: right;
  padding: 10px;
  font-size: 24px;
  background-color: #f0f0f0;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.display2 {
  grid-column: 1 / -1;
  text-align: left;
  padding: 5px;
  font-size: 15px;
  background-color: aquamarine;
  border: 1px solid black;
  border-radius: 5px;
}

.btn {
  padding: 10px;
  font-size: 20px;
  text-align: center;
  background-color: #eee;
  border: 1px solid #ccc;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.btn:hover {
  background-color: #ddd;
}

.about {
  text-align: center;
}
*********************************************************************************************
# JAVASCRIPT CODE

document.addEventListener("DOMContentLoaded", function () {
  const display = document.getElementById("display");
  let currentInput = "0";
  let currentOperator = "";
  let prevInput = "";

  function updateDisplay() {
    display.textContent = currentInput;
  }

  function handleDigitClick(digit) {
    if (
      currentInput === "0" ||
      currentInput === "Infinity" ||
      currentInput === "-Infinity"
    ) {
      currentInput = digit;
    } else {
      currentInput += digit;
    }
    updateDisplay();
  }

  function handleOperatorClick(operator) {
    prevInput = currentInput;
    currentInput = "0";
    currentOperator = operator;
  }

  function handleEqualsClick() {
    const prev = parseFloat(prevInput);
    const current = parseFloat(currentInput);

    switch (currentOperator) {
      case "+":
        currentInput = prev + current;
        break;
      case "-":
        currentInput = prev - current;
        break;
      case "*":
        currentInput = prev * current;
        break;
      case "/":
        currentInput = prev / current;
        break;
    }

    currentOperator = "";
    prevInput = "";
    updateDisplay();
  }

  function clear() {
    currentInput = "0";
    currentOperator = "";
    prevInput = "";
    updateDisplay();
  }

  // Add event listeners to digit buttons
  for (let i = 0; i <= 9; i++) {
    document.getElementById(i.toString()).addEventListener("click", () => {
      handleDigitClick(i.toString());
    });
  }

  // Add event listeners to operator buttons
  document
    .getElementById("add")
    .addEventListener("click", () => handleOperatorClick("+"));
  document
    .getElementById("subtract")
    .addEventListener("click", () => handleOperatorClick("-"));
  document
    .getElementById("multiply")
    .addEventListener("click", () => handleOperatorClick("*"));
  document
    .getElementById("divide")
    .addEventListener("click", () => handleOperatorClick("/"));

  // Add event listeners to other buttons
  document.getElementById("decimal").addEventListener("click", () => {
    if (!currentInput.includes(".")) {
      currentInput += ".";
      updateDisplay();
    }
  });

  document
    .getElementById("equals")
    .addEventListener("click", handleEqualsClick);
  document.getElementById("clear").addEventListener("click", clear);

  document.getElementById("backspace").addEventListener("click", () => {
    currentInput = currentInput.slice(0, -1);
    if (currentInput === "") {
      currentInput = "0";
    }
    updateDisplay();
  });

  updateDisplay();
});
**************************************************************************************************
