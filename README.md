<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Book Session - PsyRCare</title>

<style>
body {
  background: black;
  color: white;
  font-family: Arial, sans-serif;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  text-align: center;
}

.box {
  border: 1px solid white;
  padding: 30px 50px;
  border-radius: 10px;
}

button {
  margin-top: 20px;
  padding: 12px 30px;
  background: black;
  color: white;
  border: 1px solid white;
  cursor: pointer;
}
</style>
</head>

<body>

<div class="box">
  <h2>Your Booking</h2>
  <p id="offerName"></p>
  <p id="offerPrice"></p>

  <button onclick="confirmBooking()">Confirm Booking</button>
</div>

<script>
const name = localStorage.getItem("offerName");
const price = localStorage.getItem("offerPrice");

document.getElementById("offerName").innerText = "Session: " + name;
document.getElementById("offerPrice").innerText = "Price: $" + price;

function confirmBooking() {
  alert("Your session has been booked successfully 🤍");
}
</script>

</body>
</html>








  
