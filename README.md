<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Offers</title>

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: Arial, sans-serif;
  padding: 40px 20px;
  text-align: center;
}

/* Intro message */
#introMessage {
  font-size: 22px;
  min-height: 60px;
  margin-top: 120px;
}

/* After intro */
#mainSection {
  display: none;
}

#chooseText {
  font-size: 26px;
  margin-bottom: 10px;
  font-weight: 300;
}

#chooseSub {
  font-size: 15px;
  opacity: 0.7;
  margin-bottom: 35px;
}

/* Offers */
.offers-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 18px;
  max-width: 1000px;
  margin: auto;
}

.offer-card {
  border: 1px solid white;
  padding: 18px;
  border-radius: 14px;
  transition: 0.3s;
}

.offer-card:hover {
  transform: scale(1.03);
}

.offer-title {
  font-size: 17px;
  margin-bottom: 6px;
}

.offer-desc {
  font-size: 13px;
  opacity: 0.8;
  margin-bottom: 12px;
}

.offer-price {
  font-size: 18px;
  margin-bottom: 12px;
}

.book-btn {
  padding: 8px 22px;
  border: 1px solid white;
  background: transparent;
  color: white;
  cursor: pointer;
  border-radius: 20px;
  transition: 0.3s;
}

.book-btn:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div id="introMessage"></div>

<div id="mainSection">
  <div id="chooseText">Choose the session that feels right for you
  All offers are free until the end of February. </div>
  <div id="chooseSub">Take your time. This space is yours.</div>

  <div class="offers-container">

    <div class="offer-card">
      <div class="offer-title">Free Discovery Session</div>
      <div class="offer-desc">A short conversation to explore the platform and ask questions.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('Free Discovery Session','15 minutes','A short conversation to explore the platform and ask questions.',0)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">30 Minutes Session</div>
      <div class="offer-desc">A gentle introduction for reflection and open conversation.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('30 Minutes Session','30 minutes','A gentle introduction for reflection and open conversation.',5)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">1 Hour Session</div>
      <div class="offer-desc">A focused session for meaningful dialogue and personal insight.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('1 Hour Session','1 hour','A focused session for meaningful dialogue and personal insight.',10)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">1.5 Hours Session</div>
      <div class="offer-desc">Extended time for deeper exploration and thoughtful conversation.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('1.5 Hours Session','1.5 hours','Extended time for deeper exploration and thoughtful conversation.',15)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">2 Hours Session</div>
      <div class="offer-desc">A longer space for clarity, reflection, and awareness.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('2 Hours Session','2 hours','A longer space for clarity, reflection, and awareness.',20)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">2.5 Hours Session</div>
      <div class="offer-desc">Time dedicated to deeper understanding and exploration.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('2.5 Hours Session','2.5 hours','Time dedicated to deeper understanding and exploration.',25)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">3 Hours Session</div>
      <div class="offer-desc">A complete session for profound reflection and clarity.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('3 Hours Session','3 hours','A complete session for profound reflection and clarity.',30)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">3.5 Hours Session</div>
      <div class="offer-desc">A powerful extended session for personal growth.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('3.5 Hours Session','3.5 hours','A powerful extended session for personal growth.',35)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">4 Hours Session</div>
      <div class="offer-desc">Deep exploration of thoughts in a calm environment.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('4 Hours Session','4 hours','Deep exploration of thoughts in a calm environment.',40)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">4.5 Hours Session</div>
      <div class="offer-desc">Long-form conversation designed for awareness.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('4.5 Hours Session','4.5 hours','Long-form conversation designed for awareness.',45)">Book</button>
    </div>

    <div class="offer-card">
      <div class="offer-title">5 Hours Session</div>
      <div class="offer-desc">The most complete space for deep reflection.</div>
      <div class="offer-price">Free</div>
      <button class="book-btn" onclick="bookOffer('5 Hours Session','5 hours','The most complete space for deep reflection.',50)">Book</button>
    </div>

  </div>
</div>

<script>
let username = localStorage.getItem("userName") || "You";
let message =
  username +
  "... welcome 🤍\nIf you are looking for clarity, understanding, and a safe space where your voice truly matters — you are in the right place.";

let index = 0;
let intro = document.getElementById("introMessage");
let main = document.getElementById("mainSection");

function typeMessage() {
  if (index < message.length) {
    intro.innerHTML += message.charAt(index);
    index++;
    setTimeout(typeMessage, 45);
  } else {
    setTimeout(() => {
      intro.style.display = "none";
      main.style.display = "block";
    }, 1300);
  }
}

typeMessage();

function bookOffer(name, duration, description, price) {
  localStorage.setItem("offerName", name);
  localStorage.setItem("offerDuration", duration);
  localStorage.setItem("offerDescription", description);
  localStorage.setItem("offerPrice", price);
  window.location.href = "order.html";
}
</script>

</body>
</html>
