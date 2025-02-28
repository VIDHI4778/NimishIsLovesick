
<html lang="en"
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            background-color: #ffced6;
            color: #800000;
        }
        #proof {
            font-size: 24px;
            margin-top: 30px;
            font-weight: bold;
        }
        button {
            font-size: 18px;
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
            "saying, very achi ladis, meri favorite ladis, ladis i want to cuddle ke union mein sirf 1 element hai (🥺) ",
            "Abe Sahi hai Mere pet mein aur per mein dard ho gaya, Warna merko koi dikkat ni hoti I love you bolne mein ", 
             "Sweetheart (🥺) ",
            "Tu is just,Made for me",
            "merko toh pata bhi ni tha ki itna saara wuv kar bhi sakta hoon mai kisi ko 🥺",
            "merko only tere haath pasand hai (🙈) ",
             "Shit, Mujhe keeda hona tha ",
            "wuv uuu me is very lucky tu fren hai meri", 
            "Main Kahu ki Chini ke badle cuddles dene padege toh tu mana karega???? 😭 ... Dushman: Nahi actually (🙊)",
            "06/09, 6:39 pm Dushman: kal mera very saara time,tujhe stare karne mein gaya hai",
          "aur woh photo dekh kar merko lagta hai ki yeh meri hai?? yeh??? really?? yeh ladis??? itni sundar??? mai itna lucky thodi ho sakta hoon?? yeh real hai??",
           "mai kabhi pink saree pehnta mai toh jarur deta terko gaal pe kiss 😔",
          "Vidhi Sharma: How does pure frenship wala emotion feel like?               Dushman: very very relaxing sa (🥺)", 
          "PHEROMONES!!", 
            "Tu mere liye bas ek bhog ka vishya nahi hai!! Tu is meri vidhii, merko teri company very achi lagti, tu is woh jisse mai ache se baat kar sakta hoon (soft puppy ki tarah bhi)",
"Aur kuch bhii ho, mai can rely on youu",];
const gifProofs = [
            "https://tenor.com/bOPLQ.gif", 
        ];
         function showProof() {
            const proofText = document.getElementById("proof");}
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

    // Define words and their corresponding links
    const secretLinks = {
        "MY PLAYLIST": "https://music.youtube.com/playlist?list=PLzycAjKA4ki5HMCriZtosGnW5r4F9T81F&si=xqK2a7i9Xuk9MMqu",
          "HER PLAYLIST": "https://music.youtube.com/playlist?list=PL_wKRdAu_N2ycFIiVLoVSl0zSPTutGCgW&si=miCKkKvILMNbWAr3",  
        "GIFTSS": "https://docs.google.com/spreadsheets/d/1b8cgUfu9qa9HST7Zb6AMVNH2dBaAVUGAKBlJ-ztbJKA/edit?gid=0#gid=0"
    };

    // Check if the input matches any secret words
    if (secretLinks[input]) {
        window.location.href = secretLinks[input]; // Redirect to the corresponding link
    }
}
    </script>
</body>
</html>
