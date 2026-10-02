<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Liliana's Friendship Casino 💗</title>

<style>
:root{
  --bg:#fff0f7;
  --panel:#fff7fb;
  --panel2:#ffe4f0;
  --pink:#ff4fa3;
  --pink2:#ff87c4;
  --gold:#d99b00;
  --purple:#c64f91;
  --blue:#51c7ff;
  --green:#3aa66f;
  --red:#e34b68;
  --text:#4a1832;
  --muted:#805c6e;
  --border:#f3a8c9;
}

*{
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  margin:0;
  min-height:100vh;
  font-family:Arial,Helvetica,sans-serif;
  color:var(--text);

  /* BABY PINK / PINK BACKGROUND */
  background:
    radial-gradient(
      circle at 50% -10%,
      #fff0f7 0,
      #ffd1e5 35%,
      #ff8fbd 75%
    );
}

button,
input{
  font:inherit;
}

button{
  cursor:pointer;
}

button:disabled{
  opacity:.5;
  cursor:not-allowed;
}


/* ===============================
   TOP BAR
================================ */

.topbar{
  position:sticky;
  top:0;
  z-index:50;

  display:flex;
  justify-content:space-between;
  align-items:center;
  gap:15px;

  padding:13px 18px;

  background:rgba(255,240,247,.96);

  backdrop-filter:blur(14px);

  border-bottom:1px solid var(--border);
}

.brand{
  font-size:20px;
  font-weight:900;
  white-space:nowrap;
}

.hud{
  display:flex;
  gap:7px;
  flex-wrap:wrap;
  justify-content:flex-end;
}

.hudItem{
  padding:7px 10px;

  background:#fff7fb;

  border:1px solid #efafd0;

  border-radius:12px;

  font-size:13px;
}

.sound{
  border:1px solid #e8a0c5;

  background:#ffe3ef;

  color:#681f46;

  padding:8px 11px;

  border-radius:10px;
}


/* ===============================
   MAIN CONTAINER
================================ */

.container{
  max-width:1200px;

  margin:auto;

  padding:25px 18px 60px;
}


/* ===============================
   HERO
================================ */

.hero{
  text-align:center;

  padding:25px 10px 30px;
}

.hero h1{
  margin:0;

  font-size:clamp(30px,6vw,55px);

  color:#7b1f50;

  text-shadow:
    0 2px 0 #fff;
}

.hero p{
  color:#713e58;

  margin:10px auto 20px;

  max-width:650px;
}

.levelbar{
  max-width:500px;

  margin:15px auto;
}

.progress{
  height:10px;

  background:#ffe3ef;

  border:1px solid #e5a0c2;

  border-radius:20px;

  overflow:hidden;
}

.progressFill{
  height:100%;

  width:0%;

  background:
    linear-gradient(
      90deg,
      #ff4fa3,
      #ffd76a
    );

  transition:width .4s;
}

.daily{
  display:inline-flex;

  align-items:center;

  gap:8px;

  border:1px solid #e3a14b;

  background:
    linear-gradient(
      135deg,
      #fff1c7,
      #ffe0a4
    );

  color:#613b0a;

  border-radius:15px;

  padding:12px 18px;

  font-weight:bold;
}


/* ===============================
   SECTION TITLES
================================ */

.sectionTitle{
  display:flex;

  justify-content:space-between;

  align-items:center;

  gap:10px;

  margin:25px 0 12px;
}

.sectionTitle h2{
  margin:0;

  color:#6f2148;
}


/* ===============================
   CASINO FLOOR
================================ */

.floor{
  display:grid;

  grid-template-columns:
    repeat(auto-fit,minmax(220px,1fr));

  gap:15px;
}

.room{
  min-height:170px;

  text-align:left;

  color:#5b2442;

  padding:20px;

  border-radius:22px;

  border:1px solid #efa7c7;

  background:
    linear-gradient(
      145deg,
      #fff8fc,
      #ffe1ed
    );

  transition:.2s;

  box-shadow:
    0 8px 20px rgba(150,40,90,.10);
}

.room:hover{
  transform:translateY(-4px);

  border-color:var(--pink);

  box-shadow:
    0 12px 25px rgba(255,79,163,.18);
}

.roomIcon{
  font-size:42px;

  margin-bottom:10px;
}

.room h3{
  margin:0 0 7px;

  font-size:20px;
}

.room p{
  color:#80586c;

  margin:0;

  line-height:1.45;
}


/* ===============================
   ROOM VIEWS
================================ */

.roomView{
  display:none;

  margin-top:25px;
}

.roomView.active{
  display:block;

  animation:fade .25s ease;
}

@keyframes fade{
  from{
    opacity:0;
    transform:translateY(8px);
  }

  to{
    opacity:1;
    transform:none;
  }
}

.roomHead{
  display:flex;

  justify-content:space-between;

  align-items:center;

  gap:10px;

  margin-bottom:15px;
}

.roomHead h2{
  margin:0;

  color:#6e2048;
}

.back{
  background:#fff4f9;

  color:#681f46;

  border:1px solid #e3a2c3;

  border-radius:12px;

  padding:10px 14px;
}


/* ===============================
   GAME CARDS
================================ */

.games{
  display:grid;

  grid-template-columns:
    repeat(auto-fit,minmax(230px,1fr));

  gap:13px;
}

.gameCard{
  padding:17px;

  border-radius:18px;

  border:1px solid #edafd0;

  background:#fff8fc;

  box-shadow:
    0 6px 15px rgba(140,40,90,.08);
}

.gameCard h3{
  margin:0 0 7px;

  color:#692047;
}

.gameCard p{
  color:#80586c;

  font-size:14px;

  min-height:38px;
}

.play{
  width:100%;

  border:0;

  border-radius:12px;

  padding:11px;

  background:
    linear-gradient(
      135deg,
      #ff65ad,
      #e72f88
    );

  color:white;

  font-weight:bold;
}


/* ===============================
   PANELS
================================ */

.panel{
  background:#fff8fc;

  border:1px solid #eda9ca;

  border-radius:22px;

  padding:22px;

  box-shadow:
    0 8px 25px rgba(120,30,75,.08);
}

.gamePanel{
  margin-top:15px;
}

.hidden{
  display:none!important;
}

.bigGame{
  max-width:700px;

  margin:auto;

  text-align:center;
}

.result{
  min-height:25px;

  margin-top:12px;

  text-align:center;

  font-weight:bold;

  color:#b06c00;
}


/* ===============================
   SLOTS
================================ */

.slot{
  display:flex;

  justify-content:center;

  gap:10px;

  margin:25px 0;
}

.reel{
  width:105px;

  height:105px;

  display:grid;

  place-items:center;

  background:#fff;

  color:#222;

  border-radius:18px;

  font-size:48px;

  border:6px solid #d4a53d;

  box-shadow:
    0 8px 0 #9d711a;
}

.spin{
  background:
    linear-gradient(
      #ff75ba,
      #db267d
    );

  border:0;

  color:white;

  padding:14px 35px;

  border-radius:30px;

  font-weight:900;

  font-size:18px;
}


/* ===============================
   LUCKY WHEEL
================================ */

.wheelWrap{
  position:relative;

  width:310px;

  margin:20px auto;
}

.pointer{
  position:absolute;

  top:-13px;

  left:50%;

  transform:translateX(-50%);

  z-index:2;

  font-size:32px;
}

.wheel{
  width:300px;

  height:300px;

  border-radius:50%;

  border:8px solid white;

  background:
    conic-gradient(
      #ff4fa3 0deg 45deg,
      #ffd76a 45deg 90deg,
      #c64f91 90deg 135deg,
      #51c7ff 135deg 180deg,
      #5de39b 180deg 225deg,
      #ff637d 225deg 270deg,
      #ff9b52 270deg 315deg,
      #d46eff 315deg 360deg
    );

  transition:
    transform 3s
    cubic-bezier(.15,.7,.15,1);
}

.centerDot{
  position:absolute;

  width:52px;

  height:52px;

  border-radius:50%;

  background:white;

  color:#8b2458;

  display:grid;

  place-items:center;

  left:50%;

  top:50%;

  transform:translate(-50%,-50%);

  font-weight:900;
}


/* ===============================
   ACTION BUTTONS
================================ */

.actionRow{
  display:flex;

  flex-wrap:wrap;

  gap:9px;

  justify-content:center;
}

.action{
  border:0;

  border-radius:12px;

  padding:11px 16px;

  background:#c64f91;

  color:white;

  font-weight:bold;
}

.action.gold{
  background:#b68416;
}

.action.green{
  background:#26875a;
}

.action.red{
  background:#c93655;
}


/* ===============================
   INPUTS
================================ */

input{
  width:100%;

  padding:13px;

  border-radius:12px;

  border:1px solid #dc9cbe;

  background:#fff;

  color:#4a1832;

  outline:none;
}

input:focus{
  border-color:var(--pink);
}


/* ===============================
   CARDS
================================ */

.cards{
  display:flex;

  flex-wrap:wrap;

  justify-content:center;

  gap:8px;

  margin:15px 0;
}

.card{
  width:55px;

  height:78px;

  border-radius:9px;

  display:grid;

  place-items:center;

  background:#fff;

  color:#111;

  font-weight:bold;

  font-size:19px;

  border:2px solid #ddd;
}

.card.red{
  color:#d51e3c;
}


/* ===============================
   FRIENDSHIP CATCH
================================ */

.creatureArea{
  min-height:430px;

  position:relative;

  overflow:hidden;

  border-radius:22px;

  background:
    radial-gradient(
      circle at 30% 25%,
      #53c4e8,
      #2485aa 45%,
      #12506e 75%
    );

  border:1px solid #4eb6d7;
}

