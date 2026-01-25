<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Offers</title>

<style>
body {
  background: black;
  color: white;
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 40px 20px;
}

#welcome {
  font-size: 20px;
  margin-bottom: 20px;
}

.offer {
  border: 1px solid white;
  padding: 15px;
  margin: 12px auto;
  max-width: 400px;
  border-radius: 10px;
}

button {
  margin-top: 10px;
  padding: 8px 20px;
  background: transparent;
  color: white;
  border: 1px solid white;
  cursor: pointer;
}
button:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div id="welcome"></div>

<h1>Your sessions</h1>

<div class="offer">
  <h3>Free Discovery Session</h3>
  <p>Free</p>
  <button onclick="bookOffer('Free Discovery Session', 0)">Book</button>
</div>

<div class="offer">
  <h3>30 Minutes Session</h3>
  <p>$5</p>
  <button onclick="bookOffer('30 Minutes Session', 5)">Book</button>
</div>

<div class="offer">
  <h3>1 Hour Session</h3>
  <p>$10</p>
  <button onclick="bookOffer('1 Hour Session', 10)">Book</button>
</div>

<div class="offer">
  <h3>1.5 Hours Session</h3>
  <p>$15</p>
  <button onclick="bookOffer('1.5 Hours Session', 15)">Book</button>
</div>

<div class="offer">
  <h3>2 Hours Session</h3>
  <p>$20</p>
  <button onclick="bookOffer('2 Hours Session', 20)">Book</button>
</div>

<div class="offer">
  <h3>2.5 Hours Session</h3>
  <p>$25</p>
  <button onclick="bookOffer('2.5 Hours Session', 25)">Book</button>
</div>

<div class="offer">
  <h3>3 Hours Session</h3>
  <p>$30</p>
  <button onclick="bookOffer('3 Hours Session', 30)">Book</button>
</div>

<div class="offer">
  <h3>3.5 Hours Session</h3>
  <p>$35</p>
  <button onclick="bookOffer('3.5 Hours Session', 35)">Book</button>
</div>

<div class="offer">
  <h3>4 Hours Session</h3>
  <p>$40</p>
  <button onclick="bookOffer('4 Hours Session', 40)">Book</button>
</div>

<div class="offer">
  <h3>4.5 Hours Session</h3>
  <p>$45</p>
  <button onclick="bookOffer('4.5 Hours Session', 45)">Book</button>
</div>

<div class="offer">
  <h3>5 Hours Session</h3>
  <p>$50</p>
  <button onclick="bookOffer('5 Hours Session', 50)">Book</button>
</div>

<script>
// welcome message
let username = localStorage.getItem("username");
if (username) {
  document.getElementById("welcome").innerText = "Welcome, " + username + " 🤍";
}

// booking function
function bookOffer(name, price) {
  localStorage.setItem("offerName", name);
  localStorage.setItem("offerPrice", price);
  window.location.href = "order.html";
}
</script>

</body>
</html>

 

