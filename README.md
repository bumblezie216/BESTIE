<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Liliana's Friendship Casino ♡</title>

<style>
* {
    box-sizing: border-box;
}

:root {
    --pink: #ff72ad;
    --hot-pink: #ff3f91;
    --soft-pink: #ffd6e8;
    --light-pink: #fff0f7;
    --burgundy: #5b1635;
    --deep: #160812;
    --panel: rgba(255,255,255,.09);
    --gold: #ffd36a;
    --text: #fff7fb;
    --muted: #dcb8c9;
}

body {
    margin: 0;
    font-family: Arial, Helvetica, sans-serif;
    color: var(--text);
    background:
        radial-gradient(circle at 20% 10%, rgba(255,114,173,.18), transparent 25%),
        radial-gradient(circle at 80% 20%, rgba(255,211,106,.12), transparent 22%),
        linear-gradient(135deg, #180914, #42132d 45%, #160812);
    min-height: 100vh;
}

button {
    font: inherit;
}

button:focus,
select:focus,
input:focus,
textarea:focus {
    outline: 3px solid rgba(255,211,106,.65);
    outline-offset: 2px;
}

.hidden {
    display: none !important;
}

.app {
    width: min(1200px, 94%);
    margin: auto;
    padding: 18px 0 50px;
}

/* HEADER */

.header {
    text-align: center;
    padding: 24px 10px;
}

.logo {
    font-size: clamp(28px, 7vw, 58px);
    font-weight: 900;
    letter-spacing: 2px;
    color: var(--soft-pink);
    text-shadow: 0 0 20px rgba(255,114,173,.45);
}

.subtitle {
    margin-top: 8px;
    color: var(--muted);
    letter-spacing: 2px;
    font-size: 13px;
}

.balance {
    display: inline-flex;
    align-items: center;
    gap: 12px;
    margin-top: 18px;
    padding: 12px 20px;
    border: 1px solid rgba(255,255,255,.16);
    border-radius: 999px;
    background: rgba(0,0,0,.25);
    font-weight: bold;
}

.coin {
    color: var(--gold);
    font-size: 20px;
}

/* NAV */

.nav {
    display: flex;
    gap: 8px;
    overflow-x: auto;
    padding: 8px 2px 15px;
    scrollbar-width: thin;
}

.nav button {
    flex: 0 0 auto;
    border: 1px solid rgba(255,255,255,.15);
    background: rgba(255,255,255,.06);
    color: white;
    padding: 11px 15px;
    border-radius: 12px;
    cursor: pointer;
    transition: .2s;
}

.nav button:hover,
.nav button.active {
    background: var(--pink);
    color: #240b18;
}

/* SECTIONS */

.section {
    display: none;
}

.section.active {
    display: block;
}

.panel {
    background: var(--panel);
    border: 1px solid rgba(255,255,255,.12);
    border-radius: 22px;
    padding: 22px;
    margin-bottom: 18px;
    backdrop-filter: blur(12px);
}

.section-title {
    font-size: 27px;
    margin: 0 0 6px;
}

.section-subtitle {
    color: var(--muted);
    margin: 0 0 22px;
}

/* HOME */

.game-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 15px;
}

.game-card {
    border: 1px solid rgba(255,255,255,.13);
    background: rgba(0,0,0,.18);
    border-radius: 18px;
    padding: 20px;
    cursor: pointer;
    transition: transform .2s, background .2s;
}

.game-card:hover {
    transform: translateY(-4px);
    background: rgba(255,114,173,.13);
}

.game-icon {
    font-size: 38px;
}

.game-card h3 {
    margin: 12px 0 7px;
}

.game-card p {
    color: var(--muted);
    font-size: 14px;
    line-height: 1.5;
}

/* BUTTONS */

.btn {
    border: 0;
    border-radius: 12px;
    padding: 12px 17px;
    background: var(--pink);
    color: #280a18;
    font-weight: 800;
    cursor: pointer;
    min-height: 44px;
    transition: .18s;
}

.btn:hover {
    transform: translateY(-2px);
    background: #ff9ac5;
}

.btn.secondary {
    background: rgba(255,255,255,.1);
    color: white;
}

.btn.gold {
    background: var(--gold);
}

.btn.danger {
    background: #c83d6f;
    color: white;
}

.actions {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
}

.message {
    min-height: 28px;
    margin-top: 16px;
    color: var(--soft-pink);
    font-weight: bold;
}

/* SLOT */

.slot-machine {
    max-width: 720px;
    margin: auto;
    text-align: center;
}

.reels {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
    margin: 25px 0;
}

.reel {
    background: #fff7fb;
    color: #30101f;
    border-radius: 18px;
    min-height: 105px;
    display: grid;
    place-items: center;
    font-size: 48px;
    border: 5px solid #e9a3bf;
    box-shadow: inset 0 0 15px rgba(0,0,0,.15);
}

.reel.spin {
    animation: spin .11s infinite linear;
}

@keyframes spin {
    0% { transform: translateY(-4px); }
    50% { transform: translateY(4px); }
    100% { transform: translateY(-4px); }
}

.slot-info {
    display: flex;
    justify-content: center;
    gap: 18px;
    flex-wrap: wrap;
    color: var(--muted);
}

/* CARDS */

.playing-card {
    width: 78px;
    height: 110px;
    border-radius: 12px;
    background: #fff;
    color: #24101a;
    display: grid;
    place-items: center;
    font-size: 29px;
    font-weight: bold;
    box-shadow: 0 7px 20px rgba(0,0,0,.3);
    user-select: none;
}

.playing-card.red {
    color: #d83264;
}

.card-row {
    display: flex;
    gap: 10px;
    flex-wrap: wrap;
    justify-content: center;
    margin: 20px 0;
}

.card-choice {
    cursor: pointer;
    transition: transform .2s;
}

.card-choice:hover {
    transform: translateY(-7px);
}

.card-back {
    background:
        repeating-linear-gradient(
            45deg,
            #ff72ad 0,
            #ff72ad 5px,
            #8d2452 5px,
            #8d2452 10px
        );
    color: white;
    border: 4px solid white;
}

/* POKER */

.player-area {
    text-align: center;
    margin: 18px 0 28px;
}

.player-label {
    color: var(--muted);
    margin-bottom: 10px;
    font-weight: bold;
}

.hold-card {
    cursor: pointer;
    position: relative;
}

.hold-card.held {
    transform: translateY(-14px);
    box-shadow: 0 0 0 3px var(--gold);
}

.hold-tag {
    position: absolute;
    bottom: -22px;
    font-size: 11px;
    color: var(--gold);
}

/* BLACKJACK */

.scoreboard {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
    margin: 15px 0;
}

.score {
    font-size: 24px;
    font-weight: bold;
}

