<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Liliana's Friendship Casino 💗</title>

<style>
:root{
  --pink:#ff5fa2;
  --pink2:#ff8fc4;
  --deep:#351326;
  --purple:#6d3b68;
  --cream:#fff8fc;
  --card:#ffffff;
  --muted:#8b7180;
  --gold:#f5c451;
  --shadow:0 12px 35px rgba(88,30,67,.12);
  --radius:24px;
}

*{
  box-sizing:border-box;
}

html{
  scroll-behavior:smooth;
}

body{
  margin:0;
  font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
  background:
    radial-gradient(circle at top left,rgba(255,143,196,.22),transparent 30%),
    linear-gradient(180deg,#fff7fb 0%,#fff 45%,#fff5fa 100%);
  color:var(--deep);
  min-height:100vh;
}

button,
input{
  font:inherit;
}

button{
  cursor:pointer;
}

.hidden{
  display:none!important;
}

/* =========================
   HEADER
========================= */

.topbar{
  position:sticky;
  top:0;
  z-index:100;
  backdrop-filter:blur(18px);
  background:rgba(255,248,252,.92);
  border-bottom:1px solid rgba(255,95,162,.12);
}

.topbar-inner{
  max-width:1250px;
  margin:auto;
  padding:14px 20px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
}

.logo{
  display:flex;
  align-items:center;
  gap:10px;
  font-weight:900;
  font-size:20px;
}

.logo-heart{
  width:42px;
  height:42px;
  border-radius:14px;
  display:grid;
  place-items:center;
  background:linear-gradient(135deg,var(--pink),#ff9dcc);
  color:white;
  box-shadow:0 7px 20px rgba(255,95,162,.3);
}

.stats{
  display:flex;
  gap:8px;
  flex-wrap:wrap;
  justify-content:flex-end;
}

.stat{
  background:white;
  border:1px solid rgba(255,95,162,.12);
  border-radius:14px;
  padding:7px 11px;
  min-width:75px;
  text-align:center;
  box-shadow:0 4px 14px rgba(88,30,67,.06);
}

.stat small{
  display:block;
  color:var(--muted);
  font-size:10px;
  text-transform:uppercase;
  letter-spacing:.5px;
}

.stat strong{
  font-size:14px;
}

/* =========================
   NAVIGATION
========================= */

.nav{
  max-width:1250px;
  margin:auto;
  padding:10px 20px;
  display:flex;
  gap:8px;
  overflow-x:auto;
  scrollbar-width:none;
}

.nav::-webkit-scrollbar{
  display:none;
}

.nav button{
  border:0;
  background:white;
  color:var(--deep);
  border-radius:13px;
  padding:10px 15px;
  white-space:nowrap;
  font-weight:700;
  border:1px solid rgba(255,95,162,.1);
}

.nav button.active{
  background:var(--pink);
  color:white;
  box-shadow:0 6px 16px rgba(255,95,162,.25);
}

/* =========================
   MAIN
========================= */

main{
  max-width:1250px;
  margin:auto;
  padding:28px 20px 100px;
}

.page{
  display:none;
}

.page.active{
  display:block;
}

.hero{
  background:
    radial-gradient(circle at 85% 20%,rgba(255,255,255,.3),transparent 25%),
    linear-gradient(135deg,#ff5fa2,#b85a9d);
  color:white;
  border-radius:32px;
  padding:34px;
  box-shadow:var(--shadow);
  position:relative;
  overflow:hidden;
  margin-bottom:25px;
}

.hero:after{
  content:"💗";
  position:absolute;
  font-size:180px;
  right:15px;
  bottom:-60px;
  opacity:.09;
}

.hero h1{
  margin:0 0 8px;
  font-size:clamp(30px,5vw,52px);
}

.hero p{
  margin:0;
  max-width:650px;
  line-height:1.6;
  opacity:.94;
}

.hero-actions{
  display:flex;
  flex-wrap:wrap;
  gap:10px;
  margin-top:22px;
}

/* =========================
   BUTTONS
========================= */

.btn{
  border:0;
  border-radius:14px;
  padding:12px 17px;
  font-weight:800;
  transition:.18s ease;
}

.btn:hover{
  transform:translateY(-2px);
}

.btn-primary{
  background:var(--pink);
  color:white;
  box-shadow:0 7px 18px rgba(255,95,162,.25);
}

.btn-white{
  background:white;
  color:var(--deep);
}

.btn-gold{
  background:var(--gold);
  color:#4a3510;
}

.btn-soft{
  background:#fff0f7;
  color:#a9346d;
}

/* =========================
   SECTION HEADERS
========================= */

.section-head{
  display:flex;
  align-items:end;
  justify-content:space-between;
  gap:15px;
  margin:28px 0 15px;
}

.section-head h2{
  margin:0;
  font-size:25px;
}

.section-head p{
  margin:4px 0 0;
  color:var(--muted);
  font-size:14px;
}

/* =========================
   CARDS
========================= */

.grid{
  display:grid;
  grid-template-columns:repeat(4,minmax(0,1fr));
  gap:16px;
}

.game-card{
  background:var(--card);
  border:1px solid rgba(255,95,162,.1);
  border-radius:22px;
  padding:18px;
  box-shadow:var(--shadow);
  display:flex;
  flex-direction:column;
  min-height:210px;
  transition:.2s ease;
}

.game-card:hover{
  transform:translateY(-4px);
  box-shadow:0 18px 40px rgba(88,30,67,.14);
}

.game-icon{
  width:54px;
  height:54px;
  border-radius:17px;
  display:grid;
  place-items:center;
  font-size:28px;
  background:#fff0f7;
  margin-bottom:13px;
}

.game-card h3{
  margin:0 0 5px;
  font-size:18px;
}

.game-card p{
  margin:0;
  color:var(--muted);
  font-size:13px;
  line-height:1.45;
  flex:1;
}

.game-card .play{
  margin-top:15px;
}

/* =========================
   FEATURED
========================= */

.featured{
  display:grid;
  grid-template-columns:1.5fr 1fr 1fr;
  gap:16px;
}

.feature-card{
  border-radius:25px;
  min-height:220px;
  padding:25px;
  color:white;
  position:relative;
  overflow:hidden;
  display:flex;
  flex-direction:column;
  justify-content:flex-end;
}

.feature-card h3{
  margin:0 0 5px;
  font-size:24px;
}

.feature-card p{
  margin:0 0 15px;
  opacity:.9;
}

.mega{
  background:linear-gradient(135deg,#49304e,#b94386);
}

.wheel{
  background:linear-gradient(135deg,#7e4777,#e45a9a);
}

.catch{
  background:linear-gradient(135deg,#278b9b,#6b5fc7);
}

/* =========================
   CATEGORY HERO
========================= */

.category-banner{
  background:white;
  border:1px solid rgba(255,95,162,.1);
  border-radius:25px;
  padding:25px;
  margin-bottom:22px;
  box-shadow:var(--shadow);
}

.category-banner h1{
  margin:0 0 7px;
}

.category-banner p{
  color:var(--muted);
  margin:0;
}

/* =========================
   SEARCH
========================= */

.search{
  width:100%;
  border:1px solid rgba(255,95,162,.16);
  background:white;
  border-radius:15px;
  padding:13px 15px;
  outline:none;
  margin-top:16px;
}

.search:focus{
  border-color:var(--pink);
}

/* =========================
   MODAL
========================= */

.modal{
  position:fixed;
  inset:0;
  background:rgba(36,15,29,.58);
  z-index:300;
  display:none;
  align-items:center;
  justify-content:center;
  padding:18px;
  backdrop-filter:blur(8px);
}

.modal.open{
  display:flex;
}

.modal-box{
  width:min(680px,100%);
  max-height:90vh;
  overflow:auto;
  background:white;
  border-radius:28px;
  padding:25px;
  box-shadow:0 25px 80px rgba(0,0,0,.25);
  position:relative;
}

.close{
  position:absolute;
  top:15px;
  right:15px;
  width:38px;
  height:38px;
  border:0;
  border-radius:12px;
  background:#fff0f7;
  color:#a9346d;
  font-size:20px;
}

/* =========================
   GAME AREA
========================= */

.game-title{
  text-align:center;
  padding-right:35px;
}

.game-title h2{
  margin:0 0 5px;
}

.game-title p{
  margin:0;
  color:var(--muted);
}

.machine{
  background:linear-gradient(145deg,#39182c,#6c284e);
  border-radius:25px;
  padding:22px;
  color:white;
  margin:22px 0;
  text-align:center;
}

.reels{
  display:flex;
  justify-content:center;
  gap:10px;
  margin:20px 0;
}

.reel{
  width:90px;
  height:90px;
  border-radius:17px;
  background:white;
  color:#321526;
  display:grid;
  place-items:center;
  font-size:45px;
  box-shadow:inset 0 0 0 5px #f4d5e5;
}

.result{
  min-height:28px;
  font-weight:800;
  margin:12px 0;
}

.game-controls{
  display:flex;
  gap:10px;
  flex-wrap:wrap;
  justify-content:center;
}

/* =========================
   WHEEL
========================= */

.wheel-wrap{
  display:flex;
  justify-content:center;
  align-items:center;
  flex-direction:column;
  margin:20px 0;
}

.pointer{
  font-size:35px;
  margin-bottom:-8px;
  position:relative;
  z-index:2;
}

.wheel-circle{
  width:280px;
  height:280px;
  border-radius:50%;
  border:10px solid white;
  box-shadow:0 10px 35px rgba(0,0,0,.18);
  background:
    conic-gradient(
      #ff6ba8 0deg 45deg,
      #f5c451 45deg 90deg,
      #b66ae2 90deg 135deg,
      #62c6ca 135deg 180deg,
      #ff6ba8 180deg 225deg,
      #f5c451 225deg 270deg,
      #b66ae2 270deg 315deg,
      #62c6ca 315deg 360deg
    );
  display:grid;
  place-items:center;
  transition:transform 4s cubic-bezier(.17,.67,.12,.99);
}

.wheel-centre{
  width:75px;
  height:75px;
  background:white;
  border-radius:50%;
  display:grid;
  place-items:center;
  color:#a9346d;
  font-size:28px;
  font-weight:900;
}

/* =========================
   TABLES / CARDS
========================= */

.playing-card{
  width:70px;
  height:100px;
  border-radius:10px;
  background:white;
  border:1px solid #ddd;
  display:grid;
  place-items:center;
  font-size:22px;
  font-weight:800;
  box-shadow:0 5px 12px rgba(0,0,0,.08);
}

.hand{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  justify-content:center;
  margin:15px 0;
}

/* =========================
   CATCH
========================= */

.collection{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
  margin-top:20px;
}

.creature{
  background:#fff6fb;
  border-radius:17px;
  padding:12px;
  text-align:center;
  border:1px solid rgba(255,95,162,.12);
}

.creature .emoji{
  font-size:38px;
}

.creature small{
  display:block;
  color:var(--muted);
}

/* =========================
   QUIZ
========================= */

.quiz-question{
  background:#fff7fb;
  border-radius:18px;
  padding:18px;
  margin:12px 0;
}

.quiz-question h3{
  margin:0 0 12px;
  font-size:16px;
}

.answers{
  display:grid;
  gap:8px;
}

.answer{
  text-align:left;
  border:1px solid #f1d7e5;
  background:white;
  padding:11px;
  border-radius:12px;
}

.answer.selected{
  background:#ffd7e9;
  border-color:var(--pink);
}

/* =========================
   VAULT
========================= */

.vault{
  background:linear-gradient(135deg,#3c1931,#6f345e);
  color:white;
  border-radius:28px;
  padding:30px;
  text-align:center;
  max-width:650px;
  margin:auto;
}

.vault-input{
  width:100%;
  max-width:250px;
  padding:15px;
  border:0;
  border-radius:14px;
  text-align:center;
  font-size:22px;
  letter-spacing:7px;
  margin:15px auto;
  display:block;
}

/* =========================
   ACHIEVEMENTS
========================= */

.achievement{
  background:white;
  border:1px solid rgba(255,95,162,.1);
  border-radius:18px;
  padding:16px;
  display:flex;
  align-items:center;
  gap:13px;
}

.achievement.locked{
  opacity:.45;
}

.achievement-icon{
  font-size:28px;
}

/* =========================
   BOTTOM NAV MOBILE
========================= */

.mobile-nav{
  display:none;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width:1000px){
  .grid{
    grid-template-columns:repeat(3,1fr);
  }

  .featured{
    grid-template-columns:1fr 1fr;
  }

  .feature-card:first-child{
    grid-column:1/-1;
  }
}

@media(max-width:700px){
  .topbar-inner{
    align-items:flex-start;
    flex-direction:column;
  }

  .stats{
    width:100%;
    justify-content:flex-start;
    overflow-x:auto;
    flex-wrap:nowrap;
  }

  .stat{
    flex:0 0 auto;
  }

  .nav{
    display:none;
  }

  main{
    padding:18px 14px 90px;
  }

  .hero{
    padding:25px;
    border-radius:25px;
  }

  .hero h1{
    font-size:31px;
  }

  .grid{
    grid-template-columns:repeat(2,1fr);
    gap:11px;
  }

  .game-card{
    min-height:190px;
    padding:14px;
    border-radius:18px;
  }

  .game-icon{
    width:46px;
    height:46px;
    font-size:24px;
  }

  .featured{
    grid-template-columns:1fr;
  }

  .feature-card:first-child{
    grid-column:auto;
  }

  .collection{
    grid-template-columns:repeat(3,1fr);
  }

  .reel{
    width:75px;
    height:75px;
    font-size:37px;
  }

  .wheel-circle{
    width:245px;
    height:245px;
  }

  .mobile-nav{
    position:fixed;
    bottom:0;
    left:0;
    right:0;
    z-index:200;
    display:flex;
    background:rgba(255,255,255,.96);
    backdrop-filter:blur(15px);
    border-top:1px solid rgba(255,95,162,.13);
    padding:7px 5px;
    justify-content:space-around;
  }

  .mobile-nav button{
    border:0;
    background:none;
    color:#8b7180;
    font-size:10px;
    font-weight:800;
    display:flex;
    flex-direction:column;
    align-items:center;
    gap:2px;
    padding:5px;
  }

  .mobile-nav button span{
    font-size:20px;
  }

  .mobile-nav button.active{
    color:var(--pink);
  }
}

@media(max-width:430px){
  .grid{
    grid-template-columns:1fr 1fr;
  }

  .game-card p{
    font-size:12px;
  }

  .game-card h3{
    font-size:16px;
  }

  .reel{
    width:68px;
    height:68px;
  }
}
</style>
</head>

<body>

<header class="topbar">
  <div class="topbar-inner">

    <div class="logo">
      <div class="logo-heart">💗</div>
      <div>
        Liliana's Casino
        <small style="display:block;color:#9b7789;font-size:11px">
          Six years of friendship
        </small>
      </div>
    </div>

    <div class="stats">
      <div class="stat">
        <small>Tokens</small>
        <strong id="tokens">1,000</strong>
      </div>

      <div class="stat">
        <small>Level</small>
        <strong id="level">1</strong>
      </div>

      <div class="stat">
        <small>XP</small>
        <strong id="xp">0</strong>
      </div>

      <div class="stat">
        <small>Wins</small>
        <strong id="wins">0</strong>
      </div>

      <div class="stat">
        <small>Streak</small>
        <strong id="streak">0 🔥</strong>
      </div>
    </div>

  </div>
</header>

<nav class="nav">
  <button class="active" data-page="home">🏠 Home</button>
  <button data-page="slots">🎰 Slots</button>
  <button data-page="cards">🃏 Cards</button>
  <button data-page="casino">🎲 Casino</button>
  <button data-page="races">🏇 Races</button>
  <button data-page="mini">🎯 Mini Games</button>
  <button data-page="catch">🐾 Catch</button>
  <button data-page="liliana">💗 Liliana</button>
  <button data-page="special">✨ Special</button>
</nav>

<main>

<!-- =========================
     HOME
========================= -->

<section id="home" class="page active">

  <div class="hero">
    <h1>Welcome to Liliana's Friendship Casino 💗</h1>

    <p>
      Six years of friendship turned into one ridiculously pink casino.
      Play games, collect Friendship Tokens, unlock achievements and see
      how well you really know Liliana.
    </p>

    <div class="hero-actions">
      <button class="btn btn-white" onclick="showPage('slots')">
        🎰 Start Playing
      </button>

      <button class="btn btn-gold" onclick="showPage('special')">
        💎 Special Games
      </button>
    </div>
  </div>

  <div class="section-head">
    <div>
      <h2>⭐ Featured</h2>
      <p>The big attractions</p>
    </div>
  </div>

  <div class="featured">

    <div class="feature-card mega">
      <div>
        <h3>💎 Mega Jackpot</h3>
        <p>Win the ultimate 1,000,000 Friendship Token jackpot.</p>
        <button class="btn btn-gold" onclick="openGame('mega')">
          Play Mega Jackpot
        </button>
      </div>
    </div>

    <div class="feature-card wheel">
      <div>
        <h3>🎡 Lucky Wheel</h3>
        <p>Spin for a random prize.</p>
        <button class="btn btn-white" onclick="openGame('wheel')">
          Spin Wheel
        </button>
      </div>
    </div>

    <div class="feature-card catch">
      <div>
        <h3>🐾 Friendship Catch</h3>
        <p>Collect all the friendship creatures.</p>
        <button class="btn btn-white" onclick="showPage('catch')">
          Collect
        </button>
      </div>
    </div>

  </div>

  <div class="section-head">
    <div>
      <h2>🎮 Quick Play</h2>
      <p>Jump straight into a game</p>
    </div>
  </div>

  <div class="grid">

    <div class="game-card">
      <div class="game-icon">🦬</div>
      <h3>Buffalo Stampede</h3>
      <p>A classic three-reel Buffalo-style slot.</p>
      <button class="btn btn-primary play" onclick="openGame('buffalo')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">♠️</div>
      <h3>Poker</h3>
      <p>Challenge the computer.</p>
      <button class="btn btn-primary play" onclick="openGame('poker')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">♣️</div>
      <h3>Blackjack</h3>
      <p>Hit, stand or double down.</p>
      <button class="btn btn-primary play" onclick="openGame('blackjack')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎁</div>
      <h3>Mystery Box</h3>
      <p>Pick a box and reveal your prize.</p>
      <button class="btn btn-primary play" onclick="openGame('mystery')">Play</button>
    </div>

  </div>

</section>

<!-- =========================
     SLOTS
========================= -->

<section id="slots" class="page">

  <div class="category-banner">
    <h1>🎰 Slot Machines</h1>
    <p>Pick a machine and spin for Friendship Tokens.</p>

    <input
      class="search"
      placeholder="Search slot machines..."
      oninput="filterGames(this,'slotsGrid')"
    >
  </div>

  <div class="grid" id="slotsGrid">

    <div class="game-card" data-name="buffalo stampede buffalo">
      <div class="game-icon">🦬</div>
      <h3>Buffalo Stampede</h3>
      <p>Classic Buffalo-style reels with casino sounds.</p>
      <button class="btn btn-primary play" onclick="openGame('buffalo')">Spin</button>
    </div>

    <div class="game-card" data-name="pink palace pink slot">
      <div class="game-icon">💗</div>
      <h3>Pink Palace</h3>
      <p>A sweet pink-themed slot machine.</p>
      <button class="btn btn-primary play" onclick="openGame('pink')">Spin</button>
    </div>

    <div class="game-card" data-name="dolphin riches dolphin ocean">
      <div class="game-icon">🐬</div>
      <h3>Dolphin Riches</h3>
      <p>Ocean-themed reels.</p>
      <button class="btn btn-primary play" onclick="openGame('dolphin')">Spin</button>
    </div>

    <div class="game-card" data-name="fancy 7s seven">
      <div class="game-icon">7️⃣</div>
      <h3>Fancy 7s</h3>
      <p>Classic lucky seven action.</p>
      <button class="btn btn-primary play" onclick="openGame('sevens')">Spin</button>
    </div>

    <div class="game-card" data-name="mega jackpot million">
      <div class="game-icon">💎</div>
      <h3>Mega Jackpot</h3>
      <p>Chase the 1,000,000-token jackpot.</p>
      <button class="btn btn-gold play" onclick="openGame('mega')">PLAY BIG</button>
    </div>

  </div>

</section>

<!-- =========================
     CARDS
========================= -->

<section id="cards" class="page">

  <div class="category-banner">
    <h1>🃏 Card Room</h1>
    <p>Six different card games in one place.</p>

    <input
      class="search"
      placeholder="Search card games..."
      oninput="filterGames(this,'cardsGrid')"
    >
  </div>

  <div class="grid" id="cardsGrid">

    <div class="game-card">
      <div class="game-icon">♠️</div>
      <h3>Poker</h3>
      <p>Play poker against the computer.</p>
      <button class="btn btn-primary play" onclick="openGame('poker')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">♣️</div>
      <h3>Blackjack</h3>
      <p>Hit, stand or double down.</p>
      <button class="btn btn-primary play" onclick="openGame('blackjack')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">♦️</div>
      <h3>Baccarat</h3>
      <p>Choose your side and reveal the cards.</p>
      <button class="btn btn-primary play" onclick="openGame('baccarat')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🃏</div>
      <h3>War</h3>
      <p>Higher card wins.</p>
      <button class="btn btn-primary play" onclick="openGame('war')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🃏</div>
      <h3>Gin Rummy</h3>
      <p>Build your hand and chase melds.</p>
      <button class="btn btn-primary play" onclick="openGame('gin')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🃏</div>
      <h3>Texas Hold'em</h3>
      <p>Your cards versus the computer.</p>
      <button class="btn btn-primary play" onclick="openGame('holdem')">Play</button>
    </div>

  </div>

</section>

<!-- =========================
     CASINO
========================= -->

<section id="casino" class="page">

  <div class="category-banner">
    <h1>🎲 Casino Floor</h1>
    <p>Quick casino-style games using fictional Friendship Tokens.</p>
  </div>

  <div class="grid">

    <div class="game-card">
      <div class="game-icon">🔴</div>
      <h3>Friendship Roulette</h3>
      <p>Pick red, black or green.</p>
      <button class="btn btn-primary play" onclick="openGame('roulette')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎲</div>
      <h3>Craps</h3>
      <p>Roll the dice and test your luck.</p>
      <button class="btn btn-primary play" onclick="openGame('craps')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">📈</div>
      <h3>Hi-Lo</h3>
      <p>Guess whether the next card is higher or lower.</p>
      <button class="btn btn-primary play" onclick="openGame('hilo')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🪙</div>
      <h3>Coin Flip</h3>
      <p>Heads or tails.</p>
      <button class="btn btn-primary play" onclick="openGame('coin')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🟣</div>
      <h3>Plinko</h3>
      <p>Drop the ball and see where it lands.</p>
      <button class="btn btn-primary play" onclick="openGame('plinko')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🪙</div>
      <h3>Three Cups</h3>
      <p>Find the winning cup.</p>
      <button class="btn btn-primary play" onclick="openGame('cups')">Play</button>
    </div>

  </div>

</section>

<!-- =========================
     RACES
========================= -->

<section id="races" class="page">

  <div class="category-banner">
    <h1>🏇 Friendship Races</h1>
    <p>Pick a racer and watch the result.</p>
  </div>

  <div class="grid">

    <div class="game-card">
      <div class="game-icon">🐎</div>
      <h3>Horse Derby</h3>
      <p>Choose a horse and race.</p>
      <button class="btn btn-primary play" onclick="openGame('horse')">Race</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🐬</div>
      <h3>Dolphin Derby</h3>
      <p>Choose your dolphin.</p>
      <button class="btn btn-primary play" onclick="openGame('dolphinrace')">Race</button>
    </div>

  </div>

</section>

<!-- =========================
     MINI GAMES
========================= -->

<section id="mini" class="page">

  <div class="category-banner">
    <h1>🎯 Mini Games</h1>
    <p>Fast little games for quick Friendship Token wins.</p>

    <input
      class="search"
      placeholder="Search mini games..."
      oninput="filterGames(this,'miniGrid')"
    >
  </div>

  <div class="grid" id="miniGrid">

    <div class="game-card">
      <div class="game-icon">🎁</div>
      <h3>Mystery Boxes</h3>
      <p>Choose a mystery box.</p>
      <button class="btn btn-primary play" onclick="openGame('mystery')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">💗</div>
      <h3>Heart Scratch</h3>
      <p>Reveal your hidden prize.</p>
      <button class="btn btn-primary play" onclick="openGame('scratch')">Scratch</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎯</div>
      <h3>Lucky Darts</h3>
      <p>Hit the lucky target.</p>
      <button class="btn btn-primary play" onclick="openGame('darts')">Throw</button>
    </div>

    <div class="game-card">
      <div class="game-icon">💎</div>
      <h3>Gem Heist</h3>
      <p>Take a chance on the vault.</p>
      <button class="btn btn-primary play" onclick="openGame('gem')">Heist</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎁</div>
      <h3>Lucky Envelopes</h3>
      <p>Pick your envelope.</p>
      <button class="btn btn-primary play" onclick="openGame('envelopes')">Pick</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🔢</div>
      <h3>Lucky Number</h3>
      <p>Pick a number and test your luck.</p>
      <button class="btn btn-primary play" onclick="openGame('number')">Pick</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🐠</div>
      <h3>Ocean Treasure</h3>
      <p>Search the ocean for treasure.</p>
      <button class="btn btn-primary play" onclick="openGame('ocean')">Dive</button>
    </div>

  </div>

</section>

<!-- =========================
     CATCH
========================= -->

<section id="catch" class="page">

  <div class="category-banner">
    <h1>🐾 Friendship Catch</h1>
    <p>
      Catch original friendship creatures and complete your collection.
    </p>
  </div>

  <div class="hero" style="margin-bottom:20px">
    <h1 style="font-size:32px">✨ Go Catch Something!</h1>
    <p>
      Different creatures have different rarities. Keep playing until
      you collect them all.
    </p>

    <div class="hero-actions">
      <button class="btn btn-white" onclick="catchCreature()">
        🐾 Search for Creature
      </button>
    </div>

    <div id="catchResult" style="margin-top:18px;font-size:18px;font-weight:800"></div>
  </div>

  <div class="section-head">
    <div>
      <h2>📖 Your Collection</h2>
      <p id="collectionCount">0 creatures caught</p>
    </div>
  </div>

  <div class="collection" id="collection"></div>

</section>

<!-- =========================
     LILIANA
========================= -->

<section id="liliana" class="page">

  <div class="category-banner">
    <h1>💗 All About Liliana</h1>
    <p>How well do you really know your bestie?</p>
  </div>

  <div class="grid">

    <div class="game-card">
      <div class="game-icon">💗</div>
      <h3>Liliana Quiz</h3>
      <p>20 questions. No answers are displayed.</p>
      <button class="btn btn-primary play" onclick="openQuiz()">Take Quiz</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🧠</div>
      <h3>Personality Test</h3>
      <p>Discover which Liliana personality appears.</p>
      <button class="btn btn-primary play" onclick="personality()">Take Test</button>
    </div>

  </div>

  <div id="personalityResult" style="margin-top:20px"></div>

</section>

<!-- =========================
     SPECIAL
========================= -->

<section id="special" class="page">

  <div class="category-banner">
    <h1>✨ Special Features</h1>
    <p>The secret and high-value parts of the casino.</p>
  </div>

  <div class="grid">

    <div class="game-card">
      <div class="game-icon">💎</div>
      <h3>Mega Jackpot</h3>
      <p>One million Friendship Tokens.</p>
      <button class="btn btn-gold play" onclick="openGame('mega')">Play</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎡</div>
      <h3>Lucky Wheel</h3>
      <p>Spin for one of eight prizes.</p>
      <button class="btn btn-primary play" onclick="openGame('wheel')">Spin</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🔐</div>
      <h3>Six-Year Vault</h3>
      <p>Enter the secret six-digit code.</p>
      <button class="btn btn-primary play" onclick="openGame('vault')">Open Vault</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🏆</div>
      <h3>Achievements</h3>
      <p>See everything you've unlocked.</p>
      <button class="btn btn-primary play" onclick="openGame('achievements')">View</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🎁</div>
      <h3>Daily Bonus</h3>
      <p>Claim your daily Friendship Tokens.</p>
      <button class="btn btn-primary play" onclick="dailyBonus()">Claim</button>
    </div>

    <div class="game-card">
      <div class="game-icon">🔊</div>
      <h3>Casino Sound</h3>
      <p>Turn the casino sounds on or off.</p>
      <button class="btn btn-soft play" onclick="toggleSound()" id="soundButton">
        Sound ON
      </button>
    </div>

  </div>

</section>

</main>

<!-- MOBILE NAV -->

<nav class="mobile-nav">
  <button class="active" data-page="home">
    <span>🏠</span>Home
  </button>

  <button data-page="slots">
    <span>🎰</span>Slots
  </button>

  <button data-page="cards">
    <span>🃏</span>Cards
  </button>

  <button data-page="casino">
    <span>🎲</span>Casino
  </button>

  <button data-page="special">
    <span>✨</span>More
  </button>
</nav>

<!-- GAME MODAL -->

<div class="modal" id="gameModal">
  <div class="modal-box">
    <button class="close" onclick="closeModal()">×</button>
    <div id="gameContent"></div>
  </div>
</div>

<script>

/* =========================================================
   STATE
========================================================= */

const SAVE_KEY = "lilianaCasino";

let S = JSON.parse(localStorage.getItem(SAVE_KEY)) || {
  tokens:1000,
  xp:0,
  streak:0,
  wins:0,
  played:0,
  biggest:0,
  ach:[],
  caught:[],
  sound:true,
  lastDaily:"",
  vaultOpened:false
};

function save(){
  localStorage.setItem(SAVE_KEY,JSON.stringify(S));
}

function level(){
  return Math.max(1,Math.floor(S.xp/100)+1);
}

function add(amount,win=false){

  S.tokens += amount;

  if(S.tokens < 0){
    S.tokens = 0;
  }

  S.played++;

  if(win){
    S.wins++;
  }

  S.xp += Math.max(5,Math.floor(Math.abs(amount)/20));

  if(amount > S.biggest){
    S.biggest = amount;
  }

  save();
  render();
}

function render(){

  document.getElementById("tokens").textContent =
    S.tokens.toLocaleString();

  document.getElementById("xp").textContent =
    S.xp.toLocaleString();

  document.getElementById("level").textContent =
    level();

  document.getElementById("wins").textContent =
    S.wins;

  document.getElementById("streak").textContent =
    S.streak + " 🔥";

  document.getElementById("soundButton").textContent =
    S.sound ? "Sound ON" : "Sound OFF";

  renderCollection();
}

render();

/* =========================================================
   NAVIGATION
========================================================= */

function showPage(id){

  document.querySelectorAll(".page").forEach(p=>{
    p.classList.remove("active");
  });

  const page=document.getElementById(id);

  if(page){
    page.classList.add("active");
  }

  document.querySelectorAll("[data-page]").forEach(btn=>{
    btn.classList.toggle("active",btn.dataset.page===id);
  });

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });
}

document.querySelectorAll("[data-page]").forEach(btn=>{
  btn.addEventListener("click",()=>{
    showPage(btn.dataset.page);
  });
});

/* =========================================================
   SEARCH
========================================================= */

function filterGames(input,gridId){

  const value=input.value.toLowerCase();

  document.querySelectorAll(`#${gridId} .game-card`).forEach(card=>{
    const name=(card.dataset.name || card.innerText).toLowerCase();

    card.style.display =
      name.includes(value) ? "" : "none";
  });
}

/* =========================================================
   SOUND
========================================================= */

function tone(freq=440,duration=.12,type="sine"){

  if(!S.sound)return;

  try{

    const ctx =
      new (window.AudioContext || window.webkitAudioContext)();

    const osc=ctx.createOscillator();
    const gain=ctx.createGain();

    osc.type=type;
    osc.frequency.value=freq;

    gain.gain.setValueAtTime(.08,ctx.currentTime);
    gain.gain.exponentialRampToValueAtTime(
      .001,
      ctx.currentTime+duration
    );

    osc.connect(gain);
    gain.connect(ctx.destination);

    osc.start();
    osc.stop(ctx.currentTime+duration);

  }catch(e){}
}

function casinoSound(){

  tone(440,.08);
  setTimeout(()=>tone(660,.08),90);
  setTimeout(()=>tone(880,.13),180);
}

function winSound(){

  tone(523,.1);
  setTimeout(()=>tone(659,.1),100);
  setTimeout(()=>tone(784,.18),200);
}

function loseSound(){
  tone(180,.25,"sawtooth");
}

function toggleSound(){

  S.sound=!S.sound;

  save();
  render();

  if(S.sound){
    casinoSound();
  }
}

/* =========================================================
   MODAL
========================================================= */

function openModal(html){

  document.getElementById("gameContent").innerHTML=html;

  document.getElementById("gameModal")
    .classList.add("open");
}

function closeModal(){

  document.getElementById("gameModal")
    .classList.remove("open");
}

function openGame(game){

  const games={

    buffalo:slotHTML(
      "🦬 Buffalo Stampede",
      "buffalo"
    ),

    pink:slotHTML(
      "💗 Pink Palace",
      "pink"
    ),

    dolphin:slotHTML(
      "🐬 Dolphin Riches",
      "dolphin"
    ),

    sevens:slotHTML(
      "7️⃣ Fancy 7s",
      "sevens"
    ),

    mega:megaHTML(),

    wheel:wheelHTML(),

    poker:pokerHTML(),

    blackjack:blackjackHTML(),

    baccarat:baccaratHTML(),

    war:warHTML(),

    gin:ginHTML(),

    holdem:holdemHTML(),

    roulette:rouletteHTML(),

    craps:crapsHTML(),

    hilo:hiloHTML(),

    coin:coinHTML(),

    plinko:plinkoHTML(),

    mystery:mysteryHTML(),

    cups:cupsHTML(),

    scratch:scratchHTML(),

    darts:dartsHTML(),

    gem:gemHTML(),

    envelopes:envelopesHTML(),

    number:numberHTML(),

    ocean:oceanHTML(),

    horse:horseHTML(),

    dolphinrace:dolphinRaceHTML(),

    vault:vaultHTML(),

    achievements:achievementHTML()

  };

  openModal(
    games[game] ||
    `<div class="game-title"><h2>Game unavailable</h2></div>`
  );
}

/* =========================================================
   SLOTS
========================================================= */

const symbols=[
  "🍒",
  "🍋",
  "💗",
  "💎",
  "🐬",
  "7️⃣"
];

function slotHTML(title,type){

  return `
    <div class="game-title">
      <h2>${title}</h2>
      <p>Spin for Friendship Tokens.</p>
    </div>

    <div class="machine">

      <div class="reels">
        <div class="reel" id="r1">❔</div>
        <div class="reel" id="r2">❔</div>
        <div class="reel" id="r3">❔</div>
      </div>

      <div class="result" id="slotResult">
        Good luck 💗
      </div>

      <div class="game-controls">
        <button class="btn btn-gold"
          onclick="spinSlot('${type}')">
          🎰 SPIN — 20
        </button>
      </div>

    </div>
  `;
}

function spinSlot(type){

  if(S.tokens<20){

    document.getElementById("slotResult").textContent =
      "You need 20 tokens to spin.";

    return;
  }

  add(-20);

  casinoSound();

  const a=symbols[Math.floor(Math.random()*symbols.length)];
  const b=symbols[Math.floor(Math.random()*symbols.length)];
  const c=symbols[Math.floor(Math.random()*symbols.length)];

  document.getElementById("r1").textContent=a;
  document.getElementById("r2").textContent=b;
  document.getElementById("r3").textContent=c;

  let reward=0;

  if(a===b && b===c){
    reward=1500;
  }else if(a===b || b===c || a===c){
    reward=100;
  }

  const result=document.getElementById("slotResult");

  if(reward){

    add(reward,true);

    result.textContent=
      `🎉 WIN! +${reward.toLocaleString()} tokens!`;

    winSound();

  }else{

    result.textContent=
      "No match this time 💗";

    loseSound();
  }
}

/* =========================================================
   MEGA JACKPOT
========================================================= */

function megaHTML(){

  return `
    <div class="game-title">
      <h2>💎 Mega Jackpot</h2>
      <p>The ultimate Friendship Token machine.</p>
    </div>

    <div class="machine">

      <div style="font-size:16px;opacity:.8">
        JACKPOT
      </div>

      <div style="font-size:42px;font-weight:900;margin:10px">
        1,000,000 💰
      </div>

      <div class="reels">
        <div class="reel" id="mega1">💎</div>
        <div class="reel" id="mega2">⭐</div>
        <div class="reel" id="mega3">💎</div>
      </div>

      <div class="result" id="megaResult">
        Can you hit all three diamonds?
      </div>

      <button class="btn btn-gold"
        onclick="spinMega()">
        💎 SPIN — 20
      </button>

    </div>
  `;
}

function spinMega(){

  if(S.tokens<20){

    document.getElementById("megaResult").textContent =
      "You need 20 tokens.";

    return;
  }

  add(-20);
  casinoSound();

  const a=Math.random()<.04 ? "💎" : symbols[Math.floor(Math.random()*symbols.length)];
  const b=Math.random()<.04 ? "💎" : symbols[Math.floor(Math.random()*symbols.length)];
  const c=Math.random()<.04 ? "💎" : symbols[Math.floor(Math.random()*symbols.length)];

  document.getElementById("mega1").textContent=a;
  document.getElementById("mega2").textContent=b;
  document.getElementById("mega3").textContent=c;

  if(a==="💎" && b==="💎" && c==="💎"){

    add(1000000,true);

    S.ach.push("Million Token Club");
    save();

    document.getElementById("megaResult").textContent =
      "💎💎💎 MEGA JACKPOT! +1,000,000 TOKENS! 💎💎💎";

    winSound();

  }else{

    document.getElementById("megaResult").textContent =
      "Not this time... the jackpot is still waiting.";

  }
}

/* =========================================================
   LUCKY WHEEL
========================================================= */

function wheelHTML(){

  return `
    <div class="game-title">
      <h2>🎡 Lucky Wheel</h2>
      <p>Spin the wheel for a random prize.</p>
    </div>

    <div class="wheel-wrap">

      <div class="pointer">▼</div>

      <div class="wheel-circle" id="luckyWheel">
        <div class="wheel-centre">💗</div>
      </div>

      <div class="result" id="wheelResult">
        Spin to see what you win.
      </div>

      <button class="btn btn-primary"
        onclick="spinWheel()">
        🎡 SPIN — 10
      </button>

    </div>
  `;
}

let wheelRotation=0;

function spinWheel(){

  if(S.tokens<10){

    document.getElementById("wheelResult").textContent =
      "You need 10 tokens.";

    return;
  }

  add(-10);

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

  const prize=
    prizes[Math.floor(Math.random()*prizes.length)];

  wheelRotation +=
    1440 + Math.floor(Math.random()*360);

  document.getElementById("luckyWheel").style.transform=
    `rotate(${wheelRotation}deg)`;

  casinoSound();

  setTimeout(()=>{

    add(prize,true);

    document.getElementById("wheelResult").textContent=
      `🎉 You won ${prize.toLocaleString()} tokens!`;

    winSound();

  },4000);
}

/* =========================================================
   COIN
========================================================= */

function coinHTML(){

  return `
    <div class="game-title">
      <h2>🪙 Coin Flip</h2>
      <p>Pick heads or tails.</p>
    </div>

    <div style="text-align:center;margin:25px">

      <div style="font-size:75px" id="coin">
        🪙
      </div>

      <div class="result" id="coinResult">
        Choose your side.
      </div>

      <div class="game-controls">
        <button class="btn btn-primary"
          onclick="flipCoin('Heads')">
          Heads
        </button>

        <button class="btn btn-soft"
          onclick="flipCoin('Tails')">
          Tails
        </button>
      </div>

    </div>
  `;
}

function flipCoin(choice){

  if(S.tokens<10)return;

  add(-10);

  const result=
    Math.random()<.5 ? "Heads" : "Tails";

  document.getElementById("coin").textContent =
    result==="Heads" ? "🪙" : "🔄";

  if(choice===result){

    add(30,true);

    document.getElementById("coinResult").textContent=
      `🎉 ${result}! You won 30 tokens!`;

    winSound();

  }else{

    document.getElementById("coinResult").textContent=
      `${result}! Better luck next time.`;

    loseSound();
  }
}

/* =========================================================
   SIMPLE GAMES
========================================================= */

function mysteryHTML(){

  return `
    <div class="game-title">
      <h2>🎁 Mystery Boxes</h2>
      <p>Choose one mystery box.</p>
    </div>

    <div class="grid">

      ${[1,2,3].map(i=>`
        <button class="game-card"
          onclick="mysteryPick()">
          <div class="game-icon">🎁</div>
          <h3>Box ${i}</h3>
          <p>What's inside?</p>
        </button>
      `).join("")}

    </div>

    <div class="result" id="mysteryResult"></div>
  `;
}

function mysteryPick(){

  const prizes=[25,50,100,250,500,1000];
  const prize=prizes[Math.floor(Math.random()*prizes.length)];

  add(prize,true);

  document.getElementById("mysteryResult").textContent=
    `🎉 You found ${prize} tokens!`;

  winSound();
}

function cupsHTML(){

  return `
    <div class="game-title">
      <h2>🪙 Three Cups</h2>
      <p>Find the hidden token.</p>
    </div>

    <div class="grid">

      ${[1,2,3].map(i=>`
        <button class="game-card"
          onclick="pickCup(${i})">
          <div class="game-icon">🥤</div>
          <h3>Cup ${i}</h3>
          <p>Pick me!</p>
        </button>
      `).join("")}

    </div>

    <div class="result" id="cupResult"></div>
  `;
}

function pickCup(i){

  const winning=Math.floor(Math.random()*3)+1;

  if(i===winning){

    add(200,true);

    document.getElementById("cupResult").textContent=
      "🎉 You found it! +200 tokens!";

    winSound();

  }else{

    document.getElementById("cupResult").textContent=
      `The token was under cup ${winning}.`;

    loseSound();
  }
}

/* =========================================================
   GENERIC MINI GAME HTML
========================================================= */

function simplePrizeHTML(title,emoji,cost=10){

  return `
    <div class="game-title">
      <h2>${emoji} ${title}</h2>
      <p>Try your luck for Friendship Tokens.</p>
    </div>

    <div style="text-align:center;padding:25px">

      <div style="font-size:80px">${emoji}</div>

      <div class="result" id="simpleResult">
        Ready?
      </div>

      <button class="btn btn-primary"
        onclick="simplePrize('${title}')">
        Play — ${cost}
      </button>

    </div>
  `;
}

function simplePrize(title){

  if(S.tokens<10)return;

  add(-10);

  const prizes=[0,20,30,50,100,250,500];
  const prize=prizes[Math.floor(Math.random()*prizes.length)];

  const el=document.getElementById("simpleResult");

  if(prize){

    add(prize,true);

    el.textContent=
      `🎉 ${title}: +${prize} tokens!`;

    winSound();

  }else{

    el.textContent=
      "Nothing this time!";

    loseSound();
  }
}

function scratchHTML(){
  return simplePrizeHTML("Heart Scratch","💗");
}

function dartsHTML(){
  return simplePrizeHTML("Lucky Darts","🎯");
}

function gemHTML(){
  return simplePrizeHTML("Gem Heist","💎");
}

function envelopesHTML(){
  return simplePrizeHTML("Lucky Envelopes","🎁");
}

function numberHTML(){
  return simplePrizeHTML("Lucky Number","🔢");
}

function oceanHTML(){
  return simplePrizeHTML("Ocean Treasure","🐠");
}

function plinkoHTML(){
  return simplePrizeHTML("Plinko","🟣");
}

function crapsHTML(){
  return simplePrizeHTML("Craps","🎲");
}

function hiloHTML(){
  return simplePrizeHTML("Hi-Lo","📈");
}

function rouletteHTML(){
  return simplePrizeHTML("Friendship Roulette","🔴");
}

/* =========================================================
   CARD GAMES
========================================================= */

function cardHTML(title,emoji){

  return `
    <div class="game-title">
      <h2>${emoji} ${title}</h2>
      <p>Play a quick friendship casino round.</p>
    </div>

    <div style="text-align:center;padding:25px">

      <div class="hand">
        <div class="playing-card">?</div>
        <div class="playing-card">?</div>
      </div>

      <div class="result" id="cardResult">
        Ready to play.
      </div>

      <button class="btn btn-primary"
        onclick="playCardGame('${title}')">
        Deal Cards
      </button>

    </div>
  `;
}

function playCardGame(title){

  const win=Math.random()<.48;

  if(win){

    add(100,true);

    document.getElementById("cardResult").textContent=
      `🎉 ${title}: You won 100 tokens!`;

    winSound();

  }else{

    if(S.tokens>=20)add(-20);

    document.getElementById("cardResult").textContent=
      `The ${title} round didn't go your way.`;

    loseSound();
  }
}

function pokerHTML(){
  return cardHTML("Poker","♠️");
}

function blackjackHTML(){
  return cardHTML("Blackjack","♣️");
}

function baccaratHTML(){
  return cardHTML("Baccarat","♦️");
}

function warHTML(){
  return cardHTML("War","🃏");
}

function ginHTML(){
  return cardHTML("Gin Rummy","🃏");
}

function holdemHTML(){
  return cardHTML("Texas Hold'em","🃏");
}

/* =========================================================
   RACES
========================================================= */

function horseHTML(){
  return raceHTML("Horse Derby","🐎");
}

function dolphinRaceHTML(){
  return raceHTML("Dolphin Derby","🐬");
}

function raceHTML(title,emoji){

  return `
    <div class="game-title">
      <h2>${emoji} ${title}</h2>
      <p>Pick your racer.</p>
    </div>

    <div class="grid">

      ${[1,2,3].map(i=>`
        <button class="game-card"
          onclick="race('${title}',${i})">
          <div class="game-icon">${emoji}</div>
          <h3>${title} ${i}</h3>
          <p>Choose racer ${i}.</p>
        </button>
      `).join("")}

    </div>

    <div class="result" id="raceResult"></div>
  `;
}

function race(title,i){

  if(S.tokens<20)return;

  add(-20);

  const winner=Math.floor(Math.random()*3)+1;

  if(i===winner){

    add(150,true);

    document.getElementById("raceResult").textContent=
      `🏆 Racer ${i} won! +150 tokens!`;

    winSound();

  }else{

    document.getElementById("raceResult").textContent=
      `Racer ${winner} won this time.`;

    loseSound();
  }
}

/* =========================================================
   VAULT
========================================================= */

function vaultHTML(){

  return `
    <div class="vault">

      <div style="font-size:65px">🔐</div>

      <h2>Six-Year Friendship Vault</h2>

      <p>
        Six years. One friendship. One secret code.
      </p>

      <input
        id="vaultCode"
        class="vault-input"
        maxlength="6"
        inputmode="numeric"
        placeholder="••••••"
      >

      <button class="btn btn-gold"
        onclick="openVault()">
        Unlock
      </button>

      <div id="vaultResult" style="margin-top:18px;font-weight:800"></div>

    </div>
  `;
}

function openVault(){

  const code=
    document.getElementById("vaultCode").value;

  if(code==="060722"){

    if(!S.vaultOpened){

      add(10000,true);

      S.vaultOpened=true;
      S.ach.push("Vault Keeper");

      save();

      document.getElementById("vaultResult").textContent=
        "🔓 VAULT OPENED! +10,000 Friendship Tokens! 💗";

      winSound();

    }else{

      document.getElementById("vaultResult").textContent=
        "🔓 You've already opened the vault.";

    }

  }else{

    document.getElementById("vaultResult").textContent=
      "❌ Wrong code.";

    loseSound();
  }
}

/* =========================================================
   ACHIEVEMENTS
========================================================= */

function achievementHTML(){

  const achievements=[
    ["🎰","First Spin","Play your first game"],
    ["🏆","First Win","Win a game"],
    ["💰","Token Collector","Reach 5,000 tokens"],
    ["💎","Big Winner","Win 1,000 tokens in one go"],
    ["🐾","Creature Catcher","Catch your first creature"],
    ["🔐","Vault Keeper","Open the friendship vault"],
    ["💎","Million Token Club","Hit the Mega Jackpot"]
  ];

  return `
    <div class="game-title">
      <h2>🏆 Achievements</h2>
      <p>Everything you've unlocked.</p>
    </div>

    <div style="display:grid;gap:10px;margin-top:20px">

      ${achievements.map(a=>{

        let unlocked=false;

        if(a[1]==="First Spin" && S.played>0)unlocked=true;
        if(a[1]==="First Win" && S.wins>0)unlocked=true;
        if(a[1]==="Token Collector" && S.tokens>=5000)unlocked=true;
        if(a[1]==="Big Winner" && S.biggest>=1000)unlocked=true;
        if(a[1]==="Creature Catcher" && S.caught.length>0)unlocked=true;
        if(S.ach.includes(a[1]))unlocked=true;

        return `
          <div class="achievement ${unlocked?"":"locked"}">

            <div class="achievement-icon">
              ${a[0]}
            </div>

            <div>
              <strong>${a[1]}</strong>
              <div style="color:#8b7180;font-size:13px">
                ${a[2]}
              </div>
            </div>

            <div style="margin-left:auto">
              ${unlocked?"✅":"🔒"}
            </div>

          </div>
        `;

      }).join("")}

    </div>
  `;
}

/* =========================================================
   DAILY BONUS
========================================================= */

function dailyBonus(){

  const today=
    new Date().toISOString().slice(0,10);

  if(S.lastDaily===today){

    alert("💗 You've already claimed today's bonus!");

    return;
  }

  S.lastDaily=today;
  S.streak++;
  save();

  add(500,true);

  alert("🎁 Daily Bonus!\n\n+500 Friendship Tokens 💗");
}

/* =========================================================
   FRIENDSHIP CATCH
========================================================= */

const creatures=[

  {
    name:"Dolphini",
    emoji:"🐬",
    rarity:"Common",
    chance:.55
  },

  {
    name:"Rosibun",
    emoji:"🌹",
    rarity:"Common",
    chance:.50
  },

  {
    name:"Sunnyflo",
    emoji:"🌻",
    rarity:"Uncommon",
    chance:.38
  },

  {
    name:"Pinkyroo",
    emoji:"💗",
    rarity:"Uncommon",
    chance:.34
  },

  {
    name:"Fluttera",
    emoji:"🦋",
    rarity:"Rare",
    chance:.25
  },

  {
    name:"Shellby",
    emoji:"🐚",
    rarity:"Rare",
    chance:.22
  },

  {
    name:"Lunaboo",
    emoji:"🌙",
    rarity:"Epic",
    chance:.14
  },

  {
    name:"Gemini",
    emoji:"♊",
    rarity:"Epic",
    chance:.12
  },

  {
    name:"Royala",
    emoji:"👑",
    rarity:"Legendary",
    chance:.07
  },

  {
    name:"Starumi",
    emoji:"⭐",
    rarity:"Legendary",
    chance:.05
  }

];

function catchCreature(){

  const creature=
    creatures[Math.floor(Math.random()*creatures.length)];

  const caught=
    Math.random()<creature.chance;

  const result=
    document.getElementById("catchResult");

  if(caught){

    if(!S.caught.includes(creature.name)){

      S.caught.push(creature.name);

      add(
        creature.rarity==="Legendary" ? 1000 :
        creature.rarity==="Epic" ? 500 :
        creature.rarity==="Rare" ? 250 :
        100,
        true
      );

      result.innerHTML=
        `✨ You caught ${creature.emoji} ${creature.name}!<br>
        <small>${creature.rarity}</small>`;

      winSound();

    }else{

      add(50,true);

      result.innerHTML=
        `You found another ${creature.emoji} ${creature.name}!<br>
        +50 duplicate bonus`;

    }

  }else{

    result.textContent=
      "The creature escaped! Try again. 🐾";

    loseSound();
  }

  save();
  renderCollection();
}

function renderCollection(){

  const container=
    document.getElementById("collection");

  if(!container)return;

  container.innerHTML="";

  creatures.forEach(c=>{

    const owned=
      S.caught.includes(c.name);

    const div=
      document.createElement("div");

    div.className="creature";

    div.innerHTML=`

      <div class="emoji">
        ${owned?c.emoji:"❔"}
      </div>

      <strong>
        ${owned?c.name:"Mystery"}
      </strong>

      <small>
        ${owned?c.rarity:"Not caught"}
      </small>

    `;

    container.appendChild(div);

  });

  document.getElementById("collectionCount").textContent=
    `${S.caught.length}/${creatures.length} creatures caught`;
}

/* =========================================================
   PERSONALITY
========================================================= */

function personality(){

  const types=[

    [
      "🌸 The Soft Liliana",
      "Sweet, caring, empathetic and always looking after the people she loves."
    ],

    [
      "💋 The Flirty Liliana",
      "Charismatic, playful and effortlessly flirtatious."
    ],

    [
      "🎰 The Gambler Liliana",
      "Give her a casino and she is absolutely ready to take her chances."
    ],

    [
      "🐬 The Dreamer Liliana",
      "A romantic who loves big dreams, poetry and meaningful moments."
    ],

    [
      "👑 The Main Character Liliana",
      "Confident, unforgettable and somehow always the centre of the story."
    ]

  ];

  const pick=
    types[Math.floor(Math.random()*types.length)];

  add(300,true);

  document.getElementById("personalityResult").innerHTML=`

    <div class="game-card">

      <div class="game-icon">💗</div>

      <h3>${pick[0]}</h3>

      <p>${pick[1]}</p>

      <strong style="margin-top:15px">
        +300 Friendship Tokens
      </strong>

    </div>

  `;

  winSound();
}

/* =========================================================
   QUIZ
========================================================= */

const quiz=[

  ["Favourite colour?",["Baby pink","Blue","Green","Red"],0],

  ["Favourite number?",["3","7","9","22"],0],

  ["Favourite animal?",["Dolphins","Cats","Rabbits","Horses"],0],

  ["Favourite food?",["Sushi","Pizza","Pasta","Tacos"],0],

  ["Birthday?",["22 July","7 February","2 July","27 July"],0],

  ["Favourite movie?",["Me Before You","Titanic","Frozen","The Notebook"],0],

  ["How many nieces?",["1","2","3","4"],0],

  ["How many nephews?",["4","1","2","5"],0],

  ["How many tattoos?",["1","2","3","4"],0],

  ["Eye colour?",["Green","Blue","Brown","Hazel"],0],

  ["How many piercings?",["4","2","6","8"],0],

  ["Dogs' names?",["Aayla & Arlo","Luna & Milo","Bella & Arlo","Aayla & Leo"],0],

  ["How many siblings?",["5","3","4","6"],0],

  ["Star sign?",["Leo","Cancer","Virgo","Gemini"],0],

  ["What is she afraid of?",["Drowning","Thunder","Heights","Spiders"],0],

  ["What did she study at university?",["Psychology","Law","Nursing","Art"],0],

  ["Favourite flowers?",["Sunflowers & roses","Lilies","Tulips","Daisies"],0],

  ["What does she like?",["Sad songs & poetry","Only comedy","Only rock","Only podcasts"],0],

  ["Future dream?",["Be a mum to a baby girl","Travel to space","Own a casino","Become a pilot"],0],

  ["Which interests fit Liliana?",["Children, poker and gambling","Only sport","Only cooking","Cars and fishing"],0]

];

let quizAnswers=[];

function openQuiz(){

  quizAnswers=[];

  let html=`

    <div class="game-title">

      <h2>💗 How Well Do You Know Liliana?</h2>

      <p>
        Answer all 20 questions.
        The correct answers are not displayed.
      </p>

    </div>

  `;

  quiz.forEach((q,index)=>{

    html+=`

      <div class="quiz-question">

        <h3>
          ${index+1}. ${q[0]}
        </h3>

        <div class="answers">

          ${q[1].map((answer,i)=>`

            <button
              class="answer"
              onclick="selectQuizAnswer(${index},${i},this)">
              ${answer}
            </button>

          `).join("")}

        </div>

      </div>

    `;

  });

  html+=`

    <button class="btn btn-primary"
      onclick="submitQuiz()">
      Submit Quiz
    </button>

    <div class="result" id="quizResult"></div>
  `;

  openModal(html);
}

function selectQuizAnswer(question,answer,button){

  quizAnswers[question]=answer;

  button.parentElement
    .querySelectorAll(".answer")
    .forEach(b=>b.classList.remove("selected"));

  button.classList.add("selected");
}

function submitQuiz(){

  let score=0;

  quiz.forEach((q,i)=>{

    if(quizAnswers[i]===q[2]){
      score++;
    }

  });

  let reward=score*100;

  if(score===20){
    reward+=5000;
  }

  add(reward,score>0);

  const result=
    document.getElementById("quizResult");

  result.innerHTML=`

    <div style="
      background:#fff4f9;
      padding:18px;
      border-radius:18px;
      margin-top:15px">

      💗 You scored <strong>${score}/20</strong>

      <br><br>

      💰 You earned
      <strong>${reward.toLocaleString()} tokens</strong>

      ${score===20
        ?"<br><br>🏆 PERFECT SCORE! +5,000 BONUS!"
        :""
      }

    </div>

  `;

  if(score>=10){
    winSound();
  }else{
    loseSound();
  }
}

/* =========================================================
   CLOSE MODAL WHEN CLICKING BACKGROUND
========================================================= */

document.getElementById("gameModal")
  .addEventListener("click",e=>{

    if(e.target.id==="gameModal"){
      closeModal();
    }

  });

</script>

</body>
</html>
