# Happy-Birthday-Sirr

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="theme-color" content="#090807">
<title>A Birthday Surprise for Sir</title>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@300;400;500;600&display=swap');

:root {
  --gold: #d6b56e;
  --light-gold: #f4dfaa;
  --bg: #090807;
  --muted: #a69b86;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  background: var(--bg);
  color: #f7f0e4;
  font-family: 'DM Sans', sans-serif;
  overflow-x: hidden;
}

body::before {
  content: "";
  position: fixed;
  inset: 0;
  pointer-events: none;
  z-index: 1;
  opacity: .13;
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 180 180' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.9' numOctaves='3' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.2'/%3E%3C/svg%3E");
}

button {
  font-family: inherit;
  cursor: pointer;
}

.gold {
  color: var(--gold);
}

.serif {
  font-family: 'Cormorant Garamond', serif;
}

.section {
  position: relative;
  z-index: 2;
  padding: 100px 22px;
  text-align: center;
}

.eyebrow {
  color: var(--gold);
  text-transform: uppercase;
  letter-spacing: 5px;
  font-size: 10px;
  font-weight: 600;
  margin-bottom: 20px;
}

.section-title {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(38px, 7vw, 65px);
  font-weight: 500;
  line-height: 1.1;
  margin-bottom: 22px;
}

.section-desc {
  max-width: 570px;
  margin: auto;
  color: #aaa08e;
  font-size: 14px;
  line-height: 2;
}

/* MUSIC PLAYER */

.music-bar {
  position: sticky;
  top: 0;
  z-index: 100;
  background: rgba(12, 11, 9, .95);
  border-bottom: 1px solid rgba(214,181,110,.25);
  backdrop-filter: blur(18px);
  padding: 12px 18px;
}

.music-inner {
  max-width: 900px;
  margin: auto;
  display: flex;
  align-items: center;
  gap: 13px;
}

.music-icon {
  color: var(--gold);
  font-size: 21px;
}

.music-info {
  flex: 1;
  min-width: 0;
}

.music-info strong {
  font-size: 12px;
  letter-spacing: 1px;
  display: block;
}

.music-info span {
  font-size: 10px;
  color: var(--muted);
}

#musicBtn {
  background: linear-gradient(135deg,#f2d99f,#b28b43);
  color: #17110a;
  border: none;
  border-radius: 30px;
  padding: 10px 19px;
  font-size: 11px;
  font-weight: bold;
  white-space: nowrap;
}

.music-bars {
  display: flex;
  gap: 3px;
  align-items: center;
  height: 22px;
}

.music-bars i {
  display: block;
  width: 3px;
  height: 5px;
  background: var(--gold);
  border-radius: 5px;
}

.music-bars.playing i {
  animation: music 0.65s ease-in-out infinite alternate;
}

.music-bars i:nth-child(2) {animation-delay:.2s}
.music-bars i:nth-child(3) {animation-delay:.4s}
.music-bars i:nth-child(4) {animation-delay:.1s}

@keyframes music {
  to {height:20px}
}

/* HERO */

.hero {
  min-height: 91vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  position: relative;
  overflow: hidden;
  padding: 70px 20px;
  background:
    radial-gradient(ellipse at center, rgba(160,115,40,.15), transparent 65%),
    #090807;
}

.hero::after {
  content: "";
  position: absolute;
  width: 320px;
  height: 320px;
  border: 1px solid rgba(214,181,110,.15);
  border-radius: 50%;
  box-shadow: 0 0 0 35px rgba(214,181,110,.025),
              0 0 0 70px rgba(214,181,110,.02);
}

.hero-content {
  position: relative;
  z-index: 3;
  max-width: 750px;
  animation: fadeUp 1.6s ease;
}

.hero-small {
  color: var(--gold);
  letter-spacing: 6px;
  font-size: 10px;
  text-transform: uppercase;
  margin-bottom: 30px;
}

.hero h1 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(70px, 14vw, 125px);
  font-weight: 500;
  line-height: .9;
  background: linear-gradient(130deg,#fff3cf,#c69a4d,#f9e8bc);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  text-shadow: 0 5px 50px rgba(214,181,110,.1);
}

.hero h2 {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(38px, 7vw, 67px);
  color: #fff7e8;
  font-weight: 400;
  margin-top: 12px;
}

.hero-line {
  width: 65px;
  height: 1px;
  background: var(--gold);
  margin: 32px auto;
}