/* WHEEL */

.wheel-wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 18px;
}

.wheel {
    width: min(300px, 75vw);
    aspect-ratio: 1;
    border-radius: 50%;
    border: 10px solid #ffd6e8;
    background:
        conic-gradient(
            #ff72ad 0deg 45deg,
            #8c2d57 45deg 90deg,
            #ffd36a 90deg 135deg,
            #d95487 135deg 180deg,
            #ff9ac5 180deg 225deg,
            #6d1c40 225deg 270deg,
            #ffd36a 270deg 315deg,
            #ff4d99 315deg 360deg
        );
    position: relative;
    transition: transform 3s cubic-bezier(.15,.75,.15,1);
}

.wheel::after {
    content: "♡";
    position: absolute;
    inset: 35%;
    display: grid;
    place-items: center;
    border-radius: 50%;
    background: #fff0f7;
    color: #8b2451;
    font-size: 34px;
    border: 5px solid #8b2451;
}

.pointer {
    font-size: 34px;
    transform: rotate(180deg);
}

/* DICE */

.dice-row {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin: 25px 0;
}

.die {
    width: 80px;
    height: 80px;
    background: white;
    color: #4a122b;
    border-radius: 15px;
    display: grid;
    place-items: center;
    font-size: 36px;
    font-weight: bold;
}

.rolling {
    animation: diceRoll .3s infinite;
}

@keyframes diceRoll {
    0% { transform: rotate(0deg); }
    50% { transform: rotate(12deg) scale(1.08); }
    100% { transform: rotate(-12deg); }
}

/* DOLPHIN */

.race {
    background: rgba(0,0,0,.2);
    border-radius: 16px;
    padding: 15px;
    overflow: hidden;
}

.track {
    position: relative;
    height: 52px;
    border-bottom: 1px dashed rgba(255,255,255,.25);
}

.dolphin {
    position: absolute;
    left: 0;
    top: 8px;
    font-size: 30px;
    transition: left 3s cubic-bezier(.15,.7,.2,1);
}

/* VAULT */

.vault {
    max-width: 650px;
    margin: auto;
    text-align: center;
}

.locks {
    display: flex;
    justify-content: center;
    gap: 10px;
    margin: 25px 0;
}

.lock {
    width: 75px;
    height: 75px;
    display: grid;
    place-items: center;
    border-radius: 15px;
    background: rgba(0,0,0,.3);
    font-size: 35px;
    border: 1px solid rgba(255,255,255,.15);
}

/* PROFILE */

.profile {
    display: grid;
    grid-template-columns: 150px 1fr;
    gap: 25px;
    align-items: center;
}