.bubble{
  position:absolute;

  border-radius:50%;

  border:1px solid
    rgba(255,255,255,.7);

  width:14px;

  height:14px;

  opacity:.7;
}

.creature{
  position:absolute;

  border:0;

  background:none;

  font-size:45px;

  animation:
    float 4s ease-in-out infinite alternate;
}

@keyframes float{
  to{
    transform:
      translate(25px,15px);
  }
}

.collection{
  display:flex;

  flex-wrap:wrap;

  gap:8px;

  margin-top:15px;
}

.creatureBadge{
  padding:8px 10px;

  border-radius:12px;

  background:#ffe5f0;

  border:1px solid #efa9c8;
}


/* ===============================
   QUIZ
================================ */

.question{
  font-size:19px;

  font-weight:bold;

  margin-bottom:12px;
}

.answers{
  display:grid;

  gap:8px;
}

.answer{
  text-align:left;

  border:1px solid #e2a4c4;

  background:#fff0f7;

  color:#5c2042;

  border-radius:12px;

  padding:13px;
}

.answer:hover{
  border-color:var(--pink);

  background:#ffe0ed;
}


/* ===============================
   TIMELINE
================================ */

.timeline{
  display:grid;

  gap:10px;
}

.year{
  border-left:4px solid var(--pink);

  padding:15px;

  background:#fff0f7;

  border-radius:
    0 14px 14px 0;
}


/* ===============================
   ACHIEVEMENTS
================================ */

.achievements{
  display:grid;

  grid-template-columns:
    repeat(auto-fit,minmax(190px,1fr));

  gap:10px;
}

.achievement{
  padding:15px;

  border-radius:15px;

  border:1px solid #e5a6c5;

  background:#fff7fb;
}

.achievement.locked{
  opacity:.4;
}

.achievement strong{
  display:block;

  margin-bottom:5px;
}


/* ===============================
   VAULT
================================ */

.vault{
  max-width:500px;

  margin:auto;

  text-align:center;
}

.codeInput{
  text-align:center;

  font-size:26px;

  letter-spacing:8px;
}


/* ===============================
   TOAST
================================ */

.toast{
  position:fixed;

  left:50%;

  bottom:25px;

  transform:translateX(-50%);

  z-index:100;

  background:#fff7fb;

  color:#631e45;

  border:1px solid var(--pink);

  padding:13px 18px;

  border-radius:14px;

  box-shadow:
    0 8px 30px rgba(90,20,60,.25);

  display:none;
}

.toast.show{
  display:block;

  animation:toast .25s;
}

@keyframes toast{
  from{
    opacity:0;

    transform:
      translate(-50%,10px);
  }

  to{
    opacity:1;

    transform:
      translate(-50%,0);
  }
}


/* ===============================
   FOOTER
================================ */

footer{
  text-align:center;

  color:#7d5267;

  padding:35px 15px;
}


/* ===============================
   MOBILE
================================ */

@media(max-width:650px){

  .topbar{
    position:relative;

    align-items:flex-start;

    flex-direction:column;
  }

  .hud{
    justify-content:flex-start;
  }

  .container{
    padding:
      15px 12px 40px;
  }

  .floor{
    grid-template-columns:
      1fr 1fr;
  }

  .room{
    min-height:155px;

    padding:15px;
  }

  .roomIcon{
    font-size:34px;
  }

  .slot{
    gap:5px;
  }

  .reel{
    width:80px;

    height:85px;

    font-size:37px;
  }

  .wheelWrap,
  .wheel{
    width:270px;

    height:270px;
  }

}

@media(max-width:400px){

  .floor{
    grid-template-columns:1fr;
  }

  .reel{
    width:72px;

    height:78px;
  }

}
</style>
</head>


<body>


<header class="topbar">

  <div class="brand">
    💗 Liliana's Friendship Casino
  </div>

  <div class="hud">

    <div class="hudItem">
      💰 <span id="tokens">1,000</span>
    </div>

    <div class="hudItem">
      ⭐ Lv.<span id="level">1</span>
    </div>

    <div class="hudItem">
      🔥 <span id="streak">0</span>
    </div>

    <div class="hudItem">
      🏆 <span id="wins">0</span>
    </div>

    <button
      class="sound"
      id="soundBtn">
      🔊
    </button>

  </div>

</header>


<main class="container">


<section class="hero">

  <h1>
    🎰 Liliana's Friendship Casino
  </h1>

  <p>
    Six years of friendship turned into one ridiculous casino.
    Play games, collect tokens, unlock secrets and become
    Friendship Royalty.
  </p>


  <div class="levelbar">

    <div>
      Level
      <span id="heroLevel">1</span>

      ·

      <span id="xp">0</span>
      XP
    </div>

    <div class="progress">

      <div
        class="progressFill"
        id="xpBar">
      </div>

    </div>

  </div>


  <button
    class="daily"
    id="dailyBtn">

    🎁 Claim Daily Friendship Bonus

  </button>

</section>


<div class="sectionTitle">

  <h2>
    🎟️ Casino Floor
  </h2>

</div>


<section class="floor">


<button
  class="room"
  data-room="slotsRoom">

  <div class="roomIcon">
    🎰
  </div>

  <h3>
    Slots Room
  </h3>

  <p>
    Buffalo, Pink Palace, Dolphin Riches,
    Fancy 7s and the Mega Jackpot.
  </p>

</button>


<button
  class="room"
  data-room="cardsRoom">

  <div class="roomIcon">
    ♠️
  </div>

  <h3>
    Card Room
  </h3>

  <p>
    Poker, Blackjack, Baccarat, War,
    Gin Rummy and Texas Hold'em.
  </p>

</button>


<button
  class="room"
  data-room="luckyRoom">

  <div class="roomIcon">
    🎡
  </div>

  <h3>
    Lucky Lounge
  </h3>

  <p>
    Lucky Wheel, Friendship Roulette,
    Craps, Hi-Lo, Coin Flip and Plinko.
  </p>

</button>


<button
  class="room"
  data-room="racesRoom">

  <div class="roomIcon">
    🏇
  </div>

  <h3>
    Derby Track
  </h3>

  <p>
    Pick your racer and race.
  </p>

</button>


<button
  class="room"
  data-room="prizeRoom">

  <div class="roomIcon">
    🎁
  </div>

  <h3>
    Prize Arcade
  </h3>

  <p>
    Mystery Boxes, Scratch Cards,
    Gem Heist, Darts and more.
  </p>

</button>


<button
  class="room"
  data-room="catchRoom">

  <div class="roomIcon">
    🐬
  </div>

  <h3>
    Friendship Catch
  </h3>

  <p>
    Catch creatures and build
    your collection.
  </p>

</button>


<button
  class="room"
  data-room="lilianaRoom">

  <div class="roomIcon">
    💗
  </div>

  <h3>
    Liliana's Corner
  </h3>

  <p>
    Quiz, personality test,
    six-year timeline and letter.
  </p>

</button>


<button
  class="room"
  data-room="vipRoom">

  <div class="roomIcon">
    🔐
  </div>

  <h3>
    VIP Vault
  </h3>

  <p>
    Find the six-digit friendship
    code and unlock the vault.
  </p>

</button>


</section>


<!-- ==========================================
     SLOTS ROOM
========================================== -->

<section
  class="roomView"
  id="slotsRoom">

<div class="roomHead">

  <h2>
    🎰 Slots Room
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">

  <h3>
    🐃 Buffalo Stampede
  </h3>

  <p>
    Classic friendship buffalo slot.
  </p>

  <button
    class="play"
    data-slot="buffalo">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    💗 Pink Palace
  </h3>

  <p>
    Sweet pink themed slot machine.
  </p>

  <button
    class="play"
    data-slot="pink">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🐬 Dolphin Riches
  </h3>

  <p>
    Dive into a dolphin themed spin.
  </p>

  <button
    class="play"
    data-slot="dolphin">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    7️⃣ Fancy 7s
  </h3>

  <p>
    Lucky sevens friendship slot.
  </p>

  <button
    class="play"
    data-slot="sevens">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    💎 Mega Jackpot
  </h3>

  <p>
    The giant 1,000,000 token jackpot.
  </p>

  <button
    class="play"
    data-slot="mega">

    PLAY

  </button>

</div>


</div>


<div
  class="panel gamePanel hidden"
  id="slotPanel">

<div class="bigGame">

  <h2 id="slotTitle">
    🎰 Slot Machine
  </h2>

  <p>
    Prize pool:
    <strong id="slotJackpot">
      10,000
    </strong>
    💰
  </p>


  <div class="slot">

    <div
      class="reel"
      id="r1">
      💎
    </div>

    <div
      class="reel"
      id="r2">
      💎
    </div>

    <div
      class="reel"
      id="r3">
      💎
    </div>

  </div>


  <button
    class="spin"
    id="slotSpin">

    SPIN 🎰

  </button>


  <div
    class="result"
    id="slotResult">
  </div>

</div>

</div>

</section>


<!-- ==========================================
     CARD ROOM
========================================== -->

<section
  class="roomView"
  id="cardsRoom">

