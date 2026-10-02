<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Liliana's Friendship Casino 💗</title>
<style>
*{box-sizing:border-box}
body{
  margin:0;
  font-family:system-ui,-apple-system,Segoe UI,sans-serif;
  background:radial-gradient(circle at top,#ffd9ed,#f7a8cf 42%,#8f376b);
  color:#fff;
  min-height:100vh
}
header{
  position:sticky;
  top:0;
  z-index:10;
  background:rgba(67,12,45,.92);
  backdrop-filter:blur(12px);
  padding:14px;
  text-align:center;
  border-bottom:1px solid #ffffff33
}
h1{margin:0;font-size:clamp(24px,6vw,42px)}
h2{margin-top:0}
.sub{opacity:.85}
.stats{
  display:flex;
  justify-content:center;
  gap:8px;
  flex-wrap:wrap;
  margin-top:10px
}
.stat{
  background:#ffffff18;
  border:1px solid #ffffff30;
  border-radius:999px;
  padding:7px 12px
}
nav{
  display:flex;
  gap:7px;
  overflow:auto;
  padding:10px;
  justify-content:center;
  background:#4b1234
}
.tab{
  border:0;
  border-radius:20px;
  padding:9px 13px;
  background:#ffffff16;
  color:#fff;
  white-space:nowrap;
  font-weight:700;
  cursor:pointer
}
main{
  max-width:1200px;
  margin:auto;
  padding:16px
}
.page{display:none}
.page.active{display:block}
.grid{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
  gap:14px
}
.card{
  background:#ffffff13;
  border:1px solid #ffffff2b;
  border-radius:20px;
  padding:18px;
  box-shadow:0 10px 30px #3b0b2930
}
.game{text-align:center}
button{
  border:0;
  border-radius:14px;
  padding:11px 16px;
  background:#ff75b9;
  color:#fff;
  font-weight:800;
  cursor:pointer;
  margin:4px;
  box-shadow:0 5px 15px #0002
}
button:hover{filter:brightness(1.08)}
button:disabled{
  opacity:.45;
  cursor:not-allowed
}
.big{font-size:42px}
.muted{opacity:.75}
.result{
  min-height:28px;
  margin:10px 0;
  font-weight:800
}
.reels{
  display:flex;
  justify-content:center;
  gap:7px;
  margin:15px
}
.reel{
  width:72px;
  height:72px;
  background:#fff;
  color:#4b1234;
  border-radius:14px;
  display:grid;
  place-items:center;
  font-size:35px;
  border:4px solid #ffd3e9
}
.wheel{
  width:min(290px,75vw);
  aspect-ratio:1;
  border-radius:50%;
  margin:20px auto;
  position:relative;
  display:grid;
  place-items:center;
  border:10px solid #fff;
  background:conic-gradient(
    #ff77b9 0 12.5%,
    #ffd05c 12.5% 25%,
    #a8e8ff 25% 37.5%,
    #cda6ff 37.5% 50%,
    #ff9f9f 50% 62.5%,
    #91e5bd 62.5% 75%,
    #fff 75% 87.5%,
    #ff77b9 87.5%
  );
  transition:transform 3s cubic-bezier(.12,.72,.15,1)
}
.pointer{
  font-size:34px;
  margin-bottom:-15px
}
.wheelCenter{
  background:#5b173f;
  border:5px solid #fff;
  border-radius:50%;
  width:62px;
  height:62px;
  display:grid;
  place-items:center
}
.cards{
  display:flex;
  justify-content:center;
  flex-wrap:wrap;
  gap:6px
}
.playing{
  background:#fff;
  color:#321025;
  border-radius:10px;
  padding:12px;
  font-weight:900;
  min-width:48px
}
input,select{
  padding:11px;
  border-radius:12px;
  border:0;
  margin:4px
}
.quizq{
  background:#ffffff10;
  border-radius:15px;
  padding:12px;
  margin:10px 0;
  text-align:left
}
.quizq label{
  display:block;
  padding:6px
}
.collection{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(130px,1fr));
  gap:10px
}
.creature{
  padding:14px;
  border-radius:16px;
  background:#ffffff12;
  text-align:center;
  border:1px solid #ffffff25
}
.toast{
  position:fixed;
  right:15px;
  bottom:15px;
  background:#4b1234;
  padding:13px 17px;
  border-radius:14px;
  display:none;
  z-index:20
}
footer{
  text-align:center;
  padding:30px;
  opacity:.7
}
</style>
</head>

<body>

<header>

