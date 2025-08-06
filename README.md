<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Zümrüt - Coming Soon</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@500;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      background: #054634 url('khussa-bg.jpg.png') no-repeat center center;
      background-size: cover;
      font-family: 'Playfair Display', serif;
      color: #f9f6f1;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      text-align: center;
    }

    .overlay {
      background-color: rgba(5, 70, 52, 0.8);
      position: absolute;
      top: 0; left: 0;
      width: 100%; height: 100%;
      z-index: -1;
    }

    h1 {
      font-size: 3em;
      color: #d4af37;
      margin-bottom: 0.3em;
    }

    p {
      max-width: 500px;
      margin: 0 auto 2em;
      font-size: 1.1em;
      color: #f9f6f1;
    }

    form {
      display: flex;
      gap: 10px;
      flex-wrap: wrap;
      justify-content: center;
      margin-bottom: 2em;
    }

    input[type="email"] {
      padding: 10px;
      width: 250px;
      border: none;
      border-radius: 5px;
      font-size: 1em;
    }

    button {
      padding: 10px 20px;
      background-color: #d4af37;
      color: #054634;
      border: none;
      border-radius: 5px;
      font-size: 1em;
      cursor: pointer;
      transition: 0.3s;
    }

    button:hover {
      background-color: #b9982f;
    }

    .socials a {
      margin: 0 10px;
      color: #d4af37;
      font-size: 1.5em;
      text-decoration: none;
    }

    .countdown {
      font-size: 1.2em;
      margin: 1em 0;
      color: #f9f6f1;
    }

    footer {
      margin-top: 3em;
      font-size: 0.9em;
      color: #f9f6f1;
    }

    @media (max-width: 500px) {
      h1 {
        font-size: 2em;
      }

      input[type="email"] {
        width: 100%;
      }
    }
  </style>
  <script>
    function countdown() {
      const launchDate = new Date("2025-08-14T00:00:00").getTime();
      const timer = setInterval(function () {
        const now = new Date().getTime();
        const distance = launchDate - now;

        if (distance < 0) {
          clearInterval(timer);
          document.getElementById("timer").innerHTML = "We have launched!";
          return;
        }

        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        document.getElementById("timer").innerHTML =
          `${days}d ${hours}h ${minutes}m ${seconds}s`;
      }, 1000);
    }

    window.onload = countdown;
  </script>
</head>
<body>
  <div class="overlay"></div>
  <h1>Launching Online Soon</h1>
  <p>Our website is under construction. Sign up to receive updates and to be notified when we launch.</p>

  <form action="https://formspree.io/f/xkgzqreb" method="POST">
    <input type="email" name="email" placeholder="Enter your email" required />
    <button type="submit">Notify Me</button>
  </form>

  <div class="countdown">
    Launching in <span id="timer">Loading...</span>
  </div>

  <div class="socials">
    <a href="https://wa.me/923140432352" target="_blank" title="WhatsApp">&#x1F4F1;</a>
    <a href="https://www.instagram.com/zumrutbyamir" target="_blank" title="Instagram">&#x1F47E;</a>
    <a href="https://www.facebook.com/zumrutbyamir" target="_blank" title="Facebook">&#x1F4F7;</a>
    <a href="https://www.tiktok.com/@zumrutbyamir" target="_blank" title="TikTok">&#x1F3AC;</a>
  </div>

  <footer>
    2006 Zümrüt by Amir. All rights reserved.
  </footer>
</body>
</html>