<div class="roomHead">

  <h2>
    ♠️ Card Room
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">

  <h3>
    ♠️ Poker vs Computer
  </h3>

  <p>
    Draw five cards and compare your hand.
  </p>

  <button
    class="play"
    data-cardgame="poker">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    ♣️ Blackjack
  </h3>

  <p>
    Hit, stand or double down.
  </p>

  <button
    class="play"
    data-cardgame="blackjack">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    ♦️ Baccarat
  </h3>

  <p>
    Choose Player, Banker or Tie.
  </p>

  <button
    class="play"
    data-cardgame="baccarat">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🃏 War
  </h3>

  <p>
    Higher card wins.
  </p>

  <button
    class="play"
    data-cardgame="war">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🃏 Gin Rummy
  </h3>

  <p>
    Build the better hand.
  </p>

  <button
    class="play"
    data-cardgame="gin">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    ♠️ Texas Hold'em
  </h3>

  <p>
    Choose whether your hand is strong enough.
  </p>

  <button
    class="play"
    data-cardgame="holdem">

    PLAY

  </button>

</div>


</div>


<div
  class="panel gamePanel hidden"
  id="cardPanel">

  <h2 id="cardTitle"></h2>

  <div id="cardContent"></div>

  <div
    class="result"
    id="cardResult">
  </div>

</div>

</section>


<!-- ==========================================
     LUCKY LOUNGE
========================================== -->

<section
  class="roomView"
  id="luckyRoom">

<div class="roomHead">

  <h2>
    🎡 Lucky Lounge
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">

  <h3>
    🎡 Lucky Wheel
  </h3>

  <p>
    Spin for up to 10,000 tokens.
  </p>

  <button
    class="play"
    data-lucky="wheel">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🔴 Friendship Roulette
  </h3>

  <p>
    Pick red, black or green.
  </p>

  <button
    class="play"
    data-lucky="roulette">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🎲 Craps
  </h3>

  <p>
    Roll two dice.
  </p>

  <button
    class="play"
    data-lucky="craps">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    📈 Hi-Lo
  </h3>

  <p>
    Predict higher or lower.
  </p>

  <button
    class="play"
    data-lucky="hilo">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🪙 Coin Flip
  </h3>

  <p>
    Call heads or tails.
  </p>

  <button
    class="play"
    data-lucky="coin">

    PLAY

  </button>

</div>


<div class="gameCard">

  <h3>
    🟣 Plinko
  </h3>

  <p>
    Drop your token through the pegs.
  </p>

  <button
    class="play"
    data-lucky="plinko">

    PLAY

  </button>

</div>


</div>


<div
  class="panel gamePanel hidden"
  id="luckyPanel">

  <div
    class="bigGame"
    id="luckyContent">
  </div>

</div>

</section>


<!-- ==========================================
     RACES
========================================== -->

<section
  class="roomView"
  id="racesRoom">

<div class="roomHead">

  <h2>
    🏇 Derby Track
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">

  <h3>
    🏇 Horse Derby
  </h3>

  <p>
    Choose your horse and race.
  </p>

  <button
    class="play"
    data-race="horse">

    RACE

  </button>

</div>


<div class="gameCard">

  <h3>
    🐬 Dolphin Derby
  </h3>

  <p>
    Pick a dolphin and race.
  </p>

  <button
    class="play"
    data-race="dolphin">

    RACE

  </button>

</div>


</div>


<div
  class="panel gamePanel hidden"
  id="racePanel">

  <div class="bigGame">

    <h2 id="raceTitle"></h2>

    <div id="raceContent"></div>

    <div
      class="result"
      id="raceResult">
    </div>

  </div>

</div>

</section>


<!-- ==========================================
     PRIZE ARCADE
========================================== -->

<section
  class="roomView"
  id="prizeRoom">

<div class="roomHead">

  <h2>
    🎁 Prize Arcade
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">
  <h3>🎁 Mystery Boxes</h3>
  <p>Open a mystery reward.</p>

  <button
    class="play"
    data-mini="box">
    OPEN
  </button>
</div>


<div class="gameCard">
  <h3>🪙 Three Cups</h3>
  <p>Find the hidden token.</p>

  <button
    class="play"
    data-mini="cups">
    PLAY
  </button>
</div>


<div class="gameCard">
  <h3>💗 Heart Scratch Card</h3>
  <p>Scratch your virtual friendship card.</p>

  <button
    class="play"
    data-mini="scratch">
    SCRATCH
  </button>
</div>


<div class="gameCard">
  <h3>🎯 Lucky Darts</h3>
  <p>Hit the target.</p>

  <button
    class="play"
    data-mini="darts">
    THROW
  </button>
</div>


<div class="gameCard">
  <h3>💎 Gem Heist</h3>
  <p>Pick a vault and find gems.</p>

  <button
    class="play"
    data-mini="gems">
    HEIST
  </button>
</div>


<div class="gameCard">
  <h3>🎁 Lucky Envelopes</h3>
  <p>Choose a mysterious envelope.</p>

  <button
    class="play"
    data-mini="envelopes">
    OPEN
  </button>
</div>


<div class="gameCard">
  <h3>🔢 Lucky Number</h3>
  <p>Guess the lucky number.</p>

  <button
    class="play"
    data-mini="number">
    GUESS
  </button>
</div>


<div class="gameCard">
  <h3>🐠 Ocean Treasure</h3>
  <p>Dive for hidden treasure.</p>

  <button
    class="play"
    data-mini="treasure">
    DIVE
  </button>
</div>


</div>


<div
  class="panel gamePanel hidden"
  id="miniPanel">

  <div class="bigGame">

    <h2 id="miniTitle"></h2>

    <div id="miniContent"></div>

    <div
      class="result"
      id="miniResult">
    </div>

  </div>

</div>

</section>


<!-- ==========================================
     FRIENDSHIP CATCH
========================================== -->

<section
  class="roomView"
  id="catchRoom">

<div class="roomHead">

  <h2>
    🐬 Friendship Catch
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="panel">

<p>
  Catch the creatures swimming around the
  friendship ocean. Some creatures are much
  rarer than others.
</p>


<div
  class="creatureArea"
  id="creatureArea">


<div
  class="bubble"
  style="left:10%;top:20%">
</div>

<div
  class="bubble"
  style="left:70%;top:25%">
</div>

<div
  class="bubble"
  style="left:45%;top:75%">
</div>

<div
  class="bubble"
  style="left:85%;top:65%">
</div>


<button
  class="creature"
  style="left:12%;top:35%"
  data-creature="Dolphini">
  🐬
</button>


<button
  class="creature"
  style="left:65%;top:15%"
  data-creature="Rosibun">
  🌹🐰
</button>


<button
  class="creature"
  style="left:40%;top:60%"
  data-creature="Sunnyflo">
  🌻
</button>


<button
  class="creature"
  style="left:75%;top:65%"
  data-creature="Pinkyroo">
  🦘💗
</button>


<button
  class="creature"
  style="left:20%;top:75%"
  data-creature="Fluttera">
  🦋
</button>


<button
  class="creature"
  style="left:50%;top:25%"
  data-creature="Shellby">
  🐚
</button>


<button
  class="creature"
  style="left:82%;top:40%"
  data-creature="Lunaboo">
  🌙
</button>


</div>


<h3>
  🐾 Your Collection
</h3>


<div
  class="collection"
  id="collection">
</div>


</div>

</section>


<!-- ==========================================
     LILIANA'S CORNER
========================================== -->

<section
  class="roomView"
  id="lilianaRoom">

<div class="roomHead">

  <h2>
    💗 Liliana's Corner
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="games">


<div class="gameCard">

  <h3>
    🧠 Liliana Quiz
  </h3>

  <p>
    Answer questions and earn Friendship Tokens.
  </p>

  <button
    class="play"
    id="startQuiz">

    START QUIZ

  </button>

</div>


<div class="gameCard">

  <h3>
    🌸 Personality Test
  </h3>

  <p>
    Discover which Liliana energy you get.
  </p>

  <button
    class="play"
    id="personality">

    TAKE TEST

  </button>

</div>


<div class="gameCard">

  <h3>
    📖 Six Years Together
  </h3>

  <p>
    Explore the friendship timeline.
  </p>

  <button
    class="play"
    id="timelineBtn">

    OPEN

  </button>

</div>


<div class="gameCard">

  <h3>
    💌 Friendship Letter
  </h3>

  <p>
    A little message celebrating six years.
  </p>

  <button
    class="play"
    id="letterBtn">

    OPEN

  </button>

</div>


</div>


<div
  class="panel gamePanel"
  id="lilianaPanel">

<div id="lilianaContent">

  <h2>
    💗 Liliana's Corner
  </h2>

  <p>
    Choose something above to explore this
    part of the casino.
  </p>

</div>

</div>

</section>


<!-- ==========================================
     VIP VAULT
========================================== -->

<section
  class="roomView"
  id="vipRoom">

<div class="roomHead">

  <h2>
    🔐 VIP Friendship Vault
  </h2>

  <button class="back">
    ← Casino Floor
  </button>

</div>


<div class="panel vault">

<h2>
  💎 Six-Year Friendship Vault
</h2>

<p>
  Six digits. Six years. One secret.
</p>


<input
  class="codeInput"
  id="vaultCode"
  maxlength="6"
  inputmode="numeric"
  placeholder="••••••"
>


<br><br>


<button
  class="play"
  id="vaultButton">

  UNLOCK VAULT 🔐

</button>


<div
  class="result"
  id="vaultResult">
</div>


</div>

</section>


<!-- ==========================================
     ACHIEVEMENTS
========================================== -->

<section>

<div class="sectionTitle">

  <h2>
    🏆 Achievements
  </h2>

</div>


<div
  class="achievements"
  id="achievements">
</div>

</section>


</main>


<footer>
  💗 Six years of friendship · Liliana's Friendship Casino 💗
</footer>


<div
  class="toast"
  id="toast">
</div>


<script>

/* =====================================================
   STATE
===================================================== */