<h1>🎀 Liliana's Friendship Casino 🎀</h1>

<div class="sub">
Six years of friendship. One very pink casino.
</div>

<div class="stats">

<span class="stat">
💰 <b id="tokens">1000</b>
</span>

<span class="stat">
⭐ Lv <b id="level">1</b>
</span>

<span class="stat">
XP <b id="xp">0</b>
</span>

<span class="stat">
🔥 <b id="streak">0</b>
</span>

<span class="stat">
🏆 <b id="wins">0</b> wins
</span>

<button onclick="toggleSound()" id="soundBtn">
🔊 Sound On
</button>

</div>
</header>

<nav>

<button class="tab" onclick="show('home')">🏠 Home</button>

<button class="tab" onclick="show('slots')">
🎰 Slots
</button>

<button class="tab" onclick="show('cards')">
🃏 Cards
</button>

<button class="tab" onclick="show('games')">
🎡 Games
</button>

<button class="tab" onclick="show('catch')">
🐾 Catch
</button>

<button class="tab" onclick="show('liliana')">
💗 Liliana
</button>

<button class="tab" onclick="show('special')">
🔐 Special
</button>

</nav>

<main>

<!-- HOME -->

<section id="home" class="page active">

<div class="card">

<h2>🎀 Welcome to the Casino</h2>

<p>
Play for fictional Friendship Tokens, earn XP and unlock achievements.
</p>

<div class="grid">

<div class="card">
🎰 <b>Games</b>
<div id="played">0</div>
</div>

<div class="card">
💰 <b>Biggest Win</b>
<div id="biggest">0</div>
</div>

<div class="card">
🏆 <b>Achievements</b>
<div id="achCount">0</div>
</div>

<div class="card">
🐾 <b>Creatures</b>
<div id="caughtCount">0</div>
</div>

</div>

<h3>🎁 Daily Bonus</h3>

<button onclick="daily()">
Claim Daily Bonus
</button>

<div id="dailyResult" class="result"></div>

</div>

</section>


<!-- SLOTS -->

<section id="slots" class="page">

<h2>🎰 Slot Machines</h2>

<div class="grid">

<div class="card game">

<h3>🦬 Buffalo Stampede</h3>

<div class="reels" id="buffalo"></div>

<button onclick="slot('buffalo',['🦬','🌵','⭐','💰','7️⃣'])">
SPIN
</button>

<div id="buffaloR" class="result"></div>

</div>


<div class="card game">

<h3>💗 Pink Palace</h3>

<div class="reels" id="pink"></div>

<button onclick="slot('pink',['💗','🎀','🌸','💎','👑'])">
SPIN
</button>

<div id="pinkR" class="result"></div>

</div>


<div class="card game">

<h3>🐬 Dolphin Riches</h3>

<div class="reels" id="dolphin"></div>

<button onclick="slot('dolphin',['🐬','🌊','🐚','💎','⭐'])">
SPIN
</button>

<div id="dolphinR" class="result"></div>

</div>


<div class="card game">

<h3>7️⃣ Fancy 7s</h3>

<div class="reels" id="sevens"></div>

<button onclick="slot('sevens',['7️⃣','7️⃣','🍒','💎','⭐'])">
SPIN
</button>

<div id="sevensR" class="result"></div>

</div>


<!-- MEGA JACKPOT -->

<div class="card game" style="grid-column:1/-1">

<h2>💎 MEGA JACKPOT</h2>

<p class="big">
1,000,000 💰
</p>

<div class="reels" id="mega"></div>

<button onclick="mega()">
🎰 SPIN MEGA JACKPOT
</button>

<div id="megaR" class="result"></div>

<small>
Three 💎 symbols trigger the
1,000,000 Friendship Token jackpot.
</small>

</div>

</div>

</section>


<!-- CARD GAMES -->

<section id="cards" class="page">

<h2>🃏 Card Games</h2>

<div class="grid">


<div class="card game">

<h3>♣️ Blackjack</h3>

<div id="bj"></div>

<button onclick="bjStart()">Deal</button>

<button onclick="bjHit()">Hit</button>

<button onclick="bjStand()">Stand</button>

<button onclick="bjDouble()">Double Down</button>

<div id="bjR" class="result"></div>

</div>


<div class="card game">

<h3>♠️ Poker vs Computer</h3>

<button onclick="poker()">
Deal 5 Cards
</button>

<div id="poker" class="cards"></div>

<div id="pokerR" class="result"></div>

</div>


<div class="card game">

<h3>♦️ Baccarat</h3>

