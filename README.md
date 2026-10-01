<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Liliana's Friendship Casino ♡</title>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

:root {
  --pink: #f4a9c4;
  --light-pink: #ffe6ef;
  --dark-pink: #b94d73;
  --deep: #321c29;
  --cream: #fff9fb;
  --gold: #d8aa55;
  --white: #ffffff;
}

body {
  font-family: Georgia, "Times New Roman", serif;
  background:
    radial-gradient(circle at top, #5a3046 0%, #261722 45%, #160e14 100%);
  color: white;
  min-height: 100vh;
  overflow-x: hidden;
}

body::before {
  content: "♠ ♥ ♣ ♦";
  position: fixed;
  inset: 0;
  font-size: 70px;
  opacity: .035;
  letter-spacing: 80px;
  line-height: 180px;
  pointer-events: none;
  transform: rotate(-15deg);
}

button {
  font: inherit;
}

#app {
  width: min(1100px, 94%);
  margin: auto;
  padding: 20px 0 50px;
}

/* ---------------- HEADER ---------------- */

.header {
  text-align: center;
  padding: 30px 15px;
}

.crown {
  font-size: 35px;
  margin-bottom: 8px;
}

.header h1 {
  font-size: clamp(42px, 9vw, 80px);
  color: var(--light-pink);
  text-shadow: 0 5px 25px rgba(244,169,196,.3);
  letter-spacing: 3px;
}

.header h2 {
  color: var(--pink);
  font-size: clamp(18px, 4vw, 28px);
  margin-top: 8px;
}

.header p {
  max-width: 650px;
  margin: 15px auto;
  color: #eadce2;
  line-height: 1.7;
}

/* ---------------- CASINO BOARD ---------------- */

.board {
  background: rgba(255,255,255,.07);
  border: 1px solid rgba(255,255,255,.15);
  border-radius: 30px;
  padding: 20px;
  backdrop-filter: blur(10px);
}

.balance {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  flex-wrap: wrap;
  background: linear-gradient(135deg,#f7cad9,#e99ab8);
  color: var(--deep);
  padding: 16px 20px;
  border-radius: 18px;
  margin-bottom: 20px;
  font-weight: bold;
}

.tokens {
  font-size: 25px;
}

/* ---------------- NAV ---------------- */

.nav {
  display: grid;
  grid-template-columns: repeat(4,1fr);
  gap: 9px;
  margin-bottom: 20px;
}

.nav button {
  border: 1px solid rgba(255,255,255,.15);
  background: #432638;
  color: white;
  padding: 13px 8px;
  border-radius: 13px;
  cursor: pointer;
  min-height: 48px;
  transition: .2s;
}

.nav button:hover,
.nav button.active {
  background: var(--pink);
  color: var(--deep);
  transform: translateY(-2px);
}

.page {
  display: none;
}

.page.active {
  display: block;
}

/* ---------------- SECTIONS ---------------- */

.section {
  background: var(--cream);
  color: var(--deep);
  border-radius: 25px;
  padding: 25px;
  margin-bottom: 20px;
}

.section h2 {
  color: var(--dark-pink);
  margin-bottom: 10px;
  font-size: 30px;
}

.subtitle {
  color: #765363;
  line-height: 1.6;
  margin-bottom: 20px;
}

/* ---------------- SLOT MACHINE ---------------- */

.machine {
  max-width: 700px;
  margin: auto;
  background: linear-gradient(145deg,#6d304b,#351725);
  border: 6px solid var(--gold);
  border-radius: 30px;
  padding: 25px;
  text-align: center;
  box-shadow: 0 15px 50px rgba(0,0,0,.35);
}

.machine-title {
  color: #ffe9a8;
  letter-spacing: 3px;
  font-weight: bold;
  margin-bottom: 20px;
}

.reels {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 10px;
}

.reel {
  background: white;
  color: var(--deep);
  border-radius: 15px;
  height: 125px;
  display: grid;
  place-items: center;
  font-size: 65px;
  border: 5px solid #e8d4b2;
  overflow: hidden;
}

.reel.spin {
  animation: spin .12s linear infinite;
}

@keyframes spin {
  0% { transform: translateY(-5px); }
  50% { transform: translateY(5px); }
  100% { transform: translateY(-5px); }
}

.pull {
  margin-top: 20px;
  padding: 17px 35px;
  border-radius: 50px;
  border: 3px solid #ffe7a5;
  background: var(--pink);
  color: var(--deep);
  font-weight: bold;
  cursor: pointer;
  font-size: 18px;
}

.pull:hover {
  transform: scale(1.05);
}

.slot-result {
  min-height: 60px;
  padding-top: 18px;
  color: #ffe9a8;
  font-weight: bold;
  line-height: 1.5;
}

/* ---------------- STATS ---------------- */

.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(140px,1fr));
  gap: 12px;
  margin-top: 20px;
}

