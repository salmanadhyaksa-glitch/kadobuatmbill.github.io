
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>happy birthday veyaa &lt;3</title>
  <link rel="icon" href="https://i.ibb.co/hXZsYxZ/heart.png">
  <link href="https://fonts.googleapis.com/css2?family=Poppins&family=Dancing+Script&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      background-color: #ffffff;
      color: #1e3a8a;
      font-family: 'Poppins', sans-serif;
      overflow: hidden;
    }
    .page {
      height: 100vh;
      width: 100vw;
      position: absolute;
      top: 0;
      left: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 20px;
      opacity: 0;
      pointer-events: none;
      transition: opacity 1s ease;
      background: white;
    }
    .page.active {
      opacity: 1;
      pointer-events: auto;
      z-index: 2;
    }
    h1, h2 { margin-bottom: 1rem; }
    h1 { font-size: 2.2rem; }
    h2 { font-size: 1.8rem; }
    .highlight { color: #1e3a8a; font-weight: bold; }
    .button {
      background-color: #1e3a8a;
      color: #fff;
      border: none;
      border-radius: 25px;
      padding: 15px 30px;
      font-size: 1.2rem;
      cursor: pointer;
      margin-top: 30px;
      transition: background 0.3s;
    }
    .button:hover { background-color: #2c4ca5; }
    img { max-width: 70vw; max-height: 50vh; margin-bottom: 20px; }
    .letter {
      white-space: pre-line;
      font-size: 1.1rem;
      max-width: 600px;
      text-align: left;
      border-left: 3px solid #1e3a8a;
      padding-left: 15px;
      min-height: 200px;
    }
    .falling {
      position: fixed;
      top: -30px;
      font-size: 24px;
      animation: fall linear infinite;
      pointer-events: none;
      z-index: 9999;
    }
    .blue-heart { color: #1e3a8a; }
    .yellow-star { color: #facc15; }
    @keyframes fall {
      to {
        transform: translateY(120vh) rotate(360deg);
        opacity: 0;
      }
    }
    .display {
      font-size: 2rem;
      letter-spacing: 10px;
      margin: 10px;
    }
    .keypad {
      display: grid;
      grid-template-columns: repeat(3, 80px);
      gap: 10px;
    }
    .keypad button {
      padding: 20px;
      font-size: 1.5rem;
      border-radius: 10px;
      border: none;
      background: #e0f2fe;
      cursor: pointer;
    }
    .img-preview img {
      max-height: 300px;
      border-radius: 10px;
      margin-bottom: 10px;
    }
    @media (max-width: 600px) {
      .page {
        padding: 10px;
        min-height: 100vh;
        width: 100vw;
        max-width: 100vw;
      }
      h1 { font-size: 1.2rem; }
      h2 { font-size: 1rem; }
      .button {
        padding: 10px 10px;
        font-size: 1rem;
        width: 90vw;
        max-width: 350px;
        margin-top: 20px;
      }
      .letter {
        font-size: 0.95rem;
        max-width: 95vw;
        padding-left: 8px;
        min-height: 120px;
      }
      img, .img-preview img {
        max-width: 95vw;
        max-height: 35vh;
        margin-bottom: 10px;
      }
      .keypad {
        grid-template-columns: repeat(3, 1fr);
        gap: 6px;
        width: 100%;
        max-width: 350px;
        margin: 0 auto;
      }
      .keypad button {
        padding: 14px;
        font-size: 1.1rem;
        border-radius: 8px;
      }
      .display {
        font-size: 1.3rem;
        letter-spacing: 6px;
        margin: 8px;
      }
    }
  </style>
</head>
<body>
  <div class="page active" id="page0">
    <div class="img-preview">
      <img src="page 1.jpg" alt="eyes">
    </div>
    <h2>penasaran ga sih? yuk isi passwordnya 🤭🩷</h2>
    <div class="display" id="inputDisplay">0000</div>
    <div class="keypad">
      <button onclick="press(1)">1</button>
      <button onclick="press(2)">2</button>
      <button onclick="press(3)">3</button>
      <button onclick="press(4)">4</button>
      <button onclick="press(5)">5</button>
      <button onclick="press(6)">6</button>
      <button onclick="press(7)">7</button>
      <button onclick="press(8)">8</button>
      <button onclick="press(9)">9</button>
      <button onclick="press(0)">0</button>
    </div>
    <p>clue: tanggal kita🤫</p>
  </div>

  <div class="page" id="page1">
    <img src="1.gif" alt="Cute Birthday Cake" />
    <h1>Happy Birthday <span class="highlight">sayangkuu (^O^) ♡</span></h1>
    <p>your next surprise is just a click away ✨</p>
    <button class="button" onclick="goToPage(2)">tap <3 </button>
  </div>

  <div class="page" id="page2">
    <img src="write.gif" alt="Envelope" />
    <p>knock knock .. open me up! (ノ゜ー゜)ノ</p>
    <button class="button" onclick="goToPage(3)">open it <3 </button>
  </div>

  <div class="page" id="page3" style="font-family: 'Dancing Script', cursive;">
    <h2>Hai Sayangkuu Bacaa yaa Cantikk &lt;3 💞 </h2>
    <div class="letter" id="letterText"></div>
    <button class="button" onclick="goToPage(4)">next <3 </button>
  </div>

  <div class="page" id="page4">
    <img src="foto 1.jpg" alt="Foto 1" />
    <h1>I love u, i will say it again and again bcs my love for u keeps growing, wider, and stronger veyaa 💞</h1>
    <p>My wish everything for u, not only words, its my feling and my love for u</p>
    <button class="button" onclick="goToPage(5)">open this (♡︿‿︿♡)</button>
  </div>

  <div class="page" id="page5">
    <img src="foto 2.jpg" alt="Foto 2" />
    <h1>Semoga semua cita-cita kamu terwujud yaa, semoga kamu bisa membahagiakan orang tua, dan segala hal baik datang ke kamu♡</h1>
    <p>kita sangat serasi mbill, salah satu cita-cita kamu kan mas hehe, jadi untuk mendapatkan mas sudah terwujud yaa 🥺</p>
    <button class="button" onclick="goToPage(6)">♡</button>
  </div>

  <div class="page" id="page6">
    <img src="foto 3.jpg" style="clip-path: circle(40% at 50% 50%);" alt="Foto 3">
    <h1>Meskipun foto ini bukan awal mula mas masuk ke dunia kamu, tapi dari sini mas merasakan hal-hal indah saat bersama kamu </h1>
    <p>i'm so sorry if i'm not treating you the best sometimes, but i always say thanks to Allah because i have u sweetheart</p>
    <button class="button" onclick="goToPage(7)">♡</button>
  </div>

  <div class="page" id="page7">
    <img src="foto 4.jpg" alt="Foto 4" style="max-width: 70vw; max-height: 40vh; margin-bottom: 20px;" />
    <h2>Final Note</h2>
    <div class="letter">
      To the love of my life,
      Mas bangga punya wanita yang begitu kuat, lucu, cantik, baik, sholehah, mau belajar bersama, dan mas suka sekali dengan tingkah random kamu saat bersama mas. I will love u entire of my life 
      Thank you for existing, for choosing me every day, and for letting me love you this much. Here's to more laughs, hugs, and shared dreams.

      Happy birthday once again, my heart. I love you more than words can say. ♥
    </div>
  </div>

  <audio id="bg-music" src="passacaglia.mp3" autoplay loop muted></audio>
  <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
  <script>
    const fullLetter = `happy birthday to my mbill my sweetie pie! 🖤

i can't believe i can say this to u babee, at this moment when my girl was born and i just want to take a moment to tell you how much you mean to me. every day with you is a new adventure, and i cherish every single moment we share. 
On your birthday, i want to remind you of all the joy and love you bring into my life. your smile lights up my world, and your laughter is music to my ears. i am so grateful for every hug, every kiss, and every moment we spend together.


with all my love,
your future husband - Ayass >⩊<`;

    let password = "1020";
    let input = "";
    let fallingStarted = false;

    function press(num) {
      if (input.length < 4) {
        input += num;
        document.getElementById('inputDisplay').innerText = input.padStart(4, '0');
      }
      if (input.length === 4 && input === password) {
        goToPage(1);
      } else if (input.length === 4) {
        alert("Password salah, coba lagi yaa sayangku!");
        input = "";
        document.getElementById('inputDisplay').innerText = "0000";
      }
    }

    function goToPage(pageNum) {
      const pages = document.querySelectorAll('.page');
      pages.forEach(p => p.classList.remove('active'));
      const next = document.getElementById(`page${pageNum}`);
      next.classList.add('active');

      // Musik passacaglia.mp3 diputar dari awal dan tetap lanjut di semua page
      const music = document.getElementById("bg-music");
      music.muted = false;
      music.play().catch(e => console.log("Autoplay blocked:", e));

      if (pageNum === 3) {
        confetti({ particleCount: 150, spread: 100, origin: { y: 0.6 } });
        typeText(fullLetter, document.getElementById('letterText'), 25);
        startFallingSymbols();
      }
    }

    function typeText(text, element, speed) {
      element.innerHTML = '';
      let i = 0;
      function type() {
        if (i < text.length) {
          element.innerHTML += text.charAt(i);
          i++;
          setTimeout(type, speed);
        }
      }
      type();
    }

    function startFallingSymbols() {
      if (fallingStarted) return;
      fallingStarted = true;
      setInterval(() => {
        const el = document.createElement('div');
        el.classList.add('falling');
        const isHeart = Math.random() < 0.5;
        el.innerText = isHeart ? '💙' : '⭐';
        el.classList.add(isHeart ? 'blue-heart' : 'yellow-star');
        el.style.left = Math.random() * 100 + 'vw';
        el.style.animationDuration = (3 + Math.random() * 2) + 's';
        document.body.appendChild(el);
        setTimeout(() => el.remove(), 6000);
      }, 300);
    }
  </script>
</body>
</html>
