<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>I'm Sorry Kritika ❤️</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght=300;400;600;700&family=Great+Vibes&display=swap" rel="stylesheet">
<style>
html { scroll-behavior: smooth; }

*, *::before, *::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
}

body {
  background: linear-gradient(135deg, #090015, #120024, #22003f, #30004d);
  background-size: 400% 400%;
  animation: bg 15s ease infinite;
  overflow-x: hidden;
  color: white;
}

@keyframes bg {
  0%   { background-position: 0% 50%; }
  50%  { background-position: 100% 50%; }
  100% { background-position: 0% 50%; }
}

canvas {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  z-index: -1;
  pointer-events: none;
}

/* ── Page Loader ── */
#loader {
  position: fixed;
  inset: 0;
  background: #060010;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  z-index: 100000;
  transition: opacity 1s ease;
}
.loaderHeart { font-size: 80px; animation: heartbeat 1s infinite; }
#loader p { font-size: 22px; margin-top: 20px; color: #ff86c4; opacity: .8; }

/* ── Envelope Intro ── */
#intro {
  position: fixed;
  inset: 0;
  background: #070010;
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 99999;
  opacity: 0;
  transition: opacity 1.5s ease;
}
#intro.visible {
  display: flex;
  opacity: 1;
}

.envelope {
  position: relative;
  width: 260px;
  height: 180px;
  cursor: pointer;
}

.front {
  position: absolute;
  width: 100%; height: 100%;
  background: #ff4d8d;
  border-radius: 10px;
}
.flap {
  position: absolute;
  top: 0; left: 0;
  width: 0; height: 0;
  border-left: 130px solid transparent;
  border-right: 130px solid transparent;
  border-top: 90px solid #ff79aa;
  transform-origin: top center;
  transition: transform 1s ease;
  z-index: 2;
}
.flap.open { transform: rotateX(180deg); }
.text {
  position: absolute;
  width: 100%; height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  font-size: 24px;
  font-weight: bold;
  color: white;
  z-index: 1;
}

/* ── Scroll Progress ── */
#progress {
  position: fixed;
  top: 0; left: 0;
  height: 4px; width: 0;
  background: linear-gradient(90deg, #ff2d95, #ff5ca8);
  z-index: 999999;
  transition: width .1s linear;
  pointer-events: none;
}

/* ── Moon / Aurora ── */
.moon {
  position: fixed;
  top: 40px; right: 40px;
  width: 180px; height: 180px;
  border-radius: 50%;
  background: white;
  box-shadow: 0 0 60px white, 0 0 120px #fff, 0 0 200px rgba(255,255,255,.6);
  opacity: .25;
  z-index: -2;
  pointer-events: none;
}
.aurora {
  position: fixed;
  inset: 0;
  z-index: -3;
  pointer-events: none;
  background:
    radial-gradient(circle at 20% 20%, rgba(255,0,120,.25), transparent 35%),
    radial-gradient(circle at 80% 30%, rgba(100,150,255,.2), transparent 40%),
    radial-gradient(circle at 50% 80%, rgba(255,255,255,.08), transparent 40%);
  animation: auroraMove 15s ease-in-out infinite alternate;
}
@keyframes auroraMove {
  from { transform: scale(1) rotate(0deg); }
  to   { transform: scale(1.2) rotate(8deg); }
}

/* ── Quote ── */
.quote {
  margin: 80px auto;
  width: 90%; max-width: 700px;
  font-size: 30px;
  font-family: 'Great Vibes', cursive;
  line-height: 60px;
  text-align: center;
  color: #ffd6ea;
  text-shadow: 0 0 15px #ff77b7;
  animation: fadeQuote 3s infinite alternate;
}
@keyframes fadeQuote {
  from { opacity: .5; transform: scale(.98); }
  to   { opacity: 1;  transform: scale(1.02); }
}