const DEFAULT_STATE = {

  tokens:1000,

  xp:0,

  streak:0,

  wins:0,

  played:0,

  biggest:0,

  sound:true,

  lastDaily:"",

  vaultOpened:false,

  caught:[],

  achievements:[],

  quizBest:0

};


let S = loadState();


function loadState(){

  try{

    const saved =
      JSON.parse(
        localStorage.getItem(
          "lilianaCasino"
        )
      );

    return {
      ...DEFAULT_STATE,
      ...(saved || {})
    };

  }catch(e){

    return {
      ...DEFAULT_STATE
    };

  }

}


function save(){

  localStorage.setItem(
    "lilianaCasino",
    JSON.stringify(S)
  );

}


function format(n){

  return Number(
    n || 0
  ).toLocaleString();

}


/* =====================================================
   AUDIO
===================================================== */

let audioCtx=null;


function sound(type="click"){

  if(!S.sound)
    return;

  try{

    audioCtx =
      audioCtx ||
      new (
        window.AudioContext ||
        window.webkitAudioContext
      )();


    const osc =
      audioCtx.createOscillator();

    const gain =
      audioCtx.createGain();


    osc.connect(gain);

    gain.connect(
      audioCtx.destination
    );


    const tones={

      click:420,

      win:760,

      jackpot:980,

      lose:170,

      spin:300

    };


    osc.frequency.value =
      tones[type] || 420;


    osc.type =
      type==="win" ||
      type==="jackpot"
      ? "sine"
      : "triangle";


    gain.gain.setValueAtTime(
      .0001,
      audioCtx.currentTime
    );


    gain.gain.exponentialRampToValueAtTime(
      .08,
      audioCtx.currentTime+.02
    );


    gain.gain.exponentialRampToValueAtTime(
      .0001,
      audioCtx.currentTime+.25
    );


    osc.start();

    osc.stop(
      audioCtx.currentTime+.26
    );


  }catch(e){}

}


/* =====================================================
   TOAST
===================================================== */

let toastTimer;


function toast(message){

  const el =
    document.getElementById(
      "toast"
    );


  el.textContent=message;


  el.classList.add("show");


  clearTimeout(
    toastTimer
  );


  toastTimer =
    setTimeout(
      ()=>{
        el.classList.remove(
          "show"
        );
      },
      2500
    );

}


/* =====================================================
   TOKEN / XP SYSTEM
===================================================== */

function add(amount,win=false){

  S.tokens += amount;


  if(S.tokens<0)
    S.tokens=0;


  S.played++;


  const xpGain =
    Math.max(
      5,
      Math.min(
        100,
        Math.abs(amount)
      )
    );


  S.xp += xpGain;


  if(win){

    S.wins++;

    S.streak++;

  }


  if(amount>S.biggest)
    S.biggest=amount;


  update();

  save();

}


function level(){

  return Math.floor(
    S.xp/1000
  )+1;

}


function update(){

  const lv=level();


  document.getElementById(
    "tokens"
  ).textContent=
    format(S.tokens);


  document.getElementById(
    "level"
  ).textContent=lv;


  document.getElementById(
    "heroLevel"
  ).textContent=lv;


  document.getElementById(
    "xp"
  ).textContent=
    format(S.xp);


  document.getElementById(
    "streak"
  ).textContent=
    S.streak;


  document.getElementById(
    "wins"
  ).textContent=
    S.wins;


  const progress =
    S.xp%1000;


  document.getElementById(
    "xpBar"
  ).style.width=
    progress/10+"%";


  renderAchievements();

}


/* =====================================================
   ACHIEVEMENTS
===================================================== */

const achievementList=[

  [
    "first",
    "🌸 First Spin",
    "Play your first game."
  ],

  [
    "winner",
    "🏆 First Win",
    "Win your first game."
  ],

  [
    "rich",
    "💰 10K Club",
    "Reach 10,000 tokens."
  ],

  [
    "million",
    "💎 Million Token Club",
    "Win the Mega Jackpot."
  ],

  [
    "collector",
    "🐬 Collector",
    "Catch 5 creatures."
  ],

  [
    "quiz",
    "🧠 Liliana Expert",
    "Score 20/20 on the quiz."
  ],

  [
    "vault",
    "🔐 Vault Keeper",
    "Open the friendship vault."
  ],

  [
    "ten",
    "🎰 Casino Regular",
    "Play 10 games."
  ],

  [
    "level10",
    "👑 Friendship Royalty",
    "Reach level 10."
  ]

];


function achievement(id){

  if(
    !S.achievements.includes(id)
  ){

    S.achievements.push(id);

    save();


    const item =
      achievementList.find(
        x=>x[0]===id
      );


    if(item){

      toast(
        "🏆 Achievement unlocked: "+
        item[1]
      );

    }

  }

}


function renderAchievements(){

  const el =
    document.getElementById(
      "achievements"
    );


  el.innerHTML =
    achievementList
      .map(a=>{

        const unlocked =
          S.achievements
            .includes(a[0]);


        return `

          <div
            class="achievement
            ${unlocked?"":"locked"}">

            <strong>
              ${a[1]}
            </strong>

            <span>
              ${a[2]}
            </span>

          </div>

        `;

      })
      .join("");


  if(S.played>=1)
    achievement("first");


  if(S.wins>=1)
    achievement("winner");


  if(S.tokens>=10000)
    achievement("rich");


  if(S.caught.length>=5)
    achievement("collector");


  if(S.played>=10)
    achievement("ten");


  if(level()>=10)
    achievement("level10");

}


/* =====================================================
   ROOM NAVIGATION
===================================================== */

const rooms =
  document.querySelectorAll(
    ".room"
  );


const views =
  document.querySelectorAll(
    ".roomView"
  );


function openRoom(id){

  views.forEach(
    v=>v.classList.remove(
      "active"
    )
  );


  const target =
    document.getElementById(id);


  if(target){

    target.classList.add(
      "active"
    );


    target.scrollIntoView({
      behavior:"smooth",
      block:"start"
    });

  }

}


rooms.forEach(room=>{

  room.addEventListener(
    "click",
    ()=>{

      sound();

      openRoom(
        room.dataset.room
      );

    }
  );

});


document
  .querySelectorAll(".back")
  .forEach(btn=>{

    btn.addEventListener(
      "click",
      ()=>{

        views.forEach(
          v=>v.classList.remove(
            "active"
          )
        );


        window.scrollTo({
          top:0,
          behavior:"smooth"
        });


        sound();

      }
    );

  });


/* =====================================================
   SOUND BUTTON
===================================================== */

document
  .getElementById("soundBtn")
  .addEventListener(
    "click",
    ()=>{

      S.sound=!S.sound;


      document.getElementById(
        "soundBtn"
      ).textContent=
        S.sound
        ? "🔊"
        : "🔇";


      save();

    }
  );


/* =====================================================
   DAILY BONUS
===================================================== */

function today(){

  const d =
    new Date();


  return [

    d.getFullYear(),

    d.getMonth()+1,

    d.getDate()

  ].join("-");

}


document
  .getElementById("dailyBtn")
  .addEventListener(
    "click",
    ()=>{

      if(
        S.lastDaily===today()
      ){

        toast(
          "🎁 You already claimed today's bonus!"
        );

        return;

      }


      S.lastDaily=today();


      add(
        500,
        true
      );


      toast(
        "🎁 Daily Bonus: +500 tokens!"
      );

    }
  );


/* =====================================================
   SLOT MACHINES
===================================================== */

const slotData={

  buffalo:{
    title:"🐃 Buffalo Stampede",
    jackpot:5000,
    symbols:[
      "🐃",
      "🌹",
      "💰",
      "7️⃣",
      "💎"
    ]
  },

  pink:{
    title:"💗 Pink Palace",
    jackpot:7500,
    symbols:[
      "💗",
      "💋",
      "🌸",
      "👑",
      "💎"
    ]
  },

  dolphin:{
    title:"🐬 Dolphin Riches",
    jackpot:8000,
    symbols:[
      "🐬",
      "🌊",
      "🐚",
      "🐠",
      "💎"
    ]
  },

  sevens:{
    title:"7️⃣ Fancy 7s",
    jackpot:10000,
    symbols:[
      "7️⃣",
      "7️⃣",
      "🍒",
      "⭐",
      "💎"
    ]
  },

  mega:{
    title:"💎 MEGA JACKPOT",
    jackpot:1000000,
    symbols:[
      "💎",
      "💎",
      "7️⃣",
      "👑",
      "💗"
    ]
  }

};


let currentSlot="buffalo";


document
  .querySelectorAll(
    "[data-slot]"
  )
  .forEach(btn=>{

    btn.addEventListener(
      "click",
      ()=>{

        currentSlot =
          btn.dataset.slot;


        const data =
          slotData[
            currentSlot
          ];


        document.getElementById(
          "slotPanel"
        )
        .classList.remove(
          "hidden"
        );


        document.getElementById(
          "slotTitle"
        ).textContent=
          data.title;


        document.getElementById(
          "slotJackpot"
        ).textContent=
          format(
            data.jackpot
          );


        document.getElementById(
          "slotResult"
        ).textContent=
          "Ready to spin.";


        document.getElementById(
          "slotPanel"
        ).scrollIntoView({
          behavior:"smooth"
        });

      }
    );

  });