.hero p {
  font-family: 'Cormorant Garamond', serif;
  font-size: 22px;
  color: #bfb29a;
  line-height: 1.7;
}

.primary-btn {
  margin-top: 38px;
  padding: 16px 32px;
  border: 1px solid var(--gold);
  background: transparent;
  color: var(--light-gold);
  letter-spacing: 2px;
  font-size: 10px;
  text-transform: uppercase;
  transition: .4s;
}

.primary-btn:hover {
  background: var(--gold);
  color: #120e08;
  box-shadow: 0 0 35px rgba(214,181,110,.3);
}

/* INTRO */

.intro-card {
  max-width: 760px;
  margin: 45px auto 0;
  border: 1px solid rgba(214,181,110,.25);
  padding: 45px 30px;
  background: linear-gradient(145deg,rgba(214,181,110,.06),rgba(255,255,255,.01));
}

.intro-card p {
  font-family: 'Cormorant Garamond', serif;
  font-size: clamp(21px,4vw,29px);
  line-height: 1.8;
  color: #d5cbb9;
}

.intro-card strong {
  color: var(--light-gold);
  font-weight: 500;
}

/* PHOTO GALLERY */

.gallery {
  max-width: 850px;
  margin: 50px auto 0;
  display: grid;
  grid-template-columns: repeat(2,1fr);
  gap: 17px;
}

.photo {
  overflow: hidden;
  aspect-ratio: 1 / 1;
  border: 1px solid rgba(214,181,110,.35);
  background: #17130e;
  cursor: zoom-in;
  position: relative;
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
  transition: transform .7s ease, filter .5s;
}

.photo:hover img {
  transform: scale(1.06);
  filter: brightness(1.08);
}

.photo::after {
  content: "";
  position: absolute;
  inset: 0;
  border: 7px solid rgba(214,181,110,.04);
  pointer-events: none;
}

/* PERSONAL MESSAGE */

.message-box {
  max-width: 720px;
  margin: 45px auto 0;
  padding: 40px 30px;
  border-left: 2px solid var(--gold);
  background: rgba(255,255,255,.025);
  text-align: left;
}

.message-box p {
  font-family: 'Cormorant Garamond', serif;
  color: #d7cbb7;
  font-size: 23px;
  line-height: 1.9;
  margin-bottom: 17px;
}

.message-box p:last-child {
  margin-bottom: 0;
}

/* GRATITUDE CARDS */

.cards {
  max-width: 850px;
  margin: 50px auto 0;
  display: grid;
  grid-template-columns: repeat(3,1fr);
  gap: 15px;
}

.card {
  padding: 30px 15px;
  border: 1px solid rgba(214,181,110,.19);
  background: linear-gradient(150deg,rgba(214,181,110,.07),transparent);
  transition: .4s;
}

.card:hover {
  transform: translateY(-7px);
  border-color: var(--gold);
}

.card-icon {
  font-size: 25px;
  color: var(--gold);
  margin-bottom: 16px;
}

.card h3 {
  font-family: 'Cormorant Garamond',serif;
  font-size: 25px;
  color: var(--light-gold);
  margin-bottom: 10px;
  font-weight: 500;
}

.card p {
  color: #a99e8c;
  font-size: 12px;
  line-height: 1.8;
}

/* QUOTE */

.quote-section {
  background: linear-gradient(180deg,transparent,rgba(214,181,110,.06),transparent);
  padding: 110px 20px;
}

.quote {
  max-width: 760px;
  margin: auto;
  font-family: 'Cormorant Garamond',serif;
  font-size: clamp(31px,6vw,51px);
  line-height: 1.5;
  color: #f0e1c2;
}

.quote span {
  color: var(--gold);
}

/* SURPRISE */

.gift {
  width: 115px;
  height: 100px;
  margin: 42px auto 25px;
  position: relative;
  cursor: pointer;
  transition: .4s;
}

.gift:hover {
  transform: scale(1.1);
}

