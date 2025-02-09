
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Nimish Is Lovesick</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            background-color: #ffebf0;
        }
        #proof {
            font-size: 24px;
            margin-top: 20px;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            background-color: #ff4d79;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
        }
        button:hover {
            background-color: #e63963;
        }
    </style>
</head>
<body>
    <p>Click the button to get a proof of your lovesickness:</p>
    <button onclick="SendWuv()">Get Proof</button>
    <p id="proof"></p>
    
    <script>
        const proofsOfLovesickness = [
            "You sighed at their name again!",
            "Daydreaming about them, aren't you?",
            "You re-read their messages 5 times today!",
            "Their favorite song is suddenly your favorite too!",
            "You pretend to be busy, just to be around them!"
        ];

        function SendWuv() {
            const randomIndex = Math.floor(Math.random() * proofsOfLovesickness.length);
            document.getElementById("proof").innerText = proofsOfLovesickness[randomIndex] + " 🥺";
        }
    </script>
</body>
</html>