<button onclick="baccarat()">
Deal
</button>

<div id="bacR" class="result"></div>

</div>


<div class="card game">

<h3>🎴 War</h3>

<button onclick="war()">
Battle
</button>

<div id="warR" class="result"></div>

</div>


<div class="card game">

<h3>🃏 Gin Rummy</h3>

<p>
Build a simple hand and try to make the best meld score.
</p>

<button onclick="gin()">
Deal Hand
</button>

<div id="ginCards" class="cards"></div>

<div id="ginR" class="result"></div>

</div>


<div class="card game">

<h3>🃏 Texas Hold'em</h3>

<button onclick="holdem()">
Deal Round
</button>

<div id="holdemR" class="result"></div>

</div>

</div>

</section>


<!-- CASINO GAMES -->

<section id="games" class="page">

<h2>🎡 Casino Floor</h2>

<div class="grid">


<div class="card game">

<h3>🎡 Lucky Wheel</h3>

<div class="pointer">
🔻
</div>

<div class="wheel" id="wheel">

<div class="wheelCenter">
🎡
</div>

</div>

<button onclick="wheelSpin()">
SPIN
</button>

<div id="wheelR" class="result"></div>

</div>


<div class="card game">

<h3>🔴⚫ Friendship Roulette</h3>

<button onclick="roulette('red')">
🔴 Red
</button>

<button onclick="roulette('black')">
⚫ Black
</button>

<div id="rouletteR" class="result"></div>

</div>


<div class="card game">

<h3>🎲 Craps</h3>

<button onclick="craps()">
ROLL DICE
</button>

<div id="crapsR" class="result"></div>

</div>


<div class="card game">

<h3>📈 Hi-Lo</h3>

<button onclick="hilo('higher')">
Higher
</button>

<button onclick="hilo('lower')">
Lower
</button>

<div id="hiloR" class="result"></div>

</div>


<div class="card game">

<h3>🪙 Coin Flip</h3>

<button onclick="coin()">
FLIP
</button>

<div id="coinR" class="result"></div>

</div>


<div class="card game">

<h3>🟣 Plinko</h3>

<button onclick="plinko()">
DROP TOKEN
</button>

<div id="plinkoR" class="result"></div>

</div>


<div class="card game">

<h3>🎁 Mystery Boxes</h3>

<button onclick="mystery()">
OPEN A BOX
</button>

<div id="mysteryR" class="result"></div>

</div>


<div class="card game">

<h3>🐎 Horse Derby</h3>

<button onclick="race('horse')">
RACE
</button>

<div id="horseR" class="result"></div>

</div>


<div class="card game">

<h3>🐬 Dolphin Derby</h3>

<button onclick="race('dolphin')">
RACE
</button>

<div id="raceR" class="result"></div>

</div>


<div class="card game">

<h3>🪙 Three Cups</h3>

<button onclick="cups()">
PICK A CUP
</button>

<div id="cupsR" class="result"></div>

</div>


<div class="card game">

<h3>💗 Heart Scratch Card</h3>

<button onclick="scratch()">
SCRATCH
</button>

<div id="scratchR" class="result"></div>

</div>


<div class="card game">

<h3>🎯 Lucky Darts</h3>

<button onclick="darts()">
THROW
</button>

<div id="dartsR" class="result"></div>

</div>


<div class="card game">

<h3>💎 Gem Heist</h3>

<button onclick="gem()">
CHOOSE A DOOR
</button>

<div id="gemR" class="result"></div>

</div>


<div class="card game">

<h3>🎁 Lucky Envelopes</h3>

<button onclick="envelope()">
PICK ENVELOPE
</button>

<div id="envR" class="result"></div>

</div>


<div class="card game">

<h3>🔢 Lucky Number</h3>

<input
id="guess"
type="number"
min="1"
max="10"
placeholder="1-10"
>

<button onclick="lucky()">
GUESS
</button>

<div id="luckyR" class="result"></div>

</div>


<div class="card game">

<h3>🐠 Ocean Treasure</h3>

<button onclick="treasure()">
DIVE
</button>

<div id="treasureR" class="result"></div>

</div>

</div>

</section>


<!-- FRIENDSHIP CATCH -->

<section id="catch" class="page">

<h2>🐾 Friendship Catch</h2>

<div class="card game">

<p>
Explore for an original creature, then try to catch it with a Friendship Capsule.
</p>

<button onclick="encounter()">
🌿 EXPLORE
</button>

<div id="encounter" class="big"></div>

<div id="catchR" class="result"></div>

