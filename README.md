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
  max-width: 700px;
  line-height: 1.9;
  letter-spacing: 0.6px;
  text-align: center;
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
  max-width: 1000px;
}

.offer-card {
  background: #0e0e0e;
  border: 1px solid #222;
  border-radius: 14px;
  padding: 22px;
  margin: 15px;
  width: 260px;
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

<h1>Our Sessions</h1>

<div class="offers-container">

  <div class="offer-card">
    <div class="offer-title">Free Intro Session</div>
    <div class="offer-desc">A gentle first meeting in a safe space.</div>
    <div class="offer-price">Free</div>
    <a href="order.html" class="btn">Begin</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">30-Minute Session</div>
    <div class="offer-desc">A calm conversation to understand your feelings.</div>
    <div class="offer-price">$5</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">1-Hour Session</div>
    <div class="offer-desc">A deeper therapeutic dialogue.</div>
    <div class="offer-price">$10</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="offer-card">
    <div class="offer-title">1.5-Hour Deep Session</div>
    <div class="offer-desc">A longer journey into understanding and clarity.</div>
    <div class="offer-price">$15</div>
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
This space was created for moments like yours.

Take a breath.
You are welcome in PsyRCare.`;

  let index = 0;

  function typeText() {
    if (index < message.length) {
      textElement.innerHTML += message.charAt(index);
      index++;
      setTimeout(typeText, 45); // سرعة الكتابة (يمكن تعديلها)
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