.gift-box {
  position: absolute;
  bottom: 0;
  width: 115px;
  height: 75px;
  background: linear-gradient(120deg,#e5c477,#a47732);
  border: 1px solid #f6dfaa;
  border-radius: 4px;
}

.gift-box::before {
  content: "";
  position: absolute;
  width: 17px;
  height: 100%;
  background: #fff0c4;
  left: 49px;
}

.gift-lid {
  position: absolute;
  top: 7px;
  left: -6px;
  width: 127px;
  height: 20px;
  background: #e8cb83;
  border-radius: 3px;
  z-index: 2;
}

.gift-bow {
  position: absolute;
  width: 35px;
  height: 20px;
  border: 5px solid #f9e9c5;
  border-radius: 50%;
  top: -12px;
  left: 39px;
  z-index: 3;
}

.gift-message {
  max-width: 580px;
  margin: 25px auto 0;
  padding: 35px 25px;
  background: rgba(214,181,110,.07);
  border: 1px solid rgba(214,181,110,.35);
  display: none;
  animation: fadeUp .8s ease;
}

.gift-message.show {
  display: block;
}

.gift-message p {
  font-family: 'Cormorant Garamond',serif;
  font-size: 24px;
  line-height: 1.8;
  color: #e4d4b8;
}

/* ENVELOPE */

.envelope {
  width: 100px;
  height: 68px;
  margin: 35px auto;
  position: relative;
  background: #b9924f;
  cursor: pointer;
  transition: .3s;
}

.envelope:hover {
  transform: translateY(-5px);
}

.envelope::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  border-left: 50px solid transparent;
  border-right: 50px solid transparent;
  border-top: 40px solid #f1d49b;
  z-index: 2;
}

.envelope::after {
  content: "✦";
  position: absolute;
  color: #6e4b1b;
  top: 27px;
  left: 42px;
  z-index: 3;
}

.letter {
  display: none;
  max-width: 620px;
  margin: auto;
  padding: 35px 25px;
  background: #eee0c1;
  color: #392a18;
  animation: fadeUp .7s;
}

.letter.show {
  display: block;
}

.letter h3 {
  font-family: 'Cormorant Garamond',serif;
  font-size: 32px;
  margin-bottom: 15px;
}

.letter p {
  font-family: 'Cormorant Garamond',serif;
  font-size: 22px;
  line-height: 1.7;
}

/* FINAL */

.final-section {
  min-height: 80vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: radial-gradient(ellipse at center,rgba(160,115,40,.16),transparent 70%);
}

.final-content {
  max-width: 760px;
  padding: 40px 20px;
}

