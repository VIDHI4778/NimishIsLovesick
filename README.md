<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            background-color: #ffcccb;
            color: #800000;
        }
        #proof {
            font-size: 24px;
            margin-top: 30px;
            font-weight: bold;
        }
        button {
            font-size: 20px;
            padding: 10px 20px;
            background-color: #ff6666;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            margin-top: 40px;
        }
        button:hover {
            background-color: #B57EDC;
        }
        #love-meter {
            width: 100%;
            max-width: 300px;
            height: 20px;
            background-color: #FFFFFF;
            border-radius: 10px;
            margin: 40px auto;
            overflow: hidden;
        
        }
        #love-meter-fill {
            height: 100%;
            width: 0%;
            background-color: #B57EDC;
            transition: width 0.5s ease-in-out;
        }
    </style>
</head>
<body>
    <h1>Nimish Is Lovesick!!</h1>
    <p>Click the button to receive a proof of lovesickness:</p>
    <button onclick="showProof()">Get Proof</button>
    <p id="proof"></p>
    
    <div id="love-meter">
        <div id="love-meter-fill"></div>
    </div>
    
    <input type="text" id="secretInput" placeholder="Type here..." oninput="checkSecret()">
    
    <script>
        const proofs = [
            "Blushing whenever *their* name is mentioned! 🥺",
            "Randomly smiling at their texts like a fool! 🥺",
            "Heart skipping a beat when they reply fast! 🥺",
            "Thinking about them even while debugging code! 🥺",
            "Daydreaming mid-conversation and forgetting what was said! 🥺",
            "Checking their last seen, but pretending not to care! 🥺",
            "Feeling butterflies just by seeing their profile picture! 🥺"
        ];
        let loveMeter = 0;
        let currentIndex = 0;

        function showProof() {
            if (currentIndex < proofs.length) {
                document.getElementById("proof").innerText = proofs[currentIndex];
                currentIndex++;
                loveMeter = (currentIndex / proofs.length) * 100;
                document.getElementById("love-meter-fill").style.width = loveMeter + "%";
            }

            if (loveMeter >= 100) {
                setTimeout(() => {
                    alert("Critical lovesickness detected! Immediate attention required! 💘");
                }, 500);
            }
        }

        function checkSecret() {
            const input = document.getElementById("secretInput").value.toUpperCase();
            const secretWords = ["NIMISH", "VIDHI", "FREN", "YES", "I AM LOVESICK"];
            if (secretWords.includes(input)) {
                window.location.href = "https://xyz.com"; // Replace xyz.com with your actual link
            }
        }
    </script>
</body>
</html>
