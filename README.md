<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Liliana's Friendship Casino 💗</title>

  <style>

    /* ==========================================
       1. CASINO THEME
       ========================================== */

    :root {
      --pink: #ff4fa3;
      --dark-pink: #b51f69;
      --gold: #ffd76a;
      --purple: #7c4dff;
      --dark: #120817;
      --panel: #211126;
      --text: #fff;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background:
        radial-gradient(circle at top, #3b1645, #120817 70%);
      color: var(--text);
    }

    button {
      cursor: pointer;
    }


    /* ==========================================
       2. TOP CASINO BAR
       ========================================== */

    .top-bar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px;
      background: #180b20;
      border-bottom: 1px solid #63345f;
    }

    .casino-name {
      font-size: 1.3rem;
      font-weight: bold;
    }

    .stats {
      display: flex;
      gap: 12px;
      flex-wrap: wrap;
    }

    .stat {
      background: #2b1531;
      padding: 8px 12px;
      border-radius: 12px;
    }


    /* ==========================================
       3. MAIN CASINO FLOOR
       ========================================== */

    .casino-floor {
      max-width: 1100px;
      margin: auto;
      padding: 25px;
    }

    .welcome {
      text-align: center;
      margin-bottom: 25px;
    }

    .welcome h1 {
      font-size: 2.5rem;
      margin-bottom: 5px;
    }

    .welcome p {
      opacity: .75;
    }


    /* ==========================================
       4. INTERACTIVE CASINO ROOMS
       ========================================== */

    .rooms {
      display: grid;
      grid-template-columns:
        repeat(auto-fit, minmax(180px, 1fr));
      gap: 15px;
    }

    .room {
      min-height: 150px;
      border: 1px solid #6d3a6c;
      border-radius: 22px;
      padding: 20px;
      background: #25122d;
      transition: .25s;
    }

    .room:hover {
      transform: translateY(-5px);
      border-color: var(--pink);
    }

    .room-icon {
      font-size: 3rem;
    }

    .room-title {
      font-size: 1.2rem;
      font-weight: bold;
    }


    /* ==========================================
       5. GAME ROOM
       ========================================== */

    .game-room {
      display: none;
      margin-top: 25px;
      padding: 25px;
      background: #1b0c23;
      border: 1px solid #713c70;
      border-radius: 25px;
    }

    .game-room.active {
      display: block;
    }

    .back-button {
      margin-bottom: 20px;
    }


    /* ==========================================
       6. SLOT MACHINE
       ========================================== */

    .slot-machine {
      max-width: 650px;
      margin: auto;
      text-align: center;
      padding: 25px;
      background: #28102f;
      border-radius: 25px;
    }

    .reels {
      display: flex;
      justify-content: center;
      gap: 10px;
      margin: 25px 0;
    }

    .reel {
      width: 100px;
      height: 100px;
      display: grid;
      place-items: center;
      background: white;
      color: #222;
      border-radius: 15px;
      font-size: 3rem;
    }

    .spin-button {
      padding: 15px 40px;
      border: 0;
      border-radius: 30px;
      background: var(--pink);
      color: white;
      font-size: 1.2rem;
      font-weight: bold;
    }


    /* ==========================================
       7. LUCKY WHEEL
       ========================================== */

    .wheel-area {
      text-align: center;
    }

    .wheel {
      width: 280px;
      height: 280px;
      border-radius: 50%;
      margin: 25px auto;
      background:
        conic-gradient(
          #ff4fa3 0deg 45deg,
          #ffd76a 45deg 90deg,
          #7c4dff 90deg 135deg,
          #55d6be 135deg 180deg,
          #ff8c42 180deg 225deg,
          #ff4fa3 225deg 270deg,
          #ffd76a 270deg 315deg,
          #7c4dff 315deg 360deg
        );
      border: 8px solid white;
      transition: transform 3s ease-out;
    }


    /* ==========================================
       8. FRIENDSHIP CATCH
       ========================================== */

    .ocean {
      min-height: 400px;
      position: relative;
      overflow: hidden;
      border-radius: 25px;
      background:
        linear-gradient(#174a70, #08243d);
    }

    .creature {
      position: absolute;
      font-size: 3rem;
      border: 0;
      background: none;
      animation: swim 5s infinite alternate ease-in-out;
    }

    @keyframes swim {
      from {
        transform: translateX(0);
      }

      to {
        transform: translateX(100px);
      }
    }


    /* ==========================================
       9. QUIZ
       ========================================== */

    .quiz-option {
      display: block;
      width: 100%;
      margin: 8px 0;
      padding: 14px;
      border-radius: 12px;
      border: 1px solid #63345f;
      background: #28132f;
      color: white;
      text-align: left;
    }


    /* ==========================================
       10. MOBILE
       ========================================== */

    @media (max-width: 600px) {

      .top-bar {
        flex-direction: column;
        gap: 12px;
      }

      .welcome h1 {
        font-size: 1.8rem;
      }

      .rooms {
        grid-template-columns: 1fr 1fr;
      }

      .reel {
        width: 75px;
        height: 75px;
      }

    }

  </style>
</head>


<body>

  <!-- ==========================================
       TOP BAR
       ========================================== -->

  <header class="top-bar">

    <div class="casino-name">
      💗 Liliana's Friendship Casino
    </div>

    <div class="stats">

      <div class="stat">
        💰 <span id="tokens">1000</span>
      </div>

      <div class="stat">
        ⭐ Level <span id="level">1</span>
      </div>

      <div class="stat">
        🔥 <span id="streak">0</span>
      </div>

    </div>

  </header>


  <!-- ==========================================
       MAIN CASINO
       ========================================== -->

  <main class="casino-floor">

    <section class="welcome">

      <h1>🎰 Welcome to Liliana's Casino</h1>

      <p>
        Six years of friendship.
        One ridiculous amount of tokens.
      </p>

    </section>


    <!-- ========================================
         CASINO ROOMS
         ======================================== -->

    <section class="rooms">

      <button class="room" data-room="slots">

        <div class="room-icon">🎰</div>

        <div class="room-title">
          Slots Room
        </div>

        <p>
          Buffalo, Dolphin Riches,
          Pink Palace & Mega Jackpot
        </p>

      </button>


      <button class="room" data-room="cards">

        <div class="room-icon">♠️</div>

        <div class="room-title">
          Card Room
        </div>

        <p>
          Poker, Blackjack,
          Baccarat, War & Gin Rummy
        </p>

      </button>


      <button class="room" data-room="lucky">

        <div class="room-icon">🎡</div>

        <div class="room-title">
          Lucky Lounge
        </div>

        <p>
          Wheel, Roulette,
          Craps & Plinko
        </p>

      </button>


      <button class="room" data-room="races">

        <div class="room-icon">🏇</div>

        <div class="room-title">
          Derby Track
        </div>

        <p>
          Horse Derby &
          Dolphin Derby
        </p>

      </button>


      <button class="room" data-room="catch">

        <div class="room-icon">🐬</div>

        <div class="room-title">
          Friendship Catch
        </div>

        <p>
          Catch and collect
          friendship creatures
        </p>

      </button>


      <button class="room" data-room="prizes">

        <div class="room-icon">🎁</div>

        <div class="room-title">
          Prize Arcade
        </div>

        <p>
          Mystery Boxes,
          Scratch Cards & more
        </p>

      </button>


      <button class="room" data-room="liliana">

        <div class="room-icon">💗</div>

        <div class="room-title">
          Liliana's Corner
        </div>

        <p>
          Quiz, Personality Test,
          Memories & Letter
        </p>

      </button>


      <button class="room" data-room="vault">

        <div class="room-icon">🔐</div>

        <div class="room-title">
          VIP Vault
        </div>

        <p>
          Six-year friendship
          secret
        </p>

      </button>

    </section>


    <!-- ========================================
         SLOTS ROOM
         ======================================== -->

    <section
      id="slots"
      class="game-room">

      <button class="back-button">
        ← Back to Casino
      </button>

      <h2>🎰 Slots Room</h2>

      <div class="slot-machine">

        <h3>
          💎 MEGA JACKPOT
        </h3>

        <p>
          JACKPOT:
          <strong>1,000,000 💰</strong>
        </p>

        <div class="reels">

          <div class="reel" id="reel1">
            💎
          </div>

          <div class="reel" id="reel2">
            💎
          </div>

          <div class="reel" id="reel3">
            💎
          </div>

        </div>

        <button
          class="spin-button"
          id="megaSpin">

          SPIN 🎰

        </button>

        <p id="slotResult"></p>

      </div>

    </section>


    <!-- ========================================
         LUCKY WHEEL
         ======================================== -->

    <section
      id="lucky"
      class="game-room">

      <button class="back-button">
        ← Back to Casino
      </button>

      <h2>🎡 Lucky Lounge</h2>

      <div class="wheel-area">

        <div
          class="wheel"
          id="wheel">
        </div>

        <button
          class="spin-button"
          id="wheelSpin">

          SPIN THE WHEEL

        </button>

        <p id="wheelResult"></p>

      </div>

    </section>


    <!-- ========================================
         FRIENDSHIP CATCH
         ======================================== -->

    <section
      id="catch"
      class="game-room">

      <button class="back-button">
        ← Back to Casino
      </button>

      <h2>🐬 Friendship Catch</h2>

      <p>
        Catch creatures and build
        Liliana's Friendship Aquarium.
      </p>

      <div class="ocean">

        <button
          class="creature"
          style="left:15%;top:30%"
          data-creature="Dolphini">

          🐬

        </button>

        <button
          class="creature"
          style="left:65%;top:20%"
          data-creature="Rosibun">

          🌹🐰

        </button>

        <button
          class="creature"
          style="left:40%;top:65%"
          data-creature="Sunnyflo">

          🌻

        </button>

        <button
          class="creature"
          style="left:75%;top:65%"
          data-creature="Pinkyroo">

          🦘💗

        </button>

      </div>

      <p id="catchResult"></p>

    </section>


    <!-- ========================================
         LILIANA'S CORNER
         ======================================== -->

    <section
      id="liliana"
      class="game-room">

      <button class="back-button">
        ← Back to Casino
      </button>

      <h2>💗 Liliana's Corner</h2>

      <button class="room">
        🧠 Take Liliana's Quiz
      </button>

      <button class="room">
        🌸 Personality Test
      </button>

      <button class="room">
        📖 Six Years of Friendship
      </button>

      <button class="room">
        💌 Open Friendship Letter
      </button>

    </section>


    <!-- ========================================
         VIP VAULT
         ======================================== -->

    <section
      id="vault"
      class="game-room">

      <button class="back-button">
        ← Back to Casino
      </button>

      <h2>🔐 VIP Friendship Vault</h2>

      <p>
        Six digits.
        Six years.
        One secret.
      </p>

      <input
        id="vaultCode"
        maxlength="6"
        inputmode="numeric"
        placeholder="••••••">

      <button id="vaultButton">
        UNLOCK
      </button>

      <p id="vaultResult"></p>

    </section>

  </main>


  <script>

    /* ==========================================
       GAME STATE
       ========================================== */

    const state = {

      tokens: 1000,

      xp: 0,

      level: 1,

      streak: 0,

      wins: 0,

      played: 0,

      caught: [],

      achievements: []

    };


    /* ==========================================
       UPDATE HUD
       ========================================== */

    function updateHUD() {

      document.getElementById("tokens")
        .textContent = state.tokens;

      document.getElementById("level")
        .textContent = state.level;

      document.getElementById("streak")
        .textContent = state.streak;

    }


    /* ==========================================
       TOKEN SYSTEM
       ========================================== */

    function addTokens(amount) {

      state.tokens += amount;

      if (state.tokens < 0) {
        state.tokens = 0;
      }

      state.xp += Math.max(1, Math.abs(amount));

      updateHUD();

    }


    /* ==========================================
       ROOM NAVIGATION
       ========================================== */

    const rooms =
      document.querySelectorAll(".room");

    const gameRooms =
      document.querySelectorAll(".game-room");


    rooms.forEach(room => {

      room.addEventListener("click", () => {

        const target =
          room.dataset.room;

        gameRooms.forEach(game => {
          game.classList.remove("active");
        });

        const selected =
          document.getElementById(target);

        if (selected) {
          selected.classList.add("active");

          selected.scrollIntoView({
            behavior: "smooth"
          });
        }

      });

    });


    /* ==========================================
       BACK BUTTONS
       ========================================== */

    document
      .querySelectorAll(".back-button")
      .forEach(button => {

        button.addEventListener("click", () => {

          gameRooms.forEach(game => {
            game.classList.remove("active");
          });

          window.scrollTo({
            top: 0,
            behavior: "smooth"
          });

        });

      });


    /* ==========================================
       MEGA JACKPOT
       ========================================== */

    document
      .getElementById("megaSpin")
      .addEventListener("click", () => {

        const reels = [
          "💎",
          "🍒",
          "7️⃣",
          "💗",
          "🐬"
        ];

        const result = [
          reels[Math.floor(Math.random() * reels.length)],
          reels[Math.floor(Math.random() * reels.length)],
          reels[Math.floor(Math.random() * reels.length)]
        ];

        document.getElementById("reel1")
          .textContent = result[0];

        document.getElementById("reel2")
          .textContent = result[1];

        document.getElementById("reel3")
          .textContent = result[2];

        if (
          result[0] === "💎" &&
          result[1] === "💎" &&
          result[2] === "💎"
        ) {

          addTokens(1000000);

          document.getElementById("slotResult")
            .textContent =
            "💎💎💎 MEGA JACKPOT! +1,000,000 TOKENS!";

        } else {

          addTokens(-20);

          document.getElementById("slotResult")
            .textContent =
            "No jackpot this time. Try again!";

        }

      });


    /* ==========================================
       LUCKY WHEEL
       ========================================== */

    let wheelRotation = 0;

    const prizes = [
      50,
      100,
      250,
      500,
      1000,
      2500,
      5000,
      10000
    ];


    document
      .getElementById("wheelSpin")
      .addEventListener("click", () => {

        const wheel =
          document.getElementById("wheel");

        const prize =
          prizes[
            Math.floor(
              Math.random() * prizes.length
            )
          ];

        wheelRotation +=
          1440 + Math.random() * 720;

        wheel.style.transform =
          `rotate(${wheelRotation}deg)`;

        setTimeout(() => {

          addTokens(prize);

          document
            .getElementById("wheelResult")
            .textContent =
            `🎉 You won ${prize} tokens!`;

        }, 3000);

      });


    /* ==========================================
       FRIENDSHIP CATCH
       ========================================== */

    document
      .querySelectorAll(".creature")
      .forEach(creature => {

        creature.addEventListener("click", () => {

          const name =
            creature.dataset.creature;

          const caught =
            Math.random() < .7;

          if (caught) {

            state.caught.push(name);

            addTokens(150);

            creature.style.display = "none";

            document
              .getElementById("catchResult")
              .textContent =
              `✨ You caught ${name}! +150 tokens!`;

          } else {

            document
              .getElementById("catchResult")
              .textContent =
              `${name} escaped! 🐬`;

          }

        });

      });


    /* ==========================================
       VIP VAULT
       ========================================== */

    document
      .getElementById("vaultButton")
      .addEventListener("click", () => {

        const code =
          document
            .getElementById("vaultCode")
            .value;

        if (code === "060722") {

          addTokens(10000);

          document
            .getElementById("vaultResult")
            .textContent =
            "🔓 VAULT OPENED! +10,000 TOKENS!";

        } else {

          document
            .getElementById("vaultResult")
            .textContent =
            "❌ Incorrect code.";

        }

      });


    updateHUD();

  </script>

</body>
</html>
