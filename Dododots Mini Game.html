<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Dododots Catch Game</title>

<style>
    body {
        margin: 0;
        background-color: #4a0e2e;
        font-family: Arial, sans-serif;
        color: white;
        overflow: hidden;
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100vh;
        user-select: none;
    }

    #game-canvas {
        position: relative;
        width: 100%;
        height: 100%;
        overflow: hidden;
    }

    .header {
        position: absolute;
        top: 20px;
        width: 100%;
        display: flex;
        justify-content: space-around;
        font-size: 28px;
        font-weight: bold;
        z-index: 10;
    }

    .mascot {
        position: absolute;
        width: 120px;
        height: 120px;
        background-image: url("mascot.png");
        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        cursor: pointer;
        animation: appear 1.9s linear forwards;
    }

    .bomb {
        position: absolute;
        width: 100px;
        height: 100px;
        background-color: #222;
        border-radius: 50%;
        cursor: pointer;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 50px;
        animation: appear 1.9s linear forwards;
    }

    @keyframes appear {
        0% { transform: scale(0.5); opacity: 0; }
        20% { opacity: 1; transform: scale(1.1); }
        80% { opacity: 1; transform: scale(1); }
        100% { opacity: 0; transform: translateY(-30px); }
    }

    #overlay {
        position: fixed;
        background: rgba(74, 14, 46, 0.95);
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        z-index: 100;
        text-align: center;
    }

    button {
        background: #ffb7c5;
        border: none;
        padding: 20px 40px;
        font-size: 24px;
        border-radius: 50px;
        color: #4a0e2e;
        font-weight: bold;
        cursor: pointer;
        margin-top: 20px;
    }
</style>
</head>

<body>
<div class="header">
    <div>Score: <span id="score">0</span></div>
    <div>Time: <span id="timer">30</span>s</div>
</div>

<div id="game-canvas"></div>

<div id="overlay">
    <h1 id="title">CATCH DODODOTS!</h1>
    <p id="result">Catch the mascot. Avoid the bombs!</p>
    <button onclick="startGame()">START GAME</button>
</div>

<script>
let score = 0;
let timeLeft = 30;
let gameActive = false;

const canvas = document.getElementById("game-canvas");
const scoreDisplay = document.getElementById("score");
const timerDisplay = document.getElementById("timer");
const overlay = document.getElementById("overlay");

function startGame() {
    score = 0;
    timeLeft = 30;
    gameActive = true;

    scoreDisplay.innerText = score;
    timerDisplay.innerText = timeLeft;
    overlay.style.display = "none";

    const timerInterval = setInterval(() => {
        timeLeft--;
        timerDisplay.innerText = timeLeft;
        if (timeLeft <= 0) endGame("Time's Up!");
    }, 1000);

    spawnItems();
    window.stopTimer = () => clearInterval(timerInterval);
}

function spawnItems() {
    if (!gameActive) return;

    // Randomly decide how many mascots to spawn (2-4)
    const mascotCount = Math.floor(Math.random() * 3) + 2; // 2,3,4
    for (let i = 0; i < mascotCount; i++) {
        const isBomb = Math.random() > 0.8; // 20% chance bomb
        const item = document.createElement("div");
        item.className = isBomb ? "bomb" : "mascot";
        if (isBomb) item.innerHTML = "💣";

        const x = Math.random() * (window.innerWidth - 150);
        const y = 100 + Math.random() * (window.innerHeight - 250);

        item.style.left = x + "px";
        item.style.top = y + "px";

        item.onclick = () => {
            if (!gameActive) return;
            if (isBomb) {
                endGame("BOOM! You hit a bomb!");
            } else {
                score++;
                scoreDisplay.innerText = score;
                item.remove();
            }
        };

        canvas.appendChild(item);

        setTimeout(() => item.remove(), 1900);
    }

    // Spawn next batch every 1 second
    setTimeout(spawnItems, 1000);
}

function endGame(msg) {
    gameActive = false;
    window.stopTimer();
    overlay.style.display = "flex";
    document.getElementById("title").innerText = msg;
    document.getElementById("result").innerText = "Final Score: " + score;
    canvas.innerHTML = "";
}
</script>
</body>
</html>
