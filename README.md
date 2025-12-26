# Manishaaa-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For [Her Name]</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <audio autoplay loop>
        <source src="music.mp3" type="audio/mpeg">
    </audio>

    <section id="home">
        <h1>Hi [Her Name] 💛</h1>
        <p>This is a little something about how amazing you are…</p>
    </section>

    <section id="qualities">
        <h2>Your Amazing Qualities 🌸</h2>
        <ul>
            <li>Beautiful smile</li>
            <li>Kind heart</li>
            <li>Innocent & cute</li>
            <li>Talented and hardworking</li>
        </ul>
    </section>

    <section id="countdown">
        <h2>Birthday Countdown 🎂</h2>
        <div id="timer"></div>
    </section>

    <script src="script.js"></script>
</body>
</html>body {
    font-family: 'Comic Sans MS', cursive, sans-serif;
    text-align: center;
    background: linear-gradient(to bottom, #ffe6f0, #fff);
    color: #333;
    overflow-x: hidden;
}

h1, h2 {
    color: #ff69b4;
}

ul {
    list-style: none;
}

#timer {
    font-size: 2em;
    color: #ff1493;
    margin-top: 20px;
}// Birthday countdown
const birthday = new Date("September 9, 2025 00:00:00").getTime();

const countdown = setInterval(() => {
    const now = new Date().getTime();
    const diff = birthday - now;

    const days = Math.floor(diff / (1000 * 60 * 60 * 24));
    const hours = Math.floor((diff % (1000 * 60 * 60 * 24)) / (1000*60*60));
    const minutes = Math.floor((diff % (1000 * 60 * 60)) / (1000*60));
    const seconds = Math.floor((diff % (1000 * 60)) / 1000);

    document.getElementById("timer").innerHTML = `${days}d ${hours}h ${minutes}m ${seconds}s`;

    if(diff < 0) {
        clearInterval(countdown);
        document.getElementById("timer").innerHTML = "Happy Birthday!";
    }
}, 1000);.tulip {
    position: absolute;
    top: -50px;
    width: 30px;
    animation: fall 5s linear infinite;
}

@keyframes fall {
    to {
        transform: translateY(100vh) rotate(360deg);
    }
}for(let i=0; i<20; i++){
    let tulip = document.createElement("img");
    tulip.src = "tulip.png"; // download a tulip PNG
    tulip.className = "tulip";
    tulip.style.left = Math.random()*100 + "vw";
    tulip.style.animationDuration = 3 + Math.random()*5 + "s";
    document.body.appendChild(tulip);
}<a href="qualities.html">Next ➡️</a>
