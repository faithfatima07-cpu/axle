<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>For Axle 💙</title>
    <style>
        body {
            margin: 0;
            height: 100vh;
            font-family: 'Comic Sans MS', cursive;
            background: linear-gradient(135deg, #cce7ff, #e6f2ff);
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }

        .container {
            text-align: center;
            background: white;
            padding: 40px;
            border-radius: 25px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
            position: relative;
        }

        h1 {
            color: #4a90e2;
            margin-bottom: 15px;
        }

        .rabbits {
            font-size: 48px;
            margin-bottom: 15px;
        }

        button {
            font-size: 18px;
            padding: 12px 30px;
            border-radius: 30px;
            border: none;
            cursor: pointer;
            transition: 0.2s;
        }

        #yesBtn {
            background-color: #4a90e2;
            color: white;
            margin-right: 20px;
        }

        #noBtn {
            background-color: #ffb6c1;
            color: #333;
            position: absolute;
        }

        button:hover {
            transform: scale(1.1);
        }
    </style>
</head>
<body>

<div class="container">
    <div class="rabbits">🐰💙🐰</div>
    <h1>Will you be my Valentine, <br>Axle?</h1>

    <button id="yesBtn" onclick="goToLetter()">Yes 💖</button>
    <button id="noBtn" onmouseover="moveNo()">No 😅</button>
</div>

<!-- Background Music -->
<audio id="bgMusic" src="tahanan.mp3"></audio>

<script>
    const noBtn = document.getElementById("noBtn");
    const music = document.getElementById("bgMusic");

    function moveNo() {
        const x = Math.random() * (window.innerWidth - noBtn.offsetWidth);
        const y = Math.random() * (window.innerHeight - noBtn.offsetHeight);

        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    function goToLetter() {
        music.play();

        document.body.innerHTML = `
            <div style="
                height: 100vh;
                display: flex;
                justify-content: center;
                align-items: center;
                background: linear-gradient(135deg, #cce7ff, #e6f2ff);
                font-family: 'Comic Sans MS', cursive;
            ">
                <div style="
                    background: white;
                    padding: 50px;
                    border-radius: 25px;
                    max-width: 520px;
                    text-align: center;
                    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
                ">
                    <h2 style="color:#4a90e2;">💌 For Axle 💌</h2>
                    <p style="font-size:18px; color:#333;">
                        (Write your letter here 💙)
                    </p>
                    <p style="margin-top:25px; font-weight:bold;">
                        — From Loki 🐰💙
                    </p>
                </div>
            </div>
        `;
    }
</script>

</body>
</html>

