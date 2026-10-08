<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ad Manager</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f4f6f8;
      color: #222;
    }

    .header {
      background: #0088cc;
      color: white;
      padding: 20px;
      text-align: center;
    }

    .container {
      max-width: 500px;
      margin: auto;
      padding: 20px;
    }

    .card {
      background: white;
      padding: 20px;
      margin-bottom: 15px;
      border-radius: 15px;
      box-shadow: 0 3px 12px rgba(0,0,0,0.08);
    }

    .balance {
      font-size: 28px;
      font-weight: bold;
      color: #0088cc;
    }

    button {
      width: 100%;
      padding: 14px;
      border: 0;
      border-radius: 10px;
      background: #0088cc;
      color: white;
      font-size: 16px;
      margin-top: 10px;
    }

    button:active {
      transform: scale(0.98);
    }

    .package {
      border: 1px solid #ddd;
      padding: 15px;
      border-radius: 12px;
      margin-top: 10px;
    }

    .small {
      color: #777;
      font-size: 14px;
    }
  </style>
</head>

<body>

  <div class="header">
    <h1>📢 Ad Manager</h1>
    <p>Watch Ads & Earn</p>
  </div>

  <div class="container">

    <div class="card">
      <div class="small">আপনার Balance</div>
      <div class="balance">৳0.00</div>
      <button onclick="watchAd()">📺 Watch Ad</button>
    </div>

    <div class="card">
      <h2>📦 Packages</h2>

      <div class="package">
        <h3>Starter Package</h3>
        <p>Ads: 10</p>
        <p>Reward: ৳1 / Ad</p>
        <button onclick="buyPackage()">Buy Package</button>
      </div>

      <div class="package">
        <h3>Premium Package</h3>
        <p>Ads: 50</p>
        <p>Reward: ৳2 / Ad</p>
        <button onclick="buyPackage()">Buy Package</button>
      </div>
    </div>

    <div class="card">
      <h2>👤 Account</h2>
      <p id="userInfo">Telegram user loading...</p>
    </div>

  </div>

  <script>
    function watchAd() {
      alert("Ad system coming soon!");
    }

    function buyPackage() {
      alert("Package purchase system coming soon!");
    }

    if (window.Telegram && Telegram.WebApp) {
      Telegram.WebApp.ready();

      const user = Telegram.WebApp.initDataUnsafe?.user;

      if (user) {
        document.getElementById("userInfo").innerText =
          "Welcome, " + (user.first_name || "User");
      }
    }
  </script>

</body>
</html>
