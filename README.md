<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>PsyRCare - Offers</title>
  <style>
    body {
      background: #000;
      color: #fff;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      text-align: center;
    }

    h1 {
      margin-top: 40px;
      font-size: 36px;
    }

    .offers-container {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 40px auto;
      max-width: 1000px;
    }

    .offer-card {
      background: #111;
      border: 1px solid #333;
      border-radius: 12px;
      padding: 20px;
      margin: 15px;
      width: 260px;
      transition: 0.3s;
    }

    .offer-card:hover {
      transform: scale(1.05);
      border-color: #fff;
    }

    .offer-title {
      font-size: 20px;
      margin-bottom: 10px;
    }

    .offer-desc {
      font-size: 14px;
      color: #ccc;
      margin-bottom: 15px;
    }

    .offer-price {
      font-size: 22px;
      margin-bottom: 15px;
    }

    .btn {
      display: inline-block;
      padding: 10px 20px;
      border: 1px solid #fff;
      color: #fff;
      text-decoration: none;
      border-radius: 6px;
      transition: 0.3s;
    }

    .btn:hover {
      background: #fff;
      color: #000;
    }
  </style>
</head>
<body>

  <h1>Our Sessions</h1>

  <div class="offers-container">

    <div class="offer-card">
      <div class="offer-title">Free Intro Session</div>
      <div class="offer-desc">A short free session for new users to ask questions.</div>
      <div class="offer-price">Free</div>
      <a href="register.html" class="btn">Start</a>
    </div>

    <div class="offer-card">
      <div class="offer-title">30-Minute Session</div>
      <div class="offer-desc">A focused conversation to explore your concerns.</div>
      <div class="offer-price">$5</div>
      <a href="register.html" class="btn">Book</a>
    </div>

    <div class="offer-card">
      <div class="offer-title">1-Hour Session</div>
      <div class="offer-desc">A deeper session to understand and clarify your situation.</div>
      <div class="offer-price">$10</div>
      <a href="register.html" class="btn">Book</a>
    </div>

    <div class="offer-card">
      <div class="offer-title">1.5-Hour Deep Session</div>
      <div class="offer-desc">A structured 90-minute session as part of a progressive support plan.</div>
      <div class="offer-price">$15</div>
      <a href="register.html" class="btn">Book</a>
    </div>

  </div>

</body>
</html>