.final-content h2 {
  font-family: 'Cormorant Garamond',serif;
  font-size: clamp(48px,10vw,85px);
  font-weight: 500;
  background: linear-gradient(130deg,#fff2c9,#c59a4b);
  color: transparent;
  background-clip: text;
}

.final-content p {
  font-family: 'Cormorant Garamond',serif;
  font-size: 25px;
  line-height: 1.8;
  color: #c8b99d;
  margin-top: 20px;
}

.signature {
  margin-top: 45px;
  color: var(--gold);
  letter-spacing: 2px;
  font-size: 11px;
  line-height: 2.2;
}

.signature strong {
  display: block;
  font-family: 'Cormorant Garamond',serif;
  font-size: 32px;
  font-weight: 500;
  letter-spacing: 1px;
}

footer {
  text-align: center;
  padding: 30px 15px;
  color: #766b59;
  font-size: 10px;
  letter-spacing: 2px;
  border-top: 1px solid rgba(214,181,110,.15);
}

/* FLOATING EFFECTS */

.floating {
  position: fixed;
  z-index: 5;
  pointer-events: none;
  bottom: -30px;
  animation: floatUp linear forwards;
  opacity: 0;
}

@keyframes floatUp {
  0% {transform:translateY(0) rotate(0deg);opacity:0}
  15% {opacity:.7}
  80% {opacity:.55}
  100% {transform:translateY(-110vh) rotate(160deg);opacity:0}
}

.sparkle {
  position: fixed;
  z-index: 4;
  pointer-events: none;
  color: var(--gold);
  animation: sparkle 2.5s ease-in-out infinite;
}

@keyframes sparkle {
  0%,100% {opacity:.1;transform:scale(.5)}
  50% {opacity:.9;transform:scale(1.3)}
}

@keyframes fadeUp {
  from {opacity:0;transform:translateY(30px)}
  to {opacity:1;transform:translateY(0)}
}

/* LIGHTBOX */

.lightbox {
  display: none;
  position: fixed;
  inset: 0;
  z-index: 200;
  background: rgba(0,0,0,.94);
  align-items: center;
  justify-content: center;
  padding: 20px;
}

.lightbox.show {
  display: flex;
}

.lightbox img {
  max-width: 95%;
  max-height: 85vh;
  object-fit: contain;
  border: 1px solid var(--gold);
}

.close-lightbox {
  position: absolute;
  top: 20px;
  right: 25px;
  color: white;
  font-size: 35px;
  background: none;
  border: none;
}

/* SCROLL PROGRESS */

.progress {
  position: fixed;
  top: 0;
  left: 0;
  height: 2px;
  width: 0;
  background: var(--gold);
  z-index: 300;
}

/* REVEAL ANIMATIONS */

.reveal {
  opacity: 0;
  transform: translateY(35px);
  transition: opacity 1s ease, transform 1s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* RESPONSIVE */

@media(max-width:600px) {
  .section {padding:75px 18px}
  .hero {min-height:85vh}
  .cards {grid-template-columns:repeat(2,1fr)}
  .gallery {gap:10px}
  .intro-card {padding:30px 20px}
  .message-box {padding:28px 20px}
  .music-info strong {font-size:10px}
  #musicBtn {padding:10px 13px;font-size:10px}
}

@media(max-width:350px) {
  .cards {grid-template-columns:1fr}
}
</style>
</head>

<body>

<div class="progress" id="progress"></div>

<!-- MUSIC AT THE TOP -->
<div class="music-bar">
  <div class="music-inner">
    <div class="music-icon">♫</div>
    <div class="music-info">
      <strong>A LITTLE MUSIC FOR THIS SPECIAL DAY</strong>
      <span>One song • One special celebration</span>
    </div>
    <div class="music-bars" id="musicBars">
      <i></i><i></i><i></i><i></i>
    </div>
    <button id="musicBtn" onclick="toggleMusic()">▶ PLAY</button>
  </div>
</div>

<audio id="birthdayMusic" loop preload="auto">
  <source src="SONG.mp3" type="audio/mpeg">
</audio>

<!-- HERO -->
<header class="hero" id="home">
  <div class="hero-content">
    <div class="hero-small">A SPECIAL DAY • A SPECIAL PERSON</div>

    <h1>A LITTLE</h1>
    <h2>Birthday Surprise</h2>

    <div class="hero-line"></div>

    <p>
      Some people make ordinary moments<br>
      become beautiful memories.
    </p>

    <button class="primary-btn" onclick="document.getElementById('welcome').scrollIntoView({behavior:'smooth'})">
      DISCOVER YOUR SURPRISE &nbsp; ↓
    </button>
  </div>
</header>

<!-- WELCOME -->
<section class="section reveal" id="welcome">
  <div class="eyebrow">A small gesture from the heart</div>
  <h2 class="section-title">For You, <span class="gold">Sir.</span></h2>

  <div class="intro-card">
    <p>
      Not every special occasion needs grand celebrations.
      Sometimes, a few genuine words, a little effort,
      and a heartfelt wish are enough.
      <br><br>
      <strong>This little corner of the internet is made especially for you, Sir.</strong>
      <br><br>
      With respect, gratitude and warm wishes.
    </p>
  </div>
</section>

<!-- FOUR PHOTOS -->
<section class="section reveal" id="memories">
  <div class="eyebrow">A collection of moments</div>
  <h2 class="section-title">Beautiful <span class="gold">Memories</span></h2>
  <p class="section-desc">
    Every photograph holds a moment.
    Every moment has a story.
  </p>

  <div class="gallery">
    <div class="photo" onclick="openPhoto('Sir1.png')">
      <img src="Sir1.png" alt="Memory 1" loading="lazy">
    </div>
    <div class="photo" onclick="openPhoto('Sir2.png')">
      <img src="Sir2.png" alt="Memory 2" loading="lazy">
    </div>
    <div class="photo" onclick="openPhoto('Sir3.png')">
      <img src="Sir3.png" alt="Memory 3" loading="lazy">
    </div>
    <div class="photo" onclick="openPhoto('Sir4.png')">
      <img src="Sir4.png" alt="Memory 4" loading="lazy">
    </div>
  </div>
</section>

<!-- PERSONAL MESSAGE -->
<section class="section reveal">
  <div class="eyebrow">A few words from my heart</div>
  <h2 class="section-title">Dear <span class="gold">Sir,</span></h2>

  <div class="message-box">
    <p>
      Today, I just want to take a moment to wish you
      a very Happy Birthday.
    </p>

    <p>
      Thank you for sharing your knowledge, for your
      guidance, and for being someone whose presence
      makes a difference.
    </p>

    <p>
      There are many things a student learns in college,
      but some lessons and memories stay with us
      long after the classroom days are over.
    </p>

    <p>
      I sincerely wish you happiness, good health,
      peace and success in every chapter of life.
    </p>

    <p class="gold">
      You deserve all the wonderful things life has to offer.
    </p>
  </div>
</section>

<!-- GRATITUDE -->
<section class="section reveal">
  <div class="eyebrow">A little appreciation</div>
  <h2 class="section-title">With Respect & <span class="gold">Gratitude</span></h2>

  <p class="section-desc">
    Some qualities deserve appreciation, not just on birthdays,
    but every single day.
  </p>

  <div class="cards">

    <div class="card">
      <div class="card-icon">✧</div>
      <h3>Guidance</h3>
      <p>For the knowledge and direction that help students grow.</p>
    </div>

    <div class="card">
      <div class="card-icon">◇</div>
      <h3>Wisdom</h3>
      <p>For lessons that go beyond textbooks and classrooms.</p>
    </div>

    <div class="card">
      <div class="card-icon">♡</div>
      <h3>Kindness</h3>
      <p>For the little things that make a lasting difference.</p>
    </div>

    <div class="card">
      <div class="card-icon">✦</div>
      <h3>Inspiration</h3>
      <p>For reminding students that learning never stops.</p>
    </div>

    <div class="card">
      <div class="card-icon">∞</div>
      <h3>Memories</h3>
      <p>For moments that will remain special in the years ahead.</p>
    </div>

    <div class="card">
      <div class="card-icon">✧</div>
      <h3>Respect</h3>
      <p>For being someone who deserves genuine appreciation.</p>
    </div>

  </div>
</section>

<!-- QUOTE -->
<section class="quote-section section reveal">
  <div class="eyebrow">A thought to remember</div>

  <div class="quote">
    "A great teacher doesn't just teach lessons,
    <span>but leaves a positive mark</span>
    on the hearts and minds of students."
  </div>
</section>

<!-- GIFT SURPRISE -->
<section class="section reveal">
  <div class="eyebrow">Something special awaits</div>
  <h2 class="section-title">A Little <span class="gold">Surprise</span></h2>

  <p class="section-desc">
    Sir, I have kept a little something for you.
    Please open this gift.
  </p>

  <div class="gift" onclick="openGift()">
    <div class="gift-bow"></div>
    <div class="gift-lid"></div>
    <div class="gift-box"></div>
  </div>

  <p class="gold" style="font-size:11px;letter-spacing:3px">
    TAP TO OPEN YOUR GIFT
  </p>

  <div class="gift-message" id="giftMessage">
    <div class="eyebrow">A gift that comes from the heart</div>
    <p>
      If I could gift you something today,
      it would be endless happiness,
      excellent health, beautiful memories,
      and countless reasons to smile.
      <br><br>
      May every new day bring something
      wonderful into your life.
      <br><br>
      <span class="gold">You deserve the very best, Sir.</span>
    </p>
  </div>
</section>

<!-- SECRET LETTER -->
<section class="section reveal">
  <div class="eyebrow">One last little message</div>
  <h2 class="section-title">A Letter <span class="gold">For You</span></h2>

  <p class="section-desc">
    Before you leave, there is one more thing
    I would like to say.
  </p>

  <div class="envelope" onclick="openLetter()"></div>

  <p class="gold" style="font-size:10px;letter-spacing:2px">
    TAP TO OPEN THE LETTER
  </p>

  <div class="letter" id="letter">
    <h3>Dear Sir,</h3>
    <p>
      I may not always express it in words,
      but I genuinely appreciate the opportunity
      to learn from you.
      <br><br>
      Years may pass, college days may become
      memories, but the respect we have for
      good teachers remains.
      <br><br>
      Thank you for being a part of my journey.
      <br><br>
      Wishing you a beautiful birthday and
      an even more beautiful year ahead.
      <br><br>
      With sincere respect,<br>
      <strong>Biraja</strong>
    </p>
  </div>
</section>

<!-- FINAL BIRTHDAY -->
<section class="section final-section reveal" id="final">
  <div class="final-content">

    <div class="eyebrow">A wish from the heart</div>

    <h2>Happy Birthday, Sir!</h2>

    <div class="hero-line"></div>

    <p>
      Some teachers teach lessons.<br>
      Some leave memories.<br>
      And some become a beautiful part
      of our journey.
      <br><br>
      Thank you for being one of them.
    </p>

    <p class="gold">
      May your life always be filled with
      happiness, good health, peace and success.
    </p>

    <div class="signature">
      WITH SINCERE RESPECT & GRATITUDE
      <strong>Biraja</strong>
      <span>One of your students.</span>
    </div>

    <button class="primary-btn" onclick="celebrate()">
      ✦ CELEBRATE AGAIN ✦
    </button>

  </div>
</section>

<footer>
  MADE WITH RESPECT, GRATITUDE & HEARTFELT WISHES
  <br><br>
  A LITTLE BIRTHDAY GIFT BY BIRAJA
</footer>

<!-- PHOTO LIGHTBOX -->
<div class="lightbox" id="lightbox" onclick="closePhoto()">
  <button class="close-lightbox" onclick="closePhoto()">×</button>
  <img id="lightboxImg" src="" alt="Enlarged photograph">
</div>

<script>
const music = document.getElementById('birthdayMusic');
const musicBtn = document.getElementById('musicBtn');
const musicBars = document.getElementById('musicBars');

let isPlaying = false;

function toggleMusic() {
  if (isPlaying) {
    music.pause();
    isPlaying = false;
    musicBtn.innerHTML = '▶ PLAY';
    musicBars.classList.remove('playing');
  } else {
    music.play().then(() => {
      isPlaying = true;
      musicBtn.innerHTML = 'Ⅱ PAUSE';
      musicBars.classList.add('playing');
    }).catch(() => {
      alert('Please check that SONG.mp3 is uploaded correctly.');
    });
  }
}

music.addEventListener('ended', () => {
  isPlaying = false;
  musicBtn.innerHTML = '▶ PLAY';
  musicBars.classList.remove('playing');
});

// Floating hearts and sparkles
const symbols = ['♡','✦','✧','♥','⋆','✴'];

function createFloating() {
  const el = document.createElement('div');
  el.className = 'floating';
  el.innerHTML = symbols[Math.floor(Math.random()*symbols.length)];

  el.style.left = Math.random()*100 + 'vw';
  el.style.fontSize = (10+Math.random()*16)+'px';
  el.style.color = Math.random() > .45 ? '#d6b56e' : '#d99b9b';
  el.style.animationDuration = (8+Math.random()*10)+'s';

  document.body.appendChild(el);

  setTimeout(() => el.remove(),19000);
}

setInterval(createFloating,550);

// Static background sparkles
function createSparkle() {
  const el = document.createElement('div');
  el.className = 'sparkle';
  el.innerHTML = '✦';
  el.style.left = Math.random()*100+'vw';
  el.style.top = Math.random()*100+'vh';
  el.style.fontSize = (7+Math.random()*12)+'px';
  el.style.animationDelay = Math.random()*3+'s';

  document.body.appendChild(el);
}

for(let i=0;i<24;i++) createSparkle();

// Scroll progress
window.addEventListener('scroll', () => {
  const total = document.documentElement.scrollHeight-window.innerHeight;
  const progress = total > 0 ? (window.scrollY/total)*100 : 0;
  document.getElementById('progress').style.width=progress+'%';
});

// Reveal sections
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting) {
      entry.target.classList.add('visible');
    }
  });
},{threshold:.12});

