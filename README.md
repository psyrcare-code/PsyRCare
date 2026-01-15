<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Register | PsyRCare</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: Arial, sans-serif;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.container {
  width: 100%;
  max-width: 420px;
  padding: 40px;
  text-align: center;
}

h1 {
  margin-bottom: 10px;
}

p {
  font-family: 'Playfair Display', serif;
  font-size: 17px;
  opacity: 0.9;
  margin-bottom: 30px;
}

input {
  width: 100%;
  padding: 14px;
  margin-bottom: 16px;
  background: transparent;
  border: 1px solid white;
  color: white;
  font-size: 15px;
}

input::placeholder {
  color: #aaa;
}

button {
  width: 100%;
  padding: 14px;
  background: white;
  color: black;
  border: none;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  opacity: 0.85;
}

.back {
  margin-top: 20px;
  display: inline-block;
  color: white;
  text-decoration: none;
  font-size: 14px;
  opacity: 0.8;
}

.back:hover {
  opacity: 1;
}
</style>
</head>

<body>

<div class="container">
  <h1>Register</h1>
  <p>
    This is a first step.  
    You will be contacted to schedule your session.
  </p>

  <form>
    <input type="text" placeholder="Full name" required>
    <input type="email" placeholder="Email address" required>
    <input type="tel" placeholder="Phone number (optional)">
    <button type="submit">Continue</button>
  </form>

  <a href="home.html" class="back">← Back</a>
</div>

</body>
</html>
