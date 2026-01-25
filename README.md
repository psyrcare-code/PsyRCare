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
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 40px 20px;
}

h1 {
  font-size: 36px;
  margin-bottom: 10px;
  font-weight: normal;
}

.subtitle {
  font-size: 16px;
  opacity: 0.7;
  margin-bottom: 35px;
}

.offers-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 20px;
  width: 100%;
  max-width: 1000px;
}

.offer-card {
  border: 1px solid white;
  padding: 20px;
  border-radius: 14px;
  text-align: center;
  transition: 0.3s;
}

.offer-card:hover {
  transform: scale(1.03);
}

.offer-title {
  font-size: 18px;
  margin-bottom: 8px;
}

.offer-desc {
  font-size: 13px;
  opacity: 0.8;
  margin-bottom: 14px;
}

.offer-price {
  font-size: 18px;
  margin-bottom: 14px;
}

.book-btn {
  padding: 9px 24px;
  background: transparent;
  color: white;
  border: 1px solid white;
  cursor: pointer;
  transition: 0.3s;
  border-radius: 20px;
}

.book-btn:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<h1>Find the session that resonates with you</h1>
<div class="subtitle">Each space is designed for calm conversation and personal clarity.</div>

<div class="offers-container">

  <!-- Free -->
  <div class="offer-card">
    <div class="offer-title">Free Discovery Session</div>
    <div class="offer-desc">
      A short conversation to explore the platform and ask questions.
    </div>
    <div class="offer-price">Free</div>
    <button class="book-btn" onclick="bookOffer('Free Discovery Session', 0)">Book</button>
  </div>

  <!-- 30 min -->
  <div class="offer-card">
    <div class="offer-title">30 Minutes Session</div>
    <div class="offer-desc">
      A gentle introduction for reflection and open conversation.
    </div>
    <div class="offer-price">$5</div>
    <button class="book-btn" onclick="bookOffer('30 Minutes Session', 5)">Book</button>
  </div>

  <!-- 1 hour -->
  <div class="offer-card">
    <div class="offer-title">1 Hour Session</div>
    <div class="offer-desc">
      A focused session for meaningful dialogue and personal insight.
    </div>
    <div class="offer-price">$10</div>
    <button class="book-btn" onclick="bookOffer('1 Hour Session', 10)">Book</button>
  </div>

  <!-- 1.5 hours -->
  <div class="offer-card">
    <div class="offer-title">1.5 Hours Session</div>
    <div class="offer-desc">
      Extended time for deeper exploration and thoughtful conversation.
    </div>
    <div class="offer-price">$15</div>
    <button class="book-btn" onclick="bookOffer('1.5 Hours Session', 15)">Book</button>
  </div>

  <!-- 2 hours -->
  <div class="offer-card">
    <div class="offer-title">2 Hours Session</div>
    <div class="offer-desc">
      A longer space for clarity, reflection, and emotional awareness.
    </div>
    <div class="offer-price">$20</div>
    <button class="book-btn" onclick="bookOffer('2 Hours Session', 20)">Book</button>
  </div>

  <!-- 2.5 hours -->
  <div class="offer-card">
    <div class="offer-title">2.5 Hours Session</div>
    <div class="offer-desc">
      Time dedicated to deeper understanding and personal exploration.
    </div>
    <div class="offer-price">$25</div>
    <button class="book-btn" onclick="bookOffer('2.5 Hours Session', 25)">Book</button>
  </div>

  <!-- 3 hours -->
  <div class="offer-card">
    <div class="offer-title">3 Hours Session</div>
    <div class="offer-desc">
      A complete session for profound reflection and inner clarity.
    </div>
    <div class="offer-price">$30</div>
    <button class="book-btn" onclick="bookOffer('3 Hours Session', 30)">Book</button>
  </div>

  <!-- 3.5 hours -->
  <div class="offer-card">
    <div class="offer-title">3.5 Hours Session</div>
    <div class="offer-desc">
      A powerful extended session for personal growth and insight.
    </div>
    <div class="offer-price">$35</div>
    <button class="book-btn" onclick="bookOffer('3.5 Hours Session', 35)">Book</button>
  </div>

  <!-- 4 hours -->
  <div class="offer-card">
    <div class="offer-title">4 Hours Session</div>
    <div class="offer-desc">
      Deep exploration of thoughts and perspectives in a calm environment.
    </div>
    <div class="offer-price">$40</div>
    <button class="book-btn" onclick="bookOffer('4 Hours Session', 40)">Book</button>
  </div>

  <!-- 4.5 hours -->
  <div class="offer-card">
    <div class="offer-title">4.5 Hours Session</div>
    <div class="offer-desc">
      Long-form conversation designed for clarity and personal awareness.
    </div>
    <div class="offer-price">$45</div>
    <button class="book-btn" onclick="bookOffer('4.5 Hours Session', 45)">Book</button>
  </div>

  <!-- 5 hours -->
  <div class="offer-card">
    <div class="offer-title">5 Hours Session</div>
    <div class="offer-desc">
      The most complete space for deep reflection and transformation.
    </div>
    <div class="offer-price">$50</div>
    <button class="book-btn" onclick="bookOffer('5 Hours Session', 50)">Book</button>
  </div>

</div>

<script>
function bookOffer(name, price) {
  localStorage.setItem("offerName", name);
  localStorage.setItem("offerPrice", price);
  window.location.href = "order.html";
}
</script>

</body>
</html>

   
   