<button
id="catchBtn"
onclick="catchCreature()"
disabled
>
🟣 CATCH!
</button>

</div>

<h3>📖 Creature Collection</h3>

<div id="collection" class="collection"></div>

</section>


<!-- LILIANA -->

<section id="liliana" class="page">

<h2>💗 Liliana</h2>

<div class="card">

<h3>
🧠 How Well Do You Know Liliana?
</h3>

<div id="quiz"></div>

<button onclick="submitQuiz()">
SUBMIT QUIZ
</button>

<div id="quizR" class="result"></div>

</div>


<div
class="card"
style="margin-top:14px"
>

<h3>
🌸 Liliana Personality Test
</h3>

<div id="personality"></div>

<button onclick="personality()">
REVEAL MY RESULT
</button>

<div id="personR" class="result"></div>

</div>

</section>


<!-- SPECIAL -->

<section id="special" class="page">

<div class="card game">

<h2>
🔐 Friendship Vault
</h2>

<p>
Six years. One special birthday. Enter the six-digit code.
</p>

<input
id="vaultInput"
maxlength="6"
inputmode="numeric"
placeholder="6-digit code"
>

<button onclick="vault()">
UNLOCK
</button>

<div id="vaultR" class="result"></div>

</div>


<div
class="card"
style="margin-top:14px"
>

<h2>
🏆 Achievements
</h2>

<div id="achievements"></div>

</div>

</section>

</main>


<footer>
💗 Friendship Casino • Fictional Friendship Tokens only • Made for Liliana
</footer>

<div class="toast" id="toast"></div>


<script>

let S =
JSON.parse(localStorage.getItem('lilianaCasino') || 'null')
||
{
  tokens:1000,
  xp:0,
  streak:0,
  wins:0,
  played:0,
  biggest:0,
  ach:[],
  caught:[],
  sound:true,
  lastDaily:''
};


function save(){
  localStorage.setItem(
    'lilianaCasino',
    JSON.stringify(S)
  );
  render();
}


function render(){

  tokens.textContent =
    S.tokens.toLocaleString();

  xp.textContent =
    S.xp;

  level.textContent =
    Math.floor(S.xp/500)+1;

  streak.textContent =
    S.streak;

  wins.textContent =
    S.wins;

  played.textContent =
    S.played;

  biggest.textContent =
    S.biggest.toLocaleString();

  achCount.textContent =
    S.ach.length;

  caughtCount.textContent =
    S.caught.length;

  soundBtn.textContent =
    S.sound
    ? '🔊 Sound On'
    : '🔇 Sound Off';

  renderAch();
  renderCollection();
}


function show(id){

  document
    .querySelectorAll('.page')
    .forEach(x =>
      x.classList.remove('active')
    );

  document
    .getElementById(id)
    .classList.add('active');
}


function add(n,win=false){

  S.tokens += n;

  S.xp +=
    Math.max(
      5,
      Math.floor(Math.abs(n)/20)
    );

  S.played++;

  if(win){

    S.wins++;

    if(n > S.biggest)
      S.biggest = n;

  }

  save();
}


function msg(id,t){

  document
    .getElementById(id)
    .textContent = t;
}


function rand(a,b){

  return Math.floor(
    Math.random()*(b-a+1)
  )+a;

}


let audioCtx;


function tone(f,d=.12){

  if(!S.sound)return;

  audioCtx ??=
    new AudioContext();

  let o =
    audioCtx.createOscillator();

  let g =
    audioCtx.createGain();

  o.frequency.value=f;

  o.connect(g);

  g.connect(
    audioCtx.destination
  );

  g.gain.value=.05;

  o.start();

  o.stop(
    audioCtx.currentTime+d
  );

}


function toggleSound(){

  S.sound=!S.sound;

  save();

}


function slot(id,syms){

  tone(180,.15);

  let r=[];

  for(let i=0;i<3;i++)
    r.push(
      syms[
        rand(0,syms.length-1)
      ]
    );

  document.getElementById(id)
    .innerHTML =
      r.map(
        x =>
        `<div class="reel">${x}</div>`
      ).join('');

  let win =
    r[0]===r[1] &&
    r[1]===r[2];

  let n =
    win
    ? rand(300,3000)
    : rand(10,120);

  if(win){

    tone(700,.4);

    add(n,true);

  }else{

    add(
      -Math.min(S.tokens,20)
    );

  }

  msg(
    id+'R',
    win
    ? `🎉 WIN! +${n.toLocaleString()} tokens`
    : `No match. Try again!`
  );

}


