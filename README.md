<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Birthday Surprise</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Comic Sans MS', cursive;
      background: linear-gradient(to right, #ff9a9e, #fad0c4);
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
    }

    #popup, #birthdayMessage, #naughtyMessage, #finalMessage, #awwMessage, #byeMessage {
      background: white;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.2);
      text-align: center;
      max-width: 90%;
      width: 300px;
      animation: pop 0.4s ease;
    }

    button {
      background-color: #ff6b81;
      color: white;
      border: none;
      padding: 10px 20px;
      margin: 10px;
      border-radius: 10px;
      font-size: 1em;
      cursor: pointer;
      transition: background 0.3s;
    }

    button:hover {
      background-color: #ff4757;
    }

    #birthdayMessage, #naughtyMessage, #finalMessage, #awwMessage, #byeMessage {
      display: none;
    }

    @keyframes pop {
      0% { transform: scale(0.8); opacity: 0; }
      100% { transform: scale(1); opacity: 1; }
    }

    .funny {
      font-size: 1.4em;
      color: #ff4757;
      animation: bounce 1s infinite;
    }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-10px); }
    }

    .message-box {
      background-color: #94a1a8;
      color: #ffffff;
      border-radius: 15px;
      padding: 15px;
      margin-top: 15px;
    }

    .final-cat-gif {
      max-width: 100%;
      border-radius: 15px;
      margin-top: 15px;
    }

    .gif-row {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 15px;
    }

    .gif-row img {
      width: 80px;
      height: 80px;
      object-fit: cover;
      border-radius: 10px;
    }
  </style>
</head>
<body>

  <div id="popup">
    <h2>Bbg, is it your birthday today?</h2>
    <button onclick="handleAnswer(true)">Yes!</button>
    <button onclick="handleAnswer(false)">No :(</button>
  </div>

  <div id="birthdayMessage">
    <h2 class="funny">Adhi!!!</h2>
    <img src="https://media1.tenor.com/m/-tIQxWRT_UgAAAAC/dancing-cat-dance.gif" alt="cat meme gif" style="max-width: 100%; border-radius: 15px; margin-top: 10px;">
    <p>💃🕺💃🕺💃🕺💃🕺💃🕺</p>
    <button onclick="showFinalMessage()">Where is my present?</button>
  </div>

  <div id="naughtyMessage">
    <h2>Aww sad :( Try again on ur day...</h2>
    <button onclick="resetPopup()">Try again</button>
  </div>

  <div id="finalMessage">
    <h2>For my pookie! 💌</h2>
    <div class="message-box">
      Mr. Chandrabhanu, yk I am too broke to be ur sugar mommy and too far for actual gifts hence I can only provide u with this shitty html and my paintings... I am sorry my boi :( Anywayss velya kutti aambo lemme see u on billboards someday and be proud of u like I told you okie! And adjust with these 'pictorial gifts' :D Ly lots &lt;3
    </div>
    <img class="final-cat-gif" src="https://media.tenor.com/bTll4UIXbqYAAAAi/catsmirk.gif" alt="cat smirk gif">

    <div class="gif-row">
      <img src="https://media1.tenor.com/m/2OIHEpqXmr4AAAAd/white-monster-wmster.gif" alt="white monster">
      <img src="https://media1.tenor.com/m/EEzGdX9PtGcAAAAC/spiderkurwamen.gif" alt="spider meme">
      <img src="https://media1.tenor.com/m/hoHJwIKmOUoAAAAd/black-sexy-panigale.gif" alt="panigale gif">
    </div>

    <div>
      <button onclick="showAwwMessage()">ly too &lt;3</button>
      <button onclick="showByeMessage()">k bye</button>
    </div>
  </div>

  <div id="awwMessage">
    <h2>Aww :(</h2>
    <img src="https://media1.tenor.com/m/ARpdqU7uIM0AAAAC/pampered.gif" alt="pampered gif" style="max-width: 100%; border-radius: 15px;">
    <button onclick="location.reload()">Replay</button>
  </div>

  <div id="byeMessage">
    <img src="https://media1.tenor.com/m/uXf2iTNrIdcAAAAC/so-cute.gif" alt="so cute gif" style="max-width: 100%; border-radius: 15px;">
    <div class="message-box">
      <button onclick="showAwwMessage()">ow sorry! ly &lt;3</button>
    </div>
  </div>

  <script>
    function handleAnswer(isBirthday) {
      document.getElementById('popup').style.display = 'none';
      if (isBirthday) {
        document.getElementById('birthdayMessage').style.display = 'block';
      } else {
        document.getElementById('naughtyMessage').style.display = 'block';
      }
    }

    function resetPopup() {
      document.getElementById('naughtyMessage').style.display = 'none';
      document.getElementById('popup').style.display = 'block';
    }

    function showFinalMessage() {
      document.getElementById('birthdayMessage').style.display = 'none';
      document.getElementById('finalMessage').style.display = 'block';
    }

    function showAwwMessage() {
      document.getElementById('finalMessage').style.display = 'none';
      document.getElementById('byeMessage').style.display = 'none';
      document.getElementById('awwMessage').style.display = 'block';
    }

    function showByeMessage() {
      document.getElementById('finalMessage').style.display = 'none';
      document.getElementById('byeMessage').style.display = 'block';
    }
  </script>

</body>
</html>
 