document
  .getElementById(
    "slotSpin"
  )
  .addEventListener(
    "click",
    ()=>{

      if(S.tokens<20){

        toast(
          "You need at least 20 tokens."
        );

        return;

      }


      const data =
        slotData[
          currentSlot
        ];


      sound("spin");


      const r=[

        data.symbols[
          Math.floor(
            Math.random()*
            data.symbols.length
          )
        ],

        data.symbols[
          Math.floor(
            Math.random()*
            data.symbols.length
          )
        ],

        data.symbols[
          Math.floor(
            Math.random()*
            data.symbols.length
          )
        ]

      ];


      const reels=[

        document.getElementById("r1"),

        document.getElementById("r2"),

        document.getElementById("r3")

      ];


      let count=0;


      const interval =
        setInterval(
          ()=>{

            reels.forEach(
              x=>{

                x.textContent=
                  data.symbols[
                    Math.floor(
                      Math.random()*
                      data.symbols.length
                    )
                  ];

              }
            );


            count++;


            if(count>=12){

              clearInterval(
                interval
              );


              reels[0].textContent=r[0];

              reels[1].textContent=r[1];

              reels[2].textContent=r[2];


              if(
                r[0]===r[1] &&
                r[1]===r[2]
              ){

                const prize =
                  data.jackpot;


                add(
                  prize,
                  true
                );


                if(
                  currentSlot==="mega" &&
                  r[0]==="💎"
                ){

                  achievement(
                    "million"
                  );


                  document.getElementById(
                    "slotResult"
                  ).textContent=
                    "💎💎💎 MEGA JACKPOT! +1,000,000 TOKENS!";


                  sound(
                    "jackpot"
                  );

                }else{

                  document.getElementById(
                    "slotResult"
                  ).textContent=
                    "🎉 JACKPOT! +"+
                    format(prize)+
                    " TOKENS!";


                  sound(
                    "win"
                  );

                }

              }else{

                add(-20);


                document.getElementById(
                  "slotResult"
                ).textContent=
                  "No match. -20 tokens.";


                sound(
                  "lose"
                );

              }

            }

          },
          90
        );

    }
  );


/* =====================================================
   CARD UTILITIES
===================================================== */

const suits=[
  "♠",
  "♥",
  "♦",
  "♣"
];


const ranks=[

  "2",
  "3",
  "4",
  "5",
  "6",
  "7",
  "8",
  "9",
  "10",
  "J",
  "Q",
  "K",
  "A"

];


function randomCard(){

  return {

    rank:
      ranks[
        Math.floor(
          Math.random()*
          ranks.length
        )
      ],

    suit:
      suits[
        Math.floor(
          Math.random()*
          suits.length
        )
      ]

  };

}


function cardValue(card){

  if(
    ["J","Q","K"]
    .includes(card.rank)
  )
    return 10;


  if(
    card.rank==="A"
  )
    return 11;


  return Number(
    card.rank
  );

}


function cardHTML(card){

  const red =
    card.suit==="♥" ||
    card.suit==="♦";


  return `

    <div
      class="card
      ${red?"red":""}">

      ${card.rank}${card.suit}

    </div>

  `;

}


/* =====================================================
   CARD GAMES
===================================================== */

document
  .querySelectorAll(
    "[data-cardgame]"
  )
  .forEach(btn=>{

    btn.addEventListener(
      "click",
      ()=>{

        const game =
          btn.dataset.cardgame;


        const panel =
          document.getElementById(
            "cardPanel"
          );


        panel.classList.remove(
          "hidden"
        );


        playCardGame(
          game
        );


        panel.scrollIntoView({
          behavior:"smooth"
        });

      }
    );

  });


function playCardGame(game){

  const title =
    document.getElementById(
      "cardTitle"
    );


  const content =
    document.getElementById(
      "cardContent"
    );


  const result =
    document.getElementById(
      "cardResult"
    );


  result.textContent="";


  if(game==="poker"){

    title.textContent=
      "♠️ Poker vs Computer";


    const player =
      Array.from(
        {length:5},
        randomCard
      );


    const computer =
      Array.from(
        {length:5},
        randomCard
      );


    const pScore =
      player.reduce(
        (s,c)=>
          s+cardValue(c),
        0
      );


    const cScore =
      computer.reduce(
        (s,c)=>
          s+cardValue(c),
        0
      );


    content.innerHTML=`

      <p>
        Your hand
      </p>

      <div class="cards">

        ${player
          .map(cardHTML)
          .join("")}

      </div>


      <p>
        Computer hand
      </p>

      <div class="cards">

        ${computer
          .map(cardHTML)
          .join("")}

      </div>


      <button
        class="action"
        id="cardAgain">

        DEAL AGAIN

      </button>

    `;


    if(pScore>=cScore){

      add(
        250,
        true
      );


      result.textContent=
        "🏆 You win! +250 tokens";


      sound("win");

    }else{

      add(-30);


      result.textContent=
        "The computer wins. -30 tokens";


      sound("lose");

    }

  }


  else if(game==="blackjack"){

    title.textContent=
      "♣️ Blackjack";


    let player=[

      randomCard(),
      randomCard()

    ];


    let dealer=[

      randomCard(),
      randomCard()

    ];


    const total =
      cardsTotal(
        player
      );


    const dTotal =
      cardsTotal(
        dealer
      );


    content.innerHTML=`

      <p>
        Your hand:
        ${total}
      </p>


      <div class="cards">

        ${player
          .map(cardHTML)
          .join("")}

      </div>


      <p>
        Dealer:
        ${dTotal}
      </p>


      <div class="cards">

        ${dealer
          .map(cardHTML)
          .join("")}

      </div>


      <div class="actionRow">

        <button
          class="action"
          id="hitBtn">

          HIT

        </button>


        <button
          class="action green"
          id="standBtn">

          STAND

        </button>


        <button
          class="action gold"
          id="doubleBtn">

          DOUBLE DOWN

        </button>

      </div>

    `;


    const finish=()=>{

      const p =
        cardsTotal(
          player
        );


      const d =
        cardsTotal(
          dealer
        );


      if(p>21){

        add(-40);


        result.textContent=
          "💥 Bust! -40 tokens";


        sound("lose");

      }

      else if(
        d>21 ||
        p>d
      ){

        add(
          150,
          true
        );


        result.textContent=
          "🏆 Blackjack win! +150";


        sound("win");

      }

      else if(
        p===d
      ){

        result.textContent=
          "🤝 Push! No tokens lost.";

      }

      else{

        add(-40);


        result.textContent=
          "Dealer wins. -40 tokens";


        sound("lose");

      }

    };


    document
      .getElementById(
        "hitBtn"
      )
      .onclick=()=>{

        player.push(
          randomCard()
        );


        content
          .querySelector("p")
          .textContent=
            "Your hand: "+
            cardsTotal(player);


        content
          .querySelector(".cards")
          .innerHTML=
            player
              .map(cardHTML)
              .join("");


        if(
          cardsTotal(player)>=21
        )
          finish();

      };


    document
      .getElementById(
        "standBtn"
      )
      .onclick=finish;


    document
      .getElementById(
        "doubleBtn"
      )
      .onclick=()=>{

        if(S.tokens<80){

          toast(
            "Not enough tokens."
          );

          return;

        }


        player.push(
          randomCard()
        );


        finish();

      };

  }


  else if(game==="baccarat"){

    title.textContent=
      "♦️ Baccarat";


    content.innerHTML=`

      <p>
        Choose your side.
      </p>


      <div class="actionRow">

        <button
          class="action"
          data-bac="Player">

          PLAYER

        </button>


        <button
          class="action gold"
          data-bac="Banker">

          BANKER

        </button>


        <button
          class="action green"
          data-bac="Tie">

          TIE

        </button>

      </div>

    `;


    content
      .querySelectorAll(
        "[data-bac]"
      )
      .forEach(b=>{

        b.onclick=()=>{

          const choice =
            b.dataset.bac;


          const outcomes=[
            "Player",
            "Banker",
            "Tie"
          ];


          const outcome =
            outcomes[
              Math.floor(
                Math.random()*3
              )
            ];


          if(
            choice===outcome
          ){

            add(
              outcome==="Tie"
              ? 500
              : 200,
              true
            );


            result.textContent=
              `🎉 ${outcome} wins!`;


            sound("win");

          }else{

            add(-30);


            result.textContent=
              `Dealer result: ${outcome}`;


            sound("lose");

          }

        };

      });

  }


  else if(game==="war"){

    title.textContent=
      "🃏 War";


    const player =
      randomCard();


    const computer =
      randomCard();


    const pv =
      cardValue(player);


    const cv =
      cardValue(computer);


    content.innerHTML=`

      <div class="cards">

        ${cardHTML(player)}

        ${cardHTML(computer)}

      </div>


      <button
        class="action"
        id="warAgain">

        PLAY WAR

      </button>

    `;


    if(pv>cv){

      add(
        100,
        true
      );


      result.textContent=
        "🏆 Your card wins! +100";


      sound("win");

    }

    else if(pv<cv){

      add(-20);


      result.textContent=
        "Computer wins. -20";


      sound("lose");

    }

    else{

      add(
        50,
        true
      );


      result.textContent=
        "⚔️ WAR! +50";

    }

  }


  else if(game==="gin"){

    title.textContent=
      "🃏 Gin Rummy";


    const hand =
      Array.from(
        {length:10},
        randomCard
      );


    const score =
      hand.reduce(
        (s,c)=>
          s+cardValue(c),
        0
      );


    content.innerHTML=`

      <p>
        Your 10-card hand
      </p>


      <div class="cards">

        ${hand
          .map(cardHTML)
          .join("")}

      </div>


      <p>
        Meld score:
        ${score}
      </p>


      <button
        class="action"
        id="ginBtn">

        KNOCK

      </button>

    `;


    document
      .getElementById(
        "ginBtn"
      )
      .onclick=()=>{

        if(score>=60){

          add(
            300,
            true
          );


          result.textContent=
            "🎉 Great meld! +300";


          sound("win");

        }else{

          add(
            40,
            true
          );


          result.textContent=
            "Nice hand! +40";

        }

      };

  }


  else if(game==="holdem"){

    title.textContent=
      "♠️ Texas Hold'em";


    const hand =
      Array.from(
        {length:2},
        randomCard
      );


    const board =
      Array.from(
        {length:5},
        randomCard
      );


    const score =
      [
        ...hand,
        ...board
      ].reduce(
        (s,c)=>
          s+cardValue(c),
        0
      );


    content.innerHTML=`

      <p>
        Your hand
      </p>


      <div class="cards">

        ${hand
          .map(cardHTML)
          .join("")}

      </div>


      <p>
        Community cards
      </p>


      <div class="cards">

        ${board
          .map(cardHTML)
          .join("")}

      </div>


      <button
        class="action"
        id="holdemBtn">

        REVEAL RESULT

      </button>

    `;


    document
      .getElementById(
        "holdemBtn"
      )
      .onclick=()=>{

        if(score>=55){

          add(
            250,
            true
          );


          result.textContent=
            "🔥 Strong Hold'em hand! +250";


          sound("win");

        }else{

          add(-30);


          result.textContent=
            "The table beats you. -30";


          sound("lose");

        }

      };

  }

}