function mega(){

  tone(120,.2);

  let r =
    Math.random()<.003
    ?
    ['💎','💎','💎']
    :
    [
      ['💎','👑','7️⃣'][rand(0,2)],
      ['💎','👑','7️⃣'][rand(0,2)],
      ['💎','👑','7️⃣'][rand(0,2)]
    ];

  mega.innerHTML =
    r.map(
      x =>
      `<div class="reel">${x}</div>`
    ).join('');

  if(
    r.every(
      x => x==='💎'
    )
  ){

    add(
      1000000,
      true
    );

    unlock(
      'Million Token Club'
    );

    msg(
      'megaR',
      '💎💎💎 MEGA JACKPOT! +1,000,000 Friendship Tokens! 🎉'
    );

  }else{

    add(-20);

    msg(
      'megaR',
      'Not this time... the Mega Jackpot is still waiting!'
    );

  }

}


let deck=[];


function newDeck(){

  let s=[
    '♠',
    '♥',
    '♦',
    '♣'
  ];

  let v=[
    2,3,4,5,6,7,8,9,10,
    'J','Q','K','A'
  ];

  return s.flatMap(
    a =>
    v.map(
      b => ({
        s:a,
        v:b,
        n:
          ['J','Q','K'].includes(b)
          ?10
          :b==='A'
          ?11
          :b
      })
    )
  );

}


function draw(){

  if(!deck.length)
    deck=newDeck();

  return deck.splice(
    rand(0,deck.length-1),
    1
  )[0];

}


function handVal(h){

  let n =
    h.reduce(
      (a,c)=>a+c.n,
      0
    );

  let aces =
    h.filter(
      c=>c.v==='A'
    ).length;

  while(
    n>21 &&
    aces--
  )
    n-=10;

  return n;

}


let bh=[];


function bjStart(){

  bh=[
    draw(),
    draw()
  ];

  msg(
    'bjR',
    'Your hand: '+
    bh.map(
      c=>c.v+c.s
    ).join(' ')
    +' = '+
    handVal(bh)
  );

}


function bjHit(){

  if(!bh.length)
    bjStart();

  else{

    bh.push(draw());

    let v =
      handVal(bh);

    msg(
      'bjR',
      'Your hand: '+
      bh.map(
        c=>c.v+c.s
      ).join(' ')
      +' = '+v
    );

    if(v>21){

      add(-30);

      bh=[];

      msg(
        'bjR',
        '💥 Bust!'
      );

    }

  }

}


function bjStand(){

  if(!bh.length)
    return;

  let d=[
    draw(),
    draw()
  ];

  while(
    handVal(d)<17
  )
    d.push(draw());

  let a=handVal(bh);
  let b=handVal(d);

  let n =
    a>b && a<=21
    ?100
    :a===b
    ?0
    :-40;

  add(
    n,
    n>0
  );

  msg(
    'bjR',
    `You ${
      a>b && a<=21
      ?'win 🎉'
      :a===b
      ?'push'
      :'lose'
    } • You ${a} / Dealer ${b}`
  );

  bh=[];

}


function bjDouble(){

  if(!bh.length)
    return;

  add(-20);

  bjHit();

  if(bh.length)
    bjStand();

}


function poker(){

  let h =
    [
      draw(),
      draw(),
      draw(),
      draw(),
      draw()
    ];

  poker.innerHTML =
    h.map(
      c =>
      `<span class="playing">
        ${c.v}${c.s}
      </span>`
    ).join('');

  let vals =
    h.map(c=>c.v);

  let pair =
    new Set(vals).size<5;

  let n =
    pair
    ?250
    :50;

  add(n,true);

  msg(
    'pokerR',
    pair
    ?'🎉 Pair or better! +250'
    :'Nice hand! +50'
  );

}


function baccarat(){

  let p=[
    draw(),
    draw()
  ];

  let b=[
    draw(),
    draw()
  ];

  let v =
    h =>
    h.reduce(
      (a,c)=>a+c.n,
      0
    )%10;

  let a=v(p);
  let d=v(b);

  let n =
    a>d
    ?200
    :a===d
    ?0
    :-50;

  add(n,n>0);

  msg(
    'bacR',
    `Player ${a} • Banker ${d} • ${
      n>0
      ?'You win!'
      :n===0
      ?'Tie'
      :'Banker wins'
    }`
  );

}


