<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Cake</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
        .cake {
            position: relative;
            width: 200px;
            height: 200px;
            margin: 0 auto;
            background: pink;
            border-radius: 10px;
            box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
            cursor: pointer;
        }
        .cake:after {
            content: "";
            position: absolute;
            top: -20px;
            left: 50%;
            width: 0;
            height: 0;
            border-left: 20px solid transparent;
            border-right: 20px solid transparent;
            border-bottom: 20px solid pink;
            transform: translateX(-50%);
        }
        .candles {
            position: absolute;
            top: -20px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 5px;
        }
        .candle {
            width: 5px;
            height: 20px;
            background: yellow;
            border-radius: 2px;
        }
    </style>
</head>
<body>
    <h1>🎂 Birthday Cake 🎂</h1>
    <p>Enter your age to light the candles:</p>
    <input type="number" id="ageInput" min="1" placeholder="Enter your age" />
    <button onclick="addCandles()">Add Candles</button>
    <div class="cake" onclick="sayHappyBirthday()">
        <div id="candles" class="candles"></div>
    </div>

    <script>
        function addCandles() {
            const age = document.getElementById("ageInput").value;
            const candlesDiv = document.getElementById("candles");

            // Clear existing candles
            candlesDiv.innerHTML = "";

            // Add candles based on the entered age
            for (let i = 0; i < age; i++) {
                const candle = document.createElement("div");
                candle.className = "candle";
                candlesDiv.appendChild(candle);
            }
        }

        function sayHappyBirthday() {
            alert("Happy Birthday Malika!");
        }
    </script>
</body>
</html>
