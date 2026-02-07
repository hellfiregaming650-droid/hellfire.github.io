<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body, html {
            margin: 0;
            padding: 0;
            height: 100%;
            width: 100%;
            overflow: hidden;
            background-color: white;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        /* Overlay for Autoplay Workaround */
        #startOverlay {
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: white;
            z-index: 100;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
        }

        .container {
            position: relative;
            z-index: 10;
            text-align: center;
            background: rgba(255, 255, 255, 0.9);
            padding: 50px;
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(255, 77, 109, 0.2);
        }

        h1 {
            color: #ff4d6d;
            font-size: 3rem;
            margin-bottom: 40px;
            text-shadow: 2px 2px #ffe5ec;
        }

        .buttons {
            display: flex;
            gap: 30px;
            justify-content: center;
            align-items: center;
        }

        button {
            padding: 15px 40px;
            font-size: 1.5rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
            font-weight: bold;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
            box-shadow: 0 5px 15px rgba(255, 77, 109, 0.4);
        }

        #noBtn {
            background-color: #adb5bd;
            color: white;
            position: relative;
        }

        /* Falling Hearts Animation */
        .heart {
            position: fixed;
            top: -10px;
            color: #ff4d6d;
            font-size: 20px;
            user-select: none;
            z-index: 1;
            animation: fall linear forwards;
        }

        @keyframes fall {
            to {
                transform: translateY(105vh) rotate(360deg);
            }
        }
    </style>
</head>
<body>

    <div id="startOverlay" onclick="startSurprise()">
        <h2 style="color: #ff4d6d;">Click to open your surprise... ❤️</h2>
    </div>

    <div class="container">
        <h1>Will you be my valentine? ❤️</h1>
        <div class="buttons">
            <button id="yesBtn" onclick="celebrate()">Yes</button>
            <button id="noBtn" onmouseover="moveButton()">No</button>
        </div>
    </div>

    <audio id="bgMusic" loop>
        <source src="https://www.myinstants.com/media/sounds/charlie-puth-one-call-away-lyrics.mp3" type="audio/mpeg">
    </audio>

    <script>
        function startSurprise() {
            document.getElementById('startOverlay').style.display = 'none';
            document.getElementById('bgMusic').play();
            setInterval(createHeart, 300);
        }

        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerHTML = '❤️';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 2 + 's';
            heart.style.opacity = Math.random();
            heart.style.fontSize = Math.random() * 20 + 10 + 'px';
            
            document.body.appendChild(heart);
            
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        function moveButton() {
            const btn = document.getElementById('noBtn');
            const x = Math.random() * (window.innerWidth - btn.offsetWidth);
            const y = Math.random() * (window.innerHeight - btn.offsetHeight);
            
            btn.style.position = "fixed";
            btn.style.left = x + 'px';
            btn.style.top = y + 'px';
        }

        function celebrate() {
            alert("I'm only one call away! See you on Valentine's Day! ❤️😘");
            // You can add a redirect here if you want
        }
    </script>
</body>
</html>
