<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<meta name="theme-color" content="#f04f91">
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
<meta name="apple-mobile-web-app-title" content="Friendship Casino">

<title>💗 Liliana's Friendship Casino</title>

<style>
:root{
  --bg:#f04f91;
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
  --shadow:0 12px 35px rgba(91,20,55,.20);
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

  background:
    radial-gradient(
      circle at 50% -10%,
      #ffc1dc 0,
      #ff78ad 35%,
      #f04f91 75%
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
  opacity:.55;
  cursor:not-allowed;
}

.hidden{
  display:none!important;
}

/* =========================
   ENTRY SCREEN
========================= */

#entryScreen{
  position:fixed;
  inset:0;
  z-index:9999;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:20px;
  background:
    radial-gradient(circle at 50% 20%,#ffcae1 0,#ff78ad 40%,#d93278 100%);
}

.entryBox{
  width:min(520px,100%);
  padding:42px 28px;
  text-align:center;
  border-radius:32px;
  background:rgba(255,247,251,.95);
  border:2px solid rgba(255,255,255,.8);
  box-shadow:0 25px 70px rgba(84,10,45,.3);
  animation:entryPop .8s ease;
}

@keyframes entryPop{
  from{
    opacity:0;
    transform:scale(.85) translateY(30px);
  }
  to{
    opacity:1;
    transform:none;
  }
}

.entryLogo{
  font-size:68px;
  animation:heartFloat 2s ease-in-out infinite;
}

@keyframes heartFloat{
  0%,100%{transform:translateY(0) rotate(-3deg)}
  50%{transform:translateY(-10px) rotate(3deg)}
}

.entryBox h1{
  margin:12px 0 8px;
  font-size:clamp(30px,8vw,48px);
}

.entryBox p{
  color:var(--muted);
  line-height:1.6;
}

.enterBtn{
  margin-top:20px;
  width:100%;
  padding:17px;
  border:0;
  border-radius:18px;
  background:linear-gradient(135deg,#ff4fa3,#d92f78);
  color:white;
  font-weight:900;
  font-size:18px;
  box-shadow:0 10px 25px rgba(217,47,120,.3);
  transition:.2s;
}

.enterBtn:hover{
  transform:translateY(-3px);
}

/* =========================
   TOP BAR
========================= */

.topbar{
  position:sticky;
  top:0;
  z-index:1000;
  padding:12px 16px;
  background:rgba(85,13,48,.94);
  backdrop-filter:blur(15px);
  color:white;
  box-shadow:0 4px 18px rgba(50,0,25,.25);
}

.topInner{
  max-width:1400px;
  margin:auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:12px;
}

.brand{
  font-size:20px;
  font-weight:900;
  white-space:nowrap;
}

.hud{
  display:flex;
  gap:8px;
  align-items:center;
  flex-wrap:wrap;
  justify-content:flex-end;
}

.hudItem{
  padding:8px 11px;
  border-radius:12px;
  background:rgba(255,255,255,.11);
  font-size:13px;
  white-space:nowrap;
}

.soundButtons{
  display:flex;
  gap:5px;
}

.soundBtn{
  border:1px solid rgba(255,255,255,.2);
  background:rgba(255,255,255,.1);
  color:white;
  border-radius:10px;
  padding:8px 10px;
}

/* =========================
   HERO
========================= */

.hero{
  max-width:1400px;
  margin:25px auto 18px;
  padding:0 16px;
}

.heroCard{
  position:relative;
  overflow:hidden;
  padding:30px;
  border-radius:30px;
  background:
    linear-gradient(135deg,rgba(255,247,251,.98),rgba(255,221,237,.96));
  box-shadow:var(--shadow);
  border:1px solid rgba(255,255,255,.7);
}

.heroCard:before,
.heroCard:after{
  content:"";
  position:absolute;
  border-radius:50%;
  pointer-events:none;
}

.heroCard:before{
  width:260px;
  height:260px;
  right:-80px;
  top:-110px;
  background:rgba(255,79,163,.14);
}

.heroCard:after{
  width:180px;
  height:180px;
  left:-80px;
  bottom:-90px;
  background:rgba(255,255,255,.55);
}

.heroContent{
  position:relative;
  z-index:1;
}

.hero h1{
  margin:0 0 8px;
  font-size:clamp(30px,7vw,55px);
  line-height:1;
}

.hero p{
  max-width:760px;
  color:var(--muted);
  line-height:1.6;
}

.progressWrap{
  margin-top:20px;
  max-width:700px;
}

.progressLabels{
  display:flex;
  justify-content:space-between;
  font-size:13px;
  font-weight:bold;
  margin-bottom:7px;
}

.progress{
  height:15px;
  overflow:hidden;
  border-radius:999px;
  background:#f4bfd4;
}

.progressBar{
  width:0;
  height:100%;
  border-radius:999px;
  background:linear-gradient(90deg,#ff4fa3,#ffb0d2);
  transition:width .5s;
}

/* =========================
   LOBBY
========================= */

.lobby{
  max-width:1400px;
  margin:auto;
  padding:0 16px 50px;
}

.featured{
  display:grid;
  grid-template-columns:1.5fr 1fr 1fr;
  gap:15px;
  margin-bottom:20px;
}

.featureCard{
  min-height:190px;
  position:relative;
  overflow:hidden;
  padding:24px;
  border-radius:26px;
  color:white;
  box-shadow:var(--shadow);
  cursor:pointer;
  transition:.25s;
}

.featureCard:hover{
  transform:translateY(-5px);
}

.featureCard.jackpot{
  background:linear-gradient(135deg,#8e174f,#ff3f93);
}

.featureCard.wheel{
  background:linear-gradient(135deg,#a52c6c,#ff75b5);
}

.featureCard.catch{
  background:linear-gradient(135deg,#176c8e,#39b9d7);
}

.featureCard h2{
  margin:5px 0;
}

.featureEmoji{
  font-size:58px;
}

.jackpotAmount{
  font-size:clamp(28px,5vw,45px);
  font-weight:1000;
  color:#fff1a8;
  text-shadow:0 3px 15px rgba(0,0,0,.3);
}

.categoryGrid{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:12px;
}

.category{
  padding:20px 14px;
  border:2px solid rgba(255,255,255,.6);
  border-radius:22px;
  background:rgba(255,247,251,.94);
  box-shadow:var(--shadow);
  text-align:center;
  transition:.2s;
  cursor:pointer;
}

.category:hover{
  transform:translateY(-4px);
  border-color:var(--pink);
}

.categoryIcon{
  font-size:38px;
}

.category h3{
  margin:8px 0 3px;
}

.category p{
  margin:0;
  color:var(--muted);
  font-size:12px;
}

/* =========================
   ROOMS
========================= */

.roomView{
  display:none;
  max-width:1400px;
  margin:20px auto;
  padding:0 16px 50px;
}

.roomView.active{
  display:block;
  animation:roomIn .35s ease;
}

@keyframes roomIn{
  from{
    opacity:0;
    transform:translateY(15px);
  }
  to{
    opacity:1;
    transform:none;
  }
}

.roomHeader{
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:15px;
  margin-bottom:15px;
}

.roomHeader h2{
  margin:0;
  font-size:clamp(25px,5vw,40px);
}

.backBtn{
  border:0;
  padding:11px 15px;
  border-radius:13px;
  background:#fff7fb;
  color:var(--text);
  font-weight:bold;
  box-shadow:var(--shadow);
}

.gameGrid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:16px;
}

.gameCard{
  background:rgba(255,247,251,.97);
  border:1px solid rgba(255,255,255,.7);
  border-radius:25px;
  padding:20px;
  box-shadow:var(--shadow);
  overflow:hidden;
}

.gameCard h3{
  margin:0 0 8px;
}

.gameCard p{
  color:var(--muted);
  font-size:14px;
  line-height:1.5;
}

.gameIcon{
  font-size:45px;
  margin-bottom:5px;
}

.gameArea{
  margin-top:15px;
  min-height:120px;
  padding:15px;
  border-radius:18px;
  background:#fff0f7;
  border:1px solid var(--border);
}

.playBtn{
  width:100%;
  padding:12px;
  border:0;
  border-radius:13px;
  background:linear-gradient(135deg,#ff4fa3,#d8327b);
  color:white;
  font-weight:900;
  margin-top:10px;
}

.secondaryBtn{
  padding:10px 13px;
  border:0;
  border-radius:11px;
  background:#f8c5da;
  color:var(--text);
  font-weight:bold;
}

/* =========================
   SLOTS
========================= */

.slotMachine{
  background:linear-gradient(145deg,#5b1239,#92184f);
  padding:18px;
  border-radius:20px;
  color:white;
  box-shadow:inset 0 0 0 3px #d997b6;
}

.reels{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:8px;
}

.reel{
  height:85px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:43px;
  border-radius:13px;
  background:#fff;
  color:#4a1832;
  border:4px solid #e6a2c2;
  overflow:hidden;
}

.reel.spinning{
  animation:reelShake .09s linear infinite;
}

@keyframes reelShake{
  0%{transform:translateY(-2px)}
  50%{transform:translateY(3px)}
  100%{transform:translateY(-2px)}
}

.winGlow{
  animation:winGlow .5s ease-in-out infinite alternate;
}

@keyframes winGlow{
  from{box-shadow:0 0 5px #fff}
  to{box-shadow:0 0 30px #ffe27a}
}

/* =========================
   CARDS
========================= */

.cardTable{
  padding:15px;
  border-radius:18px;
  background:radial-gradient(circle,#187b53,#075438);
  color:white;
}

.hand{
  display:flex;
  flex-wrap:wrap;
  gap:7px;
  min-height:65px;
}

.playingCard{
  width:45px;
  height:62px;
  border-radius:7px;
  background:white;
  color:#222;
  display:flex;
  align-items:center;
  justify-content:center;
  font-weight:900;
  box-shadow:0 4px 8px rgba(0,0,0,.2);
  animation:cardDeal .35s ease;
}

@keyframes cardDeal{
  from{
    transform:translateY(-30px) rotate(-10deg);
    opacity:0;
  }
  to{
    transform:none;
    opacity:1;
  }
}

.cardRed{
  color:#d92e52;
}

.cardBack{
  background:linear-gradient(135deg,#e82f78,#70143f);
  color:white;
}

/* =========================
   WHEEL
========================= */

.wheelWrap{
  display:flex;
  justify-content:center;
  align-items:center;
  padding:15px;
}

.wheel{
  width:min(280px,70vw);
  aspect-ratio:1;
  border-radius:50%;
  border:12px solid #fff;
  position:relative;
  background:conic-gradient(
    #ff4fa3 0deg 45deg,
    #ffbf42 45deg 90deg,
    #51c7ff 90deg 135deg,
    #9b5de5 135deg 180deg,
    #ff4fa3 180deg 225deg,
    #ffbf42 225deg 270deg,
    #51c7ff 270deg 315deg,
    #9b5de5 315deg 360deg
  );
  box-shadow:0 10px 25px rgba(0,0,0,.2);
  transition:transform 3.5s cubic-bezier(.1,.7,.15,1);
}

.wheel:after{
  content:"💗";
  position:absolute;
  inset:50% auto auto 50%;
  transform:translate(-50%,-50%);
  width:55px;
  height:55px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:white;
  border-radius:50%;
  box-shadow:0 4px 12px rgba(0,0,0,.25);
}

.pointer{
  width:0;
  height:0;
  border-left:12px solid transparent;
  border-right:12px solid transparent;
  border-top:30px solid #4a1832;
  margin:auto;
  position:relative;
  z-index:3;
}

/* =========================
   RACING
========================= */

.raceControls{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  margin-bottom:12px;
}

.raceTrack{
  position:relative;
  height:370px;
  overflow:hidden;
  border-radius:22px;
  border:4px solid #572038;
  box-shadow:inset 0 0 35px rgba(0,0,0,.25);
}

.horseTrack{
  background:
    repeating-linear-gradient(
      0deg,
      #4d9a49 0,
      #4d9a49 69px,
      #65b65d 70px,
      #65b65d 71px
    );
}

.dolphinTrack{
  background:
    linear-gradient(
      180deg,
      #62d9f5 0,
      #168bb5 55%,
      #075579 100%
    );
}

.raceLane{
  position:absolute;
  left:0;
  right:0;
  height:70px;
  border-bottom:2px dashed rgba(255,255,255,.55);
}

.lane1{top:0}
.lane2{top:70px}
.lane3{top:140px}
.lane4{top:210px}
.lane5{top:280px}

.laneLabel{
  position:absolute;
  left:7px;
  top:7px;
  z-index:2;
  padding:3px 7px;
  border-radius:6px;
  background:rgba(0,0,0,.3);
  color:white;
  font-size:11px;
  font-weight:bold;
}

.finishLine{
  position:absolute;
  right:35px;
  top:0;
  bottom:0;
  width:24px;
  z-index:4;
  background:
    repeating-conic-gradient(#fff 0 25%,#222 0 50%)
    0/24px 24px;
  opacity:.9;
}

.startLine{
  position:absolute;
  left:55px;
  top:0;
  bottom:0;
  width:6px;
  background:white;
  z-index:4;
}

.racer{
  position:absolute;
  left:55px;
  z-index:6;
  width:60px;
  height:60px;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:44px;
  filter:drop-shadow(0 5px 4px rgba(0,0,0,.3));
  transform:translateX(0);
}

.horseRacer{
  animation:horseRun .28s ease-in-out infinite alternate;
}

.dolphinRacer{
  animation:dolphinSwim .7s ease-in-out infinite alternate;
}

@keyframes horseRun{
  from{transform:translateY(-2px) rotate(-2deg)}
  to{transform:translateY(3px) rotate(2deg)}
}

@keyframes dolphinSwim{
  from{transform:translateY(-5px) rotate(-3deg)}
  to{transform:translateY(5px) rotate(3deg)}
}

.oceanBubble{
  position:absolute;
  width:8px;
  height:8px;
  border-radius:50%;
  background:rgba(255,255,255,.65);
  animation:bubbleRise 2.5s linear infinite;
}

@keyframes bubbleRise{
  from{
    transform:translateY(30px);
    opacity:0;
  }
  30%{opacity:1}
  to{
    transform:translateY(-100px);
    opacity:0;
  }
}

.countdown{
  position:absolute;
  inset:0;
  z-index:20;
  display:flex;
  align-items:center;
  justify-content:center;
  font-size:100px;
  font-weight:1000;
  color:white;
  text-shadow:0 6px 25px rgba(0,0,0,.55);
  pointer-events:none;
}

.countdown.go{
  color:#ffe27a;
}

.raceWinner{
  position:absolute;
  inset:0;
  z-index:25;
  display:flex;
  align-items:center;
  justify-content:center;
  flex-direction:column;
  background:rgba(30,0,15,.48);
  color:white;
  text-align:center;
  backdrop-filter:blur(2px);
}

.raceWinner .big{
  font-size:60px;
}

.confetti{
  position:absolute;
  width:9px;
  height:14px;
  top:-20px;
  z-index:30;
  animation:confettiFall 2.5s linear forwards;
}

@keyframes confettiFall{
  to{
    transform:translateY(450px) rotate(720deg);
    opacity:0;
  }
}

.raceStatus{
  margin-top:10px;
  font-weight:bold;
}

/* =========================
   PLINKO
========================= */

.plinkoBoard{
  position:relative;
  height:300px;
  overflow:hidden;
  border-radius:18px;
  background:linear-gradient(#8d5bc7,#e58ac1);
}

.plinkoPeg{
  position:absolute;
  width:8px;
  height:8px;
  background:white;
  border-radius:50%;
}

.plinkoBall{
  position:absolute;
  top:5px;
  left:50%;
  width:20px;
  height:20px;
  margin-left:-10px;
  border-radius:50%;
  background:#ffd75a;
  box-shadow:0 3px 10px rgba(0,0,0,.3);
}

/* =========================
   CATCH GAME
========================= */

.catchScene{
  min-height:250px;
  position:relative;
  overflow:hidden;
  border-radius:18px;
  background:
    linear-gradient(#74dcf3 0,#259fc5 55%,#0a6588 100%);
}

.catchCreature{
  position:absolute;
  font-size:65px;
  left:50%;
  top:45%;
  transform:translate(-50%,-50%);
  animation:creatureFloat 1.8s ease-in-out infinite;
}

@keyframes creatureFloat{
  0%,100%{transform:translate(-50%,-50%) rotate(-3deg)}
  50%{transform:translate(-50%,-58%) rotate(3deg)}
}

.catchBall{
  position:absolute;
  bottom:25px;
  left:50%;
  font-size:38px;
  transform:translateX(-50%);
  transition:all .7s cubic-bezier(.2,.8,.3,1);
}

.catchBall.throw{
  left:50%;
  top:45%;
  bottom:auto;
  transform:translate(-50%,-50%) scale(.7);
}

.catchBall.shake{
  animation:captureShake .35s ease-in-out 3;
}

@keyframes captureShake{
  0%,100%{transform:translate(-50%,-50%) rotate(0)}
  25%{transform:translate(-60%,-50%) rotate(-12deg)}
  75%{transform:translate(-40%,-50%) rotate(12deg)}
}

/* =========================
   MINI GAMES
========================= */

.choiceRow{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
}

.bigNumber{
  font-size:55px;
  font-weight:1000;
  text-align:center;
  padding:10px;
}

.diceArea{
  display:flex;
  justify-content:center;
  gap:20px;
  padding:20px;
}

.die{
  width:65px;
  height:65px;
  display:flex;
  align-items:center;
  justify-content:center;
  border-radius:13px;
  background:white;
  font-size:35px;
  box-shadow:0 6px 12px rgba(0,0,0,.18);
}

.rolling{
  animation:diceRoll .25s linear infinite;
}

@keyframes diceRoll{
  0%{transform:rotate(0) scale(1)}
  50%{transform:rotate(180deg) scale(1.1)}
  100%{transform:rotate(360deg) scale(1)}
}

.boxRow{
  display:flex;
  justify-content:center;
  gap:10px;
  flex-wrap:wrap;
}

.mysteryBox{
  width:75px;
  height:75px;
  border:0;
  border-radius:15px;
  background:linear-gradient(#ff77b7,#c92872);
  font-size:35px;
  transition:.25s;
}

.mysteryBox:hover{
  transform:translateY(-5px) rotate(2deg);
}

.cup{
  width:70px;
  height:70px;
  border:0;
  border-radius:50% 50% 15px 15px;
  background:linear-gradient(#fff,#ffc1dc);
  font-size:30px;
  transition:.3s;
}

.cup.shuffle{
  animation:cupShuffle .35s ease-in-out infinite alternate;
}

@keyframes cupShuffle{
  from{transform:translateX(-12px) rotate(-4deg)}
  to{transform:translateX(12px) rotate(4deg)}
}

.scratch{
  padding:30px;
  border-radius:15px;
  text-align:center;
  background:linear-gradient(135deg,#c8c8c8,#f5f5f5);
  cursor:pointer;
  font-weight:1000;
  font-size:20px;
}

/* =========================
   QUIZ / LETTER / TIMELINE
========================= */

.quizQuestion{
  font-weight:900;
  font-size:18px;
  margin-bottom:12px;
}

.quizOptions{
  display:grid;
  gap:8px;
}

.quizOption{
  padding:12px;
  border:2px solid var(--border);
  background:white;
  color:var(--text);
  border-radius:12px;
  text-align:left;
  font-weight:bold;
}

.quizOption.selected{
  background:#ffd1e3;
  border-color:var(--pink);
}

.timeline{
  position:relative;
  margin:20px 0;
  padding-left:25px;
  border-left:4px solid var(--pink);
}

.timelineItem{
  position:relative;
  margin-bottom:25px;
  padding:15px;
  border-radius:15px;
  background:#fff;
}

.timelineItem:before{
  content:"";
  position:absolute;
  left:-36px;
  top:18px;
  width:17px;
  height:17px;
  border-radius:50%;
  background:var(--pink);
  border:4px solid #fff;
}

.letter{
  padding:24px;
  border-radius:20px;
  background:
    linear-gradient(135deg,#fff,#fff0f7);
  line-height:1.8;
  font-family:Georgia,serif;
  font-size:16px;
}

/* =========================
   VAULT
========================= */

.vault{
  text-align:center;
  padding:30px 20px;
  border-radius:25px;
  background:linear-gradient(135deg,#4d1640,#180a25);
  color:white;
}

.vaultLock{
  font-size:75px;
  animation:lockFloat 2s ease-in-out infinite;
}

@keyframes lockFloat{
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-8px)}
}

.vaultInput{
  max-width:260px;
  padding:14px;
  border:0;
  border-radius:12px;
  text-align:center;
  letter-spacing:7px;
  font-size:22px;
  margin:15px auto;
  display:block;
}

/* =========================
   ACHIEVEMENTS
========================= */

.achievementGrid{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:10px;
}

.achievement{
  padding:14px;
  border-radius:15px;
  background:#fff;
  border:2px solid #eee;
  opacity:.45;
}

.achievement.unlocked{
  opacity:1;
  border-color:#ffb7d4;
  box-shadow:0 5px 15px rgba(255,79,163,.15);
}

/* =========================
   TOAST
========================= */

#toast{
  position:fixed;
  left:50%;
  bottom:25px;
  z-index:10000;
  transform:translateX(-50%) translateY(30px);
  opacity:0;
  pointer-events:none;
  padding:14px 20px;
  border-radius:15px;
  background:#4a1832;
  color:white;
  box-shadow:0 12px 30px rgba(0,0,0,.25);
  transition:.3s;
  max-width:90%;
  text-align:center;
  font-weight:bold;
}

#toast.show{
  opacity:1;
  transform:translateX(-50%) translateY(0);
}

/* =========================
   MOBILE
========================= */

@media(max-width:1050px){
  .featured{
    grid-template-columns:1fr 1fr;
  }

  .featured .jackpot{
    grid-column:1/-1;
  }

  .categoryGrid{
    grid-template-columns:repeat(3,1fr);
  }

  .gameGrid{
    grid-template-columns:repeat(2,1fr);
  }
}

@media(max-width:700px){
  .topInner{
    align-items:flex-start;
    flex-direction:column;
  }

  .hud{
    justify-content:flex-start;
  }

  .heroCard{
    padding:22px;
  }

  .featured{
    grid-template-columns:1fr;
  }

  .featured .jackpot{
    grid-column:auto;
  }

  .categoryGrid{
    grid-template-columns:repeat(2,1fr);
  }

  .gameGrid{
    grid-template-columns:1fr;
  }

  .raceTrack{
    height:340px;
  }

  .racer{
    font-size:34px;
    width:50px;
  }

  .countdown{
    font-size:75px;
  }

  .finishLine{
    right:18px;
  }
}

@media(max-width:430px){
  .brand{
    font-size:17px;
  }

  .hudItem{
    font-size:11px;
    padding:7px 8px;
  }

  .categoryGrid{
    grid-template-columns:1fr 1fr;
  }

  .featureCard{
    min-height:160px;
  }

  .raceTrack{
    height:320px;
  }

  .lane1{top:0}
  .lane2{top:62px}
  .lane3{top:124px}
  .lane4{top:186px}
  .lane5{top:248px}

  .raceLane{
    height:62px;
  }
}
</style>
</head>

<body>

<!-- =========================
     ENTRY
========================= -->

<div id="entryScreen">
  <div class="entryBox">
    <div class="entryLogo">🎰💗</div>
    <h1>Liliana's Friendship Casino</h1>
    <p>
      Six years of friendship, turned into one ridiculous little casino.
      Play the games, collect Friendship Tokens and see how well you know Liliana.
    </p>
    <button class="enterBtn" onclick="enterCasino()">
      🎰 ENTER THE CASINO
    </button>
    <p style="font-size:12px;margin-top:15px">
      Friendship Tokens have no real monetary value.
    </p>
  </div>
</div>

<!-- =========================
     TOP BAR
========================= -->

<header class="topbar">
  <div class="topInner">

    <div class="brand">
      💗 Liliana's Friendship Casino
    </div>

    <div class="hud">

      <div class="hudItem">
        💰 <span id="tokenDisplay">1,000</span>
      </div>

      <div class="hudItem">
        ⭐ Lv. <span id="levelDisplay">1</span>
      </div>

      <div class="hudItem">
        🔥 <span id="streakDisplay">0</span>
      </div>

      <div class="hudItem">
        🏆 <span id="winsDisplay">0</span>
      </div>

      <div class="soundButtons">
        <button class="soundBtn" id="musicBtn" onclick="toggleMusic()">
          🎵 Music
        </button>

        <button class="soundBtn" id="soundBtn" onclick="toggleSound()">
          🔊 SFX
        </button>
      </div>

    </div>
  </div>
</header>

<!-- =========================
     HERO
========================= -->

<section class="hero">

  <div class="heroCard">

    <div class="heroContent">

      <h1>🎰 Welcome to the Friendship Casino</h1>

      <p>
        A completely fictional casino made for one very special best friend.
        Spin, race, gamble your Friendship Tokens and unlock Liliana's secrets.
      </p>

      <div class="progressWrap">

        <div class="progressLabels">
          <span>Friendship Level <span id="heroLevel">1</span></span>
          <span><span id="xpDisplay">0</span> XP</span>
        </div>

        <div class="progress">
          <div class="progressBar" id="xpBar"></div>
        </div>

      </div>

      <button
        class="playBtn"
        style="max-width:260px"
        onclick="dailyBonus()">
        🎁 Claim Daily Bonus
      </button>

    </div>
  </div>

</section>

<!-- =========================
     LOBBY
========================= -->

<main class="lobby" id="lobby">

  <div class="featured">

    <div
      class="featureCard jackpot"
      onclick="openRoom('slots')">

      <div class="featureEmoji">💎🎰</div>
      <h2>MEGA JACKPOT</h2>
      <div class="jackpotAmount">1,000,000</div>
      <p>Hit three diamonds to enter the Friendship Casino Hall of Fame.</p>

    </div>

    <div
      class="featureCard wheel"
      onclick="openRoom('lucky')">

      <div class="featureEmoji">🎡</div>
      <h2>Lucky Lounge</h2>
      <p>Spin the wheel and try your luck.</p>

    </div>

    <div
      class="featureCard catch"
      onclick="openRoom('catch')">

      <div class="featureEmoji">🐬</div>
      <h2>Friendship Catch</h2>
      <p>Catch all seven friendship creatures.</p>

    </div>

  </div>

  <div class="categoryGrid">

    <div class="category" onclick="openRoom('slots')">
      <div class="categoryIcon">🎰</div>
      <h3>Slots</h3>
      <p>5 machines</p>
    </div>

    <div class="category" onclick="openRoom('cards')">
      <div class="categoryIcon">🃏</div>
      <h3>Card Room</h3>
      <p>6 games</p>
    </div>

    <div class="category" onclick="openRoom('lucky')">
      <div class="categoryIcon">🎡</div>
      <h3>Lucky Lounge</h3>
      <p>6 games</p>
    </div>

    <div class="category" onclick="openRoom('races')">
      <div class="categoryIcon">🏇</div>
      <h3>Derby Track</h3>
      <p>2 races</p>
    </div>

    <div class="category" onclick="openRoom('arcade')">
      <div class="categoryIcon">🎁</div>
      <h3>Prize Arcade</h3>
      <p>8 games</p>
    </div>

    <div class="category" onclick="openRoom('catch')">
      <div class="categoryIcon">🐬</div>
      <h3>Friendship Catch</h3>
      <p>7 creatures</p>
    </div>

    <div class="category" onclick="openRoom('corner')">
      <div class="categoryIcon">💗</div>
      <h3>Liliana's Corner</h3>
      <p>Quiz & memories</p>
    </div>

    <div class="category" onclick="openRoom('vault')">
      <div class="categoryIcon">🔐</div>
      <h3>VIP Vault</h3>
      <p>Secret room</p>
    </div>

    <div class="category" onclick="openRoom('achievements')">
      <div class="categoryIcon">🏆</div>
      <h3>Achievements</h3>
      <p>Collect them all</p>
    </div>

    <div class="category" onclick="openRoom('corner')">
      <div class="categoryIcon">💌</div>
      <h3>Friendship</h3>
      <p>Six years</p>
    </div>

  </div>

</main>

<!-- =========================
     SLOTS ROOM
========================= -->

<section class="roomView" id="room-slots">

  <div class="roomHeader">
    <h2>🎰 Slots Room</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard">
      <div class="gameIcon">🐃</div>
      <h3>Buffalo Stampede</h3>
      <p>Spin for a chance at 5,000 Friendship Tokens.</p>
      <div class="gameArea">
        <div id="buffaloGame"></div>
        <button class="playBtn" onclick="spinSlot('buffalo')">SPIN</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">💗</div>
      <h3>Pink Palace</h3>
      <p>A glamorous pink slot machine.</p>
      <div class="gameArea">
        <div id="pinkGame"></div>
        <button class="playBtn" onclick="spinSlot('pink')">SPIN</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🐬</div>
      <h3>Dolphin Riches</h3>
      <p>Swim into a jackpot of 8,000.</p>
      <div class="gameArea">
        <div id="dolphinGame"></div>
        <button class="playBtn" onclick="spinSlot('dolphin')">SPIN</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">7️⃣</div>
      <h3>Fancy 7s</h3>
      <p>Classic lucky sevens.</p>
      <div class="gameArea">
        <div id="sevensGame"></div>
        <button class="playBtn" onclick="spinSlot('sevens')">SPIN</button>
      </div>
    </div>

    <div class="gameCard" style="grid-column:span 2">
      <div class="gameIcon">💎</div>
      <h3>MEGA JACKPOT</h3>
      <p>Three diamonds = 1,000,000 Friendship Tokens.</p>
      <div class="gameArea">
        <div id="megaGame"></div>
        <button class="playBtn" onclick="spinSlot('mega')">
          💎 SPIN FOR 1,000,000
        </button>
      </div>
    </div>

  </div>
</section>

<!-- =========================
     CARD ROOM
========================= -->

<section class="roomView" id="room-cards">

  <div class="roomHeader">
    <h2>🃏 Card Room</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard">
      <div class="gameIcon">♠️</div>
      <h3>Poker vs Computer</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div>Computer</div>
          <div class="hand" id="pokerComputer"></div>
          <hr>
          <div>You</div>
          <div class="hand" id="pokerPlayer"></div>
        </div>
        <button class="playBtn" onclick="playPoker()">DEAL POKER</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🂡</div>
      <h3>Blackjack</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div>Dealer</div>
          <div class="hand" id="dealerHand"></div>
          <div id="dealerTotal"></div>
          <hr>
          <div>You</div>
          <div class="hand" id="blackjackHand"></div>
          <div id="blackjackTotal"></div>
        </div>

        <div class="choiceRow">
          <button class="secondaryBtn" onclick="blackjackHit()">Hit</button>
          <button class="secondaryBtn" onclick="blackjackStand()">Stand</button>
          <button class="secondaryBtn" onclick="blackjackDouble()">Double</button>
        </div>

        <button class="playBtn" onclick="startBlackjack()">NEW HAND</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">♦️</div>
      <h3>Baccarat</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div id="baccaratArea">Choose your side.</div>
        </div>
        <div class="choiceRow">
          <button class="secondaryBtn" onclick="playBaccarat('Player')">Player</button>
          <button class="secondaryBtn" onclick="playBaccarat('Banker')">Banker</button>
          <button class="secondaryBtn" onclick="playBaccarat('Tie')">Tie</button>
        </div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">⚔️</div>
      <h3>War</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div class="hand" id="warArea"></div>
        </div>
        <button class="playBtn" onclick="playWar()">PLAY WAR</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🃏</div>
      <h3>Gin Rummy</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div class="hand" id="ginArea"></div>
        </div>
        <button class="playBtn" onclick="playGin()">DEAL HAND</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">♣️</div>
      <h3>Texas Hold'em</h3>
      <div class="gameArea">
        <div class="cardTable">
          <div>Community</div>
          <div class="hand" id="holdemBoard"></div>
          <hr>
          <div>Your Hand</div>
          <div class="hand" id="holdemPlayer"></div>
        </div>
        <button class="playBtn" onclick="playHoldem()">DEAL HAND</button>
      </div>
    </div>

  </div>
</section>

<!-- =========================
     LUCKY ROOM
========================= -->

<section class="roomView" id="room-lucky">

  <div class="roomHeader">
    <h2>🎡 Lucky Lounge</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard">
      <div class="gameIcon">🎡</div>
      <h3>Lucky Wheel</h3>
      <div class="gameArea">
        <div class="pointer"></div>
        <div class="wheelWrap">
          <div class="wheel" id="luckyWheel"></div>
        </div>
        <button class="playBtn" onclick="spinWheel()">SPIN WHEEL</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🔴</div>
      <h3>Friendship Roulette</h3>
      <div class="gameArea">
        <div class="bigNumber" id="rouletteResult">?</div>
        <div class="choiceRow">
          <button class="secondaryBtn" onclick="playRoulette('red')">🔴 Red</button>
          <button class="secondaryBtn" onclick="playRoulette('black')">⚫ Black</button>
          <button class="secondaryBtn" onclick="playRoulette('green')">🟢 Green</button>
        </div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🎲</div>
      <h3>Craps</h3>
      <div class="gameArea">
        <div class="diceArea">
          <div class="die" id="die1">?</div>
          <div class="die" id="die2">?</div>
        </div>
        <button class="playBtn" onclick="playCraps()">ROLL DICE</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">📈</div>
      <h3>Hi-Lo</h3>
      <div class="gameArea">
        <div class="bigNumber" id="hiloCard">?</div>
        <div class="choiceRow">
          <button class="secondaryBtn" onclick="playHiLo('higher')">Higher</button>
          <button class="secondaryBtn" onclick="playHiLo('lower')">Lower</button>
        </div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🪙</div>
      <h3>Coin Flip</h3>
      <div class="gameArea">
        <div class="bigNumber" id="coinResult">🪙</div>
        <div class="choiceRow">
          <button class="secondaryBtn" onclick="coinFlip('heads')">Heads</button>
          <button class="secondaryBtn" onclick="coinFlip('tails')">Tails</button>
        </div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🟣</div>
      <h3>Plinko</h3>
      <div class="gameArea">
        <div class="plinkoBoard" id="plinkoBoard"></div>
        <button class="playBtn" onclick="playPlinko()">DROP BALL</button>
      </div>
    </div>

  </div>
</section>

<!-- =========================
     RACE ROOM
========================= -->

<section class="roomView" id="room-races">

  <div class="roomHeader">
    <h2>🏇 Derby Track</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard" style="grid-column:1/-1">
      <div class="gameIcon">🐎</div>
      <h3>Horse Derby</h3>
      <p>
        Pick a horse and watch the entire race unfold.
      </p>

      <div class="raceControls" id="horseChoices"></div>

      <div class="raceTrack horseTrack" id="horseTrack">

        <div class="startLine"></div>
        <div class="finishLine"></div>

        <div class="raceLane lane1"><span class="laneLabel">1</span></div>
        <div class="raceLane lane2"><span class="laneLabel">2</span></div>
        <div class="raceLane lane3"><span class="laneLabel">3</span></div>
        <div class="raceLane lane4"><span class="laneLabel">4</span></div>
        <div class="raceLane lane5"><span class="laneLabel">5</span></div>

        <div id="horseRacers"></div>
        <div id="horseCountdown"></div>

      </div>

      <div class="raceStatus" id="horseStatus">
        Choose your horse.
      </div>

      <button class="playBtn" id="horseStart" onclick="startRace('horse')">
        🏁 START HORSE DERBY
      </button>
    </div>

    <div class="gameCard" style="grid-column:1/-1">
      <div class="gameIcon">🐬</div>
      <h3>Dolphin Derby</h3>
      <p>
        Watch five dolphins race through the ocean.
      </p>

      <div class="raceControls" id="dolphinChoices"></div>

      <div class="raceTrack dolphinTrack" id="dolphinTrack">

        <div class="startLine"></div>
        <div class="finishLine"></div>

        <div class="raceLane lane1"><span class="laneLabel">1</span></div>
        <div class="raceLane lane2"><span class="laneLabel">2</span></div>
        <div class="raceLane lane3"><span class="laneLabel">3</span></div>
        <div class="raceLane lane4"><span class="laneLabel">4</span></div>
        <div class="raceLane lane5"><span class="laneLabel">5</span></div>

        <div id="dolphinBubbles"></div>
        <div id="dolphinRacers"></div>
        <div id="dolphinCountdown"></div>

      </div>

      <div class="raceStatus" id="dolphinStatus">
        Choose your dolphin.
      </div>

      <button class="playBtn" id="dolphinStart" onclick="startRace('dolphin')">
        🌊 START DOLPHIN DERBY
      </button>
    </div>

  </div>
</section>

<!-- =========================
     ARCADE
========================= -->

<section class="roomView" id="room-arcade">

  <div class="roomHeader">
    <h2>🎁 Prize Arcade</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard">
      <div class="gameIcon">🎁</div>
      <h3>Mystery Boxes</h3>
      <div class="gameArea">
        <div class="boxRow">
          <button class="mysteryBox" onclick="openBox(0)">🎁</button>
          <button class="mysteryBox" onclick="openBox(1)">🎁</button>
          <button class="mysteryBox" onclick="openBox(2)">🎁</button>
        </div>
        <div id="boxResult"></div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🥤</div>
      <h3>Three Cups</h3>
      <div class="gameArea">
        <div class="boxRow" id="cups">
          <button class="cup" onclick="chooseCup(0)">🥤</button>
          <button class="cup" onclick="chooseCup(1)">🥤</button>
          <button class="cup" onclick="chooseCup(2)">🥤</button>
        </div>
        <button class="playBtn" onclick="shuffleCups()">SHUFFLE CUPS</button>
        <div id="cupResult"></div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">💗</div>
      <h3>Heart Scratch Card</h3>
      <div class="gameArea">
        <div class="scratch" onclick="scratchCard(this)">
          💗 SCRATCH ME 💗
        </div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🎯</div>
      <h3>Lucky Darts</h3>
      <div class="gameArea">
        <div class="bigNumber" id="dartBoard">🎯</div>
        <button class="playBtn" onclick="throwDart()">THROW DART</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">💎</div>
      <h3>Gem Heist</h3>
      <div class="gameArea">
        <div class="bigNumber" id="gemVault">🔐</div>
        <button class="playBtn" onclick="gemHeist()">BREAK THE VAULT</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">✉️</div>
      <h3>Lucky Envelopes</h3>
      <div class="gameArea">
        <div class="boxRow">
          <button class="mysteryBox" onclick="openEnvelope(0)">✉️</button>
          <button class="mysteryBox" onclick="openEnvelope(1)">✉️</button>
          <button class="mysteryBox" onclick="openEnvelope(2)">✉️</button>
        </div>
        <div id="envelopeResult"></div>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🔢</div>
      <h3>Lucky Number</h3>
      <div class="gameArea">
        <div class="bigNumber" id="luckyNumberDisplay">?</div>
        <input
          id="luckyGuess"
          type="number"
          min="1"
          max="10"
          placeholder="1 to 10"
          style="width:100%;padding:12px;border:1px solid var(--border);border-radius:10px"
        >
        <button class="playBtn" onclick="luckyNumber()">DRAW NUMBER</button>
      </div>
    </div>

    <div class="gameCard">
      <div class="gameIcon">🌊</div>
      <h3>Ocean Treasure</h3>
      <div class="gameArea">
        <div class="bigNumber" id="treasureChest">🌊</div>
        <button class="playBtn" onclick="oceanTreasure()">SEARCH OCEAN</button>
      </div>
    </div>

  </div>
</section>

<!-- =========================
     CATCH
========================= -->

<section class="roomView" id="room-catch">

  <div class="roomHeader">
    <h2>🐬 Friendship Catch</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard" style="grid-column:1/-1">

      <div class="gameIcon">🐾</div>

      <h3>Catch the Friendship Creatures</h3>

      <p>
        Find all seven original Friendship creatures.
      </p>

      <div class="catchScene" id="catchScene">

        <div class="catchCreature" id="catchCreature">
          🐬
        </div>

        <div class="catchBall" id="catchBall">
          💗
        </div>

      </div>

      <button class="playBtn" onclick="startCatch()">
        💗 THROW CATCH HEART
      </button>

      <div id="catchResult"></div>

      <hr>

      <h3>Your Collection</h3>

      <div id="collection"></div>

    </div>

  </div>
</section>

<!-- =========================
     LILIANA CORNER
========================= -->

<section class="roomView" id="room-corner">

  <div class="roomHeader">
    <h2>💗 Liliana's Corner</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameGrid">

    <div class="gameCard" style="grid-column:1/-1">

      <div class="gameIcon">🧠</div>

      <h3>How Well Do You Know Liliana?</h3>

      <p>
        There are no answers displayed. You have to actually know her.
      </p>

      <div id="quizArea"></div>

    </div>

    <div class="gameCard">

      <div class="gameIcon">✨</div>

      <h3>Liliana Personality Test</h3>

      <p>Choose what feels most like her.</p>

      <div id="personalityArea"></div>

    </div>

    <div class="gameCard">

      <div class="gameIcon">🕰️</div>

      <h3>Six Years Together</h3>

      <div class="timeline">

        <div class="timelineItem">
          <strong>Year 1</strong>
          <p>The beginning of the friendship.</p>
        </div>

        <div class="timelineItem">
          <strong>Year 2</strong>
          <p>More memories, more chaos.</p>
        </div>

        <div class="timelineItem">
          <strong>Year 3</strong>
          <p>The friendship got stronger.</p>
        </div>

        <div class="timelineItem">
          <strong>Year 4</strong>
          <p>Still here. Still laughing.</p>
        </div>

        <div class="timelineItem">
          <strong>Year 5</strong>
          <p>Five years of friendship.</p>
        </div>

        <div class="timelineItem">
          <strong>Year 6</strong>
          <p>Six years and counting. 💗</p>
        </div>

      </div>

    </div>

    <div class="gameCard" style="grid-column:1/-1">

      <div class="gameIcon">💌</div>

      <h3>Friendship Letter</h3>

      <div class="letter">

        Liliana,

        <br><br>

        Six years of friendship is a ridiculous amount of memories,
        laughter, chaos and moments that I wouldn't trade for anything.

        <br><br>

        You're one of those people who can make an ordinary day feel
        completely different just by being there.

        <br><br>

        So this little ridiculous casino exists because apparently
        six years of friendship deserved something equally ridiculous.

        <br><br>

        Here's to every memory we've already made and all the ones
        still waiting for us.

        <br><br>

        Six years down.

        <br>

        Many more to go. 💗

        <br><br>

        Love always,<br>
        Your bestie

      </div>

    </div>

  </div>
</section>

<!-- =========================
     VAULT
========================= -->

<section class="roomView" id="room-vault">

  <div class="roomHeader">
    <h2>🔐 VIP Vault</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="vault">

    <div class="vaultLock">🔐</div>

    <h2>VIP FRIENDSHIP VAULT</h2>

    <p>
      Six digits stand between you and the secret reward.
    </p>

    <input
      id="vaultInput"
      class="vaultInput"
      maxlength="6"
      inputmode="numeric"
      placeholder="••••••"
    >

    <button class="playBtn" style="max-width:260px" onclick="openVault()">
      UNLOCK
    </button>

    <div id="vaultResult"></div>

  </div>

</section>

<!-- =========================
     ACHIEVEMENTS
========================= -->

<section class="roomView" id="room-achievements">

  <div class="roomHeader">
    <h2>🏆 Achievements</h2>
    <button class="backBtn" onclick="closeRooms()">← Casino Lobby</button>
  </div>

  <div class="gameCard">

    <div class="achievementGrid" id="achievementGrid"></div>

  </div>

</section>

<div id="toast"></div>

<script>

/* =========================================================
   STATE
========================================================= */

const DEFAULT_STATE = {
  tokens:1000,
  xp:0,
  streak:0,
  wins:0,
  played:0,
  biggest:0,
  sound:true,
  music:true,
  lastDaily:"",
  vaultOpened:false,
  caught:[],
  achievements:[],
  quizBest:0
};

let S = {
  ...DEFAULT_STATE,
  ...(JSON.parse(localStorage.getItem("lilianaCasino") || "null") || {})
};

function save(){
  localStorage.setItem("lilianaCasino",JSON.stringify(S));
}

function format(n){
  return Number(n || 0).toLocaleString();
}

function level(){
  return Math.floor(S.xp / 1000) + 1;
}

/* =========================================================
   AUDIO ENGINE
========================================================= */

let audioCtx = null;
let musicTimer = null;
let musicPlaying = false;

function ensureAudio(){
  if(!audioCtx){
    audioCtx = new (window.AudioContext || window.webkitAudioContext)();
  }

  if(audioCtx.state === "suspended"){
    audioCtx.resume();
  }
}

function tone(freq,duration=.12,type="sine",volume=.06,delay=0){

  if(!S.sound) return;

  ensureAudio();

  const osc = audioCtx.createOscillator();
  const gain = audioCtx.createGain();

  osc.type = type;
  osc.frequency.value = freq;

  gain.gain.setValueAtTime(0.0001,audioCtx.currentTime+delay);
  gain.gain.exponentialRampToValueAtTime(
    volume,
    audioCtx.currentTime+delay+.01
  );

  gain.gain.exponentialRampToValueAtTime(
    0.0001,
    audioCtx.currentTime+delay+duration
  );

  osc.connect(gain);
  gain.connect(audioCtx.destination);

  osc.start(audioCtx.currentTime+delay);
  osc.stop(audioCtx.currentTime+delay+duration+.02);
}

function soundEffect(type){

  if(!S.sound) return;

  switch(type){

    case "click":
      tone(500,.07,"square",.04);
      break;

    case "spin":
      for(let i=0;i<7;i++){
        tone(220+i*55,.06,"square",.035,i*.07);
      }
      break;

    case "card":
      tone(350,.08,"triangle",.04);
      tone(500,.08,"triangle",.03,.08);
      break;

    case "dice":
      tone(180,.08,"square",.05);
      tone(280,.08,"square",.04,.1);
      tone(390,.08,"square",.03,.2);
      break;

    case "win":
      tone(523,.12,"triangle",.07);
      tone(659,.12,"triangle",.07,.12);
      tone(784,.2,"triangle",.09,.24);
      break;

    case "bigwin":
      tone(523,.12,"triangle",.08);
      tone(659,.12,"triangle",.08,.12);
      tone(784,.12,"triangle",.08,.24);
      tone(1046,.35,"triangle",.1,.36);
      break;

    case "lose":
      tone(220,.2,"sawtooth",.045);
      tone(160,.3,"sawtooth",.035,.15);
      break;

    case "race":
      tone(300,.08,"square",.05);
      break;

    case "go":
      tone(523,.1,"square",.06);
      tone(784,.3,"square",.08,.1);
      break;

    case "coin":
      tone(650,.07,"triangle",.04);
      tone(800,.07,"triangle",.04,.08);
      tone(950,.1,"triangle",.04,.16);
      break;

    case "catch":
      tone(500,.1,"triangle",.05);
      tone(700,.1,"triangle",.05,.1);
      tone(900,.2,"triangle",.07,.2);
      break;
  }
}

/* =========================================================
   GENERATED CASINO MUSIC
========================================================= */

function startMusic(){

  if(!S.music || musicPlaying) return;

  ensureAudio();

  musicPlaying = true;

  const notes = [
    261.63,
    329.63,
    392.00,
    329.63,
    293.66,
    349.23,
    440.00,
    349.23
  ];

  let i=0;

  function beat(){

    if(!musicPlaying || !S.music) return;

    tone(notes[i % notes.length],.18,"triangle",.018);
    tone(notes[(i+2) % notes.length]/2,.25,"sine",.012,.02);

    i++;

    musicTimer = setTimeout(beat,520);
  }

  beat();
}

function stopMusic(){

  musicPlaying = false;

  if(musicTimer){
    clearTimeout(musicTimer);
    musicTimer = null;
  }
}

function toggleMusic(){

  S.music = !S.music;

  if(S.music){
    startMusic();
    toast("🎵 Casino music ON");
  }else{
    stopMusic();
    toast("🔇 Casino music OFF");
  }

  update();
  save();
}

function toggleSound(){

  S.sound = !S.sound;

  toast(S.sound ? "🔊 Sound effects ON" : "🔇 Sound effects OFF");

  update();
  save();
}

function enterCasino(){

  ensureAudio();
  startMusic();

  document.getElementById("entryScreen").classList.add("hidden");

  soundEffect("win");

  toast("🎰 Welcome to Liliana's Friendship Casino!");

  update();
}

/* =========================================================
   UI
========================================================= */

function toast(message){

  const el=document.getElementById("toast");

  el.textContent=message;
  el.classList.add("show");

  clearTimeout(window.toastTimer);

  window.toastTimer=setTimeout(()=>{
    el.classList.remove("show");
  },2800);
}

function update(){

  document.getElementById("tokenDisplay").textContent=format(S.tokens);
  document.getElementById("levelDisplay").textContent=level();
  document.getElementById("heroLevel").textContent=level();
  document.getElementById("xpDisplay").textContent=format(S.xp);
  document.getElementById("streakDisplay").textContent=S.streak;
  document.getElementById("winsDisplay").textContent=S.wins;

  const xpInLevel=S.xp % 1000;

  document.getElementById("xpBar").style.width =
    xpInLevel/10+"%";

  document.getElementById("musicBtn").textContent =
    S.music ? "🎵 Music" : "🔇 Music";

  document.getElementById("soundBtn").textContent =
    S.sound ? "🔊 SFX" : "🔇 SFX";

  renderAchievements();
  renderCollection();

  save();
}

function add(amount,win=false){

  S.tokens=Math.max(0,S.tokens+amount);

  S.played++;

  S.xp += Math.max(10,Math.abs(amount));

  if(win){
    S.wins++;
    S.streak++;
  }else{
    S.streak=0;
  }

  if(amount>S.biggest){
    S.biggest=amount;
  }

  if(S.tokens>=10000){
    achievement("tenK");
  }

  if(S.tokens>=1000000){
    achievement("million");
  }

  update();
}

/* =========================================================
   ACHIEVEMENTS
========================================================= */

const achievementData = {

  firstSpin:["🎰","First Spin","Play your first slot."],

  firstWin:["🏆","First Win","Win your first game."],

  tenK:["💰","10K Club","Reach 10,000 tokens."],

  million:["💎","Million Token Club","Reach 1,000,000 tokens."],

  collector:["🐾","Collector","Catch every creature."],

  expert:["🧠","Liliana Expert","Get 20/20 on the quiz."],

  vault:["🔐","Vault Keeper","Open the VIP Vault."],

  regular:["🎰","Casino Regular","Play 25 games."],

  royalty:["👑","Friendship Royalty","Reach level 10."]
};

function achievement(id){

  if(!achievementData[id]) return;

  if(S.achievements.includes(id)) return;

  S.achievements.push(id);

  soundEffect("win");

  toast(
    "🏆 Achievement unlocked: "+
    achievementData[id][1]
  );

  update();
}

function renderAchievements(){

  const grid=document.getElementById("achievementGrid");

  if(!grid) return;

  grid.innerHTML="";

  Object.entries(achievementData).forEach(([id,data])=>{

    const unlocked=S.achievements.includes(id);

    const div=document.createElement("div");

    div.className="achievement"+
      (unlocked?" unlocked":"");

    div.innerHTML=`
      <div style="font-size:30px">${data[0]}</div>
      <strong>${data[1]}</strong>
      <p style="margin:5px 0 0;color:var(--muted);font-size:12px">
        ${data[2]}
      </p>
    `;

    grid.appendChild(div);
  });

  if(S.played>=25){
    achievement("regular");
  }

  if(level()>=10){
    achievement("royalty");
  }
}

/* =========================================================
   ROOMS
========================================================= */

function openRoom(room){

  document.getElementById("lobby").style.display="none";

  document.querySelectorAll(".roomView")
    .forEach(r=>r.classList.remove("active"));

  document
    .getElementById("room-"+room)
    .classList.add("active");

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

  soundEffect("click");
}

function closeRooms(){

  document.querySelectorAll(".roomView")
    .forEach(r=>r.classList.remove("active"));

  document.getElementById("lobby").style.display="block";

  window.scrollTo({
    top:0,
    behavior:"smooth"
  });

  soundEffect("click");
}

/* =========================================================
   DAILY BONUS
========================================================= */

function dailyBonus(){

  const today=new Date().toISOString().slice(0,10);

  if(S.lastDaily===today){

    toast("🎁 You already claimed today's bonus!");

    return;
  }

  S.lastDaily=today;

  add(500,true);

  achievement("firstWin");

  toast("🎁 Daily bonus: +500 Friendship Tokens!");
}

/* =========================================================
   SLOTS
========================================================= */

const slotData={

  buffalo:{
    title:"🐃 Buffalo Stampede",
    jackpot:5000,
    symbols:["🐃","🌹","💰","7️⃣","💎"]
  },

  pink:{
    title:"💗 Pink Palace",
    jackpot:7500,
    symbols:["💗","💋","🌸","👑","💎"]
  },

  dolphin:{
    title:"🐬 Dolphin Riches",
    jackpot:8000,
    symbols:["🐬","🌊","🐚","🐠","💎"]
  },

  sevens:{
    title:"7️⃣ Fancy 7s",
    jackpot:10000,
    symbols:["7️⃣","7️⃣","🍒","⭐","💎"]
  },

  mega:{
    title:"💎 MEGA JACKPOT",
    jackpot:1000000,
    symbols:["💎","💎","7️⃣","👑","💗"]
  }

};

function initSlot(id){

  const el=document.getElementById(id+"Game");

  if(!el) return;

  el.innerHTML=`
    <div class="slotMachine">
      <div class="reels">
        <div class="reel" id="${id}r1">❔</div>
        <div class="reel" id="${id}r2">❔</div>
        <div class="reel" id="${id}r3">❔</div>
      </div>
    </div>
  `;
}

Object.keys(slotData).forEach(initSlot);

function spinSlot(id){

  const data=slotData[id];

  const reels=[
    document.getElementById(id+"r1"),
    document.getElementById(id+"r2"),
    document.getElementById(id+"r3")
  ];

  if(reels.some(r=>!r)) return;

  achievement("firstSpin");

  soundEffect("spin");

  reels.forEach(r=>{
    r.classList.add("spinning");
    r.classList.remove("winGlow");
  });

  let cycles=0;

  const timer=setInterval(()=>{

    reels.forEach(r=>{
      r.textContent=
        data.symbols[
          Math.floor(Math.random()*data.symbols.length)
        ];
    });

    cycles++;

    if(cycles>=20){

      clearInterval(timer);

      reels.forEach(r=>r.classList.remove("spinning"));

      const forceJackpot=Math.random()<.025;

      let result;

      if(forceJackpot){

        const symbol =
          data.symbols[
            Math.floor(Math.random()*data.symbols.length)
          ];

        result=[symbol,symbol,symbol];

      }else{

        result=[
          data.symbols[Math.floor(Math.random()*data.symbols.length)],
          data.symbols[Math.floor(Math.random()*data.symbols.length)],
          data.symbols[Math.floor(Math.random()*data.symbols.length)]
        ];

      }

      reels.forEach((r,i)=>{
        setTimeout(()=>{
          r.textContent=result[i];

          if(
            result[0]===result[1] &&
            result[1]===result[2]
          ){
            r.classList.add("winGlow");
          }

        },i*300);
      });

      setTimeout(()=>{

        const triple =
          result[0]===result[1] &&
          result[1]===result[2];

        if(triple){

          let reward=data.jackpot;

          if(id==="mega" && result[0]==="💎"){

            reward=1000000;

            achievement("million");

            soundEffect("bigwin");

            toast("💎💎💎 MEGA JACKPOT!!! +1,000,000");

          }else{

            soundEffect("bigwin");

            toast("🎉 JACKPOT! +"+format(reward));

          }

          add(reward,true);

        }else{

          add(-20,false);

          soundEffect("lose");

          toast("The reels missed. -20 tokens.");

        }

      },1100);
    }

  },90);
}

/* =========================================================
   CARDS
========================================================= */

const suits=["♠","♥","♦","♣"];
const ranks=[
  ["A",11],
  ["2",2],
  ["3",3],
  ["4",4],
  ["5",5],
  ["6",6],
  ["7",7],
  ["8",8],
  ["9",9],
  ["10",10],
  ["J",10],
  ["Q",10],
  ["K",10]
];

function randomCard(){

  const rank=ranks[Math.floor(Math.random()*ranks.length)];
  const suit=suits[Math.floor(Math.random()*suits.length)];

  return {
    rank:rank[0],
    value:rank[1],
    suit
  };
}

function cardHTML(card,hidden=false){

  if(hidden){

    return `<div class="playingCard cardBack">💗</div>`;

  }

  const red=
    card.suit==="♥" ||
    card.suit==="♦";

  return `
    <div class="playingCard ${red?"cardRed":""}">
      ${card.rank}${card.suit}
    </div>
  `;
}

function cardsTotal(cards){

  let total=cards.reduce((a,c)=>a+c.value,0);

  let aces=cards.filter(c=>c.rank==="A").length;

  while(total>21 && aces>0){

    total-=10;
    aces--;

  }

  return total;
}

/* =========================================================
   POKER
========================================================= */

function playPoker(){

  const player=Array.from({length:5},randomCard);
  const computer=Array.from({length:5},randomCard);

  document.getElementById("pokerPlayer").innerHTML="";

  document.getElementById("pokerComputer").innerHTML="";

  player.forEach((card,i)=>{
    setTimeout(()=>{
      document.getElementById("pokerPlayer")
        .insertAdjacentHTML("beforeend",cardHTML(card));

      soundEffect("card");
    },i*220);
  });

  computer.forEach((card,i)=>{
    setTimeout(()=>{
      document.getElementById("pokerComputer")
        .insertAdjacentHTML("beforeend",cardHTML(card));

      soundEffect("card");
    },i*220+1100);
  });

  setTimeout(()=>{

    const p=player.reduce((a,c)=>a+c.value,0);
    const c=computer.reduce((a,c)=>a+c.value,0);

    if(p>=c){

      add(250,true);
      achievement("firstWin");
      soundEffect("win");
      toast("♠️ You won Poker! +250");

    }else{

      add(-30,false);
      soundEffect("lose");
      toast("Computer wins. -30");

    }

  },2300);
}

/* =========================================================
   BLACKJACK
========================================================= */

let blackjack={
  player:[],
  dealer:[],
  active:false
};

function startBlackjack(){

  blackjack={
    player:[randomCard(),randomCard()],
    dealer:[randomCard(),randomCard()],
    active:true
  };

  renderBlackjack();

  soundEffect("card");
}

function renderBlackjack(){

  document.getElementById("blackjackHand").innerHTML =
    blackjack.player.map(c=>cardHTML(c)).join("");

  document.getElementById("dealerHand").innerHTML =
    cardHTML(blackjack.dealer[0])+
    cardHTML(blackjack.dealer[1],blackjack.active);

  document.getElementById("blackjackTotal").textContent =
    "Total: "+cardsTotal(blackjack.player);

  document.getElementById("dealerTotal").textContent =
    blackjack.active
      ? "Dealer is hiding a card"
      : "Total: "+cardsTotal(blackjack.dealer);
}

function blackjackHit(){

  if(!blackjack.active){

    startBlackjack();
    return;

  }

  blackjack.player.push(randomCard());

  soundEffect("card");

  renderBlackjack();

  if(cardsTotal(blackjack.player)>21){

    blackjack.active=false;

    renderBlackjack();

    add(-30,false);

    soundEffect("lose");

    toast("💥 Bust! -30");

  }

}

function blackjackStand(){

  if(!blackjack.active) return;

  while(cardsTotal(blackjack.dealer)<17){

    blackjack.dealer.push(randomCard());

  }

  blackjack.active=false;

  renderBlackjack();

  const p=cardsTotal(blackjack.player);
  const d=cardsTotal(blackjack.dealer);

  if(d>21 || p>d){

    add(250,true);
    soundEffect("win");
    toast("🃏 Blackjack win! +250");

  }else if(p===d){

    toast("🤝 Push. No tokens lost.");

  }else{

    add(-30,false);
    soundEffect("lose");
    toast("Dealer wins. -30");

  }

}

function blackjackDouble(){

  if(!blackjack.active) return;

  blackjack.player.push(randomCard());

  soundEffect("card");

  if(cardsTotal(blackjack.player)>21){

    blackjack.active=false;

    renderBlackjack();

    add(-60,false);

    toast("💥 Double down bust! -60");

    return;

  }

  blackjackStand();

}

/* =========================================================
   BACCARAT
========================================================= */

function playBaccarat(choice){

  const area=document.getElementById("baccaratArea");

  area.innerHTML="Dealing...";

  soundEffect("card");

  const player=[randomCard(),randomCard()];
  const banker=[randomCard(),randomCard()];

  setTimeout(()=>{

    const p=cardsTotal(player)%10;
    const b=cardsTotal(banker)%10;

    let winner;

    if(p>b) winner="Player";
    else if(b>p) winner="Banker";
    else winner="Tie";

    area.innerHTML=`
      <div class="hand">
        ${player.map(cardHTML).join("")}
      </div>
      <strong>Player: ${p}</strong>
      <hr>
      <div class="hand">
        ${banker.map(cardHTML).join("")}
      </div>
      <strong>Banker: ${b}</strong>
      <p><strong>${winner} wins!</strong></p>
    `;

    if(choice===winner){

      const reward=
        choice==="Tie"
          ? 1000
          : 180;

      add(reward,true);

      soundEffect("win");

      toast("🎉 Baccarat win! +"+reward);

    }else{

      add(-25,false);

      soundEffect("lose");

      toast("Baccarat loss. -25");

    }

  },1000);
}

/* =========================================================
   WAR
========================================================= */

function playWar(){

  const area=document.getElementById("warArea");

  area.innerHTML="";

  const player=randomCard();
  const computer=randomCard();

  setTimeout(()=>{
    area.innerHTML=cardHTML(player);
    soundEffect("card");
  },300);

  setTimeout(()=>{
    area.innerHTML+=cardHTML(computer);
    soundEffect("card");
  },900);

  setTimeout(()=>{

    if(player.value>computer.value){

      add(150,true);
      soundEffect("win");
      toast("⚔️ You won War! +150");

    }else if(player.value===computer.value){

      add(100,true);
      toast("⚔️ WAR! +100");

    }else{

      add(-20,false);
      soundEffect("lose");
      toast("Computer wins. -20");

    }

  },1400);
}

/* =========================================================
   GIN
========================================================= */

function playGin(){

  const area=document.getElementById("ginArea");

  area.innerHTML="";

  const hand=Array.from({length:10},randomCard);

  hand.forEach((card,i)=>{

    setTimeout(()=>{

      area.insertAdjacentHTML(
        "beforeend",
        cardHTML(card)
      );

      soundEffect("card");

    },i*120);

  });

  setTimeout(()=>{

    const score=hand.reduce((a,c)=>a+c.value,0);

    if(score>=60){

      add(300,true);
      soundEffect("win");
      toast("🃏 Great Gin hand! +300");

    }else{

      add(40,true);
      toast("You completed your hand. +40");

    }

  },1500);
}

/* =========================================================
   TEXAS HOLD'EM
========================================================= */

function playHoldem(){

  const board=document.getElementById("holdemBoard");
  const player=document.getElementById("holdemPlayer");

  board.innerHTML="";
  player.innerHTML="";

  const hole=[randomCard(),randomCard()];
  const community=Array.from({length:5},randomCard);

  hole.forEach((c,i)=>{

    setTimeout(()=>{

      player.insertAdjacentHTML(
        "beforeend",
        cardHTML(c)
      );

      soundEffect("card");

    },i*300);

  });

  community.forEach((c,i)=>{

    setTimeout(()=>{

      board.insertAdjacentHTML(
        "beforeend",
        cardHTML(c)
      );

      soundEffect("card");

    },800+i*350);

  });

  setTimeout(()=>{

    const score=
      hole.reduce((a,c)=>a+c.value,0)+
      community.reduce((a,c)=>a+c.value,0);

    if(score>=55){

      add(250,true);
      soundEffect("win");
      toast("♣️ Great Hold'em hand! +250");

    }else{

      add(-30,false);
      soundEffect("lose");
      toast("Hold'em loss. -30");

    }

  },3000);
}

/* =========================================================
   LUCKY WHEEL
========================================================= */

const wheelPrizes=[
  50,
  100,
  250,
  500,
  1000,
  2500,
  5000,
  10000
];

let wheelRotation=0;

function spinWheel(){

  const wheel=document.getElementById("luckyWheel");

  const prizeIndex=
    Math.floor(Math.random()*wheelPrizes.length);

  const segment=360/wheelPrizes.length;

  const target=
    360*6+
    (360-(prizeIndex*segment+segment/2));

  wheelRotation+=target;

  wheel.style.transform=
    `rotate(${wheelRotation}deg)`;

  soundEffect("spin");

  setTimeout(()=>{

    const prize=wheelPrizes[prizeIndex];

    add(prize,true);

    soundEffect(prize>=5000?"bigwin":"win");

    toast("🎡 Lucky Wheel: +"+format(prize));

  },3600);
}

/* =========================================================
   ROULETTE
========================================================= */

function playRoulette(choice){

  const result=document.getElementById("rouletteResult");

  result.textContent="🎰";

  soundEffect("spin");

  setTimeout(()=>{

    const options=["red","black","green"];

    const outcome=
      options[Math.floor(Math.random()*options.length)];

    result.textContent=
      outcome==="red"?"🔴":
      outcome==="black"?"⚫":"🟢";

    if(choice===outcome){

      const reward=
        outcome==="green"
          ?1000
          :150;

      add(reward,true);
      soundEffect("win");
      toast("🎉 Roulette win! +"+reward);

    }else{

      add(-30,false);
      soundEffect("lose");
      toast("Roulette loss. -30");

    }

  },1500);
}

/* =========================================================
   CRAPS
========================================================= */

function playCraps(){

  const d1=document.getElementById("die1");
  const d2=document.getElementById("die2");

  d1.classList.add("rolling");
  d2.classList.add("rolling");

  soundEffect("dice");

  let cycles=0;

  const timer=setInterval(()=>{

    d1.textContent=Math.ceil(Math.random()*6);
    d2.textContent=Math.ceil(Math.random()*6);

    cycles++;

    if(cycles>=15){

      clearInterval(timer);

      d1.classList.remove("rolling");
      d2.classList.remove("rolling");

      const a=Number(d1.textContent);
      const b=Number(d2.textContent);

      const total=a+b;

      if(total===7 || total===11){

        add(200,true);
        soundEffect("win");
        toast("🎲 CRAPS WIN! +200");

      }else{

        add(-20,false);
        soundEffect("lose");
        toast("Craps loss. -20");

      }

    }

  },90);
}

/* =========================================================
   HI LO
========================================================= */

let hiloCurrent=null;

function playHiLo(choice){

  const el=document.getElementById("hiloCard");

  if(hiloCurrent===null){

    hiloCurrent=Math.ceil(Math.random()*13);

    el.textContent=hiloCurrent;

    toast("Choose Higher or Lower.");

    return;
  }

  const next=Math.ceil(Math.random()*13);

  el.textContent="🎴";

  soundEffect("card");

  setTimeout(()=>{

    el.textContent=next;

    const win=
      choice==="higher"
        ?next>hiloCurrent
        :next<hiloCurrent;

    if(next===hiloCurrent){

      toast("Tie! Try again.");

    }else if(win){

      add(120,true);
      soundEffect("win");
      toast("📈 Correct! +120");

    }else{

      add(-25,false);
      soundEffect("lose");
      toast("Wrong prediction. -25");

    }

    hiloCurrent=next;

  },700);
}

/* =========================================================
   COIN
========================================================= */

function coinFlip(choice){

  const el=document.getElementById("coinResult");

  el.style.animation="coinSpin .7s linear";

  soundEffect("coin");

  setTimeout(()=>{

    el.style.animation="";

    const outcome=
      Math.random()<.5
        ?"heads"
        :"tails";

    el.textContent=
      outcome==="heads"
        ?"🪙 HEADS"
        :"🪙 TAILS";

    if(choice===outcome){

      add(100,true);
      soundEffect("win");
      toast("🪙 Correct! +100");

    }else{

      add(-20,false);
      soundEffect("lose");
      toast("Coin flip loss. -20");

    }

  },700);
}

/* =========================================================
   PLINKO
========================================================= */

function initPlinko(){

  const board=document.getElementById("plinkoBoard");

  board.innerHTML="";

  for(let row=0;row<7;row++){

    for(let col=0;col<7;col++){

      const peg=document.createElement("div");

      peg.className="plinkoPeg";

      peg.style.left=
        (25+col*8+(row%2)*4)+"%";

      peg.style.top=
        (18+row*11)+"%";

      board.appendChild(peg);
    }
  }
}

initPlinko();

function playPlinko(){

  const board=document.getElementById("plinkoBoard");

  const ball=document.createElement("div");

  ball.className="plinkoBall";

  board.appendChild(ball);

  soundEffect("click");

  let x=50;
  let y=5;

  const interval=setInterval(()=>{

    y+=2.8;
    x+=
      (Math.random()>.5?1:-1)*
      (1+Math.random()*3);

    x=Math.max(8,Math.min(92,x));

    ball.style.top=y+"%";
    ball.style.left=x+"%";

    soundEffect("click");

    if(y>=91){

      clearInterval(interval);

      const prizes=[
        0,50,100,250,500,1000,2500
      ];

      const prize=
        prizes[
          Math.floor(Math.random()*prizes.length)
        ];

      setTimeout(()=>{

        ball.remove();

        if(prize===0){

          add(-20,false);
          soundEffect("lose");
          toast("Plinko missed. -20");

        }else{

          add(prize,true);
          soundEffect(prize>=1000?"bigwin":"win");
          toast("🟣 Plinko prize: +"+prize);

        }

      },500);

    }

  },120);
}

/* =========================================================
   RACING
========================================================= */

const horseNames=[
  "Rosie",
  "Lucky",
  "Princess",
  "Storm",
  "Diamond"
];

const dolphinNames=[
  "Splash",
  "Pearl",
  "Blue",
  "Wave",
  "Bubbles"
];

let raceState={
  horse:null,
  dolphin:null
};

function initRaceChoices(){

  const horseBox=document.getElementById("horseChoices");
  const dolphinBox=document.getElementById("dolphinChoices");

  horseNames.forEach((name,i)=>{

    const b=document.createElement("button");

    b.className="secondaryBtn";

    b.textContent=`🐎 ${name}`;

    b.onclick=()=>{

      if(raceState.horse?.running) return;

      raceState.horse={
        ...(raceState.horse||{}),
        choice:i
      };

      document.querySelectorAll("#horseChoices button")
        .forEach(x=>x.style.outline="");

      b.style.outline="3px solid #ff4fa3";

      toast("You picked "+name);

    };

    horseBox.appendChild(b);
  });

  dolphinNames.forEach((name,i)=>{

    const b=document.createElement("button");

    b.className="secondaryBtn";

    b.textContent=`🐬 ${name}`;

    b.onclick=()=>{

      if(raceState.dolphin?.running) return;

      raceState.dolphin={
        ...(raceState.dolphin||{}),
        choice:i
      };

      document.querySelectorAll("#dolphinChoices button")
        .forEach(x=>x.style.outline="");

      b.style.outline="3px solid #ff4fa3";

      toast("You picked "+name);

    };

    dolphinBox.appendChild(b);
  });
}

initRaceChoices();

function createBubbles(){

  const box=document.getElementById("dolphinBubbles");

  box.innerHTML="";

  for(let i=0;i<22;i++){

    const bubble=document.createElement("div");

    bubble.className="oceanBubble";

    bubble.style.left=
      Math.random()*100+"%";

    bubble.style.top=
      50+Math.random()*45+"%";

    bubble.style.animationDelay=
      Math.random()*2+"s";

    bubble.style.animationDuration=
      1.5+Math.random()*2+"s";

    box.appendChild(bubble);
  }
}

createBubbles();

function countdown(el,callback){

  const box=document.getElementById(el);

  let count=3;

  box.innerHTML=
    `<div class="countdown">${count}</div>`;

  soundEffect("race");

  const timer=setInterval(()=>{

    count--;

    if(count>0){

      box.innerHTML=
        `<div class="countdown">${count}</div>`;

      soundEffect("race");

    }else{

      clearInterval(timer);

      box.innerHTML=
        `<div class="countdown go">GO!</div>`;

      soundEffect("go");

      setTimeout(()=>{
        box.innerHTML="";
        callback();
      },550);

    }

  },850);
}

function startRace(type){

  const state=raceState[type]||{};

  if(state.running){

    return;
  }

  if(state.choice===undefined){

    toast(
      type==="horse"
        ?"Choose a horse first."
        :"Choose a dolphin first."
    );

    return;
  }

  state.running=true;

  raceState[type]=state;

  const names=
    type==="horse"
      ?horseNames
      :dolphinNames;

  const track=
    document.getElementById(
      type==="horse"
        ?"horseRacers"
        :"dolphinRacers"
    );

  const startButton=
    document.getElementById(
      type==="horse"
        ?"horseStart"
        :"dolphinStart"
    );

  const status=
    document.getElementById(
      type==="horse"
        ?"horseStatus"
        :"dolphinStatus"
    );

  track.innerHTML="";

  startButton.disabled=true;

  status.textContent="🏁 Getting ready...";

  const racers=[];

  names.forEach((name,i)=>{

    const racer=document.createElement("div");

    racer.className=
      "racer "+
      (type==="horse"
        ?"horseRacer"
        :"dolphinRacer");

    racer.style.top=
      (i*70+5)+"px";

    racer.style.left="55px";

    racer.innerHTML=
      type==="horse"
        ?`🐎`
        :`🐬`;

    racer.title=name;

    track.appendChild(racer);

    racers.push(racer);
  });

  countdown(
    type==="horse"
      ?"horseCountdown"
      :"dolphinCountdown",
    ()=>{
      runRace(type,racers,names);
    }
  );
}

function runRace(type,racers,names){

  const track=
    document.getElementById(
      type==="horse"
        ?"horseTrack"
        :"dolphinTrack"
    );

  const state=raceState[type];

  const finish=
    track.clientWidth-105;

  /*
    Each racer receives a slightly different speed.
    The animation uses those speeds directly so the
    winner shown visually is the winner calculated.
  */

  const speeds=racers.map(()=>{
    return .72+Math.random()*.42;
  });

  /* Small boost/penalty variation */
  const winnerIndex=
    speeds.indexOf(Math.max(...speeds));

  let positions=racers.map(()=>55);

  let lastTime=performance.now();

  function frame(now){

    const dt=Math.min(40,now-lastTime);

    lastTime=now;

    let finished=false;

    racers.forEach((racer,i)=>{

      if(positions[i]<finish){

        positions[i]+=
          speeds[i]*
          dt*
          .16;

        /* occasional little burst */
        if(Math.random()<.012){
          positions[i]+=5+Math.random()*8;
        }

        positions[i]=Math.min(
          finish,
          positions[i]
        );

        racer.style.left=
          positions[i]+"px";

      }

      if(positions[i]>=finish){
        finished=true;
      }

    });

    if(!finished){

      if(Math.random()<.12){
        soundEffect("race");
      }

      requestAnimationFrame(frame);

    }else{

      /* Ensure all racers reach final positions */
      racers.forEach((racer,i)=>{
        racer.style.left=
          Math.min(
            finish,
            positions[i]
          )+"px";
      });

      finishRace(type,winnerIndex,names);
    }
  }

  requestAnimationFrame(frame);
}

function finishRace(type,winnerIndex,names){

  const state=raceState[type];

  const chosen=state.choice;

  const winner=names[winnerIndex];

  const status=
    document.getElementById(
      type==="horse"
        ?"horseStatus"
        :"dolphinStatus"
    );

  const startButton=
    document.getElementById(
      type==="horse"
        ?"horseStart"
        :"dolphinStart"
    );

  if(chosen===winnerIndex){

    add(500,true);

    soundEffect("bigwin");

    status.innerHTML=
      `🏆 <strong>${winner} WINS!</strong><br>
       🎉 You picked the winner! +500 Friendship Tokens`;

    createConfetti(
      type==="horse"
        ?"horseTrack"
        :"dolphinTrack"
    );

    achievement("firstWin");

  }else{

    add(-30,false);

    soundEffect("lose");

    status.innerHTML=
      `🏁 <strong>${winner} wins!</strong><br>
       Your racer finished behind them. -30 Friendship Tokens`;

  }

  state.running=false;

  startButton.disabled=false;
}

function createConfetti(trackId){

  const track=document.getElementById(trackId);

  for(let i=0;i<45;i++){

    const piece=document.createElement("div");

    piece.className="confetti";

    piece.style.left=
      Math.random()*100+"%";

    piece.style.animationDelay=
      Math.random()*.7+"s";

    piece.style.transform=
      `rotate(${Math.random()*360}deg)`;

    track.appendChild(piece);

    setTimeout(()=>{
      piece.remove();
    },3200);
  }
}

/* =========================================================
   MYSTERY BOXES
========================================================= */

let boxUsed=false;

function openBox(index){

  if(boxUsed){

    toast("Choose a new game.");

    return;
  }

  boxUsed=true;

  const boxes=
    document.querySelectorAll(".mysteryBox");

  boxes.forEach(b=>b.disabled=true);

  soundEffect("click");

  setTimeout(()=>{

    const prize=
      [50,100,250,500,1000]
      [Math.floor(Math.random()*5)];

    document.getElementById("boxResult").innerHTML=
      `<p>🎁 Box ${index+1} opened!</p>`;

    add(prize,true);

    soundEffect("win");

    toast("🎁 Mystery Box: +"+prize);

    setTimeout(()=>{
      boxUsed=false;
      boxes.forEach(b=>b.disabled=false);
    },1000);

  },800);
}

/* =========================================================
   CUPS
========================================================= */

let cupsShuffled=false;
let cupWinner=0;

function shuffleCups(){

  cupsShuffled=true;

  cupWinner=Math.floor(Math.random()*3);

  const cups=document.querySelectorAll("#cups .cup");

  cups.forEach(c=>{

    c.classList.add("shuffle");

  });

  soundEffect("click");

  setTimeout(()=>{

    cups.forEach(c=>c.classList.remove("shuffle"));

    toast("🥤 Cups shuffled! Pick one.");

  },1800);
}

function chooseCup(index){

  if(!cupsShuffled){

    toast("Shuffle the cups first.");

    return;
  }

  cupsShuffled=false;

  if(index===cupWinner){

    add(300,true);

    soundEffect("win");

    document.getElementById("cupResult").innerHTML=
      "💎 You found the prize!";

    toast("🥤 Cup win! +300");

  }else{

    add(-20,false);

    soundEffect("lose");

    document.getElementById("cupResult").innerHTML=
      "Empty cup!";

    toast("🥤 Empty cup. -20");

  }
}

/* =========================================================
   SCRATCH
========================================================= */

function scratchCard(el){

  if(el.dataset.used) return;

  el.dataset.used="true";

  el.textContent="✨ Revealing...";

  soundEffect("click");

  setTimeout(()=>{

    const prizes=[
      0,
      100,
      200,
      300,
      500
    ];

    const prize=
      prizes[Math.floor(Math.random()*prizes.length)];

    el.textContent=
      prize
        ?`💗 ${prize} TOKENS!`
        :"💔 Nothing this time";

    if(prize){

      add(prize,true);
      soundEffect("win");

    }else{

      add(-10,false);
      soundEffect("lose");

    }

  },1200);
}

/* =========================================================
   DARTS
========================================================= */

function throwDart(){

  const board=document.getElementById("dartBoard");

  board.textContent="🎯";

  board.animate(
    [
      {transform:"translateX(-150px) rotate(-40deg)",opacity:.3},
      {transform:"translateX(0) rotate(0)",opacity:1}
    ],
    {
      duration:900,
      easing:"cubic-bezier(.2,.8,.2,1)"
    }
  );

  soundEffect("click");

  setTimeout(()=>{

    const score=
      Math.floor(Math.random()*100)+1;

    let prize=0;

    if(score>=90) prize=1000;
    else if(score>=75) prize=500;
    else if(score>=50) prize=250;
    else if(score>=25) prize=100;

    board.textContent=
      "🎯 "+score;

    if(prize){

      add(prize,true);
      soundEffect("win");
      toast("🎯 Dart score "+score+"! +"+prize);

    }else{

      add(-20,false);
      soundEffect("lose");
      toast("🎯 Missed the prize. -20");

    }

  },900);
}

/* =========================================================
   GEM HEIST
========================================================= */

function gemHeist(){

  const el=document.getElementById("gemVault");

  el.textContent="🔐";

  soundEffect("click");

  setTimeout(()=>{
    el.textContent="🔓";
  },600);

  setTimeout(()=>{

    const prizes=[100,250,500,1000];

    const prize=
      prizes[Math.floor(Math.random()*prizes.length)];

    el.textContent="💎";

    add(prize,true);

    soundEffect("win");

    toast("💎 Gem Heist: +"+prize);

  },1200);
}

/* =========================================================
   ENVELOPES
========================================================= */

function openEnvelope(index){

  const prizes=[100,250,500,1000];

  const prize=
    prizes[Math.floor(Math.random()*prizes.length)];

  document.getElementById("envelopeResult").innerHTML=
    `<p>✉️ Envelope ${index+1} opened!</p>`;

  add(prize,true);

  soundEffect("win");

  toast("✉️ Lucky Envelope: +"+prize);
}

/* =========================================================
   LUCKY NUMBER
========================================================= */

function luckyNumber(){

  const input=document.getElementById("luckyGuess");

  const guess=Number(input.value);

  if(guess<1 || guess>10){

    toast("Choose a number from 1 to 10.");

    return;
  }

  const display=
    document.getElementById("luckyNumberDisplay");

  let cycles=0;

  soundEffect("spin");

  const timer=setInterval(()=>{

    display.textContent=
      Math.ceil(Math.random()*10);

    cycles++;

    if(cycles>=20){

      clearInterval(timer);

      const result=
        Math.ceil(Math.random()*10);

      display.textContent=result;

      if(result===guess){

        add(1000,true);

        soundEffect("bigwin");

        toast("🔢 JACKPOT NUMBER! +1,000");

      }else{

        add(-25,false);

        soundEffect("lose");

        toast("Number was "+result+". -25");

      }

    }

  },80);
}

/* =========================================================
   OCEAN TREASURE
========================================================= */

function oceanTreasure(){

  const el=document.getElementById("treasureChest");

  el.textContent="🌊";

  soundEffect("click");

  setTimeout(()=>{
    el.textContent="🐚";
  },500);

  setTimeout(()=>{
    el.textContent="🧰";
  },1000);

  setTimeout(()=>{

    const prizes=[
      50,
      100,
      250,
      500,
      1500
    ];

    const prize=
      prizes[Math.floor(Math.random()*prizes.length)];

    el.textContent="💎";

    add(prize,true);

    soundEffect("win");

    toast("🌊 Ocean Treasure: +"+prize);

  },1500);
}

/* =========================================================
   FRIENDSHIP CATCH
========================================================= */

const creatureInfo={

  Dolphini:["🐬","Common",100],

  Rosibun:["🌹🐰","Uncommon",150],

  Sunnyflo:["🌻","Common",100],

  Pinkyroo:["🦘💗","Rare",300],

  Fluttera:["🦋","Rare",300],

  Shellby:["🐚","Epic",500],

  Lunaboo:["🌙","Legendary",1000]

};

let currentCreature=null;

function chooseCreature(){

  const keys=Object.keys(creatureInfo);

  const available=
    keys.filter(k=>!S.caught.includes(k));

  if(!available.length){

    return null;
  }

  return available[
    Math.floor(Math.random()*available.length)
  ];
}

function startCatch(){

  if(S.caught.length>=Object.keys(creatureInfo).length){

    toast("🐾 You caught every creature!");

    return;
  }

  currentCreature=chooseCreature();

  const data=creatureInfo[currentCreature];

  const creature=
    document.getElementById("catchCreature");

  const ball=
    document.getElementById("catchBall");

  creature.textContent=data[0];

  creature.style.opacity="1";

  ball.textContent="💗";

  ball.classList.remove("throw","shake");

  soundEffect("catch");

  setTimeout(()=>{

    ball.classList.add("throw");

  },100);

  setTimeout(()=>{

    ball.classList.remove("throw");
    ball.classList.add("shake");

    creature.style.opacity=".25";

  },850);

  setTimeout(()=>{

    ball.classList.remove("shake");

    const rarity=data[1];

    const chance=
      rarity==="Legendary"
        ?0.25
        :rarity==="Epic"
          ?0.45
          :rarity==="Rare"
            ?0.65
            :rarity==="Uncommon"
              ?0.74
              :0.82;

    if(Math.random()<chance){

      S.caught.push(currentCreature);

      add(data[2],true);

      soundEffect("bigwin");

      document.getElementById("catchResult").innerHTML=
        `<p>✨ You caught <strong>${currentCreature}</strong>!
        ${data[0]} ${rarity} +${data[2]} tokens.</p>`;

      if(S.caught.length===Object.keys(creatureInfo).length){

        achievement("collector");
      }

    }else{

      add(-10,false);

      soundEffect("lose");

      document.getElementById("catchResult").innerHTML=
        `<p>💨 ${currentCreature} escaped!</p>`;

    }

    update();

  },1500);
}

function renderCollection(){

  const box=document.getElementById("collection");

  if(!box) return;

  box.innerHTML="";

  Object.entries(creatureInfo).forEach(([name,data])=>{

    const caught=S.caught.includes(name);

    const item=document.createElement("span");

    item.style.display="inline-flex";
    item.style.alignItems="center";
    item.style.gap="6px";
    item.style.margin="5px";
    item.style.padding="9px 12px";
    item.style.borderRadius="12px";
    item.style.background=caught
      ?"white"
      :"#eee";

    item.innerHTML=
      caught
        ?`${data[0]} ${name}`
        :"❓ Mystery";

    box.appendChild(item);
  });
}

/* =========================================================
   QUIZ
========================================================= */

const quiz=[

  ["What is Liliana's favourite colour?",
    ["Baby pink","Purple","Burgundy","Blue"],0],

  ["What food does Liliana love?",
    ["Pizza","Sushi","Tacos","Pasta"],1],

  ["What animal does Liliana love?",
    ["Dolphins","Lions","Penguins","Koalas"],0],

  ["What is Liliana's favourite number?",
    ["7","13","3","9"],2],

  ["What flowers does Liliana like?",
    ["Sunflowers and roses","Tulips","Lilies","Daisies"],0],

  ["What is Liliana's star sign?",
    ["Cancer","Leo","Virgo","Aries"],1],

  ["How many tattoos does Liliana have?",
    ["1","2","3","4"],0],

  ["What colour are Liliana's eyes?",
    ["Blue","Brown","Green","Hazel"],2],

  ["How many siblings does Liliana have?",
    ["2","3","4","5"],3],

  ["How many nieces does Liliana have?",
    ["1","2","3","4"],0],

  ["How many nephews does Liliana have?",
    ["2","3","4","5"],2],

  ["What are Liliana's dogs called?",
    ["Aayla & Arlo","Luna & Max","Milo & Bella","Coco & Rose"],0],

  ["What does Liliana want one day?",
    ["To be a pilot","To be a mum to a baby girl","To live alone","To own a restaurant"],1],

  ["What subject did Liliana study at university?",
    ["Law","Medicine","Psychology","Business"],2],

  ["What movie does Liliana love?",
    ["Titanic","Me Before You","Frozen","The Notebook"],1],

  ["What is Liliana afraid of?",
    ["Heights","Drowning","Thunder","Dogs"],1],

  ["What hobby does Liliana enjoy?",
    ["Poker","Golf","Fishing","Running"],0],

  ["What does Liliana enjoy listening to?",
    ["Only classical music","Sad songs","Country only","Heavy metal only"],1],

  ["What is Liliana known for in the friend group?",
    ["The player","The quiet one","The teacher","The athlete"],0],

  ["How long have you been best friends?",
    ["2 years","4 years","6 years","10 years"],2]

];

let quizIndex=0;
let quizScore=0;
let quizChoices=[];

function renderQuiz(){

  const area=document.getElementById("quizArea");

  if(quizIndex>=quiz.length){

    const reward=
      quizScore===20
        ?5000
        :quizScore*100;

    add(reward, true);

    if(quizScore===20){
      achievement("expert");
      soundEffect("bigwin");
    }else{
      soundEffect("win");
    }

    if(quizScore>S.quizBest){
      S.quizBest=quizScore;
    }

    area.innerHTML=`
      <div style="text-align:center;padding:25px">
        <div style="font-size:55px">🎉</div>
        <h2>${quizScore}/20</h2>
        <p>
          Your best score: ${S.quizBest}/20
        </p>
        <p>
          You earned ${format(reward)} Friendship Tokens!
        </p>
        <button class="playBtn" onclick="restartQuiz()">
          PLAY AGAIN
        </button>
      </div>
    `;

    update();

    return;
  }

  const q=quiz[quizIndex];

  area.innerHTML=`
    <div class="quizQuestion">
      ${quizIndex+1}/20 — ${q[0]}
    </div>

    <div class="quizOptions">
      ${q[1].map((answer,i)=>`
        <button
          class="quizOption"
          onclick="answerQuiz(${i})">
          ${answer}
        </button>
      `).join("")}
    </div>
  `;
}

function answerQuiz(choice){

  const correct=quiz[quizIndex][2];

  if(choice===correct){
    quizScore++;
    soundEffect("win");
  }else{
    soundEffect("lose");
  }

  quizIndex++;

  renderQuiz();
}

function restartQuiz(){

  quizIndex=0;
  quizScore=0;

  renderQuiz();
}

renderQuiz();

/* =========================================================
   PERSONALITY
========================================================= */

function renderPersonality(){

  const area=document.getElementById("personalityArea");

  area.innerHTML=`
    <button class="quizOption" onclick="personality('soft')">
      💗 Sweet and caring
    </button>

    <button class="quizOption" onclick="personality('flirty')">
      💋 Flirty and charismatic
    </button>

    <button class="quizOption" onclick="personality('gambler')">
      🎰 Give me the casino
    </button>

    <button class="quizOption" onclick="personality('dreamer')">
      🌙 Sad songs and poetry
    </button>

    <button class="quizOption" onclick="personality('main')">
      👑 Main character energy
    </button>

    <div id="personalityResult"></div>
  `;
}

function personality(type){

  const results={

    soft:[
      "The Soft Liliana",
      "Sweet, caring and deeply empathetic. 💗"
    ],

    flirty:[
      "The Flirty Liliana",
      "Charismatic, playful and impossible to ignore. 💋"
    ],

    gambler:[
      "The Gambler Liliana",
      "Give her poker, casino games and a little luck. 🎰"
    ],

    dreamer:[
      "The Dreamer Liliana",
      "Poetry, sad songs and a head full of dreams. 🌙"
    ],

    main:[
      "The Main Character Liliana",
      "Because obviously the universe revolves around her. 👑"
    ]

  };

  const result=results[type];

  document.getElementById("personalityResult").innerHTML=`
    <div style="
      margin-top:15px;
      padding:18px;
      border-radius:15px;
      background:#fff;
      text-align:center
    ">
      <div style="font-size:40px">✨</div>
      <h3>${result[0]}</h3>
      <p>${result[1]}</p>
    </div>
  `;

  add(300,true);

  soundEffect("win");

  toast("✨ Personality result unlocked! +300");
}

renderPersonality();

/* =========================================================
   VAULT
========================================================= */

function openVault(){

  const code=
    document.getElementById("vaultInput").value;

  if(code==="060722"){

    if(S.vaultOpened){

      toast("🔐 The VIP Vault is already unlocked.");

      return;
    }

    S.vaultOpened=true;

    add(10000,true);

    achievement("vault");

    soundEffect("bigwin");

    document.getElementById("vaultResult").innerHTML=`
      <div style="margin-top:20px">
        <div style="font-size:60px">💎</div>
        <h2>VAULT UNLOCKED!</h2>
        <p>
          The secret friendship reward is yours.
        </p>
      </div>
    `;

    toast("🔐 VIP Vault unlocked! +10,000");

  }else{

    soundEffect("lose");

    toast("❌ Wrong code.");

  }
}

/* =========================================================
   INITIALISE
========================================================= */

update();

</script>

</body>
</html>
