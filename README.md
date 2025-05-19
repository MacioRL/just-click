<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Just Click</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 100px;
    }

    button {
      font-size: 20px;
      padding: 10px 20px;
    }

    #counter {
      margin-top: 20px;
      font-size: 24px;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Just Click</h1>
  <button onclick="addClick()">Click</button>
  <div id="counter">Clicks: 0</div>

  <script>
    // Get stored counter value from localStorage
    let counter = localStorage.getItem("clicks");
    if (counter === null) {
      counter = 0;
    } else {
      counter = parseInt(counter);
    }

    // Show initial value
    document.getElementById("counter").innerText = "Clicks: " + counter;

    function addClick() {
      counter++;
      document.getElementById("counter").innerText = "Clicks: " + counter;
      localStorage.setItem("clicks", counter);
    }
  </script>
</body>
</html>