/* ── Main Container / Card ── */
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 30px;
}
.card {
  width: 900px;
  max-width: 95%;
  padding: 50px;
  border-radius: 30px;
  background: rgba(255,255,255,.08);
  backdrop-filter: blur(25px);
  -webkit-backdrop-filter: blur(25px);
  border: 1px solid rgba(255,255,255,.15);
  box-shadow: 0 15px 45px rgba(0,0,0,.35), 0 0 80px rgba(255,80,170,.25);
  text-align: center;
  animation: fadeIn 2s ease;
  transition: opacity 1.2s ease;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(40px); }
  to   { opacity: 1; transform: translateY(0); }
}

h1 {
  font-size: 70px;
  font-family: 'Great Vibes', cursive;
  color: #ff5ca8;
  text-shadow: 0 0 15px #ff2d95, 0 0 35px #ff5ca8;
  margin-bottom: 20px;
}
h2 { font-size: 32px; margin-bottom: 30px; font-weight: 300; }

#line {
  font-size: 20px;
  line-height: 40px;
  min-height: 350px;
  text-align: left;
  white-space: pre-line;
}

/* ── Button ── */
button {
  margin-top: 40px;
  padding: 18px 45px;
  border: none;
  border-radius: 50px;
  font-size: 20px;
  cursor: pointer;
  background: #ff2d95;
  color: white;
  transition: transform .4s;
  animation: glow 2s infinite alternate;
  -webkit-tap-highlight-color: transparent;
}
@keyframes glow {
  from { box-shadow: 0 0 15px #ff2d95; }
  to   { box-shadow: 0 0 35px #ff2d95, 0 0 60px #ff5ca8; }
}
button:hover { transform: scale(1.08); }
button:active { transform: scale(.97); }

/* ── Timeline ── */
.timeline { margin-top: 70px; text-align: left; }
.timeline h2 { text-align: center; margin-bottom: 35px; color: #ff86c4; }
.memory {
  display: flex; gap: 20px;
  padding: 20px; margin: 20px 0;
  background: rgba(255,255,255,.06);
  border-radius: 20px;
  transition: .4s;
}
.memory:hover { transform: translateX(10px); background: rgba(255,255,255,.12); }
.memory span { font-size: 35px; flex-shrink: 0; }
.memory p { font-size: 18px; line-height: 32px; }

/* ── Promise ── */
.promise {
  margin-top: 70px; padding: 35px;
  border-radius: 25px;
  background: rgba(255,255,255,.08);
  text-align: center;
}
.promise h2 { color: #ff7bb9; margin-bottom: 25px; }
.promise p { font-size: 20px; line-height: 40px; }

/* ── Sorry Section ── */
.sorrySection { margin-top: 80px; text-align: center; }
.reason {
  margin: 25px auto; padding: 20px;
  max-width: 700px;
  background: rgba(255,255,255,.08);
  border-radius: 18px;
  font-size: 22px; line-height: 35px;
  transition: .4s;
}
.reason:hover { transform: scale(1.04); background: rgba(255,255,255,.15); }

/* ── Heart Box ── */
.heartBox { margin-top: 70px; }
.bigHeart { font-size: 90px; animation: heartbeat 1s infinite; }
@keyframes heartbeat {
  0%   { transform: scale(1); }
  25%  { transform: scale(1.2); }
  50%  { transform: scale(.95); }
  75%  { transform: scale(1.25); }
  100% { transform: scale(1); }
}
.heartBox h3 { margin-top: 20px; font-size: 34px; color: #ff7fbf; }
.heartBox p  { font-size: 28px; margin-top: 15px; }

/* ── Ending Section ── */
.ending {
  margin-top: 120px; padding: 60px;
  text-align: center;
  background: rgba(255,255,255,.06);
  border-radius: 25px;
}
.ending h1 { font-family: 'Great Vibes', cursive; font-size: 70px; color: #ff80bf; }
.ending p  { font-size: 22px; line-height: 40px; margin-top: 30px; }

/* ── Signature ── */
.signature {
  margin-top: 60px;
  font-family: 'Great Vibes', cursive;
  font-size: 36px;
  opacity: .8;
  animation: fadeQuote 3s infinite alternate;
}

footer { margin-top: 40px; font-size: 15px; opacity: .7; }

/* ── Floating Hearts keyframe ── */
@keyframes floatHeart {
  0%   { transform: translateY(0) rotate(0deg); opacity: .15; }
  100% { transform: translateY(-130vh) rotate(360deg); opacity: 0; }
}

/* ── Ending Card special styles ── */
.ending-card-title {
  font-size: 75px;
  font-family: 'Great Vibes', cursive;
  color: #ff5ca8;
  text-shadow: 0 0 15px #ff2d95, 0 0 35px #ff5ca8;
}
.ending-card-sig {
  margin-top: 60px;
  font-family: 'Great Vibes', cursive;
  font-size: 36px;
  opacity: .8;
  animation: fadeQuote 3s infinite alternate;
}

/* ── Mobile ── */
@media (max-width: 768px) {
  .card  { padding: 25px; }
  h1     { font-size: 50px; }
  h2     { font-size: 24px; }
  #line  { font-size: 17px; line-height: 32px; }
  button { width: 100%; }
  .moon  { width: 100px; height: 100px; top: 15px; right: 15px; }
  .quote { font-size: 22px; line-height: 45px; }
  .ending-card-title { font-size: 50px; }
}
</style>
</head>
<body>

<div id="loader">
  <div class="loaderHeart">❤️</div>
  <p>Loading Memories...</p>
</div>

<div id="progress"></div>

<canvas id="stars"></canvas>
<div class="aurora"></div>
<div class="moon"></div>

<div id="intro">
  <div class="envelope" id="envelope" role="button" aria-label="Open the letter">
    <div class="front"></div>
    <div class="flap" id="flap"></div>
    <div class="text">💌<br>Open Me</div>
  </div>
</div>

<div id="mainContainer" style="display:none;">

  <div class="quote">
"If I could go back in time...
I would still choose you,

but this time...

I would choose my words more carefully."
  </div>

  <div class="container">
    <div class="card" id="card">
      <h1>I'm Sorry ❤️</h1>
      <h2>Dear Kritika</h2>
      <div id="line"></div>
      <button id="forgiveMeBtn">Can You Forgive Me? 🥺❤️</button>

      <div class="timeline">
        <h2>Our Memories ❤️</h2>
        <div class="memory">
          <span>🌸</span>
          <p>The day you came into my life,
everything started feeling beautiful.</p>
        </div>
        <div class="memory">
          <span>😊</span>
          <p>Your smile became my favourite reason
to smile every day.</p>
        </div>
        <div class="memory">
          <span>💬</span>
          <p>Every conversation with you
became my happiest memory.</p>
        </div>
        <div class="memory">
          <span>❤️</span>
          <p>I never wanted to lose you...
I only wanted to build a beautiful future with you.</p>
        </div>
        <div class="memory">
          <span>🥺</span>
          <p>If I could go back to that day,
I would choose my words more carefully.</p>
        </div>
      </div>

      <div class="promise">
        <h2>One Promise...</h2>
        <p>
          I cannot change the past.

          But I can promise one thing...

          I'll never stop respecting you.

          I'll never stop being thankful
          for every beautiful memory
          you gave me.

          Whether you forgive me or not...

          You'll always have
          a special place in my heart.

          ❤️
        </p>
      </div>

      <section class="sorrySection">
        <h2>Why I'm Sorry...</h2>
        <div class="reason">💔 I never wanted to hurt you.</div>
        <div class="reason">🥺 I chose the wrong words.</div>
        <div class="reason">❤️ My intention was to build our future,
not to lose you.</div>
        <div class="reason">🌹 You were never a burden.
You were always my happiness.</div>
        <div class="reason">✨ If I could relive that moment,
I would choose love over fear.</div>

        <div class="heartBox">
          <div class="bigHeart">❤️</div>
          <h3>Every Beat Says...</h3>
          <p>I'm Sorry, Kritika</p>
        </div>
      </section>

      <section class="ending">
        <h1>Thank You ❤️</h1>
        <p>
          Thank you for every smile.

          Thank you for every memory.

          Thank you for making me feel special.

          No matter what happens,

          I will always respect you.

          I wish you happiness,

          today and always.
        </p>
      </section>

      <div class="signature">Made by Sarthak ❤️</div>
      <footer>Made with all my heart ❤️</footer>
    </div>
  </div>

</div>

<script>
(function () {
  "use strict";

  var loader        = document.getElementById("loader");
  var intro         = document.getElementById("intro");
  var flap          = document.getElementById("flap");
  var envelope      = document.getElementById("envelope");
  var mainContainer = document.getElementById("mainContainer");
  var lineEl        = document.getElementById("line");
  var card          = document.getElementById("card");
  var progressBar   = document.getElementById("progress");
  var canvas        = document.getElementById("stars");
  var ctx           = canvas.getContext("2d");

  /* ── Stars ── */
  var stars = [];

  function resizeCanvas() {
    canvas.width  = window.innerWidth;
    canvas.height = window.innerHeight;
    stars = [];
    for (var i = 0; i < 250; i++) {
      stars.push({
        x: Math.random() * canvas.width,
        y: Math.random() * canvas.height,
        r: Math.random() * 2,
        d: 0.3 + Math.random() * 0.7
      });
    }
  }
  resizeCanvas();
  window.addEventListener("resize", resizeCanvas);

  function drawStars() {
    ctx.clearRect(0, 0, canvas.width, canvas.height);
    ctx.fillStyle = "white";
    for (var i = 0; i < stars.length; i++) {
      var s = stars[i];
      ctx.beginPath();
      ctx.arc(s.x, s.y, s.r, 0, Math.PI * 2);
      ctx.fill();
      s.y += s.d;
      if (s.y > canvas.height) {
        s.y = 0;
        s.x = Math.random() * canvas.width;
      }
    }
    requestAnimationFrame(drawStars);
  }
  drawStars();

  /* ── Loader → Envelope ── */
  function startSequence() {
    setTimeout(function () {
      loader.style.opacity = "0";
      setTimeout(function () {
        loader.style.display = "none";
        intro.style.display = "flex";
        intro.offsetHeight;
        intro.classList.add("visible");
      }, 1000);
    }, 1800);
  }

  if (document.readyState === "loading") {
    document.addEventListener("DOMContentLoaded", startSequence);
  } else {
    startSequence();
  }

  /* ── Envelope open ── */
  function openLetter() {
    flap.classList.add("open");
    setTimeout(function () {
      intro.classList.remove("visible");
      intro.style.opacity = "0";
      setTimeout(function () {
        intro.style.display = "none";
        mainContainer.style.display = "block";
        typing();
      }, 1200);
    }, 1000);
  }

  envelope.addEventListener("click", openLetter);
  envelope.addEventListener("touchend", function (e) {
    e.preventDefault();
    openLetter();
  });

  /* ── Typewriter ── */
  var text = "Pata nahi ye words tumhare dil tak pahunch payenge ya nahi...\n\nLekin mujhe apni baat sachai se kehni hai.\n\nJo maine uss din kaha tha,\nwoh mere dil ki baat nahi thi.\n\nFever aur stress ki wajah se\nmain apne emotions ko sahi tarah express nahi kar paya.\n\nMera kabhi bhi tumse door jaana\nya tumhe lose karna intention nahi tha.\n\nMain sirf itna chahta tha\nki main apni studies aur future par focus karun,\ntaaki ek din hum dono ka future secure ho.\n\nLekin maine apni baat itni galat tarike se boli\nki tumhe laga main tumhe chhod raha hoon.\n\nUs baat ka mujhe har din regret hota hai.\n\nTumne kabhi mera time waste nahi kiya.\n\nTum meri life ka sabse beautiful part thi...\naur ho.\n\nAgar meri wajah se tumhari aankhon mein aansu aaye hain,\n\nI'm Truly Sorry.\n\nMain tumse koi pressure nahi kar raha.\n\nBas ek baar meri baat samajhne ki koshish karna.\n\nAgar tum mujhe ek chance dogi,\n\nToh main words se nahi,\napne actions se prove karunga.\n\nThank You...\n\nFor Every Smile ❤️\n\nFor Every Memory ❤️\n\nFor Every Moment ❤️\n\nI'm Sorry Kritika... ❤️";

  var charIndex = 0;
  var typingTimer = null;

  function typing() {
    if (charIndex < text.length) {
      lineEl.textContent += text[charIndex++];
      typingTimer = setTimeout(typing, 35);
    }
  }

  /* ── Scroll progress bar ── */
  window.addEventListener("scroll", function () {
    var total = document.documentElement.scrollHeight - window.innerHeight;
    var pct   = total > 0 ? (window.scrollY / total) * 100 : 0;
    progressBar.style.width = pct + "%";
  });

  /* ── Floating background hearts ── */
  setInterval(function () {
    var h = document.createElement("div");
    h.textContent = "🤍";
    h.style.cssText =
      "position:fixed;" +
      "left:" + (Math.random() * 100) + "vw;" +
      "bottom:-60px;" +
      "font-size:" + (20 + Math.random() * 25) + "px;" +
      "pointer-events:none;" +
      "z-index:0;" +
      "animation:floatHeart " + (10 + Math.random() * 8) + "s linear forwards;";
    document.body.appendChild(h);
    setTimeout(function () { if (h.parentNode) h.parentNode.removeChild(h); }, 18000);
  }, 1200);

  /* ── Confetti ── */
  function confetti() {
    for (var i = 0; i < 150; i++) {
      (function () {
        var c = document.createElement("div");
        c.textContent = "✨";
        c.style.position      = "fixed";
        c.style.left          = (Math.random() * 100) + "vw";
        c.style.top           = "-30px";
        c.style.fontSize      = "20px";
        c.style.zIndex        = "9999";
        c.style.pointerEvents = "none";
        c.style.transition    = "top 4s linear, opacity 4s linear";
        document.body.appendChild(c);
        requestAnimationFrame(function () {
          requestAnimationFrame(function () {
            c.style.top     = "110vh";
            c.style.opacity = "0";
          });
        });
        setTimeout(function () { if (c.parentNode) c.parentNode.removeChild(c); }, 4200);
      })();
    }
  }

  /* ── Fireworks ── */
  function fireworks() {
    var emojis = ["❤️", "💖", "✨", "🌹"];
    for (var i = 0; i < 30; i++) {
      (function (delay) {
        setTimeout(function () {
          var el = document.createElement("div");
          el.textContent         = emojis[Math.floor(Math.random() * emojis.length)];
          el.style.position      = "fixed";
          el.style.left          = (Math.random() * 100) + "vw";
          el.style.top           = (Math.random() * 80)  + "vh";
          el.style.fontSize      = (20 + Math.random() * 30) + "px";
          el.style.pointerEvents = "none";
          el.style.zIndex        = "9999";
          el.style.opacity       = "1";
          el.style.transition    = "transform 2s ease-out, opacity 2s ease-out";
          document.body.appendChild(el);
          requestAnimationFrame(function () {
            requestAnimationFrame(function () {
              el.style.transform = "translateY(-" + (80 + Math.random() * 120) + "px) scale(2)";
              el.style.opacity   = "0";
            });
          });
          setTimeout(function () { if (el.parentNode) el.parentNode.removeChild(el); }, 2200);
        }, delay);
      })(i * 80);
    }
  }

  /* ── Show Ending ── */
  var endingShown = false;

  function showEnding() {
    if (endingShown) return;
    endingShown = true;

    confetti();
    fireworks();

    if (typingTimer) clearTimeout(typingTimer);

    card.style.opacity = "0";

    setTimeout(function () {
      card.innerHTML =
        '<div class="ending-card-title">❤️</div>' +
        '<h2 style="margin-top:20px;">No Matter What Happens...</h2>' +
        '<p style="font-size:24px;line-height:45px;margin-top:40px;">' +
        'You will always have a special place inside my heart.<br><br>' +
        'I never wanted to lose you.<br><br>' +
        "I'm Sorry...<br><br>Forever." +
        '</p>' +
        '<div class="ending-card-sig">Made by Sarthak ❤️</div>';

      card.style.opacity = "1";
    }, 1200);
  }

  document.getElementById("forgiveMeBtn").addEventListener("click", showEnding);

})();
</script>
</body>
</html>