function cardsTotal(cards){

  let total=0;

  let aces=0;


  cards.forEach(card=>{

    total +=
      cardValue(card);


    if(
      card.rank==="A"
    )
      aces++;

  });


  while(
    total>21 &&
    aces>0
  ){

    total-=10;

    aces--;

  }


  return total;

}


/* =====================================================
   LUCKY GAMES
===================================================== */

document
  .querySelectorAll(
    "[data-lucky]"
  )
  .forEach(btn=>{

    btn.onclick=()=>{

      const game =
        btn.dataset.lucky;


      const panel =
        document.getElementById(
          "luckyPanel"
        );


      panel.classList.remove(
        "hidden"
      );


      luckyGame(
        game,
        document.getElementById(
          "luckyContent"
        )
      );


      panel.scrollIntoView({
        behavior:"smooth"
      });

    };

  });


function luckyGame(
  game,
  content
){

  if(game==="wheel"){

    content.innerHTML=`

      <h2>
        🎡 Lucky Wheel
      </h2>


      <div class="wheelWrap">

        <div class="pointer">
          ▼
        </div>


        <div
          class="wheel"
          id="wheel">
        </div>


        <div class="centerDot">
          💗
        </div>

      </div>


      <button
        class="spin"
        id="wheelSpin">

        SPIN

      </button>


      <div
        class="result"
        id="wheelResult">
      </div>

    `;


    let rotation=0;


    document
      .getElementById(
        "wheelSpin"
      )
      .onclick=()=>{

        const prizes=[

          50,
          100,
          250,
          500,
          1000,
          2500,
          5000,
          10000

        ];


        const prize =
          prizes[
            Math.floor(
              Math.random()*
              prizes.length
            )
          ];


        rotation +=
          1440 +
          Math.floor(
            Math.random()*720
          );


        document
          .getElementById(
            "wheel"
          )
          .style.transform=
            `rotate(${rotation}deg)`;


        sound("spin");


        setTimeout(
          ()=>{

            add(
              prize,
              true
            );


            document
              .getElementById(
                "wheelResult"
              )
              .textContent=
                `🎉 You won ${format(prize)} tokens!`;


            sound("win");

          },
          3000
        );

      };

  }


  else if(
    game==="roulette"
  ){

    content.innerHTML=`

      <h2>
        🔴⚫ Friendship Roulette
      </h2>


      <div class="actionRow">

        <button
          class="action red"
          data-choice="red">

          🔴 RED

        </button>


        <button
          class="action"
          data-choice="black">

          ⚫ BLACK

        </button>


        <button
          class="action green"
          data-choice="green">

          🟢 GREEN

        </button>

      </div>


      <div
        class="result"
        id="rouletteResult">
      </div>

    `;


    content
      .querySelectorAll(
        "[data-choice]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const choices=[
            "red",
            "black",
            "green"
          ];


          const result =
            choices[
              Math.floor(
                Math.random()*3
              )
            ];


          if(
            btn.dataset.choice===
            result
          ){

            const prize =
              result==="green"
              ? 1000
              : 150;


            add(
              prize,
              true
            );


            document
              .getElementById(
                "rouletteResult"
              )
              .textContent=
                `🎉 ${result.toUpperCase()}! +${prize}`;


            sound("win");

          }else{

            add(-30);


            document
              .getElementById(
                "rouletteResult"
              )
              .textContent=
                `The wheel landed ${result}. -30`;


            sound("lose");

          }

        };

      });

  }


  else if(
    game==="craps"
  ){

    content.innerHTML=`

      <h2>
        🎲 Craps
      </h2>


      <button
        class="action"
        id="rollDice">

        ROLL DICE

      </button>


      <div
        class="result"
        id="diceResult">
      </div>

    `;


    document
      .getElementById(
        "rollDice"
      )
      .onclick=()=>{

        const a =
          Math.floor(
            Math.random()*6
          )+1;


        const b =
          Math.floor(
            Math.random()*6
          )+1;


        const total =
          a+b;


        if(
          total===7 ||
          total===11
        ){

          add(
            200,
            true
          );


          diceResult.textContent=
            `🎉 ${a}+${b} = ${total}. +200`;


          sound("win");

        }else{

          add(-20);


          diceResult.textContent=
            `${a}+${b} = ${total}. -20`;


          sound("lose");

        }

      };

  }


  else if(
    game==="hilo"
  ){

    let current =
      Math.floor(
        Math.random()*13
      )+1;


    content.innerHTML=`

      <h2>
        📈 Hi-Lo
      </h2>


      <h3>
        Current card:
        ${current}
      </h3>


      <div class="actionRow">

        <button
          class="action"
          data-hilo="higher">

          HIGHER

        </button>


        <button
          class="action gold"
          data-hilo="lower">

          LOWER

        </button>

      </div>


      <div
        class="result"
        id="hiloResult">
      </div>

    `;


    content
      .querySelectorAll(
        "[data-hilo]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const next =
            Math.floor(
              Math.random()*13
            )+1;


          const prediction =
            btn.dataset.hilo;


          const won =
            prediction==="higher"
            ? next>current
            : next<current;


          if(won){

            add(
              120,
              true
            );


            hiloResult.textContent=
              `🎉 Next card: ${next}. +120`;


            sound("win");

          }else{

            add(-25);


            hiloResult.textContent=
              `Next card: ${next}. -25`;


            sound("lose");

          }


          current=next;

        };

      });

  }


  else if(
    game==="coin"
  ){

    content.innerHTML=`

      <h2>
        🪙 Coin Flip
      </h2>


      <div class="actionRow">

        <button
          class="action"
          data-coin="Heads">

          HEADS

        </button>


        <button
          class="action gold"
          data-coin="Tails">

          TAILS

        </button>

      </div>


      <div
        class="result"
        id="coinResult">
      </div>

    `;


    content
      .querySelectorAll(
        "[data-coin]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const result =
            Math.random()<.5
            ? "Heads"
            : "Tails";


          if(
            btn.dataset.coin===
            result
          ){

            add(
              100,
              true
            );


            coinResult.textContent=
              `🪙 ${result}! +100`;


            sound("win");

          }else{

            add(-20);


            coinResult.textContent=
              `🪙 ${result}. -20`;


            sound("lose");

          }

        };

      });

  }


  else if(
    game==="plinko"
  ){

    content.innerHTML=`

      <h2>
        🟣 Plinko
      </h2>


      <p>
        Drop the token and see where it lands.
      </p>


      <button
        class="action"
        id="plinkoBtn">

        DROP TOKEN

      </button>


      <div
        class="result"
        id="plinkoResult">
      </div>

    `;


    document
      .getElementById(
        "plinkoBtn"
      )
      .onclick=()=>{

        const prizes=[

          0,
          50,
          100,
          250,
          500,
          1000,
          2500

        ];


        const prize =
          prizes[
            Math.floor(
              Math.random()*
              prizes.length
            )
          ];


        if(prize===0){

          add(-20);


          plinkoResult.textContent=
            "The token fell into the 0 pocket. -20";

        }else{

          add(
            prize,
            true
          );


          plinkoResult.textContent=
            `🟣 Plinko landed on ${prize}!`;


          sound("win");

        }

      };

  }

}


/* =====================================================
   RACES
===================================================== */

document
  .querySelectorAll(
    "[data-race]"
  )
  .forEach(btn=>{

    btn.onclick=()=>{

      const type =
        btn.dataset.race;


      const panel =
        document.getElementById(
          "racePanel"
        );


      panel.classList.remove(
        "hidden"
      );


      race(type);


      panel.scrollIntoView({
        behavior:"smooth"
      });

    };

  });


function race(type){

  const names =
    type==="horse"

    ? [
        "Thunder",
        "Rose",
        "Lucky",
        "Rocket"
      ]

    : [
        "Dolphini",
        "Splash",
        "Pearl",
        "Wave"
      ];


  document.getElementById(
    "raceTitle"
  ).textContent=
    type==="horse"
    ? "🏇 Horse Derby"
    : "🐬 Dolphin Derby";


  document.getElementById(
    "raceContent"
  ).innerHTML=`

    <p>
      Choose your racer.
    </p>


    <div class="actionRow">

      ${names.map(
        (n,i)=>`

          <button
            class="action"
            data-racer="${i}">

            ${
              type==="horse"
              ? "🏇"
              : "🐬"
            }

            ${n}

          </button>

        `
      ).join("")}

    </div>

  `;


  document
    .querySelectorAll(
      "[data-racer]"
    )
    .forEach(btn=>{

      btn.onclick=()=>{

        const chosen =
          Number(
            btn.dataset.racer
          );


        const winner =
          Math.floor(
            Math.random()*
            names.length
          );


        if(
          chosen===winner
        ){

          add(
            500,
            true
          );


          document.getElementById(
            "raceResult"
          ).textContent=
            `🏆 ${names[winner]} wins! +500`;


          sound("win");

        }else{

          add(-30);


          document.getElementById(
            "raceResult"
          ).textContent=
            `🏁 ${names[winner]} wins. -30`;


          sound("lose");

        }

      };

    });

}


