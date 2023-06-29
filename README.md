# LGM-VIM-Task-1-java
#letsgrowmore  #LGMVIP

*//currency.html//

<!DOCTYPE html>
<html>
<head>
  <title>Currency Converter</title>
  <link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
  <h1>Currency Converter</h1>
  <div class="converter">
    <input type="number" id="amount" placeholder="Enter Amount">
    <select id="fromCurrency">
      <option value="USD">USD</option>
      <option value="EUR">EUR</option>
      <option value="GBP">GBP</option>
    </select>
    <select id="toCurrency">
      <option value="USD">USD</option>
      <option value="EUR">EUR</option>
      <option value="GBP">GBP</option>
    </select>
    <button onclick="convertCurrency()">Convert</button>
    <p id="result"></p>
  </div>
  <script src="script.js"></script>
</body>
</html>

**//style.css//
body {
  font-family: Arial, sans-serif;
  text-align: center;
}

h1 {
  color: #333;
}

.converter {
  margin-top: 50px;
}

input[type="number"] {
  width: 150px;
  padding: 5px;
}

select {
  width: 80px;
  padding: 5px;
}

button {
  padding: 5px 15px;
  background-color: #4CAF50;
  color: white;
  border: none;
  cursor: pointer;
}

#result {
  margin-top: 20px;
  font-weight: bold;
}


***//script.js//
function convertCurrency() {
  var amount = document.getElementById("amount").value;
  var fromCurrency = document.getElementById("fromCurrency").value;
  var toCurrency = document.getElementById("toCurrency").value;
  var resultElement = document.getElementById("result");

  // Perform the currency conversion logic here
  // You can use APIs or predefined conversion rates for different currencies

  // Example conversion rates (1 USD = 0.85 EUR, 1 USD = 0.74 GBP)
  var conversionRates = {
    USD: {
      EUR: 0.85,
      GBP: 0.74
    },
    EUR: {
      USD: 1.18,
      GBP: 0.87
    },
    GBP: {
      USD: 1.35,
      EUR: 1.15
    }
  };

  var convertedAmount = amount * conversionRates[fromCurrency][toCurrency];
  resultElement.innerText = convertedAmount.toFixed(2) + " " + toCurrency;
}

