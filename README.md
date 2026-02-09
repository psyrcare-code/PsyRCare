<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="google-site-verification" content="Lh7kgs0uNARLIjz_tQC9flE5l4sIPxFGYGgFeJ20SXI" />

  <meta name="description" content="A calm and safe space for emotional support and guided self-reflection sessions. PsyRCare offers respectful conversations designed to help you feel heard and supported.">
  
  <title>PsyRCare</title>
  <style>
    body {
      margin: 0;
      background: black;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      font-family: Arial, sans-serif;
      cursor: pointer;
    }

    #time {
      font-size: 90px;
      letter-spacing: 6px;
      margin-bottom: 40px;
    }

    #arrow {
      font-size: 40px;
      opacity: 0;
      transition: opacity 1s;
    }

    #arrow.show {
      opacity: 1;
    }
  </style>
</head>
<body>

  <div id="time">22:21</div>
  <div id="arrow">↓</div>

  <audio id="flatline" src="flatline.mp3"></audio>
  <audio id="heartbeat" src="heartbeat.mp3" loop></audio>

  <script>
    let started = false;

    document.body.addEventListener("click", () => {
      if (started) return;
      started = true;

      const flatline = document.getElementById("flatline");
      const heartbeat = document.getElementById("heartbeat");
      const time = document.getElementById("time");
      const arrow = document.getElementById("arrow");

      flatline.play();

      setTimeout(() => {
        time.innerText = "22:22";
        flatline.pause();
        heartbeat.play();
        arrow.classList.add("show");
      }, 3000);

      arrow.addEventListener("click", (e) => {
        e.stopPropagation();
        heartbeat.pause();
        document.body.style.opacity = 0;
        setTimeout(() => {
          window.location.href = "home.html";
        }, 1000);
      });
    });
  </script>

</body>
</html>


