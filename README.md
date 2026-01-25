<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Offers</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: 'Playfair Display', serif;
  text-align: center;
}

/* شاشة الترحيب */
#intro {
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

#text {
  font-size: 24px;
  max-width: 720px;
  line-height: 1.8;
  white-space: pre-line;
}

/* العنوان */
h1 {
  margin-top: 40px;
  font-size: 32px;
  font-weight: normal;
}

/* العروض */
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 30px auto;
  max-width: 1200px;
}

.card {
  background: #111;
  border: 1px solid #333;
  border-radius: 14px;
  padding: 20px;
  margin: 12px;
  width: 260px;
  transition: 0.3s;
}

.card:hover {
  transform: scale(1.03);
  border-color: #666;
}

.title {
  font-size: 18px;
  margin-bottom: 10px;
}

.desc {
  font-size: 14px;
  color: #bbb;
  margin-bottom: 12px;
}

.price {
  font-size: 18px;
  margin-bottom: 12px;
}

.btn {
  border: 1px solid white;
  padding: 8px 16px;
  color: white;
  text-decoration: none;
  display: inline-block;
  transition: 0.3s;
}

.btn:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div id="intro">
  <div id="text"></div>
</div>

<h1>Available Conversations</h1>

<div class="container">

  <div class="card">
    <div class="title">Free Introduction</div>
    <div class="desc">A short meeting to ask questions and understand how PsyRCare works.</div>
    <div class="price">Free</div>
    <a href="order.html" class="btn">Start</a>
  </div>

  <div class="card">
    <div class="title">30-Minute Conversation</div>
    <div class="desc">A calm and respectful space to share thoughts and ideas.</div>
    <div class="price">$5</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">1-Hour Conversation</div>
    <div class="desc">A longer dialogue to explore questions and personal perspectives.</div>
    <div class="price">$10</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">1.5-Hour Conversation</div>
    <div class="desc">A deeper exchange designed for reflection and meaningful discussion.</div>
    <div class="price">$15</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">2-Hour Conversation</div>
    <div class="desc">Extended time to express ideas and explore topics in depth.</div>
    <div class="price">$20</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">2.5-Hour Conversation</div>
    <div class="desc">A long and focused conversation for deeper understanding and clarity.</div>
    <div class="price">$25</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">3-Hour Conversation</div>
    <div class="desc">A complete session for extended discussion and thoughtful exploration.</div>
    <div class="price">$30</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">3.5-Hour Conversation</div>
    <div class="desc">A long-form dialogue for those who need more time and focus.</div>
    <div class="price">$35</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">4-Hour Conversation</div>
    <div class="desc">An immersive exchange with space for reflection and deep discussion.</div>
    <div class="price">$40</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">4.5-Hour Conversation</div>
    <div class="desc">A long and calm conversation designed for meaningful dialogue.</div>
    <div class="price">$45</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

  <div class="card">
    <div class="title">5-Hour Full Conversation</div>
    <div class="desc">A complete extended conversation for maximum time and focus.</div>
    <div class="price">$50</div>
    <a href="order.html" class="btn">Continue</a>
  </div>

</div>

<script>
const name = localStorage.getItem("userName") || "Friend";

const message = `${name},

you did not arrive here by chance.
This space was created for thoughtful conversations,
calm reflection, and honest dialogue.

Take your time.
Welcome to PsyRCare.`;

let i = 0;
const textDiv = document.getElementById("text");
const intro = document.getElementById("intro");

function type() {
  if (i < message.length) {
    textDiv.innerHTML += message.charAt(i);
    i++;
    setTimeout(type, 40);
  } else {
    setTimeout(() => {
      intro.style.display = "none";
    }, 1800);
  }
}

type();
</script>

</body>
</html>
