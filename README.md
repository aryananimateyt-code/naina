# naina
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Chocolate Day, Kareja! ❤️</title>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;700&family=Poppins:wght@300;400&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(to bottom, #ffe6f2, #ffb3d9, #ff69b4);
            color: #d63384;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden;
            position: relative;
        }
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-image: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><circle cx="50" cy="50" r="2" fill="%23ff1493" opacity="0.1"/><circle cx="20" cy="20" r="1" fill="%23dc143c" opacity="0.1"/><circle cx="80" cy="80" r="1.5" fill="%23ffa500" opacity="0.1"/></svg>');
            background-size: 50px 50px;
            pointer-events: none;
            z-index: -1;
        }
        .page {
            display: none;
        }
        .page.active {
            display: block;
        }
        .intro {
            padding-top: 200px;
        }
        .intro h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 4em;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.3);
            animation: pulse 2s infinite;
        }
        .intro p {
            font-size: 1.5em;
            margin: 20px;
        }
        .button {
            background: linear-gradient(45deg, #ff69b4, #ff1493);
            color: white;
            border: none;
            padding: 20px 40px;
            font-size: 1.5em;
            font-family: 'Dancing Script', cursive;
            border-radius: 50px;
            cursor: pointer;
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        .button::before {
            content: '💖';
            position: absolute;
            top: 10px;
            left: 20px;
            font-size: 1.2em;
        }
        .button::after {
            content: '🌹';
            position: absolute;
            top: 10px;
            right: 20px;
            font-size: 1.2em;
        }
        .button:hover {
            transform: scale(1.1);
            box-shadow: 0 15px 30px rgba(0,0,0,0.4);
        }
        .button:active {
            transform: scale(0.95);
        }
        .main h1 {
            font-family: 'Dancing Script', cursive;
            font-size: 4em;
            margin-top: 50px;
            text-shadow: 3px 3px 6px rgba(0,0,0,0.3);
            animation: pulse 2s infinite;
        }
        .main p {
            font-size: 1.5em;
            margin: 20px;
            line-height: 1.6;
            animation: fadeIn 3s ease-in;
        }
        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        .message {
            max-width: 700px;
            margin: 0 auto;
            padding: 30px;
            background: rgba(255, 255, 255, 0.9);
            border-radius: 20px;
            box-shadow: 0 0 20px rgba(0,0,0,0.2);
            border: 2px solid #ff69b4;
            position: relative;
        }
        .message::before {
            content: '💖';
            position: absolute;
            top: -10px;
            left: -10px;
            font-size: 2em;
        }
        .message::after {
            content: '💖';
            position: absolute;
            bottom: -10px;
            right: -10px;
            font-size: 2em;
        }
        .emojis {
            font-size: 2.5em;
            margin: 20px 0;
            animation: bounce 2s infinite;
        }
        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }
        .floating {
            position: absolute;
            font-size: 2.5em;
            animation: float 12s linear infinite;
            pointer-events: none;
            z-index: 1;
        }
        @keyframes float {
            0% { bottom: -50px; opacity: 1; transform: rotate(0deg); }
            100% { bottom: 100vh; opacity: 0; transform: rotate(360deg); }
        }
        .heart { color: #ff1493; }
        .rose { color: #dc143c; }
        .cat { color: #ffa500; }
        .chocolate { color: #8b4513; }
        .star { color: #ffd700; }
        .kiss { color: #ff69b4; }
        .reveal-button {
            background: linear-gradient(45deg, #ff69b4, #ff1493);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 1.2em;
            border-radius: 25px;
            cursor: pointer;
            margin-top: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            transition: transform 0.3s;
        }
        .reveal-button:hover {
            transform: scale(1.1);
        }
        .hidden {
            display: none;
        }
        .image-container {
            margin: 20px 0;
        }
        .image-container img {
            width: 150px;
            height: auto;
            border-radius: 15px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
    </style>
</head>
<body>
    <!-- Intro Page -->
    <div id="intro" class="page active intro">
        <h1>Welcome to a Sweet Surprise! 🍫❤️</h1>
        <p>Hey Kareja, are you ready for some chocolatey romance? Click the button below to enter the magical world of love! 🌹🐱</p>
        <button class="button" onclick="showMain()">Open Your Heart 💖🌹</button>

        <!-- Floating Emojis on Intro Page -->
        <div class="floating heart" style="left: 10%; animation-delay: 0s;">❤️</div>
        <div class="floating rose" style="left: 20%; animation-delay: 1s;">🌹</div>
        <div class="floating cat" style="left: 30%; animation-delay: 2s;">🐱</div>
        <div class="floating chocolate" style="left: 40%; animation-delay: 3s;">🍫</div>
        <div class="floating star" style="left: 50%; animation-delay: 4s;">🌟</div>
        <div class="floating kiss" style="left: 60%; animation-delay: 5s;">😘</div>
        <div class="floating heart" style="left: 70%; animation-delay: 6s;">💕</div>
        <div class="floating rose" style="left: 80%; animation-delay: 7s;">🌸</div>
        <div class="floating cat" style="left: 90%; animation-delay: 8s;">😺</div>
    </div>

    <!-- Main Page -->
    <div id="main" class="page main">
        <h1>Happy Chocolate Day, Kareja! ❤️🌹🐱🍫</h1>
        <div class="message">
            <p>Dear Naina, my sweet Kareja,</p>
            <p>Today is Chocolate Day, and I wanted to share something sweeter than any chocolate in the world – my love for you! 🌟 You are the light of my life, the beat of my heart, and the reason I smile every day. 💖</p>
            <p>You are everything to me, Kareja. My dreams, my happiness, my forever. Every moment with you is magical, and I cherish you more than words can express. You make my world colorful and full of joy. 😍</p>
            <p>Here's to sharing chocolates, stealing kisses, and creating endless memories together! I like you endlessly, my love. 😘</p>
            <p>And my dearest Kareja, I’m sorry if I couldn’t do what you told me, but for you, I’ll always try my hardest — because you mean everything to me. 🫀💕</p>
            <p>With all my heart,<br>Your Devoted Admirer 💕</p>
            <div class="image-container">
                <img src="https://via.placeholder.com/150x150/ff69b4/ffffff?text=🍫" alt="Chocolate">
                <img src="https://via.placeholder.com/150x150/dc143c/ffffff?text=🌹" alt="Rose">
                <img src="https://via.placeholder.com/150x150/ffa500/ffffff?text=🐱" alt="Cat">
            </div>
            <div class="emojis">
                ❤️ 🌹 🐱 💕 🌸 😺 💖 🌷 🐾 🍫 💗
            </div>
            <button class="reveal-button" onclick="revealMore()">Click for a Special Surprise! 🎁</button>
            <div id="surprise" class="hidden">
                <p>Just a little extra: You are my favorite person, Kareja. Thinking of you makes my day brighter! 🌈💞</p>
                <div class="emojis">😻❤️🌹🐾🍫</div>
            </div>
        </div>

        <!-- Floating Emojis on Main Page -->
        <div class="floating heart" style="left: 5%; animation-delay: 0s;">❤️</div>
        <div class="floating rose" style="left: 15%; animation-delay: 1s;">🌹</div>
        <div class="floating cat" style="left: 25%; animation-delay: 2s;">🐱</div>
        <div class="floating heart" style="left: 35%; animation-delay: 3s;">💖</div>
        <div class="floating rose" style="left: 45%; animation-delay: 4s;">🌸</div>
        <div class="floating cat" style="left: 55%; animation-delay: 5s;">😺</div>
        <div class="floating heart" style="left: 65%; animation-delay: 6s;">💕</div>
        <div class="floating rose" style="left: 75%; animation-delay: 7s;">🌷</div>
        <div class="floating cat" style="left: 85%; animation-delay: 8s;">🐾</div>
        <div class="floating chocolate" style="left: 10%; animation-delay: 9s;">🍫</div>
        <div class="floating star" style="left: 20%; animation-delay: 10s;">🌟</div>
        <div class="floating kiss" style="left: 30%; animation-delay: 11s;">😘</div>
        <div class="floating heart" style="left: 40%; animation-delay: 12s;">❤️</div>
        <div class="floating rose" style="left: 50%; animation-delay: 13s;">🌹</div>
        <div class="floating cat" style="left: 60%; animation-delay: 14s;">🐱</div>
        <div class="floating heart" style="left: 70%; animation-delay: 15s;">💖</div>
        <div class="floating rose" style="left: 80%; animation-delay: 16s;">🌸</div>
        <div class="floating cat" style="left: 90%; animation-delay: 17s;">😺</div>
        <div class="floating chocolate" style="left: 95%; animation-delay: 18s;">🍫</div>
        <div class="floating star" style="left: 12%; animation-delay: 19s;">🌟</div>
        <div class="floating kiss" style="left: 22%; animation-delay: 20s;">😘</div>
        <div class="floating heart" style="left: 32%; animation-delay: 21s;">💕</div>
        <div class="floating rose" style="left: 42%; animation-delay: 22s;">🌷</div>
        <div class="floating cat" style="left: 52%; animation-delay: 23s;">🐾</div>
        <div class="floating chocolate" style="left: 62%; animation-delay: 24s;">🍫</div>
        <div class="floating star" style="left: 72%; animation-delay: 25s;">🌟</div>
        <div class="floating kiss" style="left: 82%; animation-delay: 26s;">😘</div>
        <div class="floating heart" style="left: 92%; animation-delay: 27s;">❤️</div>
    </div>

    <script>
        function showMain() {
            document.getElementById('intro').classList.remove('active');
            document.getElementById('main').classList.add('active');
        }

        function revealMore() {
            const surprise = document.getElementById('surprise');
            surprise.classList.toggle('hidden');
        }

        // Create more dynamic floating emojis
        function createFloatingEmoji(emoji, colorClass) {
            const div = document.createElement('div');
            div.className = `floating ${colorClass}`;
            div.textContent = emoji;
            div.style.left = Math.random() * 100 + '%';
            div.style.animationDelay = Math.random() * 10 + 's';
            document.body.appendChild(div);
            setTimeout(() => div.remove(), 12000);
        }

        // Add new floating emojis periodically
        setInterval(() => {
            const emojis = ['❤️', '🌹', '🐱', '💖', '🌸', '😺', '💕', '🌷', '🐾', '🍫', '🌟', '😘'];
            const colors = ['heart', 'rose', 'cat', 'chocolate', 'star', 'kiss'];
            const randomEmoji = emojis[Math.floor(Math.random() * emojis.length)];
            const randomColor = colors[Math.floor(Math.random() * colors.length)];
            createFloatingEmoji(randomEmoji, randomColor);
        }, 1500);
    </script>
</body>
</html>
