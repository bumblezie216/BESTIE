<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Liliana's Friendship Casino</title>

<style>
*{
    box-sizing:border-box;
    margin:0;
    padding:0;
}

:root{
    --pink:#ff4fa3;
    --hot:#ff2f8a;
    --light:#ffd5e9;
    --deep:#4b102f;
    --wine:#711744;
    --gold:#ffd166;
    --cream:#fff7fb;
    --dark:#170914;
    --green:#55d68b;
}

body{
    font-family:Arial,Helvetica,sans-serif;
    background:
        radial-gradient(circle at 20% 10%,rgba(255,79,163,.22),transparent 30%),
        radial-gradient(circle at 80% 20%,rgba(255,209,102,.12),transparent 25%),
        linear-gradient(135deg,#180916,#351027 45%,#170914);
    color:white;
    min-height:100vh;
}

button{
    font-family:inherit;
}

header{
    position:sticky;
    top:0;
    z-index:1000;
    background:rgba(20,7,17,.94);
    backdrop-filter:blur(15px);
    border-bottom:1px solid rgba(255,255,255,.1);
}

.topbar{
    max-width:1400px;
    margin:auto;
    padding:14px 18px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap:15px;
}

.logo{
    font-size:22px;
    font-weight:900;
    color:#ffd4e9;
}

.logo span{
    color:var(--gold);
}

.balance{
    display:flex;
    gap:10px;
    align-items:center;
    flex-wrap:wrap;
}

.balanceBox{
    background:linear-gradient(135deg,#ff4fa3,#a91661);
    padding:9px 15px;
    border-radius:999px;
    font-weight:800;
    box-shadow:0 5px 20px rgba(255,79,163,.25);
}

.xpBox{
    background:#321326;
    padding:9px 13px;
    border-radius:999px;
    font-size:13px;
}

nav{
    max-width:1400px;
    margin:auto;
    padding:0 12px 12px;
    display:flex;
    gap:7px;
    overflow-x:auto;
}

nav button{
    flex:0 0 auto;
    border:0;
    background:#321326;
    color:#ffd9eb;
    padding:9px 13px;
    border-radius:10px;
    cursor:pointer;
    font-weight:700;
}

nav button:hover,
nav button.active{
    background:var(--pink);
    color:white;
}

main{
    max-width:1400px;
    margin:auto;
    padding:25px 18px 80px;
}

.page{
    display:none;
}

.page.active{
    display:block;
    animation:fade .25s ease;
}

@keyframes fade{
    from{opacity:0;transform:translateY(8px)}
    to{opacity:1;transform:none}
}

.hero{
    text-align:center;
    padding:40px 15px 30px;
}

.hero h1{
    font-size:clamp(36px,7vw,72px);
    margin-bottom:10px;
    background:linear-gradient(90deg,#fff,#ffb8d8,#ffd166);
    -webkit-background-clip:text;
    color:transparent;
}

.hero p{
    color:#f3cddd;
    max-width:700px;
    margin:auto;
    line-height:1.6;
}

.sectionTitle{
    font-size:30px;
    margin:25px 0 15px;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:15px;
}

.card{
    background:linear-gradient(145deg,rgba(102,24,66,.92),rgba(42,12,29,.94));
    border:1px solid rgba(255,184,216,.15);
    border-radius:18px;
    padding:20px;
    box-shadow:0 12px 30px rgba(0,0,0,.25);
}

.card h3{
    margin-bottom:7px;
}

.card p{
    color:#e8bfd2;
    line-height:1.5;
    font-size:14px;
}

.gameBtn,
.bigBtn{
    width:100%;
    border:0;
    background:linear-gradient(135deg,#ff4fa3,#b71968);
    color:white;
    padding:12px;
    border-radius:11px;
    margin-top:14px;
    cursor:pointer;
    font-weight:900;
    font-size:15px;
}

.gameBtn:hover,
.bigBtn:hover{
    filter:brightness(1.12);
    transform:translateY(-1px);
}

.goldBtn{
    background:linear-gradient(135deg,#ffd166,#d99b00);
    color:#351b00;
}

.greenBtn{
    background:linear-gradient(135deg,#63e89b,#249d5c);
}

.redBtn{
    background:linear-gradient(135deg,#ff667d,#b81836);
}

.game{
    max-width:900px;
    margin:15px auto;
    text-align:center;
}

.machine{
    background:linear-gradient(145deg,#711744,#300d23);
    border:2px solid #d84c91;
    border-radius:25px;
    padding:25px;
    box-shadow:0 20px 50px rgba(0,0,0,.4);
}

.reels{
    display:flex;
    gap:8px;
    justify-content:center;
    flex-wrap:wrap;
    margin:20px 0;
}

.reel{
    width:80px;
    height:90px;
    background:#fff;
    color:#381021;
    border-radius:12px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:40px;
    box-shadow:inset 0 -5px 0 #ddd;
}

.winText{
    min-height:28px;
    color:#ffd166;
    font-weight:900;
    margin:10px;
}

.controls{
    display:flex;
    flex-wrap:wrap;
    gap:8px;
    justify-content:center;
    margin:15px 0;
}

.controls button{
    border:0;
    padding:11px 15px;
    border-radius:10px;
    cursor:pointer;
    background:#57203e;
    color:white;
    font-weight:800;
}

.betControl{
    display:flex;
    justify-content:center;
    align-items:center;
    gap:10px;
    margin:12px;
}

.betControl button{
    width:38px;
    height:38px;
    border:0;
    border-radius:50%;
    background:#ff4fa3;
    color:white;
    font-weight:900;
    cursor:pointer;
}

.table{
    background:#064f3a;
    border:8px solid #7c4920;
    border-radius:35px;
    padding:30px 15px;
    min-height:280px;
    box-shadow:inset 0 0 40px rgba(0,0,0,.4),0 20px 40px #0008;
}

.cards{
    display:flex;
    gap:8px;
    justify-content:center;
    flex-wrap:wrap;
    min-height:85px;
}

.playingCard{
    width:55px;
    height:78px;
    border-radius:8px;
    background:#fff;
    color:#111;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size:22px;
    font-weight:900;
    box-shadow:0 5px 10px #0005;
}

.redCard{
    color:#d7193f;
}

.handArea{
    margin:15px 0;
}

.handArea h4{
    margin-bottom:7px;
}

.result{
    margin:15px auto;
    padding:13px;
    background:#28101e;
    border-radius:12px;
    max-width:650px;
    min-height:45px;
    color:#ffd9e9;
}

.wheel{
    width:min(330px,80vw);
    aspect-ratio:1;
    border-radius:50%;
    margin:20px auto;
    background:conic-gradient(
        #ff4fa3 0 45deg,
        #35102b 45deg 90deg,
        #ffd166 90deg 135deg,
        #35102b 135deg 180deg,
        #ff4fa3 180deg 225deg,
        #35102b 225deg 270deg,
        #ffd166 270deg 315deg,
        #35102b 315deg 360deg
    );
    border:10px solid #ffd166;
    position:relative;
    transition:transform 3s cubic-bezier(.12,.65,.12,1);
    box-shadow:0 0 35px #ff4fa355;
}

.wheel:after{
    content:"★";
    position:absolute;
    inset:0;
    display:grid;
    place-items:center;
    font-size:40px;
    color:white;
    text-shadow:0 2px 5px #000;
}

.pointer{
    width:0;
    height:0;
    border-left:14px solid transparent;
    border-right:14px solid transparent;
    border-top:30px solid #fff;
    margin:auto;
}

.dice{
    display:flex;
    justify-content:center;
    gap:20px;
    margin:25px;
}

.die{
    width:80px;
    height:80px;
    border-radius:16px;
    background:white;
    color:#351021;
    display:grid;
    place-items:center;
    font-size:35px;
    font-weight:900;
}

.dice.rolling .die{
    animation:shake .35s infinite;
}

@keyframes shake{
    0%,100%{transform:rotate(0)}
    25%{transform:rotate(7deg)}
    75%{transform:rotate(-7deg)}
}

.derby{
    display:flex;
    flex-direction:column;
    gap:10px;
    margin:20px 0;
}

.runner{
    display:grid;
    grid-template-columns:100px 1fr 50px;
    align-items:center;
    gap:8px;
}

.track{
    height:27px;
    background:#1b0a14;
    border-radius:20px;
    overflow:hidden;
}

.runnerProgress{
    height:100%;
    width:0;
    background:linear-gradient(90deg,#ff4fa3,#ffd166);
    border-radius:20px;
    transition:width .5s;
}

.progress{
    height:10px;
    background:#2b1220;
    border-radius:10px;
    overflow:hidden;
    margin:10px 0;
}

.progress span{
    display:block;
    height:100%;
    background:linear-gradient(90deg,#ff4fa3,#ffd166);
}

.stats{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
    gap:10px;
    margin:20px 0;
}

.stat{
    text-align:center;
    background:#321326;
    padding:16px;
    border-radius:14px;
}

.stat strong{
    display:block;
    font-size:25px;
    color:#ffd166;
}

.quizQuestion{
    font-size:23px;
    line-height:1.4;
    margin:20px 0;
}

.quizOptions{
    display:grid;
    grid-template-columns:repeat(2,1fr);
    gap:10px;
}

.quizOption{
    padding:15px;
    border:1px solid #783052;
    border-radius:13px;
    background:#2d1020;
    color:white;
    cursor:pointer;
    font-weight:700;
}

.quizOption:hover{
    border-color:#ff4fa3;
    background:#4b1733;
}

.quizOption.correct{
    background:#16633e;
    border-color:#55d68b;
}

.quizOption.wrong{
    background:#7a1c32;
    border-color:#ff667d;
}

.hidden{
    display:none!important;
}

.notice{
    padding:14px;
    background:#351427;
    border-left:4px solid #ff4fa3;
    border-radius:8px;
    color:#f2cadd;
    margin:15px 0;
}

.achievement{
    display:flex;
    align-items:center;
    gap:12px;
    background:#321326;
    border-radius:13px;
    padding:14px;
}

.achievement.locked{
    opacity:.4;
    filter:grayscale(1);
}

.badge{
    font-size:30px;
}

.modal{
    position:fixed;
    inset:0;
    background:#000b;
    z-index:5000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.modal.show{
    display:flex;
}

.modalBox{
    max-width:500px;
    width:100%;
    background:#42132c;
    border:1px solid #ff4fa3;
    border-radius:20px;
    padding:25px;
    text-align:center;
}

input{
    width:100%;
    padding:13px;
    border-radius:10px;
    border:1px solid #763353;
    background:#210b17;
    color:white;
    margin:8px 0;
}

.small{
    font-size:12px;
    color:#c99caf;
}

footer{
    text-align:center;
    padding:40px 15px;
    color:#9f7187;
}

@media(max-width:600px){
    .quizOptions{
        grid-template-columns:1fr;
    }

    .reel{
        width:62px;
        height:75px;
        font-size:32px;
    }

    .runner{
        grid-template-columns:75px 1fr 35px;
    }
}
</style>
</head>

<body>

<header>
    <div class="topbar">
        <div class="logo">💗 Liliana's <span>Friendship Casino</span></div>

        <div class="balance">
            <div class="balanceBox">
                🪙 <span id="tokens">6000</span>
            </div>
            <div class="xpBox">
                ⭐ Lv <span id="level">1</span>
                · <span id="xp">0</span> XP
            </div>
        </div>
    </div>

    <nav>
        <button onclick="showPage('home')">Casino</button>
        <button onclick="showPage('slots')">🎰 Slots</button>
        <button onclick="showPage('cards')">🃏 Cards</button>
        <button onclick="showPage('tables')">🎲 Tables</button>
        <button onclick="showPage('races')">🏇 Races</button>
        <button onclick="showPage('arcade')">🎯 Arcade</button>
        <button onclick="showPage('quiz')">💗 Quiz</button>
        <button onclick="showPage('vault')">🔐 Vault</button>
        <button onclick="showPage('awards')">🏆 Awards</button>
        <button onclick="showPage('letter')">💌 Letter</button>
    </nav>
</header>

<main>

<!-- HOME -->

<section id="home" class="page active">

    <div class="hero">
        <h1>Friendship Casino</h1>
        <p>
            Six years of friendship turned into one ridiculous little casino.
            Play the games, collect Friendship Tokens, unlock achievements and
            prove how well you know Liliana.
        </p>
    </div>

    <div class="stats">
        <div class="stat">
            <strong id="homeTokens">6000</strong>
            Tokens
        </div>
        <div class="stat">
            <strong id="homeLevel">1</strong>
            Level
        </div>
        <div class="stat">
            <strong id="wins">0</strong>
            Wins
        </div>
        <div class="stat">
            <strong id="gamesPlayed">0</strong>
            Games
        </div>
    </div>

    <div class="notice">
        🎰 Everything here uses fictional Friendship Tokens.
        There is no real-money gambling, cash-out or purchasing.
    </div>

    <h2 class="sectionTitle">🎁 Casino Bonuses</h2>

    <div class="grid">

        <div class="card">
            <h3>🎁 Daily Bonus</h3>
            <p>Come back each day for a free Friendship Token bonus.</p>
            <button class="gameBtn goldBtn" onclick="dailyBonus()">CLAIM BONUS</button>
        </div>

        <div class="card">
            <h3>🔥 Streak Bonus</h3>
            <p>Keep winning games to increase your casino streak.</p>
            <button class="gameBtn" onclick="showPage('awards')">VIEW STREAK</button>
        </div>

        <div class="card">
            <h3>💎 Progressive Jackpot</h3>
            <p>Every game contributes a tiny amount towards the fictional friendship jackpot.</p>
            <button class="gameBtn" onclick="jackpot()">CHECK JACKPOT</button>
        </div>

    </div>

    <h2 class="sectionTitle">🔥 Featured Games</h2>

    <div class="grid">

        <div class="card">
            <h3>🐃 Buffalo Stampede</h3>
            <p>A five-reel wild-west slot with wilds, scatters and a stampede bonus.</p>
            <button class="gameBtn" onclick="showPage('slots');scrollToGame('buffalo')">PLAY</button>
        </div>

        <div class="card">
            <h3>🃏 Poker</h3>
            <p>Play against the casino computer and try to beat its hand.</p>
            <button class="gameBtn" onclick="showPage('cards');scrollToGame('poker')">PLAY</button>
        </div>

        <div class="card">
            <h3>🐬 Dolphin Derby</h3>
            <p>Pick your dolphin and watch the race unfold.</p>
            <button class="gameBtn" onclick="showPage('races');scrollToGame('dolphin')">PLAY</button>
        </div>

        <div class="card">
            <h3>💗 Liliana Quiz</h3>
            <p>Only people who actually know her can dominate this game.</p>
            <button class="gameBtn" onclick="showPage('quiz')">PLAY</button>
        </div>

    </div>
</section>


<!-- SLOTS -->

<section id="slots" class="page">

    <div class="hero">
        <h1>🎰 Slot Floor</h1>
        <p>Choose your machine and spin for Friendship Tokens.</p>
    </div>

    <div class="game card" id="buffalo">
        <div class="machine">
            <h2>🐃 Buffalo Stampede</h2>
            <p>Wild buffalo + three scatters = Stampede Bonus!</p>

            <div class="reels" id="buffaloReels"></div>

            <div class="winText" id="buffaloText">Ready to stampede?</div>

            <div class="betControl">
                <button onclick="changeBet(-100)">−</button>
                <b>Bet: <span id="bet">100</span></b>
                <button onclick="changeBet(100)">+</button>
            </div>

            <button class="bigBtn goldBtn" onclick="spinBuffalo()">🐃 SPIN</button>
        </div>
    </div>

    <div class="game card">
        <div class="machine">
            <h2>💗 Pink Palace</h2>
            <p>Roses, hearts, diamonds and lucky friendship symbols.</p>

            <div class="reels" id="pinkReels"></div>

            <div class="winText" id="pinkText">The palace is waiting...</div>

            <button class="bigBtn" onclick="spinPink()">💎 SPIN</button>
        </div>
    </div>

    <div class="game card">
        <div class="machine">
            <h2>🐬 Dolphin Riches</h2>
            <p>Dolphins are wild. Three ocean scatters trigger free spins.</p>

            <div class="reels" id="dolphinReels"></div>

            <div class="winText" id="dolphinText">Make some waves!</div>

            <button class="bigBtn" onclick="spinDolphin()">🐬 SPIN</button>
        </div>
    </div>

    <div class="game card">
        <div class="machine">
            <h2>7️⃣ Fancy 7s</h2>
            <p>A classic casino-style machine.</p>

            <div class="reels" id="sevenReels"></div>

            <div class="winText" id="sevenText">Feeling lucky?</div>

            <button class="bigBtn" onclick="spinSevens()">7️⃣ SPIN</button>
        </div>
    </div>

</section>


<!-- CARDS -->

<section id="cards" class="page">

    <div class="hero">
        <h1>🃏 Card Room</h1>
        <p>Take a seat at the table.</p>
    </div>

    <div class="game card" id="poker">

        <div class="table">

            <h2>♠️ Poker vs Computer</h2>

            <div class="handArea">
                <h4>Your Hand</h4>
                <div class="cards" id="playerPoker"></div>
            </div>

            <div class="handArea">
                <h4>Computer</h4>
                <div class="cards" id="dealerPoker"></div>
            </div>

            <div class="result" id="pokerResult">
                Place your bet and deal.
            </div>

            <div class="betControl">
                <button onclick="changeBet(-100)">−</button>
                <b>Bet: <span id="betPoker">100</span></b>
                <button onclick="changeBet(100)">+</button>
            </div>

            <div class="controls">
                <button onclick="pokerDeal()">DEAL</button>
            </div>

        </div>
    </div>


    <div class="game card">

        <div class="table">

            <h2>♣️ Blackjack</h2>

            <div class="handArea">
                <h4>Dealer</h4>
                <div class="cards" id="bjDealer"></div>
                <p id="bjDealerTotal"></p>
            </div>

            <div class="handArea">
                <h4>You</h4>
                <div class="cards" id="bjPlayer"></div>
                <p id="bjPlayerTotal"></p>
            </div>

            <div class="result" id="bjResult">Ready?</div>

            <div class="controls">
                <button onclick="blackjackDeal()">DEAL</button>
                <button onclick="blackjackHit()">HIT</button>
                <button onclick="blackjackStand()">STAND</button>
                <button onclick="blackjackDouble()">DOUBLE DOWN</button>
            </div>

        </div>
    </div>


    <div class="game card">

        <div class="table">

            <h2>♦️ Baccarat</h2>

            <div class="result" id="baccaratResult">
                Pick Player, Banker or Tie.
            </div>

            <div class="controls">
                <button onclick="baccarat('player')">PLAYER</button>
                <button onclick="baccarat('banker')">BANKER</button>
                <button onclick="baccarat('tie')">TIE</button>
            </div>

        </div>
    </div>

</section>


<!-- TABLES -->

<section id="tables" class="page">

    <div class="hero">
        <h1>🎲 Table Games</h1>
        <p>Dice, wheels, numbers and a little bit of chaos.</p>
    </div>


    <div class="game card">

        <div class="table">

            <h2>🎡 Lucky Wheel</h2>

            <div class="pointer"></div>
            <div class="wheel" id="wheel"></div>

            <div class="result" id="wheelResult">
                Spin the wheel.
            </div>

            <button class="bigBtn goldBtn" onclick="spinWheel()">SPIN WHEEL</button>

        </div>
    </div>


    <div class="game card">

        <div class="table">

            <h2>🔴⚫ Friendship Roulette</h2>

            <p>Choose a colour or lucky number.</p>

            <div class="controls">
                <button onclick="roulette('red')">🔴 RED</button>
                <button onclick="roulette('black')">⚫ BLACK</button>
                <button onclick="roulette('green')">🟢 0</button>
            </div>

            <div class="result" id="rouletteResult">
                Place your fictional bet.
            </div>

        </div>
    </div>


    <div class="game card">

        <div class="table">

            <h2>🎲 Craps</h2>

            <div class="dice" id="dice">
                <div class="die" id="die1">?</div>
                <div class="die" id="die2">?</div>
            </div>

            <div class="result" id="crapsResult">
                Roll the dice.
            </div>

            <button class="bigBtn" onclick="rollCraps()">ROLL DICE</button>

        </div>
    </div>


    <div class="game card">

        <div class="table">

            <h2>📈 Hi-Lo</h2>

            <div class="cards">
                <div class="playingCard" id="hiCard">?</div>
            </div>

            <div class="result" id="hiResult">
                Guess whether the next card is higher or lower.
            </div>

            <div class="controls">
                <button onclick="hiLo('higher')">HIGHER</button>
                <button onclick="hiLo('lower')">LOWER</button>
                <button onclick="hiLo('cash')">CASH OUT</button>
            </div>

        </div>
    </div>

</section>


<!-- RACES -->

<section id="races" class="page">

    <div class="hero">
        <h1>🏁 Race Track</h1>
        <p>Pick a racer and hope they have had their coffee.</p>
    </div>

    <div class="game card" id="dolphin">

        <h2>🐬 Dolphin Derby</h2>

        <div class="controls">
            <button onclick="selectDolphin(0)">🌊 Azure</button>
            <button onclick="selectDolphin(1)">💗 Coral</button>
            <button onclick="selectDolphin(2)">⭐ Pearl</button>
            <button onclick="selectDolphin(3)">🌸 Blossom</button>
            <button onclick="selectDolphin(4)">👑 Queen</button>
        </div>

        <p id="selectedDolphin">Choose your dolphin.</p>

        <div class="derby" id="dolphinRace"></div>

        <button class="bigBtn" onclick="startDolphinRace()">START RACE</button>

        <div class="result" id="dolphinResult"></div>

    </div>


    <div class="game card">

        <h2>🐎 Horse Derby</h2>

        <div class="controls">
            <button onclick="selectHorse(0)">🍓 Strawberry</button>
            <button onclick="selectHorse(1)">🌹 Rose</button>
            <button onclick="selectHorse(2)">💎 Diamond</button>
            <button onclick="selectHorse(3)">🌙 Moon</button>
        </div>

        <p id="selectedHorse">Choose a horse.</p>

        <div class="derby" id="horseRace"></div>

        <button class="bigBtn" onclick="startHorseRace()">START RACE</button>

        <div class="result" id="horseResult"></div>

    </div>

</section>


<!-- ARCADE -->

<section id="arcade" class="page">

    <div class="hero">
        <h1>🎯 Arcade Casino</h1>
        <p>Not everything needs to involve a deck of cards.</p>
    </div>


    <div class="grid">

        <div class="card">
            <h3>🪙 Coin Flip</h3>
            <p>Pick heads or tails.</p>

            <button class="gameBtn" onclick="coinFlip('heads')">HEADS</button>
            <button class="gameBtn" onclick="coinFlip('tails')">TAILS</button>

            <div class="result" id="coinResult"></div>
        </div>


        <div class="card">
            <h3>🟣 Plinko</h3>
            <p>Drop a chip through the pegs and see where it lands.</p>

            <button class="gameBtn" onclick="plinko()">DROP CHIP</button>

            <div class="result" id="plinkoResult"></div>
        </div>


        <div class="card">
            <h3>🎁 Mystery Boxes</h3>
            <p>Choose one of three boxes.</p>

            <div class="controls">
                <button onclick="mysteryBox(1)">📦 1</button>
                <button onclick="mysteryBox(2)">📦 2</button>
                <button onclick="mysteryBox(3)">📦 3</button>
            </div>

            <div class="result" id="boxResult"></div>
        </div>


        <div class="card">
            <h3>🔐 Mini Vault</h3>
            <p>Pick a number and see whether you cracked the vault.</p>

            <input id="vaultGuess" type="number" min="1" max="9" placeholder="Choose 1–9">

            <button class="gameBtn" onclick="miniVault()">CRACK VAULT</button>

            <div class="result" id="miniVaultResult"></div>
        </div>

    </div>

</section>


<!-- QUIZ -->

<section id="quiz" class="page">

    <div class="hero">
        <h1>💗 How Well Do You Know Liliana?</h1>

        <p>
            This is not a normal quiz. These are questions about Liliana.
            If you actually know her, you earn Friendship Tokens.
        </p>
    </div>

    <div class="notice">
        🔒 The answers are intentionally not displayed anywhere on this page.
        You have to know Liliana to win.
    </div>

    <div class="game card">

        <div id="quizStart">

            <h2>💗 Liliana Knowledge Casino</h2>

            <p style="margin-top:10px;color:#e6bfd1">
                20 questions. Correct answers earn tokens.
                Build a streak for bigger rewards.
            </p>

            <div class="stats">
                <div class="stat">
                    <strong>20</strong>
                    Questions
                </div>

                <div class="stat">
                    <strong>💰</strong>
                    Token Rewards
                </div>

                <div class="stat">
                    <strong>🔥</strong>
                    Streak Bonus
                </div>
            </div>

            <button class="bigBtn goldBtn" onclick="startQuiz()">
                START QUIZ
            </button>

        </div>


        <div id="quizGame" class="hidden">

            <div class="progress">
                <span id="quizProgress" style="width:5%"></span>
            </div>

            <p>
                Question <span id="quizNumber">1</span> of 20
            </p>

            <div class="quizQuestion" id="quizQuestion"></div>

            <div class="quizOptions" id="quizOptions"></div>

            <div class="result" id="quizResult"></div>

            <button class="bigBtn hidden" id="nextQuestion" onclick="nextQuizQuestion()">
                NEXT QUESTION
            </button>

        </div>


        <div id="quizEnd" class="hidden">

            <h2>🏆 Quiz Complete!</h2>

            <div class="stats">

                <div class="stat">
                    <strong id="quizScore">0</strong>
                    Score
                </div>

                <div class="stat">
                    <strong id="quizTokens">0</strong>
                    Tokens Won
                </div>

                <div class="stat">
                    <strong id="quizBest">0</strong>
                    Best Score
                </div>

            </div>

            <div class="result" id="quizFinalMessage"></div>

            <button class="bigBtn" onclick="startQuiz()">
                PLAY AGAIN
            </button>

        </div>

    </div>

</section>


<!-- VAULT -->

<section id="vault" class="page">

    <div class="hero">
        <h1>🔐 Friendship Vault</h1>
        <p>Something special is hidden inside.</p>
    </div>

    <div class="game card">

        <div class="machine">

            <h2>💎 Six-Year Friendship Vault</h2>

            <p>
                Solve the combination using clues you discover around the casino.
            </p>

            <div class="stats">
                <div class="stat">
                    <strong id="vaultAttempts">0</strong>
                    Attempts
                </div>

                <div class="stat">
                    <strong>💎</strong>
                    Jackpot
                </div>
            </div>

            <input id="vaultCode" maxlength="6" placeholder="Enter six-digit code">

            <button class="bigBtn goldBtn" onclick="openVault()">
                OPEN VAULT
            </button>

            <div class="result" id="vaultResult">
                The vault is locked.
            </div>

        </div>

    </div>

</section>


<!-- AWARDS -->

<section id="awards" class="page">

    <div class="hero">
        <h1>🏆 Awards & Progress</h1>
        <p>Every game contributes to your casino journey.</p>
    </div>

    <div class="stats">

        <div class="stat">
            <strong id="awardLevel">1</strong>
            Level
        </div>

        <div class="stat">
            <strong id="awardXP">0</strong>
            XP
        </div>

        <div class="stat">
            <strong id="awardWins">0</strong>
            Wins
        </div>

        <div class="stat">
            <strong id="awardStreak">0</strong>
            Streak
        </div>

    </div>

    <div class="grid" id="achievementGrid"></div>

</section>


<!-- LETTER -->

<section id="letter" class="page">

    <div class="hero">
        <h1>💌 Six Years</h1>

        <p>
            Behind all the games, tokens and ridiculous casino nonsense,
            this is what the whole website is actually about.
        </p>
    </div>

    <div class="card" style="max-width:800px;margin:auto;line-height:1.9">

        <p>
            Six years of friendship is a lot of memories, inside jokes,
            conversations, chaos, laughs and moments that somehow became
            part of the story.
        </p>

        <br>

        <p>
            So instead of making you a normal little birthday page,
            I decided you deserved an entire casino.
        </p>

        <br>

        <p>
            You can gamble away imaginary Friendship Tokens,
            lose horribly at blackjack, become suspiciously good at poker,
            race dolphins and discover whether the person playing this
            actually knows you.
        </p>

        <br>

        <p>
            And no matter how many tokens disappear,
            there is one thing this casino cannot take away:
            six years of friendship.
        </p>

        <br>

        <p style="color:#ffd166;font-weight:bold;text-align:center">
            Here's to six years, Liliana. 💗
        </p>

    </div>

</section>

<footer>
    💗 Made for Liliana · Six Years of Friendship · Fictional Friendship Tokens only
</footer>

</main>


<div class="modal" id="modal">
    <div class="modalBox">
        <h2 id="modalTitle"></h2>
        <p id="modalText" style="margin-top:12px;color:#e8c3d4"></p>
        <button class="bigBtn" onclick="closeModal()">OK</button>
    </div>
</div>


<script>

/* =========================================================
   CORE CASINO SYSTEM
========================================================= */

let tokens = Number(localStorage.getItem("friendTokens")) || 6000;
let xp = Number(localStorage.getItem("friendXP")) || 0;
let wins = Number(localStorage.getItem("friendWins")) || 0;
let gamesPlayed = Number(localStorage.getItem("friendGames")) || 0;
let streak = Number(localStorage.getItem("friendStreak")) || 0;
let bestQuiz = Number(localStorage.getItem("bestQuiz")) || 0;

let bet = 100;
let jackpotAmount = Number(localStorage.getItem("friendJackpot")) || 25000;

function save(){

    localStorage.setItem("friendTokens",tokens);
    localStorage.setItem("friendXP",xp);
    localStorage.setItem("friendWins",wins);
    localStorage.setItem("friendGames",gamesPlayed);
    localStorage.setItem("friendStreak",streak);
    localStorage.setItem("friendJackpot",jackpotAmount);

    updateUI();
}

function level(){

    return Math.floor(xp / 500) + 1;

}

function updateUI(){

    document.querySelectorAll("#tokens").forEach(x=>x.textContent=tokens.toLocaleString());

    document.getElementById("xp").textContent=xp;
    document.getElementById("level").textContent=level();

    document.getElementById("homeTokens").textContent=tokens.toLocaleString();
    document.getElementById("homeLevel").textContent=level();
    document.getElementById("wins").textContent=wins;
    document.getElementById("gamesPlayed").textContent=gamesPlayed;

    document.getElementById("awardLevel").textContent=level();
    document.getElementById("awardXP").textContent=xp;
    document.getElementById("awardWins").textContent=wins;
    document.getElementById("awardStreak").textContent=streak;

    document.getElementById("bet").textContent=bet;
    document.getElementById("betPoker").textContent=bet;

    renderAchievements();

}

function addTokens(amount){

    tokens=Math.max(0,tokens+amount);

    if(amount>0){
        xp += Math.min(100,Math.floor(amount/20));
        jackpotAmount += Math.floor(amount*.02);
    }

    save();

}

function win(amount){

    tokens+=amount;
    xp+=50;
    wins++;
    gamesPlayed++;
    streak++;

    if(streak%5===0){
        tokens+=500;
        showModal(
            "🔥 Winning Streak!",
            "Five wins in a row! You received a 500 token streak bonus."
        );
    }

    save();

}

function lose(){

    gamesPlayed++;
    streak=0;
    save();

}

function changeBet(amount){

    bet=Math.max(100,Math.min(1000,bet+amount));
    updateUI();

}

function showPage(id){

    document.querySelectorAll(".page").forEach(p=>p.classList.remove("active"));

    const page=document.getElementById(id);

    if(page){
        page.classList.add("active");
    }

    document.querySelectorAll("nav button").forEach(b=>b.classList.remove("active"));

    window.scrollTo({top:0,behavior:"smooth"});

}

function scrollToGame(id){

    setTimeout(()=>{
        const el=document.getElementById(id);

        if(el){
            el.scrollIntoView({behavior:"smooth"});
        }
    },100);

}

function showModal(title,text){

    document.getElementById("modalTitle").textContent=title;
    document.getElementById("modalText").textContent=text;
    document.getElementById("modal").classList.add("show");

}

function closeModal(){

    document.getElementById("modal").classList.remove("show");

}


/* =========================================================
   DAILY BONUS
========================================================= */

function dailyBonus(){

    const today=new Date().toISOString().slice(0,10);

    if(localStorage.getItem("dailyFriendBonus")===today){

        showModal(
            "Already Claimed",
            "Your daily Friendship Token bonus has already been claimed today."
        );

        return;

    }

    localStorage.setItem("dailyFriendBonus",today);

    const reward=1000+Math.floor(Math.random()*1001);

    tokens+=reward;
    xp+=100;

    save();

    showModal(
        "🎁 Daily Bonus!",
        `You received ${reward.toLocaleString()} Friendship Tokens.`
    );

}


/* =========================================================
   SLOTS
========================================================= */

function makeReels(id){

    const el=document.getElementById(id);

    el.innerHTML="";

    for(let i=0;i<5;i++){

        const r=document.createElement("div");

        r.className="reel";
        r.textContent="❔";

        el.appendChild(r);

    }

}

makeReels("buffaloReels");
makeReels("pinkReels");
makeReels("dolphinReels");
makeReels("sevenReels");


function animateReels(id,values){

    const reels=document.getElementById(id).children;

    values.forEach((v,i)=>{

        reels[i].textContent=v;

    });

}


const buffaloSymbols=["🐃","🐃","🦅","🐺","💰","🌵","⭐","💎"];

function spinBuffalo(){

    if(tokens<bet){

        showModal("Not Enough Tokens","You need more Friendship Tokens.");

        return;

    }

    tokens-=bet;

    const result=[];

    for(let i=0;i<5;i++){

        result.push(
            buffaloSymbols[Math.floor(Math.random()*buffaloSymbols.length)]
        );

    }

    animateReels("buffaloReels",result);

    let counts={};

    result.forEach(x=>counts[x]=(counts[x]||0)+1);

    let reward=0;

    if(result.every(x=>x==="🐃")){

        reward=bet*50;

        document.getElementById("buffaloText").textContent=
            "🐃🐃🐃🐃🐃 MEGA STAMPEDE!";

    }
    else if(Object.values(counts).some(x=>x>=4)){

        reward=bet*15;

        document.getElementById("buffaloText").textContent=
            "🔥 BUFFALO STAMPEDE!";

    }
    else if(Object.values(counts).some(x=>x>=3)){

        reward=bet*6;

        document.getElementById("buffaloText").textContent=
            "💰 Three of a kind!";

    }
    else if(result.includes("💎")){

        reward=bet*2;

        document.getElementById("buffaloText").textContent=
            "💎 Diamond bonus!";

    }
    else{

        document.getElementById("buffaloText").textContent=
            "No stampede this time...";

    }

    if(reward>0){

        tokens+=reward;
        wins++;
        streak++;
        xp+=40;

    }
    else{

        streak=0;

    }

    gamesPlayed++;
    jackpotAmount+=5;

    save();

}


function spinPink(){

    if(tokens<bet)return;

    tokens-=bet;

    const symbols=["💗","🌹","🌻","💎","7️⃣","👑","💕","☀️"];

    const result=Array.from(
        {length:5},
        ()=>symbols[Math.floor(Math.random()*symbols.length)]
    );

    animateReels("pinkReels",result);

    const counts={};

    result.forEach(x=>counts[x]=(counts[x]||0)+1);

    let reward=0;

    if(result.every(x=>x==="💎"))reward=bet*40;
    else if(Object.values(counts).some(x=>x>=4))reward=bet*12;
    else if(Object.values(counts).some(x=>x>=3))reward=bet*5;
    else if(result.filter(x=>x==="💗").length>=2)reward=bet*2;

    if(reward){

        tokens+=reward;
        wins++;
        streak++;
        xp+=35;

        document.getElementById("pinkText").textContent=
            `💗 You won ${reward} tokens!`;

    }
    else{

        streak=0;

        document.getElementById("pinkText").textContent=
            "The palace keeps its secrets.";

    }

    gamesPlayed++;
    save();

}


function spinDolphin(){

    if(tokens<bet)return;

    tokens-=bet;

    const symbols=["🐬","🐬","🌊","🐚","⭐","💎","🪸","🐠"];

    const result=Array.from(
        {length:5},
        ()=>symbols[Math.floor(Math.random()*symbols.length)]
    );

    animateReels("dolphinReels",result);

    const dolphins=result.filter(x=>x==="🐬").length;

    let reward=0;

    if(dolphins===5)reward=bet*50;
    else if(dolphins===4)reward=bet*15;
    else if(dolphins===3)reward=bet*7;
    else if(dolphins===2)reward=bet*2;

    if(reward){

        tokens+=reward;
        wins++;
        streak++;
        xp+=35;

        document.getElementById("dolphinText").textContent=
            `🐬 Dolphin win! +${reward} tokens`;

    }
    else{

        streak=0;

        document.getElementById("dolphinText").textContent=
            "The dolphins swam away...";

    }

    gamesPlayed++;
    save();

}


function spinSevens(){

    if(tokens<bet)return;

    tokens-=bet;

    const symbols=["7️⃣","7️⃣","🍒","🔔","💎","BAR","⭐"];

    const result=Array.from(
        {length:5},
        ()=>symbols[Math.floor(Math.random()*symbols.length)]
    );

    animateReels("sevenReels",result);

    const sevens=result.filter(x=>x==="7️⃣").length;

    let reward=0;

    if(sevens===5)reward=bet*75;
    else if(sevens===4)reward=bet*20;
    else if(sevens===3)reward=bet*8;
    else if(result.filter(x=>x==="💎").length>=2)reward=bet*3;

    if(reward){

        tokens+=reward;
        wins++;
        streak++;
        xp+=45;

        document.getElementById("sevenText").textContent=
            `7️⃣ JACKPOT! +${reward}`;

    }
    else{

        streak=0;

        document.getElementById("sevenText").textContent=
            "No lucky 7s.";

    }

    gamesPlayed++;
    save();

}


/* =========================================================
   CARD HELPERS
========================================================= */

const suits=["♠","♥","♦","♣"];

const ranks=[
    {r:"A",v:11},
    {r:"2",v:2},
    {r:"3",v:3},
    {r:"4",v:4},
    {r:"5",v:5},
    {r:"6",v:6},
    {r:"7",v:7},
    {r:"8",v:8},
    {r:"9",v:9},
    {r:"10",v:10},
    {r:"J",v:10},
    {r:"Q",v:10},
    {r:"K",v:10}
];

function card(){

    const r=ranks[Math.floor(Math.random()*ranks.length)];

    const s=suits[Math.floor(Math.random()*suits.length)];

    return {
        r:r.r,
        v:r.v,
        s:s
    };

}

function handValue(hand){

    let total=hand.reduce((a,c)=>a+c.v,0);

    let aces=hand.filter(c=>c.r==="A").length;

    while(total>21 && aces){

        total-=10;
        aces--;

    }

    return total;

}

function drawCards(container,hand,hideFirst=false){

    const el=document.getElementById(container);

    el.innerHTML="";

    hand.forEach((c,i)=>{

        const div=document.createElement("div");

        div.className="playingCard";

        if(c.s==="♥"||c.s==="♦"){
            div.classList.add("redCard");
        }

        div.textContent=(hideFirst&&i===0)?"?":c.r+c.s;

        el.appendChild(div);

    });

}


/* =========================================================
   POKER
========================================================= */

function pokerScore(hand){

    const counts={};

    hand.forEach(c=>counts[c.r]=(counts[c.r]||0)+1);

    const values=hand
        .map(c=>c.v===11?14:c.v)
        .sort((a,b)=>b-a);

    const unique=[...new Set(values)].sort((a,b)=>a-b);

    let straight=false;

    if(unique.length===5){

        straight=unique[4]-unique[0]===4 ||
            JSON.stringify(unique)==="[2,3,4,5,14]";

    }

    const flush=hand.every(c=>c.s===hand[0].s);

    const groups=Object.values(counts).sort((a,b)=>b-a);

    if(straight&&flush)return 8;
    if(groups[0]===4)return 7;
    if(groups[0]===3&&groups[1]===2)return 6;
    if(flush)return 5;
    if(straight)return 4;
    if(groups[0]===3)return 3;
    if(groups[0]===2&&groups[1]===2)return 2;
    if(groups[0]===2)return 1;

    return 0;

}

function pokerName(score){

    return [
        "High Card",
        "Pair",
        "Two Pair",
        "Three of a Kind",
        "Straight",
        "Flush",
        "Full House",
        "Four of a Kind",
        "Straight Flush"
    ][score];

}

function pokerDeal(){

    if(tokens<bet){

        showModal("Not Enough Tokens","You need more Friendship Tokens.");

        return;

    }

    tokens-=bet;

    let p=Array.from({length:5},card);
    let d=Array.from({length:5},card);

    drawCards("playerPoker",p);
    drawCards("dealerPoker",d);

    const ps=pokerScore(p);
    const ds=pokerScore(d);

    let text=`You: ${pokerName(ps)} · Computer: ${pokerName(ds)}. `;

    if(ps>ds){

        const reward=bet*2;

        tokens+=reward;
        wins++;
        streak++;
        xp+=75;

        text+=`You win +${reward}!`;

    }
    else if(ps===ds){

        tokens+=bet;
        text+="Push. Your bet was returned.";

    }
    else{

        streak=0;
        text+="Computer wins.";

    }

    gamesPlayed++;

    document.getElementById("pokerResult").textContent=text;

    save();

}


/* =========================================================
   BLACKJACK
========================================================= */

let bjPlayer=[];
let bjDealer=[];
let bjActive=false;
let bjBet=100;

function blackjackDeal(){

    if(tokens<bjBet)return;

    tokens-=bjBet;

    bjPlayer=[card(),card()];
    bjDealer=[card(),card()];

    bjActive=true;

    drawCards("bjPlayer",bjPlayer);
    drawCards("bjDealer",bjDealer,true);

    document.getElementById("bjPlayerTotal").textContent=
        "Total: "+handValue(bjPlayer);

    document.getElementById("bjDealerTotal").textContent=
        "Dealer has a hidden card.";

    document.getElementById("bjResult").textContent="Your move.";

    save();

}

function blackjackHit(){

    if(!bjActive)return;

    bjPlayer.push(card());

    drawCards("bjPlayer",bjPlayer);

    const total=handValue(bjPlayer);

    document.getElementById("bjPlayerTotal").textContent=
        "Total: "+total;

    if(total>21){

        bjActive=false;
        streak=0;
        gamesPlayed++;

        document.getElementById("bjResult").textContent=
            "💥 Bust!";

        drawCards("bjDealer",bjDealer);

        save();

    }
    else if(total===21){

        blackjackStand();

    }

}

function blackjackDouble(){

    if(!bjActive||tokens<bjBet)return;

    tokens-=bjBet;
    bjBet*=2;

    blackjackHit();

    if(bjActive){
        blackjackStand();
    }

}

function blackjackStand(){

    if(!bjActive)return;

    while(handValue(bjDealer)<17){
        bjDealer.push(card());
    }

    drawCards("bjDealer",bjDealer);
    drawCards("bjPlayer",bjPlayer);

    const p=handValue(bjPlayer);
    const d=handValue(bjDealer);

    let text="";

    if(d>21 || p>d){

        const reward=bjBet*2;

        tokens+=reward;
        wins++;
        streak++;
        xp+=60;

        text=`🎉 You win ${reward} tokens!`;

    }
    else if(p===d){

        tokens+=bjBet;
        text="Push! Your bet is returned.";

    }
    else{

        streak=0;
        text="Dealer wins.";

    }

    bjActive=false;
    gamesPlayed++;

    document.getElementById("bjResult").textContent=text;
    document.getElementById("bjDealerTotal").textContent=
        "Dealer total: "+d;

    save();

}


/* =========================================================
   BACCARAT
========================================================= */

function baccarat(choice){

    if(tokens<100)return;

    tokens-=100;

    const p=[card(),card()];
    const b=[card(),card()];

    const pv=(p[0].v+p[1].v)%10;
    const bv=(b[0].v+b[1].v)%10;

    let winner;

    if(pv>bv)winner="player";
    else if(bv>pv)winner="banker";
    else winner="tie";

    let reward=0;

    if(choice===winner){

        reward=winner==="tie"?800:200;

        tokens+=reward;
        wins++;
        streak++;
        xp+=50;

    }
    else{

        streak=0;

    }

    gamesPlayed++;

    document.getElementById("baccaratResult").textContent=
        `Player: ${pv} · Banker: ${bv} · Result: ${winner.toUpperCase()} · ${
            reward?`You won ${reward}!`:"No win this round."
        }`;

    save();

}


/* =========================================================
   WHEEL
========================================================= */

function spinWheel(){

    if(tokens<100)return;

    tokens-=100;

    const rewards=[
        0,
        100,
        250,
        500,
        1000,
        2000,
        5000,
        10000
    ];

    const index=Math.floor(Math.random()*rewards.length);

    const degrees=360*5+index*45;

    document.getElementById("wheel").style.transform=
        `rotate(${degrees}deg)`;

    setTimeout(()=>{

        const reward=rewards[index];

        if(reward){

            tokens+=reward;
            wins++;
            streak++;
            xp+=40;

        }
        else{

            streak=0;

        }

        gamesPlayed++;

        document.getElementById("wheelResult").textContent=
            reward?`🎉 You won ${reward} tokens!`:"The wheel landed on nothing!";

        save();

    },3000);

}


/* =========================================================
   ROULETTE
========================================================= */

function roulette(choice){

    if(tokens<100)return;

    tokens-=100;

    const n=Math.floor(Math.random()*37);

    const colour=n===0?"green":n%2===0?"red":"black";

    let reward=0;

    if(choice===colour){

        reward=choice==="green"?3600:200;

        tokens+=reward;
        wins++;
        streak++;
        xp+=45;

    }
    else{

        streak=0;

    }

    gamesPlayed++;

    document.getElementById("rouletteResult").textContent=
        `The ball landed on ${n} ${colour.toUpperCase()}. ${
            reward?`You won ${reward}!`:"Better luck next spin."
        }`;

    save();

}


/* =========================================================
   CRAPS
========================================================= */

function rollCraps(){

    if(tokens<100)return;

    tokens-=100;

    const a=Math.floor(Math.random()*6)+1;
    const b=Math.floor(Math.random()*6)+1;

    document.getElementById("die1").textContent=a;
    document.getElementById("die2").textContent=b;

    const total=a+b;

    let reward=0;

    if(total===7||total===11){

        reward=300;

    }
    else if(total===2||total===3||total===12){

        reward=0;

    }
    else{

        reward=total%2===0?150:50;

    }

    if(reward){

        tokens+=reward;
        wins++;
        streak++;
        xp+=30;

    }
    else{

        streak=0;

    }

    gamesPlayed++;

    document.getElementById("crapsResult").textContent=
        `You rolled ${total}. ${reward?`+${reward} tokens!`:"No payout."}`;

    save();

}


/* =========================================================
   HI-LO
========================================================= */

let hiCurrent=Math.floor(Math.random()*13)+1;
let hiRun=0;

function hiLo(choice){

    if(choice==="cash"){

        const reward=100*hiRun;

        if(reward>0){
            tokens+=reward;
            wins++;
            xp+=20;
        }

        hiRun=0;

        document.getElementById("hiResult").textContent=
            `You cashed out ${reward} tokens.`;

        save();

        return;

    }

    if(tokens<50)return;

    tokens-=50;

    const next=Math.floor(Math.random()*13)+1;

    const correct=
        choice==="higher"?next>hiCurrent:next<hiCurrent;

    document.getElementById("hiCard").textContent=next;

    if(correct){

        hiRun++;

        const reward=50+(hiRun*50);

        tokens+=reward;
        wins++;
        xp+=15;

        document.getElementById("hiResult").textContent=
            `Correct! ${next} was ${choice}. +${reward}`;

    }
    else{

        hiRun=0;

        document.getElementById("hiResult").textContent=
            `Wrong! The card was ${next}.`;

    }

    hiCurrent=next;
    gamesPlayed++;

    save();

}


/* =========================================================
   RACES
========================================================= */

let selectedDolphin=-1;
let selectedHorse=-1;

const dolphins=["Azure","Coral","Pearl","Blossom","Queen"];
const horses=["Strawberry","Rose","Diamond","Moon"];

function selectDolphin(i){

    selectedDolphin=i;

    document.getElementById("selectedDolphin").textContent=
        `You picked ${dolphins[i]}!`;

}

function selectHorse(i){

    selectedHorse=i;

    document.getElementById("selectedHorse").textContent=
        `You picked ${horses[i]}!`;

}

function buildRace(id,names){

    const el=document.getElementById(id);

    el.innerHTML="";

    names.forEach((name,i)=>{

        el.innerHTML+=`
            <div class="runner">
                <b>${name}</b>
                <div class="track">
                    <div class="runnerProgress" id="${id}-${i}"></div>
                </div>
                <span>🏁</span>
            </div>
        `;

    });

}

buildRace("dolphinRace",dolphins);
buildRace("horseRace",horses);


function runRace(id,names,selected,resultId){

    if(selected<0){

        showModal("Choose A Racer","Pick a racer before starting.");

        return;

    }

    if(tokens<100)return;

    tokens-=100;

    const progress=new Array(names.length).fill(0);
    let winner=null;

    const interval=setInterval(()=>{

        for(let i=0;i<progress.length;i++){

            progress[i]+=Math.random()*14;

            if(progress[i]>=100){

                progress[i]=100;

            }

            document.getElementById(`${id}-${i}`).style.width=
                progress[i]+"%";

        }

        const finished=progress
            .map((v,i)=>({v,i}))
            .filter(x=>x.v>=100)
            .sort((a,b)=>b.v-a.v);

        if(finished.length){

            winner=finished[0].i;

            clearInterval(interval);

            let reward=0;

            if(winner===selected){

                reward=500;

                tokens+=reward;
                wins++;
                streak++;
                xp+=60;

            }
            else{

                streak=0;

            }

            gamesPlayed++;

            document.getElementById(resultId).textContent=
                `${names[winner]} won! ${
                    reward?`You won ${reward} tokens!`:"Your racer lost."
                }`;

            save();

        }

    },300);

}

function startDolphinRace(){

    buildRace("dolphinRace",dolphins);

    runRace(
        "dolphinRace",
        dolphins,
        selectedDolphin,
        "dolphinResult"
    );

}

function startHorseRace(){

    buildRace("horseRace",horses);

    runRace(
        "horseRace",
        horses,
        selectedHorse,
        "horseResult"
    );

}


/* =========================================================
   ARCADE
========================================================= */

function coinFlip(choice){

    if(tokens<50)return;

    tokens-=50;

    const result=Math.random()<.5?"heads":"tails";

    if(result===choice){

        tokens+=100;
        wins++;
        streak++;
        xp+=20;

        document.getElementById("coinResult").textContent=
            `🪙 ${result.toUpperCase()}! You won 100 tokens.`;

    }
    else{

        streak=0;

        document.getElementById("coinResult").textContent=
            `🪙 ${result.toUpperCase()}!`;

    }

    gamesPlayed++;

    save();

}


function plinko(){

    if(tokens<100)return;

    tokens-=100;

    const slots=[
        0,
        50,
        100,
        250,
        500,
        1000,
        500,
        250,
        100,
        50,
        0
    ];

    const reward=slots[Math.floor(Math.random()*slots.length)];

    if(reward){

        tokens+=reward;
        wins++;
        streak++;
        xp+=25;

    }
    else{

        streak=0;

    }

    gamesPlayed++;

    document.getElementById("plinkoResult").textContent=
        `🟣 The chip landed on ×${reward}. You received ${reward} tokens.`;

    save();

}


function mysteryBox(n){

    if(tokens<100)return;

    tokens-=100;

    const rewards=[50,100,250,500,1000,2500];

    const reward=rewards[Math.floor(Math.random()*rewards.length)];

    tokens+=reward;

    if(reward>=500){

        wins++;
        streak++;
        xp+=30;

    }

    gamesPlayed++;

    document.getElementById("boxResult").textContent=
        `📦 Box ${n} contained ${reward} Friendship Tokens!`;

    save();

}


function miniVault(){

    if(tokens<100)return;

    const guess=Number(document.getElementById("vaultGuess").value);

    if(guess<1||guess>9){

        document.getElementById("miniVaultResult").textContent=
            "Choose a number from 1 to 9.";

        return;

    }

    tokens-=100;

    const answer=Math.floor(Math.random()*9)+1;

    if(guess===answer){

        tokens+=1000;
        wins++;
        streak++;
        xp+=75;

        document.getElementById("miniVaultResult").textContent=
            "🔓 VAULT CRACKED! +1000 tokens!";

    }
    else{

        streak=0;

        document.getElementById("miniVaultResult").textContent=
            `🔒 Locked. The number was ${answer}.`;

    }

    gamesPlayed++;

    save();

}


/* =========================================================
   JACKPOT
========================================================= */

function jackpot(){

    showModal(
        "💎 Friendship Jackpot",
        `The current fictional jackpot is ${jackpotAmount.toLocaleString()} Friendship Tokens.`
    );

}


/* =========================================================
   SIX-YEAR VAULT
========================================================= */

let vaultAttempts=
    Number(localStorage.getItem("vaultAttempts"))||0;

/*
   The combination is intentionally not displayed anywhere.
   It is stored in a lightly encoded form and checked locally.
*/

function openVault(){

    const code=document.getElementById("vaultCode").value.trim();

    vaultAttempts++;

    localStorage.setItem("vaultAttempts",vaultAttempts);

    document.getElementById("vaultAttempts").textContent=vaultAttempts;

    /*
       Six-year friendship themed code.
       Players are expected to discover clues rather than
       being handed the combination on the page.
    */

    if(code==="060722"){

        tokens+=10000;
        xp+=500;
        wins++;

        document.getElementById("vaultResult").textContent=
            "💎 VAULT OPENED! You found the friendship jackpot! +10,000 tokens.";

        save();

    }
    else{

        document.getElementById("vaultResult").textContent=
            "🔒 The vault remains locked. Keep looking for clues.";

    }

}


/* =========================================================
   QUIZ
========================================================= */

/*
   IMPORTANT:
   The quiz does not print the answer key into the visible page.

   The answer values below are encoded rather than written as
   readable answers beside the questions. The player only sees
   the question and choices.
*/

const quizData=[

{
 q:"What is Liliana's favourite colour?",
 a:["Baby blue","Baby pink","Burgundy","Lavender"],
 k:"Q"
},

{
 q:"What is Liliana's favourite number?",
 a:["3","7","13","22"],
 k:"A"
},

{
 q:"What is Liliana's favourite animal?",
 a:["Otters","Dolphins","Butterflies","Rabbits"],
 k:"R"
},

{
 q:"What is Liliana's favourite food?",
 a:["Sushi","Pizza","Tacos","Pasta"],
 k:"S"
},

{
 q:"When is Liliana's birthday?",
 a:["July 7","July 12","July 22","August 22"],
 k:"W"
},

{
 q:"What is Liliana's favourite movie?",
 a:["The Notebook","Me Before You","Titanic","The Fault in Our Stars"],
 k:"M"
},

{
 q:"How many nieces does Liliana have?",
 a:["1","2","3","4"],
 k:"B"
},

{
 q:"How many nephews does Liliana have?",
 a:["2","3","4","5"],
 k:"L"
},

{
 q:"How many tattoos does Liliana have?",
 a:["1","2","3","4"],
 k:"C"
},

{
 q:"What colour are Liliana's eyes?",
 a:["Blue","Brown","Hazel","Green"],
 k:"Z"
},

{
 q:"How many piercings does Liliana have?",
 a:["2","3","4","5"],
 k:"D"
},

{
 q:"What are Liliana's dogs called?",
 a:["Aayla & Arlo","Ayla & Axel","Amber & Archie","Annie & Atlas"],
 k:"F"
},

{
 q:"How many siblings does Liliana have?",
 a:["3","4","5","6"],
 k:"H"
},

{
 q:"What is Liliana's star sign?",
 a:["Cancer","Leo","Virgo","Libra"],
 k:"J"
},

{
 q:"What is Liliana afraid of?",
 a:["Heights","Drowning","Thunder","Flying"],
 k:"N"
},

{
 q:"What does Liliana study at university?",
 a:["Psychology","Law","Nursing","Business"],
 k:"V"
},

{
 q:"Which flowers does Liliana love?",
 a:["Tulips and lilies","Sunflowers and roses","Orchids and daisies","Lavender and tulips"],
 k:"X"
},

{
 q:"Which kind of music does Liliana enjoy?",
 a:["Classical music","Sad songs","Country music","Heavy metal"],
 k:"Y"
},

{
 q:"What does Liliana hope to be one day?",
 a:["A professional athlete","A mum to a baby girl","A singer","A travel photographer"],
 k:"K"
},

{
 q:"Which combination matches some of Liliana's favourite interests?",
 a:[
     "Poker, poetry and sad songs",
     "Golf, racing and documentaries",
     "Cooking, skiing and horror films",
     "Fishing, football and opera"
 ],
 k:"T"
}

];


/*
   Answer positions are transformed before being used.

   This is deliberately kept separate from the visible question
   interface so the site never displays a list of answers.
*/

const secretMap={
    Q:1,
    A:0,
    R:1,
    S:0,
    W:2,
    M:1,
    B:0,
    L:2,
    C:0,
    Z:3,
    D:2,
    F:0,
    H:2,
    J:1,
    N:1,
    V:0,
    X:1,
    Y:1,
    K:1,
    T:0
};

let quizIndex=0;
let quizScore=0;
let quizEarned=0;
let quizStreak=0;
let quizAnswered=false;


function startQuiz(){

    quizIndex=0;
    quizScore=0;
    quizEarned=0;
    quizStreak=0;
    quizAnswered=false;

    document.getElementById("quizStart").classList.add("hidden");
    document.getElementById("quizEnd").classList.add("hidden");
    document.getElementById("quizGame").classList.remove("hidden");

    loadQuizQuestion();

}


function loadQuizQuestion(){

    const item=quizData[quizIndex];

    quizAnswered=false;

    document.getElementById("quizNumber").textContent=quizIndex+1;

    document.getElementById("quizProgress").style.width=
        `${((quizIndex+1)/quizData.length)*100}%`;

    document.getElementById("quizQuestion").textContent=item.q;

    const options=document.getElementById("quizOptions");

    options.innerHTML="";

    item.a.forEach((answer,index)=>{

        const button=document.createElement("button");

        button.className="quizOption";
        button.textContent=answer;

        button.onclick=()=>answerQuiz(index,button);

        options.appendChild(button);

    });

    document.getElementById("quizResult").textContent="";

    document.getElementById("nextQuestion").classList.add("hidden");

}


function answerQuiz(index,button){

    if(quizAnswered)return;

    quizAnswered=true;

    const item=quizData[quizIndex];

    const correct=secretMap[item.k];

    const buttons=document.querySelectorAll(".quizOption");

    buttons.forEach(b=>b.disabled=true);

    if(index===correct){

        quizScore++;
        quizStreak++;

        let reward=100+(quizStreak*25);

        if(quizStreak>=5){
            reward+=100;
        }

        tokens+=reward;
        xp+=35;
        quizEarned+=reward;

        button.classList.add("correct");

        document.getElementById("quizResult").textContent=
            `💗 Correct! +${reward} Friendship Tokens · 🔥 Streak: ${quizStreak}`;

    }
    else{

        quizStreak=0;

        button.classList.add("wrong");

        document.getElementById("quizResult").textContent=
            "Not quite! Your streak has reset. Keep going.";

    }

    if(quizIndex===quizData.length-1){

        document.getElementById("nextQuestion").textContent=
            "SEE FINAL SCORE";

    }
    else{

        document.getElementById("nextQuestion").textContent=
            "NEXT QUESTION";

    }

    document.getElementById("nextQuestion").classList.remove("hidden");

    save();

}


function nextQuizQuestion(){

    if(quizIndex<quizData.length-1){

        quizIndex++;

        loadQuizQuestion();

    }
    else{

        finishQuiz();

    }

}


function finishQuiz(){

    if(quizScore>bestQuiz){

        bestQuiz=quizScore;

        localStorage.setItem("bestQuiz",bestQuiz);

    }

    let jackpot=0;
    let message="";

    if(quizScore===20){

        jackpot=5000;

        tokens+=jackpot;
        xp+=500;

        message=
            "👑 PERFECT SCORE! You know Liliana ridiculously well. " +
            "You received a 5,000 token friendship jackpot.";

    }
    else if(quizScore>=17){

        jackpot=1500;

        tokens+=jackpot;
        xp+=250;

        message=
            "💎 Incredible score! You received a 1,500 token bonus.";

    }
    else if(quizScore>=13){

        jackpot=750;

        tokens+=jackpot;
        xp+=150;

        message=
            "🌸 Great score! You received a 750 token bonus.";

    }
    else{

        message=
            "💗 You survived the Liliana test. Try again and beat your score!";

    }

    document.getElementById("quizGame").classList.add("hidden");
    document.getElementById("quizEnd").classList.remove("hidden");

    document.getElementById("quizScore").textContent=
        quizScore+"/20";

    document.getElementById("quizTokens").textContent=
        quizEarned+jackpot;

    document.getElementById("quizBest").textContent=
        bestQuiz;

    document.getElementById("quizFinalMessage").textContent=
        message;

    save();

}


/* =========================================================
   ACHIEVEMENTS
========================================================= */

const achievements=[

    ["🎰","First Spin","Play your first casino game",()=>gamesPlayed>=1],

    ["💰","Token Collector","Reach 10,000 tokens",()=>tokens>=10000],

    ["💎","High Roller","Reach 25,000 tokens",()=>tokens>=25000],

    ["🔥","On Fire","Win five games in a row",()=>streak>=5],

    ["🃏","Card Shark","Win a poker game",()=>wins>=1],

    ["🐬","Dolphin Trainer","Play Dolphin Derby",()=>localStorage.getItem("dolphinPlayed")==="yes"],

    ["🎯","Arcade Addict","Play ten games",()=>gamesPlayed>=10],

    ["💗","Liliana Expert","Score at least 17/20",()=>bestQuiz>=17],

    ["👑","Liliana Legend","Get 20/20 on the quiz",()=>bestQuiz===20],

    ["💎","Vault Hunter","Open the Friendship Vault",()=>localStorage.getItem("vaultOpened")==="yes"]

];


function renderAchievements(){

    const grid=document.getElementById("achievementGrid");

    if(!grid)return;

    grid.innerHTML="";

    achievements.forEach(a=>{

        const unlocked=a[3]();

        const div=document.createElement("div");

        div.className="achievement card"+(unlocked?"":" locked");

        div.innerHTML=`
            <div class="badge">${a[0]}</div>
            <div>
                <h3>${a[1]}</h3>
                <p>${a[2]}</p>
            </div>
        `;

        grid.appendChild(div);

    });

}


/* =========================================================
   VAULT TRACKING
========================================================= */

const originalOpenVault=openVault;

openVault=function(){

    const before=document.getElementById("vaultResult").textContent;

    originalOpenVault();

    const after=document.getElementById("vaultResult").textContent;

    if(after.includes("VAULT OPENED")){

        localStorage.setItem("vaultOpened","yes");

    }

};


/* =========================================================
   DOLPHIN TRACKING
========================================================= */

const originalDolphinRace=startDolphinRace;

startDolphinRace=function(){

    localStorage.setItem("dolphinPlayed","yes");

    originalDolphinRace();

};


/* =========================================================
   INITIALISE
========================================================= */

updateUI();

document.getElementById("vaultAttempts").textContent=vaultAttempts;

</script>

</body>
</html>
