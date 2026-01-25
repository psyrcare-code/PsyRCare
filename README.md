<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Offers</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: 'Playfair Display', serif;
  text-align: center;
}

/* شاشة الترحيب */
#intro-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: black;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

#intro-text {
  font-size: 26px;
  max-width: 720px;
  line-height: 1.9;
  letter-spacing: 0.6px;
  white-space: pre-line;
}

/* العنوان */
h1 {
  margin-top: 50px;
  font-size: 34px;
  font-weight: normal;
}

/* العروض */
.offers-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 40px auto;
  max-width: 1100px;
}

.offer-card {
  background: #0e0e0e;
  border: 1px solid #222;
  border-radius: 14px;
  padding: 22px;
  margin: 15px;
  width: 270px;
  transition: 0.3s;
}

.offer-card:hover {
  transform: scale(1.02);
  border-color: #555;
}

.offer-title {
  font-size: 20px;
  margin-bottom: 12px;
}

.offer-desc {
  font-size: 14px;
  color: #bbb;
  margin-bottom: 18px;
}

.offer-price {
  font-size: 20px;
  margin-bottom: 18px;
}

.btn {
  display: inline-block;
  padding: 10px 22px;
  border: 1px solid #777;
  color: white;
  text-decoration: none;
  border-radius: 8px;
  transition: 0.3s;
  font-size: 14px;
}

.btn:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div id="intro-overlay">
  <div id="intro-text"></div>
</div>

<h1>Available Conversations</h1>

<div class="offers-container">

  <div class="offer-card">
    <div class="offer-title">Free Introduction</div>
    <div class="offer-desc">A short meeting to ask questions and discover how PsyRCare works.</div>
    <div class="offer-price">Free</div>
    <a href="order.html" class="btn">Start</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">30-Minute Conversation</div>
    <div class="offer-desc">A simple and calm space to talk, share thoughts, and gain clarity.</div>
    <div class="offer-price">$5</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">1-Hour Conversation</div>
    <div class="offer-desc">A longer discussion to explore ideas, feelings, and personal questions.</div>
    <div class="offer-price">$10</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">1.5-Hour Conversation</div>
    <div class="offer-desc">A deeper exchange designed for reflection and meaningful dialogue.</div>
    <div class="offer-price">$15</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">2-Hour Conversation</div>
    <div class="offer-desc">An extended time to express yourself and explore your thoughts freely.</div>
    <div class="offer-price">$20</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">2.5-Hour Conversation</div>
    <div class="offer-desc">A long and focused dialogue for deeper understanding and perspective.</div>
    <div class="offer-price">$25</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">3-Hour Conversation</div>
    <div class="offer-desc">A complete session for extended discussion and thoughtful exploration.</div>
    <div class="offer-price">$30</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">3.5-Hour Conversation</div>
    <div class="offer-desc">A long-form conversation for those who need more time and depth.</div>
    <div class="offer-price">$35</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">4-Hour Conversation</div>
    <div class="offer-desc">An immersive dialogue experience with space for reflection and exchange.</div>
    <div class="offer-price">$40</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">4.5-Hour Conversation</div>
    <div class="offer-desc">A long and calm conversation designed for deep personal expression.</div>
    <div class="offer-price">$45</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">5-Hour Full Conversation</div>
    <div class="offer-desc">A complete extended dialogue for those who want maximum time and focus.</div>
    <div class="offer-price">$50</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

</div>

<script>
window.onload = function() {
  const name = localStorage.getItem("userName") || "Friend";
  const textElement = document.getElementById("intro-text");
  const overlay = document.getElementById("intro-overlay");

  const message = `${name},

you did not arrive here by chance.
This space was created for thoughtful conversations,
calm reflection, and honest dialogue.

Take your time.
You are welcome in PsyRCare.`;

  let index = 0;

  function typeText() {
    if (index < message.length) {
      textElement.innerHTML += message.charAt(index);
      index++;
      setTimeout(typeText, 45);
    } else {
      setTimeout(() => {
        overlay.style.opacity = "0";
        overlay.style.transition = "2s";
        setTimeout(() => overlay.style.display = "none", 2000);
      }, 2000);
    }
  }

  typeText();
};
</script>

</body>
</html>