function war(){

  let a=draw();
  let b=draw();

  let va =
    a.n===11
    ?14
    :a.n;

  let vb =
    b.n===11
    ?14
    :b.n;

  let n =
    va>vb
    ?150
    :va===vb
    ?0
    :-30;

  add(n,n>0);

  msg(
    'warR',
    `You ${a.v}${a.s} vs ${b.v}${b.s} • ${
      n>0
      ?'WIN!'
      :n===0
      ?'WAR!'
      :'Loss'
    }`
  );

}


function gin(){

  let h =
    Array.from(
      {length:10},
      draw
    );

  ginCards.innerHTML =
    h.map(
      c =>
      `<span class="playing">
        ${c.v}${c.s}
      </span>`
    ).join('');

  let score =
    rand(20,120);

  add(score,true);

  msg(
    'ginR',
    `Your meld score: ${score}. +${score} tokens!`
  );

}


function holdem(){

  let h=[
    draw(),
    draw()
  ];

  let c =
    Array.from(
      {length:5},
      draw
    );

  add(100,true);

  msg(
    'holdemR',
    `Your cards ${
      h.map(
        x=>x.v+x.s
      ).join(' ')
    } • Board ${
      c.map(
        x=>x.v+x.s
      ).join(' ')
    } • +100 tokens`
  );

}


function wheelSpin(){

  let n=rand(1,8);

  let prizes=[
    50,
    100,
    250,
    500,
    1000,
    2500,
    5000,
    10000
  ];

  let w=
    document.getElementById('wheel');

  w.style.transform =
    `rotate(${1440+n*45}deg)`;

  setTimeout(
    ()=>{
      add(
        prizes[n-1],
        true
      );

      msg(
        'wheelR',
        `🎉 You won ${
          prizes[n-1].toLocaleString()
        } tokens!`
      );
    },
    3000
  );

}


function roulette(c){

  let actual =
    Math.random()<.5
    ?'red'
    :'black';

  let win =
    c===actual;

  let n =
    win
    ?200
    :-30;

  add(n,n>0);

  msg(
    'rouletteR',
    `Ball: ${actual} • ${
      n>0
      ?'WIN! +200'
      :'No luck'
    }`
  );

}


function craps(){

  let a=rand(1,6);
  let b=rand(1,6);
  let s=a+b;

  let n =
    [7,11].includes(s)
    ?300
    :[2,3,12].includes(s)
    ?-60
    :80;

  add(n,n>0);

  msg(
    'crapsR',
    `🎲 ${a}+${b}=${s} • ${
      n>0
      ?'WIN!'
      :'Loss'
    }`
  );

}


let lastCard=rand(2,14);


function hilo(x){

  let n=rand(2,14);

  let win =
    x==='higher'
    ?n>lastCard
    :n<lastCard;

  add(
    win
    ?120
    :-30,
    win
  );

  msg(
    'hiloR',
    `Old ${lastCard} → New ${n} • ${
      win
      ?'Correct!'
      :'Wrong!'
    }`
  );

  lastCard=n;

}


function coin(){

  let result =
    Math.random()<.5
    ?'Heads'
    :'Tails';

  let win =
    Math.random()<.5;

  add(
    win
    ?100
    :-20,
    win
  );

  msg(
    'coinR',
    `${result} • ${
      win
      ?'WIN!'
      :'Try again'
    }`
  );

}


function plinko(){

  let n=[
    50,
    100,
    250,
    500,
    1000,
    2500
  ][rand(0,5)];

  add(n,true);

  msg(
    'plinkoR',
    `🟣 Landed on ${n.toLocaleString()} tokens!`
  );

}


function mystery(){

  let n=[
    50,
    100,
    250,
    500,
    1000,
    5000
  ][rand(0,5)];

  add(n,true);

  msg(
    'mysteryR',
    `🎁 Your box contained ${n.toLocaleString()} tokens!`
  );

}


function race(type){

  let winner=rand(1,4);
  let pick=rand(1,4);

  let win=
    winner===pick;

  let n=
    win
    ?300
    :-25;

  add(n,win);

  msg(
    type==='horse'
    ?'horseR'
    :'raceR',
    `${type==='horse'?'🐎':'🐬'} You picked ${pick}. Winner: ${winner}. ${
      win
      ?'YOU WIN!'
      :'Not this time!'
    }`
  );

}


function cups(){

  let pick=rand(1,3);
  let gem=rand(1,3);

  let win=
    pick===gem;

  let n=
    win
    ?500
    :-20;

  add(n,win);

  msg(
    'cupsR',
    `You picked cup ${pick}. Gem was in ${gem}. ${
      win
      ?'💎 WIN!'
      :'Empty!'
    }`
  );

}


