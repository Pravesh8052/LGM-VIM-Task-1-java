# LGM-VIM-Task-1-java
#letsgrowmore  #LGMVIP
//currency.java

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