.profile-avatar {
    width: 150px;
    aspect-ratio: 1;
    border-radius: 50%;
    background: linear-gradient(135deg, #ffb7d5, #ff5a9f);
    display: grid;
    place-items: center;
    font-size: 70px;
}

.facts {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 10px;
    margin-top: 18px;
}

.fact {
    background: rgba(255,255,255,.06);
    border-radius: 13px;
    padding: 13px;
}

.fact strong {
    display: block;
    color: var(--soft-pink);
    margin-bottom: 4px;
}

/* ACHIEVEMENTS */

.achievements {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
    gap: 12px;
}

.achievement {
    padding: 18px;
    border-radius: 15px;
    background: rgba(255,255,255,.05);
    border: 1px solid rgba(255,255,255,.08);
    opacity: .45;
}

.achievement.unlocked {
    opacity: 1;
    border-color: var(--gold);
    background: rgba(255,211,106,.08);
}

.achievement-icon {
    font-size: 32px;
}

/* QUIZ */

.quiz-option {
    display: block;
    width: 100%;
    text-align: left;
    margin: 8px 0;
    border: 1px solid rgba(255,255,255,.12);
    background: rgba(255,255,255,.06);
    color: white;
    padding: 14px;
    border-radius: 12px;
    cursor: pointer;
}

.quiz-option:hover {
    background: rgba(255,114,173,.18);
}

/* LETTER */

.letter {
    background: #fff0f7;
    color: #3b1227;
    padding: 30px;
    border-radius: 16px;
    line-height: 1.8;
    font-family: Georgia, serif;
}

/* RESPONSIVE */

@media (max-width: 650px) {
    .app {
        width: 94%;
    }

    .panel {
        padding: 16px;
    }

    .profile {
        grid-template-columns: 1fr;
        text-align: center;
    }

    .profile-avatar {
        margin: auto;
    }

    .playing-card {
        width: 58px;
        height: 84px;
        font-size: 22px;
    }

    .reel {
        min-height: 80px;
        font-size: 36px;
    }
}
</style>
</head>

<body>

<div class="app">

<header class="header">
    <div class="logo">LILIANA'S FRIENDSHIP CASINO ♡</div>
    <div class="subtitle">SIX YEARS OF FRIENDSHIP • ZERO REAL MONEY • JUST LUCK & MEMORIES</div>

    <div class="balance">
        <span class="coin">🪙</span>
        <span id="tokenBalance">6000</span>
        <span>Friendship Tokens</span>
    </div>
</header>

<nav class="nav">
    <button class="active" data-section="home">🎰 Casino</button>
    <button data-section="slots">🎰 Slots</button>
    <button data-section="poker">🃏 Poker</button>
    <button data-section="blackjack">♠️ Blackjack</button>
    <button data-section="wheel">🎡 Wheel</button>
    <button data-section="dice">🎲 Dice</button>
    <button data-section="dolphin">🐬 Derby</button>
    <button data-section="roulette">🎴 Roulette</button>
    <button data-section="highlow">🔴 High/Low</button>
    <button data-section="vault">🔐 Vault</button>
    <button data-section="achievements">🏆 Awards</button>
    <button data-section="liliana">🌸 Liliana</button>
    <button data-section="quiz">❓ Quiz</button>
    <button data-section="letter">💌 Letter</button>
</nav>

<!-- HOME -->

<section id="home" class="section active">

<div class="panel">
    <h1 class="section-title">Welcome to Liliana's Casino ♡</h1>
    <p class="section-subtitle">
        Six years of friendship deserve a ridiculous amount of games.
        Every token is fictional. Every prize is friendship.
    </p>

    <div class="game-grid">

        <div class="game-card" data-go="slots">
            <div class="game-icon">🎰</div>
            <h3>Lucky Three Slots</h3>
            <p>Spin the reels and hunt for Liliana's legendary 3️⃣ 3️⃣ 3️⃣ jackpot.</p>
        </div>

        <div class="game-card" data-go="poker">
            <div class="game-icon">🃏</div>
            <h3>Bestie Poker</h3>
            <p>Play an actual poker hand against the computer.</p>
        </div>

        <div class="game-card" data-go="blackjack">
            <div class="game-icon">♠️</div>
            <h3>Blackjack</h3>
            <p>Beat the dealer without going over 21.</p>
        </div>

        <div class="game-card" data-go="wheel">
            <div class="game-icon">🎡</div>
            <h3>Lucky Wheel</h3>
            <p>Spin for random friendship rewards.</p>
        </div>

        <div class="game-card" data-go="dice">
            <div class="game-icon">🎲</div>
            <h3>Dice Duel</h3>
            <p>You versus the computer. Highest roll wins.</p>
        </div>

        <div class="game-card" data-go="dolphin">
            <div class="game-icon">🐬</div>
            <h3>Dolphin Derby</h3>
            <p>Pick a dolphin and watch the race.</p>
        </div>

        <div class="game-card" data-go="roulette">
            <div class="game-icon">🎴</div>
            <h3>Friendship Roulette</h3>
            <p>Pick chambers and survive the suspense.</p>
        </div>

        <div class="game-card" data-go="highlow">
            <div class="game-icon">🔴</div>
            <h3>Red or Black</h3>
            <p>Build a streak and cash out whenever you want.</p>
        </div>

        <div class="game-card" data-go="vault">
            <div class="game-icon">🔐</div>
            <h3>Friendship Vault</h3>
            <p>Collect clues from the casino and crack the vault.</p>
        </div>

    </div>
</div>

<div class="panel">
    <h2>Casino Progress</h2>
    <p>Friendship XP: <strong id="xp">0</strong></p>
    <p>Current Level: <strong id="level">Newbie</strong></p>
</div>

</section>

<!-- SLOTS -->

<section id="slots" class="section">

<div class="panel slot-machine">

    <h2 class="section-title">🎰 Lucky Three Slots</h2>
    <p class="section-subtitle">
        Cost: 100 Friendship Tokens • Triple 3 = massive jackpot
    </p>

    <div class="reels">
        <div class="reel" id="reel1">🌹</div>
        <div class="reel" id="reel2">🐬</div>
        <div class="reel" id="reel3">3️⃣</div>
    </div>

    <div class="slot-info">
        <span>🌹 🌹 🌹 = 500</span>
        <span>🐬 🐬 🐬 = 750</span>
        <span>3️⃣ 3️⃣ 3️⃣ = 3000</span>
    </div>

    <br>

    <button class="btn gold" id="spinSlots">SPIN • 100 🪙</button>

    <div class="message" id="slotMessage"></div>

</div>

</section>

<!-- POKER -->

<section id="poker" class="section">

<div class="panel">

    <h2 class="section-title">🃏 Bestie Poker</h2>
    <p class="section-subtitle">
        You are playing against the Friendship Computer. Cost: 200 tokens.
        Tap cards to hold them, then draw.
    </p>

    <div class="player-area">
        <div class="player-label">COMPUTER</div>
        <div class="card-row" id="computerCards"></div>
        <div id="computerMessage" class="message"></div>
    </div>

    <div class="player-area">
        <div class="player-label">YOU</div>
        <div class="card-row" id="playerCards"></div>

        <div class="actions">
            <button class="btn" id="pokerDeal">DEAL • 200 🪙</button>
            <button class="btn gold hidden" id="pokerDraw">DRAW</button>
        </div>
    </div>

    <div class="message" id="pokerMessage"></div>

</div>

</section>

<!-- BLACKJACK -->

<section id="blackjack" class="section">

<div class="panel">

    <h2 class="section-title">♠️ Blackjack</h2>
    <p class="section-subtitle">
        Beat the computer by getting as close to 21 as possible without going over.
    </p>

    <div class="scoreboard">
        <div>Computer: <span class="score" id="dealerScore">?</span></div>
        <div>You: <span class="score" id="playerScore">0</span></div>
    </div>

    <div class="player-area">
        <div class="player-label">COMPUTER</div>
        <div class="card-row" id="dealerCards"></div>
    </div>

    <div class="player-area">
        <div class="player-label">YOU</div>
        <div class="card-row" id="bjPlayerCards"></div>
    </div>

    <div class="actions" style="justify-content:center">
        <button class="btn gold" id="bjDeal">DEAL • 150 🪙</button>
        <button class="btn hidden" id="bjHit">HIT</button>
        <button class="btn secondary hidden" id="bjStand">STAND</button>
    </div>

    <div class="message" id="bjMessage"></div>

</div>

</section>

<!-- WHEEL -->

<section id="wheel" class="section">

<div class="panel">

    <h2 class="section-title">🎡 Lucky Wheel</h2>
    <p class="section-subtitle">Spin for a random Friendship Token reward.</p>

    <div class="wheel-wrap">
        <div class="pointer">🔻</div>
        <div class="wheel" id="wheelGraphic"></div>

        <button class="btn gold" id="spinWheel">SPIN • 100 🪙</button>

        <div class="message" id="wheelMessage"></div>
    </div>

</div>

</section>

<!-- DICE -->

<section id="dice" class="section">

<div class="panel" style="text-align:center">

    <h2 class="section-title">🎲 Dice Duel</h2>
    <p class="section-subtitle">You and the computer roll two dice. Highest total wins.</p>

    <div class="dice-row">
        <div>
            <div class="die" id="yourDie1">?</div>
            <small>Your die</small>
        </div>

        <div>
            <div class="die" id="yourDie2">?</div>
            <small>Your die</small>
        </div>
    </div>

    <div class="dice-row">
        <div>
            <div class="die" id="cpuDie1">?</div>
            <small>Computer</small>
        </div>

        <div>
            <div class="die" id="cpuDie2">?</div>
            <small>Computer</small>
        </div>
    </div>

    <button class="btn gold" id="rollDice">ROLL • 100 🪙</button>

    <div class="message" id="diceMessage"></div>

</div>

</section>

<!-- DOLPHIN -->

<section id="dolphin" class="section">

<div class="panel">

    <h2 class="section-title">🐬 Dolphin Derby</h2>
    <p class="section-subtitle">Pick your dolphin before the race begins.</p>

    <div class="actions" style="justify-content:center">
        <button class="btn secondary dolphinPick" data-dolphin="0">🐬 Pinky</button>
        <button class="btn secondary dolphinPick" data-dolphin="1">🐬 Sunny</button>
        <button class="btn secondary dolphinPick" data-dolphin="2">🐬 Rosie</button>
        <button class="btn secondary dolphinPick" data-dolphin="3">🐬 Lucky</button>
        <button class="btn secondary dolphinPick" data-dolphin="4">🐬 Bubbles</button>
    </div>

    <br>

    <div class="race">
        <div class="track"><span class="dolphin" id="dolphin0">🐬</span></div>
        <div class="track"><span class="dolphin" id="dolphin1">🐬</span></div>
        <div class="track"><span class="dolphin" id="dolphin2">🐬</span></div>
        <div class="track"><span class="dolphin" id="dolphin3">🐬</span></div>
        <div class="track"><span class="dolphin" id="dolphin4">🐬</span></div>
    </div>

    <br>

    <button class="btn gold" id="startRace">START RACE • 150 🪙</button>

    <div class="message" id="raceMessage"></div>

</div>

</section>

<!-- FRIENDSHIP ROULETTE -->

<section id="roulette" class="section">

<div class="panel" style="text-align:center">

    <h2 class="section-title">🎴 Friendship Roulette</h2>

    <p class="section-subtitle">
        Six mystery chambers. One causes a harmless “BOOM!” and ends the round.
        No weapons, no real danger, just dramatic casino suspense.
    </p>

    <div class="card-row" id="rouletteCards"></div>

    <button class="btn gold" id="rouletteStart">START ROUND • 100 🪙</button>

    <div class="message" id="rouletteMessage"></div>

</div>

</section>

<!-- HIGH LOW -->

<section id="highlow" class="section">

<div class="panel" style="text-align:center">

    <h2 class="section-title">🔴 High or Low</h2>

    <p class="section-subtitle">
        Guess whether the next card is higher or lower. Keep your streak alive,
        then cash out your multiplier.
    </p>

    <div class="card-row">
        <div class="playing-card" id="hlCurrent">?</div>
        <div style="font-size:30px;display:grid;place-items:center">→</div>
        <div class="playing-card" id="hlNext">?</div>
    </div>

    <div>
        <strong>Streak:</strong> <span id="hlStreak">0</span>
        &nbsp; • &nbsp;
        <strong>Multiplier:</strong> <span id="hlMultiplier">1x</span>
    </div>

    <br>

    <div class="actions" style="justify-content:center">
        <button class="btn" id="hlStart">START • 100 🪙</button>
        <button class="btn secondary hidden" id="hlHigh">HIGH</button>
        <button class="btn secondary hidden" id="hlLow">LOW</button>
        <button class="btn gold hidden" id="hlCash">CASH OUT</button>
    </div>

    <div class="message" id="hlMessage"></div>

</div>

</section>

<!-- VAULT -->

<section id="vault" class="section">

<div class="panel vault">

    <h2 class="section-title">🔐 Friendship Vault</h2>

    <p class="section-subtitle">
        Find the secret three-number combination hidden throughout the casino.
    </p>

    <div class="locks">
        <div class="lock" id="lock1">?</div>
        <div class="lock" id="lock2">?</div>
        <div class="lock" id="lock3">?</div>
    </div>

    <p>
        Hint: Liliana's favourite number appears more than once.
    </p>

    <input
        id="vaultCode"
        maxlength="3"
        inputmode="numeric"
        placeholder="3 3 3"
        style="padding:13px;border-radius:10px;border:0;text-align:center;font-size:20px;width:130px"
    >

    <br><br>

    <button class="btn gold" id="openVault">OPEN VAULT</button>

    <div class="message" id="vaultMessage"></div>

</div>

</section>

<!-- ACHIEVEMENTS -->

<section id="achievements" class="section">

<div class="panel">

    <h2 class="section-title">🏆 Friendship Awards</h2>
    <p class="section-subtitle">Collect achievements as you play.</p>

    <div class="achievements">

        <div class="achievement" id="achFirst">
            <div class="achievement-icon">🌸</div>
            <strong>First Win</strong>
            <p>Win your first casino game.</p>
        </div>

        <div class="achievement" id="achThree">
            <div class="achievement-icon">3️⃣</div>
            <strong>Lucky Three</strong>
            <p>Hit three 3s on the slots.</p>
        </div>

        <div class="achievement" id="achPoker">
            <div class="achievement-icon">🃏</div>
            <strong>Poker Face</strong>
            <p>Win a poker match.</p>
        </div>

        <div class="achievement" id="achBlackjack">
            <div class="achievement-icon">♠️</div>
            <strong>21</strong>
            <p>Win at blackjack.</p>
        </div>

        <div class="achievement" id="achDolphin">
            <div class="achievement-icon">🐬</div>
            <strong>Dolphin Luck</strong>
            <p>Win the dolphin derby.</p>
        </div>

        <div class="achievement" id="achVault">
            <div class="achievement-icon">🔐</div>
            <strong>Vault Cracker</strong>
            <p>Open the Friendship Vault.</p>
        </div>

        <div class="achievement" id="achSix">
            <div class="achievement-icon">6️⃣</div>
            <strong>Six Years Strong</strong>
            <p>Reach 6000 Friendship XP.</p>
        </div>

    </div>

</div>

</section>

<!-- LILIANA -->

<section id="liliana" class="section">

<div class="panel">

    <div class="profile">

        <div class="profile-avatar">🌸</div>

        <div>
            <h2 class="section-title">Liliana</h2>
            <p class="section-subtitle">
                The woman who somehow manages to be sweet, caring, charismatic
                and a complete menace at the poker table.
            </p>

            <div class="facts">

                <div class="fact">
                    <strong>Favourite colour</strong>
                    Baby pink
                </div>

                <div class="fact">
                    <strong>Favourite number</strong>
                    3
                </div>

                <div class="fact">
                    <strong>Favourite animal</strong>
                    Dolphins
                </div>

                <div class="fact">
                    <strong>Food</strong>
                    Sushi
                </div>

                <div class="fact">
                    <strong>Birthday</strong>
                    July 22
                </div>

                <div class="fact">
                    <strong>Movie</strong>
                    Me Before You
                </div>

                <div class="fact">
                    <strong>Loves</strong>
                    Sunflowers & roses
                </div>

                <div class="fact">
                    <strong>Personality</strong>
                    Sweet & charismatic
                </div>

            </div>
        </div>

    </div>

</div>

</section>

<!-- QUIZ -->

<section id="quiz" class="section">

<div class="panel">

    <h2 class="section-title">❓ How Well Do You Know Liliana?</h2>
    <p class="section-subtitle">Answer the questions and build your friendship score.</p>

    <div id="quizContainer"></div>

    <button class="btn gold" id="quizSubmit">CHECK ANSWERS</button>

    <div class="message" id="quizMessage"></div>

</div>

</section>

<!-- LETTER -->

<section id="letter" class="section">

<div class="panel">

    <h2 class="section-title">💌 The Six-Year Letter</h2>

    <div class="letter">

        <p>Dear Liliana,</p>

        <p>
            Six years is a pretty crazy amount of time to have someone in your life.
            Somehow, through all the chaos, conversations, jokes, random moments,
            serious moments and everything in between, you became one of those people
            who feels like they were always supposed to be there.
        </p>

        <p>
            So obviously I couldn't just make you a normal birthday or friendship
            website.
        </p>

        <p>
            I had to make you an entire casino.
        </p>

        <p>
            Because if anyone deserves a ridiculous amount of games, pink lights,
            cards, dolphins, jackpots and completely unnecessary levels of drama,
            it is you.
        </p>

        <p>
            Thank you for six years of friendship.
            Here's to all the memories we've already made and all the ones we
            haven't made yet.
        </p>

        <p>
            Love always,<br>
            Bree ♡
        </p>

    </div>

</div>

</section>

</div>

<script>
(() => {

"use strict";

/* =========================
   STATE
========================= */

let tokens = Number(localStorage.getItem("lilianaTokens")) || 6000;
let xp = Number(localStorage.getItem("lilianaXP")) || 0;
let wins = Number(localStorage.getItem("lilianaWins")) || 0;

const achievements = JSON.parse(
    localStorage.getItem("lilianaAchievements") || "{}"
);

function save() {
    localStorage.setItem("lilianaTokens", tokens);
    localStorage.setItem("lilianaXP", xp);
    localStorage.setItem("lilianaWins", wins);
    localStorage.setItem("lilianaAchievements", JSON.stringify(achievements));
}

function updateBalance() {
    document.getElementById("tokenBalance").textContent =
        Math.max(0, Math.floor(tokens)).toLocaleString();

    document.getElementById("xp").textContent =
        xp.toLocaleString();

    let level = "Newbie";

    if (xp >= 10000) level = "Six Years Strong";
    else if (xp >= 6000) level = "Casino Queen";
    else if (xp >= 3000) level = "High Roller";
    else if (xp >= 1500) level = "Card Shark";
    else if (xp >= 500) level = "Lucky Bestie";

    document.getElementById("level").textContent = level;

    updateAchievements();
    save();
}

function addTokens(amount) {
    tokens += amount;
    updateBalance();
}

function spendTokens(amount) {
    if (tokens < amount) {
        alert("You don't have enough Friendship Tokens!");
        return false;
    }

    tokens -= amount;
    updateBalance();
    return true;
}

function addXP(amount) {
    xp += amount;
    updateBalance();
}

function win(amount, xpAmount = 100) {
    addTokens(amount);
    addXP(xpAmount);
    wins++;

    achievements.first = true;

    updateBalance();
}

function setMessage(id, text) {
    document.getElementById(id).textContent = text;
}

/* =========================
   NAVIGATION
========================= */

document.querySelectorAll(".nav button").forEach(button => {

    button.addEventListener("click", () => {

        const section = button.dataset.section;

        document.querySelectorAll(".section").forEach(s =>
            s.classList.remove("active")
        );

        document.getElementById(section).classList.add("active");

        document.querySelectorAll(".nav button").forEach(b =>
            b.classList.remove("active")
        );

        button.classList.add("active");

        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });
    });

});

document.querySelectorAll("[data-go]").forEach(card => {

    card.addEventListener("click", () => {

        const target = card.dataset.go;

        document.querySelector(`[data-section="${target}"]`).click();

    });

});

/* =========================
   SLOTS
========================= */

const symbols = [
    "🌹",
    "🐬",
    "🌻",
    "🍣",
    "💗",
    "🎀",
    "3️⃣"
];

document.getElementById("spinSlots").addEventListener("click", () => {

    if (!spendTokens(100)) return;

    const reels = [
        document.getElementById("reel1"),
        document.getElementById("reel2"),
        document.getElementById("reel3")
    ];

    reels.forEach(r => r.classList.add("spin"));

    setMessage("slotMessage", "SPINNING... 🎰");

    setTimeout(() => {

        reels.forEach(r => r.classList.remove("spin"));

        const result = reels.map(() =>
            symbols[Math.floor(Math.random() * symbols.length)]
        );

        reels.forEach((r, i) => {
            r.textContent = result[i];
        });

        let reward = 0;

        if (result.every(x => x === "3️⃣")) {
            reward = 3000;
            achievements.three = true;

            setMessage(
                "slotMessage",
                "🎉 LILIANA'S LUCKY THREE JACKPOT!!! +3000 🪙"
            );

            addXP(500);

        } else if (result.every(x => x === "🌹")) {
            reward = 500;

        } else if (result.every(x => x === "🐬")) {
            reward = 750;

        } else if (result[0] === result[1] || result[1] === result[2]) {
            reward = 150;
        }

        if (reward > 0) {

            addTokens(reward);
            addXP(100);

            achievements.first = true;

            if (!result.every(x => x === "3️⃣")) {
                setMessage(
                    "slotMessage",
                    `Nice spin! You won ${reward} tokens! 🎉`
                );
            }

        } else {

            setMessage(
                "slotMessage",
                "No match this time... the casino survives another day 😭"
            );

        }

        updateBalance();

    }, 900);

});

/* =========================
   CARD DECK
========================= */

const suits = ["♥", "♦", "♣", "♠"];
const ranks = [
    {name:"2", value:2},
    {name:"3", value:3},
    {name:"4", value:4},
    {name:"5", value:5},
    {name:"6", value:6},
    {name:"7", value:7},
    {name:"8", value:8},
    {name:"9", value:9},
    {name:"10", value:10},
    {name:"J", value:11},
    {name:"Q", value:12},
    {name:"K", value:13},
    {name:"A", value:14}
];

function makeDeck() {

    const deck = [];

    for (const suit of suits) {
        for (const rank of ranks) {
            deck.push({
                suit,
                name: rank.name,
                value: rank.value
            });
        }
    }

    return deck.sort(() => Math.random() - .5);
}

function cardElement(card, back = false) {

    const div = document.createElement("div");

    div.className = "playing-card";

    if (back) {
        div.classList.add("card-back");
        div.textContent = "♡";
        return div;
    }

    div.textContent = card.name + card.suit;

    if (card.suit === "♥" || card.suit === "♦") {
        div.classList.add("red");
    }

    return div;
}

/* =========================
   POKER
========================= */

let pokerDeck = [];
let playerPoker = [];
let computerPoker = [];
let pokerHeld = [];

function pokerRank(hand) {

    const values = hand.map(c => c.value).sort((a,b) => b-a);

    const counts = {};

    values.forEach(v => {
        counts[v] = (counts[v] || 0) + 1;
    });

    const groups = Object.values(counts).sort((a,b) => b-a);

    const flush = hand.every(c => c.suit === hand[0].suit);

    const unique = [...new Set(values)];

    let straight = false;

    if (unique.length === 5) {

        straight =
            unique[0] - unique[4] === 4 ||
            JSON.stringify(unique) === JSON.stringify([14,5,4,3,2]);

    }

    if (flush && straight) return 8;
    if (groups[0] === 4) return 7;
    if (groups[0] === 3 && groups[1] === 2) return 6;
    if (flush) return 5;
    if (straight) return 4;
    if (groups[0] === 3) return 3;
    if (groups[0] === 2 && groups[1] === 2) return 2;
    if (groups[0] === 2) return 1;

    return 0;
}

const pokerNames = [
    "High Card",
    "Pair",
    "Two Pair",
    "Three of a Kind",
    "Straight",
    "Flush",
    "Full House",
    "Four of a Kind",
    "Straight Flush"
];

function renderPoker() {

    const pc = document.getElementById("playerCards");
    const cc = document.getElementById("computerCards");

    pc.innerHTML = "";
    cc.innerHTML = "";

    playerPoker.forEach((card, index) => {

        const el = cardElement(card);

        el.classList.add("hold-card");

        if (pokerHeld[index]) {
            el.classList.add("held");

            const tag = document.createElement("span");
            tag.className = "hold-tag";
            tag.textContent = "HELD";
            el.appendChild(tag);
        }

        el.addEventListener("click", () => {

            if (!document.getElementById("pokerDraw").classList.contains("hidden")) {
                pokerHeld[index] = !pokerHeld[index];
                renderPoker();
            }

        });

        pc.appendChild(el);

    });

    computerPoker.forEach(() => {
        cc.appendChild(cardElement(null, true));
    });

}

document.getElementById("pokerDeal").addEventListener("click", () => {

    if (!spendTokens(200)) return;

    pokerDeck = makeDeck();

    playerPoker = pokerDeck.splice(0,5);
    computerPoker = pokerDeck.splice(0,5);

    pokerHeld = [false,false,false,false,false];

    renderPoker();

    document.getElementById("pokerDraw").classList.remove("hidden");
    document.getElementById("pokerDeal").classList.add("hidden");

    setMessage(
        "computerMessage",
        "Computer: Hmm... let's see what you've got."
    );

    setMessage(
        "pokerMessage",
        "Choose the cards you want to HOLD, then press DRAW."
    );

});

document.getElementById("pokerDraw").addEventListener("click", () => {

    for (let i = 0; i < 5; i++) {

        if (!pokerHeld[i]) {
            playerPoker[i] = pokerDeck.shift();
        }

    }

    /* Computer gets a simple strategic redraw */

    const computerRank = pokerRank(computerPoker);

    if (computerRank < 2) {

        const keep = [];

        const counts = {};

        computerPoker.forEach(c => {
            counts[c.value] = (counts[c.value] || 0) + 1;
        });

        computerPoker.forEach((c, i) => {

            if (counts[c.value] > 1) {
                keep.push(i);
            }

        });

        for (let i = 0; i < 5; i++) {

            if (!keep.includes(i)) {
                computerPoker[i] = pokerDeck.shift();
            }

        }

    }

    renderPoker();

    const playerRank = pokerRank(playerPoker);
    const finalComputerRank = pokerRank(computerPoker);

    document.getElementById("computerCards").innerHTML = "";

    computerPoker.forEach(card => {
        document.getElementById("computerCards").appendChild(
            cardElement(card)
        );
    });

    let result;

    if (playerRank > finalComputerRank) {

        result =
            `🎉 YOU WIN! ${pokerNames[playerRank]} beats ${pokerNames[finalComputerRank]}! +700 🪙`;

        win(700, 250);
        achievements.poker = true;

    } else if (playerRank < finalComputerRank) {

        result =
            `Computer wins with ${pokerNames[finalComputerRank]}. You had ${pokerNames[playerRank]}.`;

    } else {

        result =
            `It's a tie! Both have ${pokerNames[playerRank]}.`;

        addTokens(250);
    }

    setMessage("pokerMessage", result);

    setMessage(
        "computerMessage",
        finalComputerRank >= 5
            ? "Computer: OH. THAT was not what I expected. 😳"
            : "Computer: Not bad, bestie."
    );

    document.getElementById("pokerDraw").classList.add("hidden");
    document.getElementById("pokerDeal").classList.remove("hidden");

    updateBalance();

});

/* =========================
   BLACKJACK
========================= */

let bjDeck = [];
let bjPlayer = [];
let bjDealer = [];

function blackjackValue(hand) {

    let total = 0;
    let aces = 0;

    hand.forEach(card => {

        if (card.value >= 11) {
            total += 10;
        } else {
            total += card.value;
        }

        if (card.name === "A") aces++;

    });

    while (aces > 0 && total + 10 <= 21) {
        total += 10;
        aces--;
    }

    return total;
}

function renderBJ(showDealer = false) {

    const player = document.getElementById("bjPlayerCards");
    const dealer = document.getElementById("dealerCards");

    player.innerHTML = "";
    dealer.innerHTML = "";

    bjPlayer.forEach(card => player.appendChild(cardElement(card)));

    bjDealer.forEach((card, i) => {

        dealer.appendChild(
            showDealer || i === 1
                ? cardElement(card)
                : cardElement(null, true)
        );

    });

    document.getElementById("playerScore").textContent =
        blackjackValue(bjPlayer);

    document.getElementById("dealerScore").textContent =
        showDealer ? blackjackValue(bjDealer) : "?";

}

function endBlackjack() {

    const playerScore = blackjackValue(bjPlayer);

    while (blackjackValue(bjDealer) < 17) {
        bjDealer.push(bjDeck.shift());
    }

    renderBJ(true);

    const dealerScore = blackjackValue(bjDealer);

    if (playerScore > 21) {

        setMessage("bjMessage", "Bust! 💥 The computer wins.");

    } else if (dealerScore > 21 || playerScore > dealerScore) {

        setMessage(
            "bjMessage",
            `🎉 YOU WIN! ${playerScore} vs ${dealerScore}. +500 🪙`
        );

        win(500, 200);
        achievements.blackjack = true;

    } else if (playerScore === dealerScore) {

        setMessage("bjMessage", "Push! Nobody wins. +150 🪙");
        addTokens(150);

    } else {

        setMessage(
            "bjMessage",
            `Computer wins ${dealerScore} to ${playerScore}.`
        );

    }

    document.getElementById("bjHit").classList.add("hidden");
    document.getElementById("bjStand").classList.add("hidden");
    document.getElementById("bjDeal").classList.remove("hidden");

    updateBalance();
}

document.getElementById("bjDeal").addEventListener("click", () => {

    if (!spendTokens(150)) return;

    bjDeck = makeDeck();

    bjPlayer = [bjDeck.shift(), bjDeck.shift()];
    bjDealer = [bjDeck.shift(), bjDeck.shift()];

    renderBJ(false);

    document.getElementById("bjDeal").classList.add("hidden");
    document.getElementById("bjHit").classList.remove("hidden");
    document.getElementById("bjStand").classList.remove("hidden");

    setMessage("bjMessage", "Your move.");

    if (blackjackValue(bjPlayer) === 21) {
        endBlackjack();
    }

});

document.getElementById("bjHit").addEventListener("click", () => {

    bjPlayer.push(bjDeck.shift());

    renderBJ(false);

    if (blackjackValue(bjPlayer) >= 21) {
        endBlackjack();
    }

});

document.getElementById("bjStand").addEventListener("click", () => {
    endBlackjack();
});

/* =========================
   WHEEL
========================= */

let wheelRotation = 0;

document.getElementById("spinWheel").addEventListener("click", () => {

    if (!spendTokens(100)) return;

    const wheel = document.getElementById("wheelGraphic");

    const segment = Math.floor(Math.random() * 8);

    const rewards = [
        50, 100, 250, 500,
        75, 150, 1000, 200
    ];

    wheelRotation += 1440 + (segment * 45);

    wheel.style.transform =
        `rotate(${wheelRotation}deg)`;

    setMessage("wheelMessage", "The wheel is spinning... 🎡");

    setTimeout(() => {

        const reward = rewards[segment];

        addTokens(reward);
        addXP(80);

        setMessage(
            "wheelMessage",
            `🎉 The wheel landed on ${reward} tokens!`
        );

    }, 3100);

});

/* =========================
   DICE
========================= */

function rollDie() {
    return Math.floor(Math.random() * 6) + 1;
}

document.getElementById("rollDice").addEventListener("click", () => {

    if (!spendTokens(100)) return;

    const dice = [
        document.getElementById("yourDie1"),
        document.getElementById("yourDie2"),
        document.getElementById("cpuDie1"),
        document.getElementById("cpuDie2")
    ];

    dice.forEach(d => d.classList.add("rolling"));

    setMessage("diceMessage", "ROLLING... 🎲");

    setTimeout(() => {

        dice.forEach(d => d.classList.remove("rolling"));

        const your1 = rollDie();
        const your2 = rollDie();

        const cpu1 = rollDie();
        const cpu2 = rollDie();

        document.getElementById("yourDie1").textContent = your1;
        document.getElementById("yourDie2").textContent = your2;
        document.getElementById("cpuDie1").textContent = cpu1;
        document.getElementById("cpuDie2").textContent = cpu2;

        const you = your1 + your2;
        const cpu = cpu1 + cpu2;

        if (you > cpu) {

            win(400, 150);

            setMessage(
                "diceMessage",
                `🎉 You win ${you} to ${cpu}! +400 🪙`
            );

        } else if (you === cpu) {

            addTokens(150);

            setMessage(
                "diceMessage",
                `DRAW! ${you} to ${cpu}. +150 🪙`
            );

        } else {

            setMessage(
                "diceMessage",
                `Computer wins ${cpu} to ${you}.`
            );

        }

    }, 900);

});

/* =========================
   DOLPHIN DERBY
========================= */

let chosenDolphin = null;

document.querySelectorAll(".dolphinPick").forEach(button => {

    button.addEventListener("click", () => {

        chosenDolphin = Number(button.dataset.dolphin);

        document.querySelectorAll(".dolphinPick").forEach(b =>
            b.classList.remove("gold")
        );

        button.classList.add("gold");

        setMessage(
            "raceMessage",
            `You picked ${button.textContent.trim()}!`
        );

    });

});

document.getElementById("startRace").addEventListener("click", () => {

    if (chosenDolphin === null) {

        setMessage(
            "raceMessage",
            "Pick a dolphin first! 🐬"
        );

        return;
    }

    if (!spendTokens(150)) return;

    const results = [];

    for (let i = 0; i < 5; i++) {
        results.push(55 + Math.random() * 40);
    }

    const winner = results.indexOf(Math.max(...results));

    for (let i = 0; i < 5; i++) {

        document.getElementById(`dolphin${i}`).style.left =
            `${results[i]}%`;

    }

    setMessage("raceMessage", "THE RACE IS ON!!! 🐬🏁");

    setTimeout(() => {

        if (winner === chosenDolphin) {

            win(750, 300);
            achievements.dolphin = true;

            setMessage(
                "raceMessage",
                "🐬🏆 YOUR DOLPHIN WON!!! +750 🪙"
            );

        } else {

            setMessage(
                "raceMessage",
                `🐬 The winner was Dolphin ${winner + 1}!`
            );

        }

    }, 3200);

});

/* =========================
   FRIENDSHIP ROULETTE
========================= */

let rouletteActive = false;
let rouletteSafe = [];
let rouletteIndex = 0;

function createRouletteCards() {

    const container = document.getElementById("rouletteCards");

    container.innerHTML = "";

    for (let i = 0; i < 6; i++) {

        const card = document.createElement("div");

        card.className = "playing-card card-back card-choice";
        card.textContent = "?";

        card.addEventListener("click", () => {

            if (!rouletteActive) return;

            if (!rouletteSafe.includes(i)) {

                card.classList.remove("card-back");
                card.textContent = "💥";

                rouletteActive = false;

                setMessage(
                    "rouletteMessage",
                    "BOOM! 💥 Your turn ended. No tokens lost beyond the entry."
                );

                return;
            }

            card.classList.remove("card-back");
            card.textContent = "🍀";

            rouletteIndex++;

            const reward = rouletteIndex * 150;

            addTokens(reward);
            addXP(50);

            if (rouletteIndex >= 5) {

                rouletteActive = false;

                addTokens(1000);

                setMessage(
                    "rouletteMessage",
                    "🏆 YOU SURVIVED ALL SIX! FRIENDSHIP JACKPOT +1000 🪙"
                );

            } else {

                setMessage(
                    "rouletteMessage",
                    `SAFE! 🍀 +${reward} 🪙. Pick another chamber...`
                );

            }

        });

        container.appendChild(card);

    }

}

createRouletteCards();

document.getElementById("rouletteStart").addEventListener("click", () => {

    if (!spendTokens(100)) return;

    rouletteActive = true;
    rouletteIndex = 0;

    rouletteSafe = [0,1,2,3,4,5]
        .sort(() => Math.random() - .5)
        .slice(0,5);

    createRouletteCards();

    setMessage(
        "rouletteMessage",
        "Six chambers. One BOOM. Choose carefully..."
    );

});

/* =========================
   HIGH LOW
========================= */

let hlDeck = [];
let hlCurrent = null;
let hlStreak = 0;
let hlMultiplier = 1;
let hlActive = false;

function updateHighLow() {

    document.getElementById("hlStreak").textContent = hlStreak;
    document.getElementById("hlMultiplier").textContent =
        `${hlMultiplier}x`;

}

function startHighLow() {

    if (!spendTokens(100)) return;

    hlDeck = makeDeck();

    hlCurrent = hlDeck.shift();

    hlStreak = 0;
    hlMultiplier = 1;
    hlActive = true;

    document.getElementById("hlCurrent").replaceWith(
        cardElement(hlCurrent)
    );

    const current = document.querySelector("#hlCurrent");

    if (current) current.id = "hlCurrent";

    document.getElementById("hlNext").textContent = "?";

    document.getElementById("hlStart").classList.add("hidden");
    document.getElementById("hlHigh").classList.remove("hidden");
    document.getElementById("hlLow").classList.remove("hidden");
    document.getElementById("hlCash").classList.remove("hidden");

    setMessage(
        "hlMessage",
        "Will the next card be HIGHER or LOWER?"
    );

    updateHighLow();

}

document.getElementById("hlStart").addEventListener("click", startHighLow);

function highLowGuess(direction) {

    if (!hlActive) return;

    const next = hlDeck.shift();

    document.getElementById("hlNext").replaceWith(
        cardElement(next)
    );

    const nextEl = document.querySelector("#hlNext");

    if (nextEl) nextEl.id = "hlNext";

    const correct =
        direction === "high"
            ? next.value >= hlCurrent.value
            : next.value <= hlCurrent.value;

    if (correct) {

        hlStreak++;
        hlMultiplier = Math.min(10, hlMultiplier + 1);

        const reward = 100 * hlMultiplier;

        addTokens(reward);
        addXP(75);

        setMessage(
            "hlMessage",
            `CORRECT! 🎉 +${reward} 🪙`
        );

        hlCurrent = next;

    } else {

        hlActive = false;

        setMessage(
            "hlMessage",
            "Wrong! 💔 Your streak ended."
        );

        document.getElementById("hlStart").classList.remove("hidden");
        document.getElementById("hlHigh").classList.add("hidden");
        document.getElementById("hlLow").classList.add("hidden");
        document.getElementById("hlCash").classList.add("hidden");

    }

    updateHighLow();

}

document.getElementById("hlHigh").addEventListener(
    "click",
    () => highLowGuess("high")
);

document.getElementById("hlLow").addEventListener(
    "click",
    () => highLowGuess("low")
);

document.getElementById("hlCash").addEventListener("click", () => {

    if (!hlActive) return;

    const bonus = hlStreak * 250;

    addTokens(bonus);
    addXP(hlStreak * 30);

    setMessage(
        "hlMessage",
        `💰 CASHED OUT! +${bonus} bonus tokens!`
    );

    hlActive = false;

    document.getElementById("hlStart").classList.remove("hidden");
    document.getElementById("hlHigh").classList.add("hidden");
    document.getElementById("hlLow").classList.add("hidden");
    document.getElementById("hlCash").classList.add("hidden");

});

/* =========================
   VAULT
========================= */

document.getElementById("openVault").addEventListener("click", () => {

    const code =
        document.getElementById("vaultCode").value.trim();

    if (code === "333") {

        document.getElementById("lock1").textContent = "3";
        document.getElementById("lock2").textContent = "3";
        document.getElementById("lock3").textContent = "3";

        addTokens(3000);
        addXP(1000);

        achievements.vault = true;

        setMessage(
            "vaultMessage",
            "🔓 VAULT OPENED! +3000 🪙"
        );

        updateBalance();

    } else {

        setMessage(
            "vaultMessage",
            "The vault rejected that combination..."
        );

    }

});

/* =========================
   ACHIEVEMENTS
========================= */

function updateAchievements() {

    const map = {
        first: "achFirst",
        three: "achThree",
        poker: "achPoker",
        blackjack: "achBlackjack",
        dolphin: "achDolphin",
        vault: "achVault"
    };

    Object.entries(map).forEach(([key, id]) => {

        document.getElementById(id)
            .classList.toggle(
                "unlocked",
                Boolean(achievements[key])
            );

    });

    document.getElementById("achSix")
        .classList.toggle("unlocked", xp >= 6000);
}

/* =========================
   QUIZ
========================= */

const quizQuestions = [

    {
        q: "What is Liliana's favourite colour?",
        answers: ["Baby pink", "Blue", "Burgundy", "Green"],
        correct: 0
    },

    {
        q: "What is Liliana's favourite number?",
        answers: ["7", "3", "9", "22"],
        correct: 1
    },

    {
        q: "Which animal does Liliana love?",
        answers: ["Cats", "Dolphins", "Penguins", "Foxes"],
        correct: 1
    },

    {
        q: "What food does Liliana love?",
        answers: ["Pizza", "Sushi", "Tacos", "Pasta"],
        correct: 1
    },

    {
        q: "When is Liliana's birthday?",
        answers: ["July 22", "June 12", "August 3", "May 7"],
        correct: 0
    },

    {
        q: "What is Liliana's favourite movie?",
        answers: [
            "Titanic",
            "Me Before You",
            "The Notebook",
            "Frozen"
        ],
        correct: 1
    }

];

const quizContainer = document.getElementById("quizContainer");

quizQuestions.forEach((question, index) => {

    const wrapper = document.createElement("div");

    wrapper.className = "panel";

    wrapper.innerHTML =
        `<strong>${index + 1}. ${question.q}</strong>`;

    question.answers.forEach((answer, answerIndex) => {

        const button = document.createElement("button");

        button.type = "button";
        button.className = "quiz-option";
        button.textContent = answer;
        button.dataset.question = index;
        button.dataset.answer = answerIndex;

        wrapper.appendChild(button);

    });

    quizContainer.appendChild(wrapper);

});

document.getElementById("quizSubmit").addEventListener("click", () => {

    let score = 0;

    document.querySelectorAll(".quiz-option").forEach(button => {

        button.style.borderColor = "";

    });

    quizQuestions.forEach((question, index) => {

        const selected = document.querySelector(
            `.quiz-option[data-question="${index}"][data-selected="true"]`
        );

        if (selected &&
            Number(selected.dataset.answer) === question.correct) {

            score++;

            selected.style.borderColor = "#ffd36a";

        }

    });

    const reward = score * 200;

    addTokens(reward);
    addXP(score * 100);

    setMessage(
        "quizMessage",
        `You scored ${score}/${quizQuestions.length}! +${reward} 🪙`
    );

});

document.querySelectorAll(".quiz-option").forEach(button => {

    button.addEventListener("click", () => {

        const question = button.dataset.question;

        document.querySelectorAll(
            `.quiz-option[data-question="${question}"]`
        ).forEach(b => {

            delete b.dataset.selected;

        });

        button.dataset.selected = "true";

    });

});

/* =========================
   STARTUP
========================= */

updateBalance();

})();
</script>

</body>
</html>