.stat {
  background: #fff0f5;
  border-radius: 16px;
  padding: 17px;
  text-align: center;
}

.stat strong {
  display: block;
  font-size: 27px;
  color: var(--dark-pink);
}

.stat span {
  font-size: 13px;
  color: #775564;
}

/* ---------------- POKER ---------------- */

.poker-table {
  background: radial-gradient(circle,#46704e,#163a27);
  border: 6px solid var(--gold);
  border-radius: 40px;
  padding: 30px 20px;
  text-align: center;
}

.cards {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  margin: 20px 0;
}

.card {
  width: 90px;
  height: 125px;
  background: white;
  color: #21151b;
  border-radius: 12px;
  border: 3px solid #eee;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 9px;
  font-weight: bold;
  cursor: pointer;
  transition: .2s;
}

.card:hover {
  transform: translateY(-8px);
}

.card.red {
  color: #bd3e5b;
}

.card .symbol {
  font-size: 34px;
}

.poker-message {
  min-height: 55px;
  color: #ffe9a8;
  font-weight: bold;
  line-height: 1.5;
}

/* ---------------- PICK A CARD ---------------- */

.pick-cards {
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 15px;
  max-width: 650px;
  margin: 25px auto;
}

.mystery {
  min-height: 190px;
  border: 3px solid var(--gold);
  border-radius: 18px;
  background: linear-gradient(145deg,#7c3e58,#351725);
  color: white;
  cursor: pointer;
  font-size: 55px;
  transition: .25s;
}

.mystery:hover {
  transform: translateY(-7px) rotate(1deg);
}

/* ---------------- PRIZES ---------------- */

.prizes {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(210px,1fr));
  gap: 14px;
}

.prize {
  background: white;
  border: 2px solid #f1cedb;
  border-radius: 18px;
  padding: 18px;
}

.prize.locked {
  opacity: .5;
}

.prize h3 {
  color: var(--dark-pink);
  margin-bottom: 7px;
}

.prize button {
  margin-top: 12px;
  border: none;
  background: var(--dark-pink);
  color: white;
  padding: 10px 14px;
  border-radius: 10px;
  cursor: pointer;
}

/* ---------------- LILIANA FILE ---------------- */

.profile {
  display: grid;
  grid-template-columns: repeat(auto-fit,minmax(150px,1fr));
  gap: 12px;
}

.fact {
  background: #fff0f5;
  border-radius: 17px;
  padding: 17px;
  text-align: center;
}

.fact .emoji {
  font-size: 30px;
}

.fact small {
  display: block;
  color: #80616f;
  margin-top: 5px;
}

/* ---------------- SIX YEARS ---------------- */

.timeline {
  position: relative;
  display: grid;
  gap: 13px;
}

.memory {
  border-left: 6px solid var(--pink);
  background: white;
  padding: 18px;
  border-radius: 0 16px 16px 0;
}

.memory strong {
  color: var(--dark-pink);
  font-size: 21px;
}

.memory p {
  margin-top: 7px;
  line-height: 1.5;
}

textarea {
  width: 100%;
  min-height: 120px;
  margin-top: 15px;
  padding: 15px;
  border: 2px solid #edc7d4;
  border-radius: 15px;
  resize: vertical;
  font: inherit;
}

.action {
  border: none;
  background: var(--dark-pink);
  color: white;
  padding: 13px 18px;
  border-radius: 12px;
  cursor: pointer;
  margin-top: 10px;
}

.action.secondary {
  background: #ead3dc;
  color: var(--deep);
}

/* ---------------- QUIZ ---------------- */

.quiz-question {
  font-size: 23px;
  font-weight: bold;
  margin: 15px 0;
}

.quiz-options {
  display: grid;
  gap: 10px;
}

.quiz-options button {
  border: 2px solid #efd1dc;
  background: white;
  padding: 14px;
  border-radius: 13px;
  text-align: left;
  cursor: pointer;
}

.quiz-options button:hover {
  background: var(--light-pink);
}

.quiz-result {
  margin-top: 18px;
  font-size: 22px;
  font-weight: bold;
  color: var(--dark-pink);
}

/* ---------------- LETTER ---------------- */

.letter {
  background: linear-gradient(145deg,#fff5f9,#ffe2ec);
  padding: 30px;
  border-radius: 20px;
  line-height: 2;
  font-size: 18px;
}

.signature {
  margin-top: 20px;
  font-size: 24px;
  color: var(--dark-pink);
}

/* ---------------- RESPONSIVE ---------------- */

@media(max-width:650px) {

  .nav {
    grid-template-columns: repeat(2,1fr);
  }

  .reel {
    height: 95px;
    font-size: 48px;
  }

  .card {
    width: 75px;
    height: 110px;
  }

  .pick-cards {
    gap: 8px;
  }

  .mystery {
    min-height: 145px;
  }

  .section {
    padding: 18px;
  }
}
</style>
</head>

<body>

<div id="app">

<header class="header">
  <div class="crown">👑</div>

  <h1>LILIANA'S</h1>
  <h2>FRIENDSHIP CASINO ♡</h2>

  <p>
    Six years. Thousands of memories.
    One ridiculously sweet, caring, charismatic and slightly dangerous bestie.
  </p>
</header>

<div class="board">

<div class="balance">
  <div>
    ♡ BESTIE BANK
    <div class="tokens">
      <span id="tokens">6000</span> 💗
    </div>
  </div>

  <div>
    🎂 July 22nd<br>
    <small>Lucky number: 3</small>
  </div>
</div>

<nav class="nav">

<button class="active" data-page="casino">🎰 Casino</button>
<button data-page="poker">♠️ Poker</button>
<button data-page="cards">🃏 Cards</button>
<button data-page="prizes">🎟️ Prizes</button>
<button data-page="liliana">🎀 Liliana</button>
<button data-page="years">🕰️ Six Years</button>
<button data-page="quiz">🧠 Quiz</button>
<button data-page="letter">💌 Letter</button>

</nav>


<!-- ================= CASINO ================= -->

<div id="casino" class="page active">

<section class="section">

<h2>🎰 The Friendship Slot Machine</h2>

<p class="subtitle">
No real money. Just friendship tokens, ridiculous luck and six years
of memories waiting to be unlocked.
</p>

<div class="machine">

<div class="machine-title">
♠ LILIANA'S LUCKY MACHINE ♠
</div>

<div class="reels">

<div class="reel" id="reel1">🌹</div>
<div class="reel" id="reel2">🐬</div>
<div class="reel" id="reel3">3️⃣</div>

</div>

<button class="pull" id="spinButton">
🎰 PULL THE LEVER
</button>

<div class="slot-result" id="slotResult">
Your luck awaits...
</div>

</div>

<div class="stats">

<div class="stat">
<strong>6</strong>
<span>Years Besties</span>
</div>

<div class="stat">
<strong>3</strong>
<span>Lucky Number</span>
</div>

<div class="stat">
<strong>♡</strong>
<span>Best Friend</span>
</div>

<div class="stat">
<strong>∞</strong>
<span>Memories</span>
</div>

</div>

</section>

</div>


<!-- ================= POKER ================= -->

<div id="poker" class="page">

<section class="section">

<h2>♠️ Friendship Poker</h2>

<p class="subtitle">
Your cards aren't money. They're pieces of your friendship.
Click five cards to build your hand.
</p>

<div class="poker-table">

<div style="color:#d9f1df;">
BESTIE TABLE
</div>

<div class="cards" id="pokerCards"></div>

<div class="poker-message" id="pokerMessage">
Choose your five friendship cards.
</div>

<button class="pull" id="dealButton">
DEAL FRIENDSHIP HAND
</button>

</div>

</section>

</div>


<!-- ================= PICK CARDS ================= -->

<div id="cards" class="page">

<section class="section">

<h2>🃏 Pick Your Fortune</h2>

<p class="subtitle">
Liliana has three mystery cards. Only one can be chosen.
What does friendship have waiting?
</p>

<div class="pick-cards">

<button class="mystery" data-card="0">
♠️
<br>
<small>ONE</small>
</button>

<button class="mystery" data-card="1">
♥️
<br>
<small>TWO</small>
</button>

<button class="mystery" data-card="2">
♦️
<br>
<small>THREE</small>
</button>

</div>

<div id="cardResult" class="quiz-result">
Choose your card...
</div>

</section>

</div>


<!-- ================= PRIZES ================= -->

<div id="prizes" class="page">

<section class="section">

<h2>🎟️ Friendship Prize Booth</h2>

<p class="subtitle">
Use your friendship tokens to unlock things hidden around the casino.
</p>

<div class="prizes">

<div class="prize">
<h3>💗 100 Tokens</h3>
<p>A random compliment from Bree.</p>
<button data-cost="100" data-prize="compliment">
Unlock</button>
</div>

<div class="prize">
<h3>🌹 250 Tokens</h3>
<p>A Liliana fact.</p>
<button data-cost="250" data-prize="fact">
Unlock</button>
</div>

<div class="prize">
<h3>🐬 500 Tokens</h3>
<p>A friendship memory.</p>
<button data-cost="500" data-prize="memory">
Unlock</button>
</div>

<div class="prize">
<h3>📸 750 Tokens</h3>
<p>A special photo slot.</p>
<button data-cost="750" data-prize="photo">
Unlock</button>
</div>

<div class="prize">
<h3>💌 1000 Tokens</h3>
<p>A secret message.</p>
<button data-cost="1000" data-prize="secret">
Unlock</button>
</div>

<div class="prize">
<h3>👑 6000 Tokens</h3>
<p>The six-year friendship finale.</p>
<button data-cost="6000" data-prize="finale">
Unlock</button>
</div>

</div>

<div id="prizeResult" class="quiz-result"></div>

</section>

</div>


<!-- ================= LILIANA ================= -->

<div id="liliana" class="page">

<section class="section">

<h2>🎀 The Liliana File</h2>

<p class="subtitle">
Everything that makes Liliana... Liliana.
</p>

<div class="profile">

<div class="fact">
<div class="emoji">🎀</div>
<b>Baby Pink</b>
<small>Favourite colour</small>
</div>

<div class="fact">
<div class="emoji">🍣</div>
<b>Sushi</b>
<small>Favourite food</small>
</div>

<div class="fact">
<div class="emoji">🐬</div>
<b>Dolphins</b>
<small>Favourite animal</small>
</div>

<div class="fact">
<div class="emoji">🌻</div>
<b>Sunflowers</b>
<small>Favourite flower</small>
</div>

<div class="fact">
<div class="emoji">🌹</div>
<b>Roses</b>
<small>Also adored</small>
</div>

<div class="fact">
<div class="emoji">3️⃣</div>
<b>Three</b>
<small>Favourite number</small>
</div>

<div class="fact">
<div class="emoji">🎬</div>
<b>Me Before You</b>
<small>Favourite movie</small>
</div>

<div class="fact">
<div class="emoji">🎵</div>
<b>Sad Songs</b>
<small>Emotional soundtrack</small>
</div>

<div class="fact">
<div class="emoji">📖</div>
<b>Poetry</b>
<small>She loves it</small>
</div>

<div class="fact">
<div class="emoji">♠️</div>
<b>Poker</b>
<small>She likes to play</small>
</div>

<div class="fact">
<div class="emoji">;</div>
<b>Semicolon</b>
<small>Her tattoo</small>
</div>

<div class="fact">
<div class="emoji">🧸</div>
<b>Future Mum</b>
<small>Dreams of a baby girl</small>
</div>

</div>

<div class="section" style="margin-top:20px;background:#fff0f5;">

<h2>🫶 Her Superpowers</h2>

<p style="line-height:1.8;">
<strong>Sweet.</strong>
She has a genuinely soft side.

<br><br>

<strong>Caring.</strong>
She cares deeply about the people around her.

<br><br>

<strong>Charismatic.</strong>
There is something about her that naturally draws people in.

<br><br>

<strong>Empathetic.</strong>
She understands and feels other people's emotions deeply.

<br><br>

<strong>Flirtatious.</strong>
And then there is... that. 😂
</p>

</div>

</section>

</div>


<!-- ================= SIX YEARS ================= -->

<div id="years" class="page">

<section class="section">

<h2>🕰️ Six Years of Us</h2>

<p class="subtitle">
Six years deserves its own museum.
Add memories below and build your friendship timeline.
</p>

<div class="timeline">

<div class="memory">
<strong>YEAR ONE 🌱</strong>
<p>
The beginning. The year everything started.
</p>
</div>

<div class="memory">
<strong>YEAR TWO 😂</strong>
<p>
The friendship chaos begins.
</p>
</div>

<div class="memory">
<strong>YEAR THREE 📸</strong>
<p>
More memories. More inside jokes.
</p>
</div>

<div class="memory">
<strong>YEAR FOUR 🫶</strong>
<p>
The years where you learn who really has your back.
</p>
</div>

<div class="memory">
<strong>YEAR FIVE ✨</strong>
<p>
Somehow there are even more stories.
</p>
</div>

<div class="memory">
<strong>YEAR SIX 💗</strong>
<p>
Six years later... still best friends.
</p>
</div>

</div>

<h2 style="margin-top:30px;">
＋ Add Your Own Memory
</h2>

<textarea
id="memoryInput"
placeholder="Write something you never want either of you to forget..."
maxlength="600">
</textarea>

<button class="action" id="addMemory">
Add Memory ♡
</button>

<button class="action secondary" id="clearMemories">
Clear Added Memories
</button>

<div id="customMemories" style="margin-top:15px;"></div>

</section>

</div>


<!-- ================= QUIZ ================= -->

<div id="quiz" class="page">

<section class="section">

<h2>🧠 How Well Do You Know Liliana?</h2>

<p class="subtitle">
Eight questions. One bestie. Let's see if you were paying attention.
</p>

<div id="quizBox">

<div id="questionNumber"></div>

<div class="quiz-question" id="question">
Loading...
</div>

<div class="quiz-options" id="quizOptions"></div>

<div class="quiz-result" id="quizResult"></div>

<button class="action hidden" id="nextQuestion">
Next Question →
</button>

</div>

</section>

</div>


<!-- ================= LETTER ================= -->

<div id="letter" class="page">

<section class="section">

<h2>💌 A Letter From Bree</h2>

<p class="subtitle">
The casino can be chaotic. This part isn't.
</p>

<div class="letter">

Six years.

Six whole years of friendship.

When you have known someone for that long, it stops being about counting the years and starts being about remembering all the little things that filled them.

The conversations.

The laughter.

The ridiculous moments.

The difficult moments.

The inside jokes that nobody else would understand.

The memories that somehow became part of who we are.

You are one of those people who has such a naturally caring heart. You are sweet, incredibly empathetic and somehow charismatic enough to make people feel comfortable around you.

And yes... you are also ridiculously flirtatious. 😂

But underneath all of that is someone who genuinely cares.

I hope you never forget how special that is.

Six years ago, neither of us could have known how many memories we'd eventually have together.

And now here we are.

Still besties.

Still making memories.

Still collecting stories.

And hopefully still annoying each other for many years to come.

So this little ridiculous casino is for you.

Because if friendship were a game, I'd still choose you as my bestie every single time.

<div class="signature">
Love always,<br>
Bree ♡
</div>

</div>

</section>

</div>


</div>
</div>


<script>

/* =========================================================
   FRIENDSHIP CASINO
========================================================= */

let tokens = 6000;

const tokenDisplay = document.getElementById("tokens");

function updateTokens() {
  tokenDisplay.textContent = tokens;
}

function addTokens(amount) {
  tokens += amount;
  updateTokens();
}

function removeTokens(amount) {
  if (tokens < amount) return false;

  tokens -= amount;
  updateTokens();

  return true;
}


/* =========================================================
   NAVIGATION
========================================================= */

const navButtons = document.querySelectorAll(".nav button");
const pages = document.querySelectorAll(".page");

navButtons.forEach(button => {

  button.addEventListener("click", () => {

    const target = button.dataset.page;

    navButtons.forEach(b => b.classList.remove("active"));
    button.classList.add("active");

    pages.forEach(page => {
      page.classList.remove("active");
    });

    document.getElementById(target).classList.add("active");

  });

});


/* =========================================================
   SLOT MACHINE
========================================================= */

const symbols = [
  "🌹",
  "🌻",
  "🐬",
  "🎀",
  "🍣",
  "♥️",
  "♠️",
  "3️⃣"
];

const reels = [
  document.getElementById("reel1"),
  document.getElementById("reel2"),
  document.getElementById("reel3")
];

const spinButton = document.getElementById("spinButton");
const slotResult = document.getElementById("slotResult");

spinButton.addEventListener("click", () => {

  if (tokens < 50) {

    slotResult.textContent =
      "You're out of friendship tokens! Play some games to earn more.";

    return;
  }

  removeTokens(50);

  spinButton.disabled = true;

  reels.forEach(reel => {
    reel.classList.add("spin");
  });

  setTimeout(() => {

    const result = [
      symbols[Math.floor(Math.random() * symbols.length)],
      symbols[Math.floor(Math.random() * symbols.length)],
      symbols[Math.floor(Math.random() * symbols.length)]
    ];

    reels.forEach((reel, i) => {

      reel.classList.remove("spin");
      reel.textContent = result[i];

    });

    let reward = 0;
    let message = "";

    if (
      result[0] === "3️⃣" &&
      result[1] === "3️⃣" &&
      result[2] === "3️⃣"
    ) {

      reward = 3000;

      message =
        "💗 TRIPLE THREE JACKPOT! 💗<br>" +
        "Of course Liliana's favourite number had to win.";

    } else if (
      result[0] === result[1] &&
      result[1] === result[2]
    ) {

      reward = 1500;

      message =
        "🎰 THREE OF A KIND!<br>" +
        "The friendship casino is feeling generous.";

    } else if (
      result[0] === result[1] ||
      result[1] === result[2] ||
      result[0] === result[2]
    ) {

      reward = 300;

      message =
        "✨ A PAIR!<br>" +
        "Liliana got lucky.";

    } else {

      reward = 75;

      message =
        "♡ Friendship consolation prize!<br>" +
        "You still won because you have six years of friendship.";

    }

    addTokens(reward);

    slotResult.innerHTML =
      message +
      "<br><br>+" + reward + " friendship tokens";

    spinButton.disabled = false;

  }, 1400);

});


/* =========================================================
   POKER
========================================================= */

const pokerDeck = [
  ["♥️","LOVE"],
  ["♦️","KINDNESS"],
  ["♣️","CHAOS"],
  ["♠️","TRUST"],
  ["♥️","MEMORIES"],
  ["♦️","LAUGHTER"],
  ["♣️","LOYALTY"],
  ["♠️","EMPATHY"],
  ["♥️","POETRY"],
  ["♦️","SUSHI"],
  ["♣️","DOLPHIN"],
  ["♠️","LUCK"]
];

let currentPokerHand = [];

const pokerCards = document.getElementById("pokerCards");
const pokerMessage = document.getElementById("pokerMessage");

function dealPoker() {

  currentPokerHand = [];

  const shuffled = [...pokerDeck]
    .sort(() => Math.random() - .5)
    .slice(0,5);

  pokerCards.innerHTML = "";

  shuffled.forEach((card, index) => {

    const div = document.createElement("div");

    div.className =
      "card " +
      (card[0] === "♥️" || card[0] === "♦️" ? "red" : "");

    div.innerHTML = `
      <span>${card[0]}</span>
      <span class="symbol">${card[0]}</span>
      <strong>${card[1]}</strong>
    `;

    div.addEventListener("click", () => {

      div.style.transform =
        div.style.transform === "translateY(-15px)"
          ? ""
          : "translateY(-15px)";

    });

    pokerCards.appendChild(div);

    currentPokerHand.push(card);

  });

  pokerMessage.textContent =
    "Your friendship hand has been dealt. Click your cards and see what kind of bestie you have.";

  addTokens(150);

}

document.getElementById("dealButton")
  .addEventListener("click", dealPoker);


/* =========================================================
   MYSTERY CARDS
========================================================= */

const cardMessages = [

  "🌹 You drew the Rose Card!<br><br>" +
  "Liliana's soft side has been unlocked. " +
  "She gets +500 friendship tokens.",

  "🐬 You drew the Dolphin Card!<br><br>" +
  "A playful friendship bonus! +750 tokens.",

  "3️⃣ THE LUCKY THREE!<br><br>" +
  "Her favourite number has chosen you.<br>" +
  "+1500 friendship tokens."

];

document.querySelectorAll(".mystery").forEach(card => {

  card.addEventListener("click", () => {

    const index = Number(card.dataset.card);

    document.getElementById("cardResult").innerHTML =
      cardMessages[index];

    if (index === 0) addTokens(500);
    if (index === 1) addTokens(750);
    if (index === 2) addTokens(1500);

    document.querySelectorAll(".mystery")
      .forEach(c => c.disabled = true);

  });

});


/* =========================================================
   PRIZES
========================================================= */

const prizeMessages = {

  compliment:
    "💗 Liliana, you are the kind of person who makes people feel cared for.",

  fact:
    "🌹 Liliana loves baby pink, sushi, dolphins, sunflowers, roses, poetry and sad songs.",

  memory:
    "🐬 Six years of friendship means there are enough memories to fill an entire museum.",

  photo:
    "📸 PHOTO SLOT UNLOCKED!<br><br>" +
    "You can replace this with one of your favourite friendship photos.",

  secret:
    "💌 SECRET MESSAGE:<br><br>" +
    "Some friendships are measured in years. " +
    "Ours is measured in memories.",

  finale:
    "👑 SIX-YEAR JACKPOT!<br><br>" +
    "Six years. Still best friends. " +
    "That's the real prize."
};

document.querySelectorAll(".prize button").forEach(button => {

  button.addEventListener("click", () => {

    const cost = Number(button.dataset.cost);
    const type = button.dataset.prize;

    if (!removeTokens(cost)) {

      document.getElementById("prizeResult").textContent =
        "You don't have enough friendship tokens yet. ♡";

      return;

    }

    button.disabled = true;
    button.textContent = "UNLOCKED ✓";

    document.getElementById("prizeResult").innerHTML =
      prizeMessages[type];

  });

});


/* =========================================================
   SIX YEAR MEMORIES
========================================================= */

let customMemories = [];

const memoryInput = document.getElementById("memoryInput");
const customMemoriesBox =
  document.getElementById("customMemories");

document.getElementById("addMemory")
  .addEventListener("click", () => {

    const text = memoryInput.value.trim();

    if (!text) return;

    customMemories.push(text);

    memoryInput.value = "";

    renderMemories();

    addTokens(100);

  });

function renderMemories() {

  customMemoriesBox.innerHTML = "";

  customMemories.forEach((memory, index) => {

    const div = document.createElement("div");

    div.className = "memory";

    div.innerHTML = `
      <strong>♡ MEMORY ${index + 1}</strong>
      <p>${escapeHTML(memory)}</p>
    `;

    customMemoriesBox.appendChild(div);

  });

}

document.getElementById("clearMemories")
  .addEventListener("click", () => {

    customMemories = [];

    renderMemories();

  });


function escapeHTML(text) {

  const div = document.createElement("div");

  div.textContent = text;

  return div.innerHTML;

}


/* =========================================================
   QUIZ
========================================================= */

const questions = [

  {
    q: "What is Liliana's favourite colour?",
    answers: ["Baby pink","Blue","Burgundy","Green"],
    correct: 0
  },

  {
    q: "What is Liliana's favourite number?",
    answers: ["6","7","3","22"],
    correct: 2
  },

  {
    q: "What food does Liliana love?",
    answers: ["Pizza","Sushi","Pasta","Burgers"],
    correct: 1
  },

  {
    q: "Which animal does she love?",
    answers: ["Dolphins","Otters","Cats","Rabbits"],
    correct: 0
  },

  {
    q: "When is Liliana's birthday?",
    answers: ["July 2","June 22","July 22","March 3"],
    correct: 2
  },

  {
    q: "What is her favourite movie?",
    answers: [
      "Titanic",
      "Me Before You",
      "The Notebook",
      "Frozen"
    ],
    correct: 1
  },

  {
    q: "What does Liliana love?",
    answers: [
      "Sad songs and poetry",
      "Only action movies",
      "Opera",
      "Nothing emotional"
    ],
    correct: 0
  },

  {
    q: "What does she hope to be one day?",
    answers: [
      "A pilot",
      "A chef",
      "A mum to a baby girl",
      "A singer"
    ],
    correct: 2
  }

];

let questionIndex = 0;
let quizScore = 0;
let quizAnswered = false;

const questionNumber =
  document.getElementById("questionNumber");

const question =
  document.getElementById("question");

const quizOptions =
  document.getElementById("quizOptions");

const quizResult =
  document.getElementById("quizResult");

const nextQuestion =
  document.getElementById("nextQuestion");


function loadQuestion() {

  quizAnswered = false;

  const current = questions[questionIndex];

  questionNumber.textContent =
    `Question ${questionIndex + 1} of ${questions.length}`;

  question.textContent = current.q;

  quizOptions.innerHTML = "";

  quizResult.textContent = "";

  nextQuestion.classList.add("hidden");

  current.answers.forEach((answer,index) => {

    const button = document.createElement("button");

    button.textContent = answer;

    button.addEventListener("click", () => {

      if (quizAnswered) return;

      quizAnswered = true;

      if (index === current.correct) {

        quizScore++;

        button.textContent = "✓ " + answer;

        quizResult.textContent =
          "Correct! 💗 +100 tokens";

        addTokens(100);

      } else {

        button.textContent = "✗ " + answer;

        quizOptions.children[current.correct]
          .textContent =
          "✓ " + current.answers[current.correct];

        quizResult.textContent =
          "Not quite! But Liliana would forgive you. 😂";

      }

      nextQuestion.classList.remove("hidden");

    });

    quizOptions.appendChild(button);

  });

}

nextQuestion.addEventListener("click", () => {

  questionIndex++;

  if (questionIndex >= questions.length) {

    question.textContent =
      "QUIZ COMPLETE!";

    questionNumber.textContent = "";

    quizOptions.innerHTML = "";

    nextQuestion.classList.add("hidden");

    quizResult.textContent =
      `You scored ${quizScore}/${questions.length}! 💗`;

    addTokens(500);

    return;

  }

  loadQuestion();

});


loadQuestion();


/* =========================================================
   SAVE STATE
========================================================= */

function saveGame() {

  const state = {

    tokens: tokens,

    memories: customMemories

  };

  localStorage.setItem(
    "lilianaFriendshipCasino",
    JSON.stringify(state)
  );

}

function loadGame() {

  const saved =
    localStorage.getItem(
      "lilianaFriendshipCasino"
    );

  if (!saved) return;

  try {

    const state = JSON.parse(saved);

    if (typeof state.tokens === "number") {

      tokens = state.tokens;

    }

    if (Array.isArray(state.memories)) {

      customMemories = state.memories;

    }

    updateTokens();
    renderMemories();

  } catch(error) {

    console.log("Saved data could not be loaded.");

  }

}


/* Automatically save */

setInterval(saveGame, 2000);

window.addEventListener("beforeunload", saveGame);

loadGame();


</script>

</body>
</html>