document.querySelectorAll('.reveal').forEach(el=>observer.observe(el));

// Open gift
function openGift() {
  const box=document.getElementById('giftMessage');
  box.classList.toggle('show');

  if(box.classList.contains('show')) {
    burst();
  }
}

// Open letter
function openLetter() {
  const letter=document.getElementById('letter');
  letter.classList.toggle('show');

  if(letter.classList.contains('show')) {
    burst();
  }
}

// Photo enlargement
function openPhoto(src) {
  document.getElementById('lightboxImg').src=src;
  document.getElementById('lightbox').classList.add('show');
}

function closePhoto() {
  document.getElementById('lightbox').classList.remove('show');
}

// Burst animation
function burst() {
  for(let i=0;i<35;i++) {
    const el=document.createElement('div');
    el.className='floating';
    el.innerHTML=['✦','♡','♥','✨'][Math.floor(Math.random()*4)];

    el.style.left=(35+Math.random()*30)+'vw';
    el.style.bottom='30%';
    el.style.fontSize=(12+Math.random()*18)+'px';
    el.style.color='#e6c27a';
    el.style.animationDuration=(2+Math.random()*3)+'s';

    document.body.appendChild(el);
    setTimeout(()=>el.remove(),5000);
  }
}

// Final celebration
function celebrate() {
  burst();

  for(let i=0;i<5;i++) {
    setTimeout(burst,i*350);
  }
}

// Close lightbox with Escape
document.addEventListener('keydown',e=>{
  if(e.key==='Escape') closePhoto();
});
</script>

</body>
</html>