function scratch(){

  let n=rand(50,1500);

  add(n,true);

  msg(
    'scratchR',
    `💗 Scratch revealed ${n.toLocaleString()} tokens!`
  );

}


function darts(){

  let n=[
    50,
    100,
    250,
    500,
    1000
  ][rand(0,4)];

  add(n,true);

  msg(
    'dartsR',
    `🎯 Bullseye! +${n} tokens`
  );

}


function gem(){

  let win=
    Math.random()<.25;

  let n=
    win
    ?2500
    :20;

  add(n,win);

  msg(
    'gemR',
    win
    ?'💎 Diamond stolen! +2,500'
    :'You found a decoy!'
  );

}


function envelope(){

  let n=[
    100,
    250,
    500,
    1000
  ][rand(0,3)];

  add(n,true);

  msg(
    'envR',
    `💌 Envelope contained ${n} tokens!`
  );

}


function lucky(){

  let g =
    Number(
      document.getElementById('guess').value
    );

  let n=
    rand(1,10);

  let win=
    g===n;

  add(
    win
    ?1000
    :-20,
    win
  );

  msg(
    'luckyR',
    `Number was ${n}. ${
      win
      ?'🎉 JACKPOT!'
      :'Nope!'
    }`
  );

}


function treasure(){

  let n=[
    100,
    250,
    500,
    1000,
    2500
  ][rand(0,4)];

  add(n,true);

  msg(
    'treasureR',
    `🐠 You found ${n.toLocaleString()} treasure tokens!`
  );

}


/* FRIENDSHIP CATCH */

const creatures=[
  ['🐬','Dolphini','Common',100],
  ['🌸','Rosibun','Common',100],
  ['🌻','Sunnyflo','Uncommon',250],
  ['💗','Pinkyroo','Uncommon',250],
  ['🦋','Fluttera','Rare',1000],
  ['🐢','Shellby','Rare',1000],
  ['🌙','Lunaboo','Epic',5000],
  ['💎','Gemini','Epic',5000],
  ['👑','Royala','Legendary',25000],
  ['✨','Starumi','Legendary',25000]
];

let current=null;


function encounter(){

  current =
    creatures[
      rand(
        0,
        creatures.length-1
      )
    ];

  document.getElementById(
    'encounter'
  ).textContent =
    current[0];

  msg(
    'catchR',
    `A ${current[1]} appeared! ${current[2]} rarity.`
  );

  catchBtn.disabled=false;

  tone(500,.2);

}


function catchCreature(){

  let success =
    Math.random()
    <
    (
      current[2]==='Legendary'
      ? .25
      : current[2]==='Epic'
      ? .45
      : current[2]==='Rare'
      ? .6
      : .8
    );

  if(success){

    S.caught.push(
      current[1]
    );

    add(
      current[3],
      true
    );

    if(
      current[2]==='Legendary'
    )
      unlock(
        'Legendary Hunter'
      );

    msg(
      'catchR',
      `✨ CLICK! You caught ${current[1]}! +${current[3].toLocaleString()} tokens`
    );

  }else{

    add(-10);

    msg(
      'catchR',
      `${current[1]} escaped!`
    );

  }

  catchBtn.disabled=true;

  save();

}


function renderCollection(){

  collection.innerHTML =
    S.caught.length

    ?

    S.caught.map(
      n=>{

        let c=
          creatures.find(
            x=>x[1]===n
          );

        return `
        <div class="creature">

          <div class="big">
            ${c[0]}
          </div>

          <b>${n}</b>

          <br>

          <small>
            ${c[2]}
          </small>

        </div>
        `;

      }
    ).join('')

    :

    '<p class="muted">No creatures caught yet.</p>';

}


/* QUIZ */

