
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#0b251b">
  <meta name="description" content="Hyderabad Cricket Connect helps cricket players and teams find opponents, players, teams, grounds and coaches.">
  <title>Hyderabad Cricket Connect | Connect • Play • Grow</title>

  <style>
    :root {
      --green: #0b251b;
      --green2: #123d2b;
      --lime: #a8e66b;
      --white: #ffffff;
      --muted: #b9c9bf;
      --card: #143527;
      --bg: #091b14;
    }

    * { box-sizing: border-box; margin: 0; padding: 0; }

    html { scroll-behavior: smooth; }

    body {
      font-family: Arial, sans-serif;
      background: var(--bg);
      color: var(--white);
      line-height: 1.6;
    }

    a { color: inherit; text-decoration: none; }

    .container {
      width: min(1120px, 90%);
      margin: auto;
    }

    header {
      background: var(--green);
      border-bottom: 1px solid #294737;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    nav {
      min-height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: bold;
      font-size: 17px;
    }

    .logo {
      width: 43px;
      height: 43px;
      border: 2px solid var(--lime);
      border-radius: 12px;
      display: grid;
      place-items: center;
      color: var(--lime);
      font-weight: 900;
      font-size: 19px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 20px;
      font-size: 13px;
      color: var(--muted);
    }

    .nav-links a:hover { color: var(--lime); }

    .btn {
      display: inline-block;
      padding: 12px 19px;
      background: var(--lime);
      color: #10251a;
      border-radius: 8px;
      font-weight: bold;
      border: none;
      cursor: pointer;
    }

    .btn-outline {
      border: 1px solid var(--lime);
      color: var(--lime);
      background: transparent;
    }

    .hero {
      padding: 85px 0;
      background:
        radial-gradient(ellipse at 85% 30%, #245438 0%, transparent 45%),
        linear-gradient(135deg, #0b251b, #102f22);
    }

    .hero-content { max-width: 720px; }

    .eyebrow {
      color: var(--lime);
      font-size: 13px;
      font-weight: bold;
      letter-spacing: 2px;
      margin-bottom: 17px;
    }

    h1 {
      font-size: clamp(36px, 6vw, 62px);
      line-height: 1.12;
      margin-bottom: 20px;
    }

    h1 span { color: var(--lime); }

    .hero p {
      max-width: 600px;
      color: var(--muted);
      font-size: 17px;
      margin-bottom: 27px;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    section { padding: 65px 0; }

    .section-heading {
      text-align: center;
      max-width: 680px;
      margin: 0 auto 35px;
    }

    .section-heading h2 {
      font-size: clamp(26px, 4vw, 36px);
      margin-bottom: 10px;
    }

    .section-heading p { color: var(--muted); }

    .services {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .service-card {
      background: var(--card);
      padding: 24px;
      border: 1px solid #2c5140;
      border-radius: 13px;
      transition: transform .2s, border-color .2s;
    }

    .service-card:hover {
      transform: translateY(-4px);
      border-color: var(--lime);
    }

    .service-icon { font-size: 30px; margin-bottom: 13px; }

    .service-card h3 { margin-bottom: 8px; }

    .service-card p {
      color: var(--muted);
      font-size: 14px;
      margin-bottom: 14px;
    }

    .service-card a {
      color: var(--lime);
      font-weight: bold;
      font-size: 14px;
    }

    .steps {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .step {
      padding: 23px;
      background: #102a1e;
      border-radius: 12px;
      border: 1px solid #294737;
    }

    .step-number {
      color: var(--lime);
      font-size: 25px;
      font-weight: bold;
      margin-bottom: 10px;
    }

    .step p { color: var(--muted); font-size: 14px; }

    .highlight {
      background: #143b29;
      border: 1px solid #47734e;
      padding: 28px;
      border-radius: 14px;
      text-align: center;
    }

    .highlight h2 { margin-bottom: 10px; }

    .highlight p { color: var(--muted); }

    .safety {
      background: #10271c;
      border-left: 4px solid var(--lime);
      padding: 25px;
      border-radius: 9px;
    }

    .safety p { color: var(--muted); margin-top: 8px; }

    footer {
      background: #06140e;
      padding: 35px 0;
      border-top: 1px solid #294737;
      text-align: center;
    }

    footer p { color: var(--muted); font-size: 13px; }

    .footer-links {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 18px;
      margin: 16px 0;
      font-size: 13px;
    }

    .footer-links a:hover { color: var(--lime); }

    .coming {
      display: inline-block;
      margin-top: 10px;
      color: var(--lime);
      font-size: 12px;
      font-weight: bold;
    }

    @media (max-width: 760px) {
      .nav-links { display: none; }
      .services { grid-template-columns: repeat(2, 1fr); }
      .steps { grid-template-columns: 1fr; }
      .hero { padding: 65px 0; }
    }

    @media (max-width: 480px) {
      .services { grid-template-columns: 1fr; }
      .brand { font-size: 14px; }
      .logo { width: 38px; height: 38px; }
      .hero p { font-size: 15px; }
    }
  </style>
</head>

<body>

<header>
  <div class="container">
    <nav>
      <a class="brand" href="#home">
        <div class="logo">HCC</div>
        <span>HYDERABAD CRICKET CONNECT</span>
      </a>

      <div class="nav-links">
        <a href="#home">Home</a>
        <a href="#services">Services</a>
        <a href="#how">How It Works</a>
        <a href="#safety">Safety</a>
      </div>

      <a class="btn" href="#services">Explore HCC</a>
    </nav>
  </div>
</header>

<main>

  <section class="hero" id="home">
    <div class="container">
      <div class="hero-content">
        <div class="eyebrow">HYDERABAD'S CRICKET CONNECT PLATFORM</div>

        <h1>
          Find Your Team.<br>
          Find Your <span>Opponent.</span><br>
          Play More Cricket.
        </h1>

        <p>
          Connecting cricket players, captains, teams, coaches and
          grounds across Hyderabad. Your next cricket match starts here.
        </p>

        <div class="hero-actions">
          <a class="btn" href="#services">Explore Services</a>
          <a class="btn btn-outline" href="#how">How HCC Works</a>
        </div>
      </div>
    </div>
  </section>

  <section id="services">
    <div class="container">
      <div class="section-heading">
        <div class="eyebrow">WHAT YOU CAN DO</div>
        <h2>Everything Cricket Needs</h2>
        <p>One platform to connect with the Hyderabad cricket community.</p>
      </div>

      <div class="services">

        <div class="service-card">
          <div class="service-icon">🏏</div>
          <h3>Find Opponent Teams</h3>
          <p>Looking for another team? Connect with teams and arrange organised matches.</p>
          <a href="#how">Explore →</a>
        </div>

        <div class="service-card">
          <div class="service-icon">👥</div>
          <h3>Find Players</h3>
          <p>Need extra players? Find suitable players for your team's next match.</p>
          <a href="#how">Explore →</a>
        </div>

        <div class="service-card">
          <div class="service-icon">🤝</div>
          <h3>Join a Team</h3>
          <p>Register as an individual player and find teams looking for players.</p>
          <a href="#how">Explore →</a>
        </div>

        <div class="service-card">
          <div class="service-icon">🏟️</div>
          <h3>Find Cricket Grounds</h3>
          <p>Discover cricket grounds in Hyderabad and send booking enquiries.</p>
          <a href="#how">Explore →</a>
        </div>

        <div class="service-card">
          <div class="service-icon">🎓</div>
          <h3>Coaches & Academies</h3>
          <p>Discover cricket coaching opportunities, coaches and academies.</p>
          <a href="#how">Explore →</a>
        </div>

        <div class="service-card">
          <div class="service-icon">⚡</div>
          <h3>Box Cricket</h3>
          <p>Create a casual game or join an existing box cricket game.</p>
          <a href="#how">Explore →</a>
        </div>

      </div>
      <p class="coming" style="text-align:center;display:block;">
        SERVICE FEATURES ARE UNDER DEVELOPMENT
      </p>
    </div>
  </section>

  <section id="how">
    <div class="container">
      <div class="section-heading">
        <div class="eyebrow">SIMPLE PROCESS</div>
        <h2>How HCC Works</h2>
        <p>One account. One profile. Multiple cricket opportunities.</p>
      </div>

      <div class="steps">
        <div class="step">
          <div class="step-number">01</div>
          <h3>Create Your Profile</h3>
          <p>Register once as a player, captain, coach or academy.</p>
        </div>

        <div class="step">
          <div class="step-number">02</div>
          <h3>Find Your Connection</h3>
          <p>Search for opponent teams, players, teams, grounds or coaches.</p>
        </div>

        <div class="step">
          <div class="step-number">03</div>
          <h3>Connect & Play</h3>
          <p>Send requests, confirm availability and organise your match safely.</p>
        </div>
      </div>
    </div>
  </section>

  <section>
    <div class="container">
      <div class="highlight">
        <div class="eyebrow">ONE ACCOUNT, MORE CRICKET</div>
        <h2>Register Once. Play Many Matches.</h2>
        <p>
          Players can use one profile to join different matches and teams.
          No need to register again for every match.
        </p>
        <span class="coming">REGISTRATION COMING SOON</span>
      </div>
    </div>
  </section>

  <section id="cricheroes">
    <div class="container">
      <div class="highlight">
        <h2>📊 CricHeroes – Match Scoring</h2>
        <p>
          HCC focuses on connecting players and arranging matches.
          CricHeroes is used separately for cricket scoring and score tracking.
          Players and teams must have a CricHeroes account under HCC's
          participation requirements.
        </p>
        <br>
        <a class="btn" href="https://play.google.com/store/apps/details?id=com.cricheroes.cricheroes.alpha"
           target="_blank" rel="noopener noreferrer">
          Get CricHeroes
        </a>
      </div>
    </div>
  </section>

  <section id="safety">
    <div class="container">
      <div class="safety">
        <h2>🛡️ Play Fair. Play Safe. Go Home Safe.</h2>
        <p>
          Verify your opponent and ground before attending a match.
          Inform your family about the venue, date and time.
          Players under 18 must have parent or guardian permission.
          Wear appropriate protective equipment, especially for
          leather-ball cricket. Respect every player.
        </p>
      </div>
    </div>
  </section>

</main>

<footer>
  <div class="container">
    <div class="brand" style="justify-content:center;">
      <div class="logo">HCC</div>
      <span>HYDERABAD CRICKET CONNECT</span>
    </div>

    <div class="footer-links">
      <a href="#home">Home</a>
      <a href="#services">Services</a>
      <a href="#how">How It Works</a>
      <a href="#safety">Safety</a>
    </div>

    <p>Connect • Play • Grow</p>
    <p style="margin-top:10px;">
      © 2026 Hyderabad Cricket Connect. All rights reserved.
    </p>
  </div>
</footer>

</body>
</html>

