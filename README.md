
<!DOCTYPE html>
<html lang="nl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Toverlaars groep 8</title>

  <style>
    :root {
      --donkergeel: #604500;
      --bruin: #765400;
      --goud: #d99b00;
      --geel: #ffd21f;
      --lichtgeel: #fff1a3;
      --zachtgeel: #fffbea;
      --oranje: #ed9713;
      --wit: #ffffff;
      --tekst: #4c3800;
    }

    * {
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      margin: 0;
      color: var(--tekst);
      background: var(--zachtgeel);
      font-family: "Trebuchet MS", Arial, sans-serif;
      line-height: 1.6;
    }

    /* HEADER */

    header {
      position: relative;
      overflow: hidden;
      padding: 85px 20px 95px;
      color: var(--donkergeel);
      text-align: center;
      background:
        radial-gradient(
          circle at 10% 22%,
          rgba(255, 255, 255, 0.95) 0 5px,
          transparent 6px
        ),
        radial-gradient(
          circle at 85% 25%,
          rgba(255, 255, 255, 0.95) 0 4px,
          transparent 5px
        ),
        radial-gradient(
          circle at 75% 78%,
          rgba(255, 245, 160, 0.95) 0 6px,
          transparent 7px
        ),
        radial-gradient(
          circle at 25% 78%,
          rgba(255, 255, 255, 0.9) 0 3px,
          transparent 4px
        ),
        linear-gradient(135deg, #e5a800, #ffd21f 55%, #f3aa13);
    }

    header::before,
    header::after {
      position: absolute;
      color: var(--wit);
      font-size: 50px;
      content: "✦";
    }

    header::before {
      top: 25px;
      left: 12%;
      transform: rotate(-20deg);
    }

    header::after {
      right: 13%;
      bottom: 25px;
      transform: rotate(20deg);
    }

    .toverstok {
      margin-bottom: 10px;
      font-size: 2.8rem;
    }

    header h1 {
      margin: 0;
      font-size: clamp(2.4rem, 7vw, 5rem);
      letter-spacing: 1px;
    }

    header p {
      max-width: 720px;
      margin: 18px auto 0;
      font-size: 1.2rem;
    }

    /* NAVIGATIE */

    nav {
      position: sticky;
      top: 0;
      z-index: 20;
      background: var(--geel);
      border-bottom: 4px solid var(--goud);
      box-shadow: 0 4px 14px rgba(96, 69, 0, 0.25);
    }

    .nav-inner {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 8px;
      max-width: 1150px;
      margin: 0 auto;
      padding: 12px 16px;
    }

    nav a {
      padding: 11px 18px;
      color: var(--donkergeel);
      border-radius: 999px;
      font-weight: bold;
      text-decoration: none;
      transition: 0.2s ease;
    }

    nav a:hover,
    nav a:focus {
      color: var(--wit);
      background: var(--oranje);
      transform: translateY(-2px);
      outline: none;
    }

    /* ALGEMENE INHOUD */

    main {
      max-width: 1120px;
      margin: 0 auto;
      padding: 25px 20px 60px;
    }

    section {
      position: relative;
      margin: 30px 0;
      padding: 42px;
      background: var(--wit);
      border: 2px solid #f4d45a;
      border-radius: 24px;
      box-shadow: 0 8px 25px rgba(96, 69, 0, 0.1);
      scroll-margin-top: 95px;
    }

    section::after {
      position: absolute;
      top: 20px;
      right: 28px;
      color: var(--goud);
      font-size: 1.8rem;
      content: "✦";
    }

    section h2 {
      margin: 0 0 12px;
      color: var(--bruin);
      font-size: clamp(1.8rem, 4vw, 2.7rem);
    }

    section h3 {
      color: var(--donkergeel);
    }

    .intro {
      max-width: 760px;
      font-size: 1.08rem;
    }

    /* TEKST BIJ DEZE WEEK */

    .week-tekst,
    .agenda-tekst,
    .nieuws-tekst {
      margin-top: 25px;
      padding: 28px;
      background: var(--lichtgeel);
      border-left: 8px solid var(--goud);
      border-radius: 18px;
      font-size: 1.15rem;
    }

    .week-tekst:focus,
    .agenda-tekst:focus,
    .nieuws-tekst:focus {
      outline: 3px solid var(--oranje);
      background: #fff8c9;
    }

    .aanwijzing {
      margin-top: 12px;
      color: #8b6500;
      font-size: 0.95rem;
      font-style: italic;
    }

    /* AGENDA EN NIEUWS */

    .informatie-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
      margin-top: 25px;
    }

    .informatie-kaart {
      padding: 25px;
      background: linear-gradient(135deg, #fff1a3, #ffffff);
      border: 2px solid #f1c927;
      border-radius: 18px;
    }

    .informatie-kaart:nth-child(2) {
      background: linear-gradient(135deg, #ffe477, #ffffff);
    }

    .informatie-kaart h3 {
      margin-top: 0;
    }

    /* ADRES */

    .adres-box {
      margin-top: 22px;
      padding: 30px;
      color: var(--donkergeel);
      background:
        radial-gradient(
          circle at 85% 20%,
          rgba(255, 255, 255, 0.9) 0 4px,
          transparent 5px
        ),
        linear-gradient(135deg, var(--geel), var(--oranje));
      border: 3px solid var(--goud);
      border-radius: 18px;
      font-size: 1.08rem;
      font-style: normal;
    }

    /* KNOP */

    .knop {
      display: inline-block;
      margin-top: 24px;
      padding: 13px 22px;
      color: var(--donkergeel);
      background: var(--geel);
      border: 2px solid var(--goud);
      border-radius: 999px;
      font-weight: bold;
      text-decoration: none;
      box-shadow: 0 4px 0 #b88000;
      transition: 0.2s ease;
    }

    .knop:hover,
    .knop:focus {
      color: var(--wit);
      background: var(--oranje);
      transform: translateY(-2px);
      outline: none;
    }

    /* FOOTER */

    footer {
      padding: 40px 20px;
      color: var(--donkergeel);
      text-align: center;
      background: var(--geel);
      border-top: 4px solid var(--goud);
    }

    footer p {
      margin: 5px 0;
    }

    .sterretjes {
      color: var(--wit);
      font-size: 1.4rem;
      letter-spacing: 7px;
    }

    /* MOBIELE WEERGAVE */

    @media (max-width: 780px) {
      header {
        padding: 65px 18px 75px;
      }

      section {
        padding: 30px 22px;
      }

      .informatie-grid {
        grid-template-columns: 1fr;
      }

      .nav-inner {
        gap: 4px;
        padding: 9px 8px;
      }

      nav a {
        padding: 9px 11px;
        font-size: 0.9rem;
      }
    }
  </style>
</head>

<body>

  <!-- HEADER -->

  <header id="home">
    <div class="toverstok">🪄</div>

    <h1>Toverlaars groep 8</h1>

    <p>
      De Toverlaars maakt leren magisch!
    </p>
  </header>

  <!-- NAVIGATIE -->

  <nav aria-label="Hoofdnavigatie">
    <div class="nav-inner">

      <a href="#home">
        Home
      </a>

      <a href="#deze-week">
        Deze week
      </a>

      <a href="#agenda">
        Agenda
      </a>

      <a href="#nieuws">
        Nieuws
      </a>

      <a
        href="https://obsdetoverlaars.nl/"
        target="_blank"
        rel="noopener noreferrer"
      >
        Onze school
      </a>

      <a href="#adres">
        Adres
      </a>

    </div>
  </nav>

  <!-- INHOUD -->

  <main>

    <!-- DEZE WEEK -->

    <section id="deze-week">
      <h2>Deze week</h2>

      <p class="intro">
        Hier komt de tekst voor deze week te staan.
      </p>

      <p
        class="week-tekst"
        contenteditable="true"
        spellcheck="true"
      >
        Schrijf hier wat er deze week gebeurt. Bijvoorbeeld:
        Deze week werken we aan leuke opdrachten, leren we nieuwe dingen
        en bereiden we ons samen voor op de middelbare school.
      </p>

      <p class="aanwijzing">
        Klik op de tekst om deze direct aan te passen.
      </p>

      <a class="knop" href="#agenda">
        Bekijk de agenda
      </a>
    </section>

    <!-- AGENDA -->

    <section id="agenda">
      <h2>Agenda</h2>

      <p class="intro">
        Hier kun je belangrijke activiteiten, afspraken en datums neerzetten.
      </p>

      <div class="informatie-grid">

        <article class="informatie-kaart">
          <h3>Belangrijke datum</h3>

          <p
            class="agenda-tekst"
            contenteditable="true"
            spellcheck="true"
          >
            Zet hier bijvoorbeeld een belangrijke datum of activiteit.
          </p>
        </article>

        <article class="informatie-kaart">
          <h3>Activiteit</h3>

          <p
            class="agenda-tekst"
            contenteditable="true"
            spellcheck="true"
          >
            Schrijf hier wat er binnenkort gaat gebeuren.
          </p>
        </article>

      </div>

      <p class="aanwijzing">
        Klik op de tekst om de agenda aan te passen.
      </p>
    </section>

    <!-- NIEUWS -->

    <section id="nieuws">
      <h2>Nieuws</h2>

      <p class="intro">
        Hier kun je nieuws en leuke berichten van groep 8 plaatsen.
      </p>

      <p
        class="nieuws-tekst"
        contenteditable="true"
        spellcheck="true"
      >
        Schrijf hier het laatste nieuws van groep 8.
        Bijvoorbeeld: We hebben vandaag samen aan een leuke opdracht gewerkt.
      </p>

      <p class="aanwijzing">
        Klik op de tekst om het nieuws aan te passen.
      </p>
    </section>

    <!-- ADRES -->

    <section id="adres">
      <h2>Adres</h2>

      <address class="adres-box">
        <strong>Basisschool De Toverlaars</strong><br>
        Etten-Leur<br>
        Slagveld 55
      </address>
    </section>

  </main>

  <!-- FOOTER -->

  <footer>
    <div class="sterretjes">✦ ✧ ✦ ✧ ✦</div>

    <p>
      <strong>Toverlaars groep 8</strong>
    </p>

    <p>
      Samen leren, ontdekken en groeien.
    </p>
  </footer>

</body>
</html>