const qs=[

[
'Favourite colour?',
['Baby pink','Blue','Green','Red'],
0
],

[
'Favourite number?',
['3','7','9','22'],
0
],

[
'Favourite animal?',
['Dolphins','Cats','Rabbits','Horses'],
0
],

[
'Favourite food?',
['Sushi','Pizza','Pasta','Tacos'],
0
],

[
'Birthday?',
['22 July','7 February','2 July','27 July'],
0
],

[
'Favourite movie?',
['Me Before You','Titanic','Frozen','The Notebook'],
0
],

[
'Nieces?',
['1','2','3','4'],
0
],

[
'Nephews?',
['4','1','2','5'],
0
],

[
'Tattoos?',
['1','2','3','4'],
0
],

[
'Eye colour?',
['Green','Blue','Brown','Hazel'],
0
],

[
'Piercings?',
['4','2','6','8'],
0
],

[
'Dogs?',
['Aayla & Arlo','Luna & Milo','Bella & Arlo','Aayla & Leo'],
0
],

[
'Siblings?',
['5','3','4','6'],
0
],

[
'Star sign?',
['Leo','Cancer','Virgo','Gemini'],
0
],

[
'Afraid of?',
['Drowning','Thunder','Heights','Spiders'],
0
],

[
'University study?',
['Psychology','Law','Nursing','Art'],
0
],

[
'Favourite flowers?',
['Sunflowers & roses','Lilies','Tulips','Daisies'],
0
],

[
'Likes?',
['Sad songs & poetry','Only comedy','Only rock','Only podcasts'],
0
],

[
'Future wish?',
['Be a mum to a baby girl','Travel to space','Own a casino','Become a pilot'],
0
],

[
'Favourite interests?',
['Children, poker and gambling','Only sport','Only cooking','Cars and fishing'],
0
]

];


function buildQuiz(){

  quiz.innerHTML =
    qs.map(
      (q,i)=>

      `<div class="quizq">

        <b>
          ${i+1}. ${q[0]}
        </b>

        ${
          q[1].map(
            (a,j)=>

            `<label>

              <input
                type="radio"
                name="q${i}"
                value="${j}"
              >

              ${a}

            </label>`

          ).join('')
        }

      </div>`

    ).join('');

}


function submitQuiz(){

  let score=0;

  qs.forEach(
    (q,i)=>{

      let x =
        document.querySelector(
          `input[name=q${i}]:checked`
        );

      if(
        x &&
        +x.value===q[2]
      )
        score++;

    }
  );

  let reward =
    score*150 +
    (
      score===20
      ?5000
      :0
    );

  add(
    reward,
    reward>0
  );

  msg(
    'quizR',
    `You scored ${score}/20 and earned ${reward.toLocaleString()} tokens!`
  );

  if(score===20)
    unlock(
      'Quiz Master'
    );

}


/* PERSONALITY */

function personality(){

  let types=[

    '🌸 The Soft Liliana',

    '💋 The Flirty Liliana',

    '🎰 The Gambler Liliana',

    '🐬 The Dreamer Liliana',

    '👑 The Main Character Liliana'

  ];

  let r =
    types[
      rand(
        0,
        types.length-1
      )
    ];

  add(
    300,
    true
  );

  msg(
    'personR',
    `${r} • Your personality result is unlocked! +300 tokens`
  );

}


/* VAULT */

function vault(){

  let code =
    document.getElementById(
      'vaultInput'
    ).value;

  if(code==='060722'){

    if(
      !localStorage.getItem(
        'vaultOpened'
      )
    ){

      add(
        10000,
        true
      );

      localStorage.setItem(
        'vaultOpened',
        '1'
      );

      unlock(
        'Vault Keeper'
      );

      msg(
        'vaultR',
        '🔓 VAULT OPENED! +10,000 tokens!'
      );

    }else{

      msg(
        'vaultR',
        '🔐 Vault already opened on this browser.'
      );

    }

  }else{

    msg(
      'vaultR',
      '❌ Incorrect code.'
    );

  }

}


/* ACHIEVEMENTS */

function unlock(a){

  if(
    !S.ach.includes(a)
  ){

    S.ach.push(a);

    toast(
      '🏆 Achievement unlocked: '+a
    );

    save();

  }

}


function renderAch(){

  achievements.innerHTML =
    S.ach.length

    ?

    S.ach.map(
      a =>
      `<p>🏆 ${a}</p>`
    ).join('')

    :

    '<p class="muted">Play games to unlock achievements.</p>';

}


/* DAILY BONUS */

function daily(){

  let d =
    new Date().toDateString();

  if(
    S.lastDaily===d
  ){

    msg(
      'dailyResult',
      'You already claimed today!'
    );

  }else{

    S.lastDaily=d;

    S.streak++;

    let reward =
      250 +
      S.streak*25;

    add(
      reward,
      true
    );

    msg(
      'dailyResult',
      `🎁 Daily bonus claimed! +${reward} tokens`
    );

  }

  save();

}


function toast(t){

  let e =
    document.getElementById(
      'toast'
    );

  e.textContent=t;

  e.style.display='block';

  setTimeout(
    ()=>{
      e.style.display='none';
    },
    2500
  );

}


buildQuiz();

render();

</script>

</body>
</html>