/* =====================================================
   MINI GAMES
===================================================== */

document
  .querySelectorAll(
    "[data-mini]"
  )
  .forEach(btn=>{

    btn.onclick=()=>{

      const game =
        btn.dataset.mini;


      const panel =
        document.getElementById(
          "miniPanel"
        );


      panel.classList.remove(
        "hidden"
      );


      miniGame(game);


      panel.scrollIntoView({
        behavior:"smooth"
      });

    };

  });


function miniGame(game){

  const title =
    document.getElementById(
      "miniTitle"
    );


  const content =
    document.getElementById(
      "miniContent"
    );


  const result =
    document.getElementById(
      "miniResult"
    );


  result.textContent="";


  if(game==="box"){

    title.textContent=
      "🎁 Mystery Boxes";


    content.innerHTML=`

      <div class="actionRow">

        <button
          class="action"
          data-box="1">

          🎁 Box 1

        </button>


        <button
          class="action"
          data-box="2">

          🎁 Box 2

        </button>


        <button
          class="action"
          data-box="3">

          🎁 Box 3

        </button>

      </div>

    `;


    content
      .querySelectorAll(
        "[data-box]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const prizes=[
            50,
            100,
            250,
            500,
            1000
          ];


          const prize =
            prizes[
              Math.floor(
                Math.random()*
                prizes.length
              )
            ];


          add(
            prize,
            true
          );


          result.textContent=
            `🎁 You found ${prize} tokens!`;


          sound("win");

        };

      });

  }


  else if(
    game==="cups"
  ){

    title.textContent=
      "🪙 Three Cups";


    content.innerHTML=`

      <p>
        One cup hides the friendship token.
      </p>


      <div class="actionRow">

        ${[1,2,3].map(
          i=>`

            <button
              class="action"
              data-cup="${i}">

              🥤 Cup ${i}

            </button>

          `
        ).join("")}

      </div>

    `;


    content
      .querySelectorAll(
        "[data-cup]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const winner =
            Math.floor(
              Math.random()*3
            )+1;


          if(
            Number(
              btn.dataset.cup
            )===winner
          ){

            add(
              300,
              true
            );


            result.textContent=
              "🪙 You found it! +300";


            sound("win");

          }else{

            add(-20);


            result.textContent=
              `Empty cup! It was under cup ${winner}.`;


            sound("lose");

          }

        };

      });

  }


  else if(
    game==="scratch"
  ){

    title.textContent=
      "💗 Heart Scratch Card";


    content.innerHTML=`

      <button
        class="action"
        id="scratchBtn">

        💗 SCRATCH

      </button>

    `;


    scratchBtn.onclick=()=>{

      const prize =
        Math.floor(
          Math.random()*6
        )*100;


      if(prize===0){

        add(-10);


        result.textContent=
          "💔 Nothing this time.";

      }else{

        add(
          prize,
          true
        );


        result.textContent=
          `💗 You scratched ${prize} tokens!`;


        sound("win");

      }

    };

  }


  else if(
    game==="darts"
  ){

    title.textContent=
      "🎯 Lucky Darts";


    content.innerHTML=`

      <button
        class="action"
        id="dartBtn">

        🎯 THROW DART

      </button>

    `;


    dartBtn.onclick=()=>{

      const score =
        Math.floor(
          Math.random()*100
        )+1;


      const prize =
        score>=90
        ? 500
        : score>=70
        ? 200
        : score>=40
        ? 75
        : 0;


      if(prize){

        add(
          prize,
          true
        );


        result.textContent=
          `🎯 Score ${score}! +${prize}`;


        sound("win");

      }else{

        add(-20);


        result.textContent=
          `🎯 Score ${score}. -20`;

      }

    };

  }


  else if(
    game==="gems"
  ){

    title.textContent=
      "💎 Gem Heist";


    content.innerHTML=`

      <p>
        Choose a vault.
      </p>


      <div class="actionRow">

        ${[1,2,3,4].map(
          i=>`

            <button
              class="action"
              data-gem="${i}">

              💎 Vault ${i}

            </button>

          `
        ).join("")}

      </div>

    `;


    content
      .querySelectorAll(
        "[data-gem]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const prize =
            [
              100,
              250,
              500,
              1000
            ][
              Math.floor(
                Math.random()*4
              )
            ];


          add(
            prize,
            true
          );


          result.textContent=
            `💎 Heist successful! +${prize}`;


          sound("win");

        };

      });

  }


  else if(
    game==="envelopes"
  ){

    title.textContent=
      "🎁 Lucky Envelopes";


    content.innerHTML=`

      <div class="actionRow">

        ${[
          "A",
          "B",
          "C",
          "D"
        ].map(
          x=>`

            <button
              class="action"
              data-envelope="${x}">

              ✉️ ${x}

            </button>

          `
        ).join("")}

      </div>

    `;


    content
      .querySelectorAll(
        "[data-envelope]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const prize =
            [
              100,
              250,
              500,
              1000
            ][
              Math.floor(
                Math.random()*4
              )
            ];


          add(
            prize,
            true
          );


          result.textContent=
            `✉️ Envelope ${btn.dataset.envelope}: +${prize}`;


          sound("win");

        };

      });

  }


  else if(
    game==="number"
  ){

    title.textContent=
      "🔢 Lucky Number";


    content.innerHTML=`

      <p>
        Guess a number from 1 to 10.
      </p>


      <input
        id="numberGuess"
        type="number"
        min="1"
        max="10"
        placeholder="1-10"
      >


      <br><br>


      <button
        class="action"
        id="guessBtn">

        GUESS

      </button>

    `;


    guessBtn.onclick=()=>{

      const guess =
        Number(
          numberGuess.value
        );


      if(
        !Number.isInteger(guess) ||
        guess<1 ||
        guess>10
      ){

        toast(
          "Enter a number from 1 to 10."
        );

        return;

      }


      const lucky =
        Math.floor(
          Math.random()*10
        )+1;


      if(
        guess===lucky
      ){

        add(
          1000,
          true
        );


        result.textContent=
          `🎉 Correct! The number was ${lucky}. +1000`;


        sound("win");

      }else{

        add(-25);


        result.textContent=
          `The number was ${lucky}. -25`;


        sound("lose");

      }

    };

  }


  else if(
    game==="treasure"
  ){

    title.textContent=
      "🐠 Ocean Treasure";


    content.innerHTML=`

      <p>
        Choose one treasure spot.
      </p>


      <div class="actionRow">

        ${[
          1,
          2,
          3,
          4,
          5
        ].map(
          i=>`

            <button
              class="action"
              data-treasure="${i}">

              🐠 Spot ${i}

            </button>

          `
        ).join("")}

      </div>

    `;


    content
      .querySelectorAll(
        "[data-treasure]"
      )
      .forEach(btn=>{

        btn.onclick=()=>{

          const prize =
            [
              50,
              100,
              250,
              500,
              1500
            ][
              Math.floor(
                Math.random()*5
              )
            ];


          add(
            prize,
            true
          );


          result.textContent=
            `🌊 Treasure found! +${prize}`;


          sound("win");

        };

      });

  }

}


/* =====================================================
   FRIENDSHIP CATCH
===================================================== */

const creatureInfo={

  Dolphini:[
    "🐬",
    "Common",
    100
  ],

  Rosibun:[
    "🌹🐰",
    "Uncommon",
    150
  ],

  Sunnyflo:[
    "🌻",
    "Common",
    100
  ],

  Pinkyroo:[
    "🦘💗",
    "Rare",
    300
  ],

  Fluttera:[
    "🦋",
    "Rare",
    300
  ],

  Shellby:[
    "🐚",
    "Epic",
    500
  ],

  Lunaboo:[
    "🌙",
    "Legendary",
    1000
  ]

};


document
  .querySelectorAll(
    ".creature"
  )
  .forEach(btn=>{

    btn.onclick=()=>{

      const name =
        btn.dataset.creature;


      const info =
        creatureInfo[name];


      const chance =
        info[1]==="Legendary"
        ? .25
        : info[1]==="Epic"
        ? .45
        : info[1]==="Rare"
        ? .65
        : .82;


      if(
        Math.random()<chance
      ){

        if(
          !S.caught.includes(name)
        )
          S.caught.push(name);


        add(
          info[2],
          true
        );


        btn.style.display="none";


        renderCollection();


        toast(
          `✨ You caught ${name}! +${info[2]} tokens`
        );


        sound("win");


        if(
          S.caught.length>=5
        )
          achievement(
            "collector"
          );

      }else{

        toast(
          `${name} escaped! 🐬`
        );


        sound("lose");

      }


      save();

    };

  });


function renderCollection(){

  const el =
    document.getElementById(
      "collection"
    );


  if(!S.caught.length){

    el.innerHTML=
      `

        <div class="creatureBadge">

          No creatures caught yet.

        </div>

      `;

    return;

  }


  el.innerHTML =
    S.caught
      .map(name=>{

        const info =
          creatureInfo[name];


        return `

          <div
            class="creatureBadge">

            ${info[0]}
            ${name}
            · ${info[1]}

          </div>

        `;

      })
      .join("");

}


