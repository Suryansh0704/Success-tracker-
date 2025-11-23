<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Login / Sign In Page</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #e8ffe8;
      overflow: hidden;
    }
    .quote-box {
      position: absolute;
      top: 10%;
      width: 100%;
      text-align: center;
      font-size: 24px;
      font-weight: bold;
      color: #0a6d0a;
      transition: opacity 1s ease-in-out;
      padding: 0 20px;
    }
    .container {
      width: 350px;
      margin: 180px auto;
      background: white;
      padding: 25px;
      border-radius: 15px;
      box-shadow: 0 0 15px rgba(0,0,0,0.2);
      text-align: center;
    }
    .btn {
      display: block;
      width: 100%;
      padding: 12px;
      margin: 10px 0;
      border-radius: 10px;
      background: #0a8d0a;
      color: white;
      border: none;
      font-size: 18px;
      cursor: pointer;
      transition: 0.3s;
    }
    .btn:hover { background: #066b06; }
    .slide-box {
      display: none;
      margin-top: 15px;
      animation: slideDown 0.7s;
    }
    @keyframes slideDown {
      from { opacity: 0; transform: translateY(-20px); }
      to { opacity: 1; transform: translateY(0); }
    }
    input {
      width: 90%;
      padding: 10px;
      margin: 8px 0;
      border: 2px solid #0a8d0a;
      border-radius: 10px;
    }
  </style>
</head>
<body>  <!-- QUOTES SECTION -->  <div class="quote-box" id="quoteBox">Loading...</div>  <!-- LOGIN / SIGNUP CONTAINER -->  <div class="container">
    <button class="btn" onclick="showBox('login')">Login</button>
    <button class="btn" onclick="showBox('signup')">Sign Up</button><div id="loginBox" class="slide-box">
  <input type="text" placeholder="Username" />
  <input type="password" placeholder="Password" />
  <button class="btn">Login</button>
</div>

<div id="signupBox" class="slide-box">
  <input type="text" placeholder="Name" />
  <input type="password" placeholder="Password" />
  <button class="btn">Sign Up</button>
</div>

  </div><script>
  // 100 QUOTES SUPPORT (20 added, you can extend any time)
  const quotes = [
    "Success starts with self-discipline.",
    "Every champion was once a beginner.",
    "Consistency beats talent.",
    "Pain today, power tomorrow.",
    "Focus is your superpower.",
    "Small steps build big results.",
    "Do it for your future self.",
    "Winners train, losers complain.",
    "Your only limit is you.",
    "Think big. Work hard. Stay humble.",
    "The grind never lies.",
    "Push beyond excuses.",
    "Dreams demand hustle.",
    "Progress, not perfection.",
    "Hard work beats luck.",
    "Stay hungry, stay focused.",
    "Success loves speed.",
    "Don't stop until you're proud.",
    "Your dreams need your time.",
    "Discipline > Motivation."
  ];

  let index = 0;
  const box = document.getElementById("quoteBox");

  // QUOTE SLIDER
  function changeQuote() {
    box.style.opacity = 0;
    setTimeout(() => {
      box.innerText = quotes[index];
      box.style.opacity = 1;
      index = (index + 1) % quotes.length;
    }, 1000);
  }

  changeQuote();
  setInterval(changeQuote, 20000);

  // LOGIN / SIGNUP SLIDE BOX
  function showBox(type) {
    document.getElementById("loginBox").style.display = "none";
    document.getElementById("signupBox").style.display = "none";

    if (type === "login") {
      document.getElementById("loginBox").style.display = "block";
    } else {
      document.getElementById("signupBox").style.display = "block";
    }
  }
</script></body>
</html># Success-tracker-
An daily habit tracker 