/* =====================================================
   QUIZ
===================================================== */

const quiz=[

  [
    "What is Liliana's favourite colour?",
    [
      "Baby pink",
      "Blue",
      "Green",
      "Purple"
    ],
    0
  ],

  [
    "What food does Liliana love?",
    [
      "Pizza",
      "Sushi",
      "Tacos",
      "Pasta"
    ],
    1
  ],

  [
    "What animal does Liliana love?",
    [
      "Dolphins",
      "Lions",
      "Penguins",
      "Koalas"
    ],
    0
  ],

  [
    "What is Liliana's favourite number?",
    [
      "3",
      "7",
      "13",
      "22"
    ],
    0
  ],

  [
    "What is Liliana's birthday?",
    [
      "July 2",
      "July 12",
      "July 22",
      "August 22"
    ],
    2
  ],

  [
    "What is Liliana's star sign?",
    [
      "Cancer",
      "Leo",
      "Virgo",
      "Gemini"
    ],
    1
  ],

  [
    "How many nieces does Liliana have?",
    [
      "0",
      "1",
      "2",
      "3"
    ],
    1
  ],

  [
    "How many nephews does Liliana have?",
    [
      "2",
      "3",
      "4",
      "5"
    ],
    2
  ],

  [
    "How many tattoos does Liliana have?",
    [
      "1",
      "2",
      "3",
      "4"
    ],
    0
  ],

  [
    "What colour are Liliana's eyes?",
    [
      "Blue",
      "Brown",
      "Green",
      "Hazel"
    ],
    2
  ],

  [
    "How many piercings does Liliana have?",
    [
      "2",
      "3",
      "4",
      "5"
    ],
    2
  ],

  [
    "What are Liliana's dogs called?",
    [
      "Aayla & Arlo",
      "Luna & Milo",
      "Bella & Max",
      "Coco & Leo"
    ],
    0
  ],

  [
    "How many siblings does Liliana have?",
    [
      "3",
      "4",
      "5",
      "6"
    ],
    2
  ],

  [
    "What is Liliana afraid of?",
    [
      "Heights",
      "Drowning",
      "Thunder",
      "Dogs"
    ],
    1
  ],

  [
    "What does Liliana study at university?",
    [
      "Psychology",
      "Law",
      "Medicine",
      "Art"
    ],
    0
  ],

  [
    "What movie does Liliana love?",
    [
      "Titanic",
      "Me Before You",
      "Frozen",
      "The Notebook"
    ],
    1
  ],

  [
    "What does Liliana one day want to be?",
    [
      "A singer",
      "A mum to a baby girl",
      "A pilot",
      "A chef"
    ],
    1
  ],

  [
    "What does Liliana like?",
    [
      "Poetry",
      "Only sports",
      "Only horror movies",
      "None"
    ],
    0
  ],

  [
    "What kind of personality does Liliana have?",
    [
      "Empathetic",
      "Cold",
      "Shy",
      "Serious"
    ],
    0
  ],

  [
    "How long have Bree and Liliana been best friends?",
    [
      "2 years",
      "4 years",
      "6 years",
      "10 years"
    ],
    2
  ]

];


let quizIndex=0;

let quizScore=0;


document
  .getElementById(
    "startQuiz"
  )
  .onclick=()=>{

    quizIndex=0;

    quizScore=0;

    showQuiz();


    document
      .getElementById(
        "lilianaPanel"
      )
      .scrollIntoView({
        behavior:"smooth"
      });

  };


function showQuiz(){

  const content =
    document.getElementById(
      "lilianaContent"
    );


  if(
    quizIndex>=quiz.length
  ){

    S.quizBest =
      Math.max(
        S.quizBest,
        quizScore
      );


    const reward =
      quizScore===20
      ? 5000
      : quizScore*100;


    add(
      reward,
      true
    );


    if(
      quizScore===20
    )
      achievement(
        "quiz"
      );


    content.innerHTML=`

      <h2>
        🎉 Quiz Complete!
      </h2>


      <p>
        You scored
        <strong>
          ${quizScore}/20
        </strong>.
      </p>


      <p>
        💰 Reward:
        <strong>
          +${format(reward)}
        </strong>
      </p>


      <button
        class="action"
        id="restartQuiz">

        PLAY AGAIN

      </button>

    `;


    sound(
      quizScore===20
      ? "jackpot"
      : "win"
    );


    document
      .getElementById(
        "restartQuiz"
      )
      .onclick=()=>{

        quizIndex=0;

        quizScore=0;

        showQuiz();

      };


    return;

  }


  const q =
    quiz[
      quizIndex
    ];


  content.innerHTML=`

    <div class="question">

      ${quizIndex+1}/20 ·
      ${q[0]}

    </div>


    <div class="answers">

      ${q[1]
        .map(
          (answer,i)=>`

            <button
              class="answer"
              data-answer="${i}">

              ${answer}

            </button>

          `
        )
        .join("")}

    </div>

  `;


  content
    .querySelectorAll(
      "[data-answer]"
    )
    .forEach(btn=>{

      btn.onclick=()=>{

        if(
          Number(
            btn.dataset.answer
          )===q[2]
        ){

          quizScore++;

          sound("win");

        }else{

          sound("lose");

        }


        quizIndex++;


        showQuiz();

      };

    });

}


/* =====================================================
   PERSONALITY TEST
===================================================== */

document
  .getElementById(
    "personality"
  )
  .onclick=()=>{

    const results=[

      [
        "🌸 The Soft Liliana",
        "Sweet, caring and deeply empathetic."
      ],

      [
        "💋 The Flirty Liliana",
        "Charismatic, playful and impossible to ignore."
      ],

      [
        "🎰 The Gambler Liliana",
        "Risk taker, poker face and casino queen."
      ],

      [
        "🐬 The Dreamer Liliana",
        "Romantic, thoughtful and full of dreams."
      ],

      [
        "👑 The Main Character Liliana",
        "Confident, magnetic and absolutely unforgettable."
      ]

    ];


    const result =
      results[
        Math.floor(
          Math.random()*
          results.length
        )
      ];


    add(
      300,
      true
    );


    document.getElementById(
      "lilianaContent"
    ).innerHTML=`

      <h2>
        ${result[0]}
      </h2>


      <p>
        ${result[1]}
      </p>


      <p>
        💰 +300 Friendship Tokens
      </p>

    `;


    sound("win");

  };


/* =====================================================
   TIMELINE
===================================================== */

document
  .getElementById(
    "timelineBtn"
  )
  .onclick=()=>{

    document.getElementById(
      "lilianaContent"
    ).innerHTML=`

      <h2>
        📖 Six Years of Friendship
      </h2>


      <div class="timeline">


        <div class="year">

          <strong>
            Year 1 🌸
          </strong>

          <p>
            The beginning of the friendship.
          </p>

        </div>


        <div class="year">

          <strong>
            Year 2 💗
          </strong>

          <p>
            More memories, more chaos and more laughs.
          </p>

        </div>


        <div class="year">

          <strong>
            Year 3 🌻
          </strong>

          <p>
            The friendship keeps growing.
          </p>

        </div>


        <div class="year">

          <strong>
            Year 4 🦋
          </strong>

          <p>
            Six years starts feeling inevitable.
          </p>

        </div>


        <div class="year">

          <strong>
            Year 5 💎
          </strong>

          <p>
            Still here. Still best friends.
          </p>

        </div>


        <div class="year">

          <strong>
            Year 6 👑
          </strong>

          <p>
            Six years down. Many more memories to come.
          </p>

        </div>


      </div>

    `;

  };


/* =====================================================
   FRIENDSHIP LETTER
===================================================== */

document
  .getElementById(
    "letterBtn"
  )
  .onclick=()=>{

    document.getElementById(
      "lilianaContent"
    ).innerHTML=`

      <div class="panel">

        <h2>
          💌 To My Best Friend
        </h2>


        <p>
          Six years is a lot of memories,
          laughs, chaos, conversations and
          moments that somehow became part
          of who we are.
        </p>


        <p>
          Through every version of life,
          one thing has stayed the same:
          you're my best friend.
        </p>


        <p>
          So this ridiculous little casino
          is basically six years of friendship
          turned into tokens, games and
          questionable financial decisions. 😂
        </p>


        <p>
          Here's to everything we've already
          lived through and everything still
          waiting for us.
        </p>


        <p>
          💗 Happy six years, bestie.
        </p>

      </div>

    `;

  };


/* =====================================================
   VIP VAULT
===================================================== */

document
  .getElementById(
    "vaultButton"
  )
  .onclick=()=>{

    const input =
      document.getElementById(
        "vaultCode"
      );


    const code =
      input.value.trim();


    const result =
      document.getElementById(
        "vaultResult"
      );


    if(
      code==="060722"
    ){

      if(S.vaultOpened){

        result.textContent=
          "🔓 The vault is already open.";

        return;

      }


      S.vaultOpened=true;


      add(
        10000,
        true
      );


      achievement(
        "vault"
      );


      result.textContent=
        "🔓 VAULT OPENED! +10,000 TOKENS!";


      sound("jackpot");


      save();

    }else{

      result.textContent=
        "❌ Incorrect six-digit code.";


      sound("lose");

    }

  };


/* =====================================================
   INITIALISE
===================================================== */

renderCollection();

update();


if(
  S.sound===false
){

  document.getElementById(
    "soundBtn"
  ).textContent="🔇";

}

</script>

</body>
</html>
