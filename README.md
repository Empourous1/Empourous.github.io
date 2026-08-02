# Empourous.github.io
Pray the Chaplet of Our Lady of Champion
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Chaplet of Our Lady of Champion</title>
  <meta name="description" content="Pray the Chaplet of Our Lady of Champion with an accessible, web-based bead counter and printable prayers." />
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header class="site-header" role="banner">
    <div class="container">
      <h1 id="site-title">Chaplet of Our Lady of Champion</h1>
      <p class="tagline">An accessible web chaplet: pray, count, and reflect.</p>
      <nav aria-label="Main navigation">
        <button id="theme-toggle" aria-pressed="false" title="Toggle dark mode">🌙</button>
      </nav>
    </div>
  </header>

  <main class="container" id="main" role="main">
    <section id="about" class="card">
      <h2>About</h2>
      <p>
        This page guides you through the Chaplet of Our Lady of Champion. Use the bead controls or keyboard to advance; themes are announced before each decade. Replace or edit any text in the "Prayers" section if you want alternate wording.
      </p>
    </section>

    <section id="how-to" class="card">
      <h2>How to Pray</h2>
      <ol>
        <li>The chaplet begins with the Apostles' Creed and the Our Lady of Champion Prayer (the site will show these first).</li>
        <li>After the opening prayers you will be guided through the stem (Our Father, 3 Hail Marys, Glory Be) and then 5 decades.</li>
        <li>Before each decade a theme is announced on screen; then pray the Our Father for that decade and the decade beads which in this chaplet are the short invocation to Our Lady of Champion (repeated for each bead in the decade). After each decade say the Glory Be and the post-decade invocation shown below.</li>
        <li>At the end the Our Lady of Champion Prayer is prayed again as a closing prayer.</li>
      </ol>
    </section>

    <section id="pray-now" class="card">
      <h2 id="praynow-heading">Pray Now</h2>

      <div class="bead-panel" aria-labelledby="praynow-heading">
        <div class="bead-controls">
          <div class="bead-display" aria-live="polite" id="bead-announcer">Bead 0 of 0</div>
          <div class="bead-visual" id="bead-visual" aria-hidden="true">—</div>
        </div>

        <div class="controls">
          <button id="prev-btn" class="btn" aria-label="Previous bead">◀ Previous</button>
          <button id="next-btn" class="btn primary" aria-label="Next bead">Next ▶</button>
          <button id="reset-btn" class="btn" aria-label="Reset bead counter">Reset</button>
          <button id="print-btn" class="btn" aria-label="Print prayers">Print</button>
        </div>

        <div class="prayer-display" id="prayer-text" tabindex="0" aria-labelledby="praynow-heading">
          <!-- prayer text populated by script -->
        </div>

        <!-- Prominent theme banner (appears for theme-steps and also when a step has a theme) -->
        <div id="theme-banner" class="theme-banner" aria-live="assertive" aria-atomic="true" hidden></div>

        <div class="shortcuts">
          <strong>Keyboard:</strong> Space or Enter = Next, ← = Previous, R = Reset
        </div>
      </div>
    </section>

    <section id="prayers" class="card">
      <h2>Prayers (Edit these)</h2>
      <p>Edit the prayers below or edit <code>script.js</code> if you want alternate wording or a different sequence.</p>

      <h3>Opening Prayers</h3>
      <div class="prayer-block" id="intro-prayers">
        <p id="apostles-creed"><strong>Apostles' Creed:</strong>
        I believe in God, the Father almighty, Creator of heaven and earth; and in Jesus Christ, his only Son, our Lord, who was conceived by the Holy Spirit, born of the Virgin Mary, suffered under Pontius Pilate, was crucified, died and was buried; he descended into hell; on the third day he rose again from the dead; he ascended into heaven, and is seated at the right hand of God the Father almighty; from there he will come to judge the living and the dead. I believe in the Holy Spirit, the holy catholic Church, the communion of saints, the forgiveness of sins, the resurrection of the body, and life everlasting. Amen.</p>

        <p id="our-lady-long"><strong>Our Lady of Champion Prayer:</strong><br>
        O Dear Lady of Champion, you revealed yourself as the Queen of Heaven to your servant Adele. You gave her a mission to pray for the conversion of sinners, to bring the Good News of Jesus Christ to others and to prepare the children for the reception of the sacraments. I trust that as you called Adele to holiness, you are calling me, in my station in life, to live a holy life, devoted to Jesus Christ with the help of your maternal love. I bring before you now my worries and anxieties. I abandon my attachments to them and place them at your feet. I ask you to hear the deepest longings of my heart as I pray most earnestly for: __________ (your intention). Dear Lady, you told Adele and you say to all of us “Do not be afraid; I will help you.” Help me now as I place this intention with complete confidence and trust. Amen.</p>
      </div>

      <h3>Core Prayers</h3>
      <div class="prayer-block" id="core-prayers">
        <p id="our-father"><strong>Our Father:</strong> Our Father, who art in heaven, hallowed be Thy name; Thy kingdom come; Thy will be done on earth as it is in heaven. Give us this day our daily bread; and forgive us our trespasses, as we forgive those who trespass against us; and lead us not into temptation, but deliver us from evil. Amen.</p>

        <p id="hail-mary"><strong>Hail Mary (used in the stem only):</strong> Hail Mary, full of grace. The Lord is with thee. Blessed art thou among women, and blessed is the fruit of thy womb, Jesus. Holy Mary, Mother of God, pray for us sinners now, and at the hour of our death. Amen.</p>

        <p id="glory-be"><strong>Glory Be:</strong> Glory be to the Father, and to the Son, and to the Holy Spirit. As it was in the beginning, is now, and ever shall be, world without end. Amen.</p>

        <p id="short-invocation"><strong>Short Invocation (used for decade beads):</strong><br>
        Queen of Heaven, Our Lady of Champion, who prays for the conversion of sinners, pray for us, and intercede for us.</p>

        <p id="post-decade-invocation"><strong>Post-decade invocation (used after each Glory Be):</strong><br>
        Our Lady of Champion, pray for us and bring us closer to your son Lord Jesus.</p>
      </div>
    </section>

    <section id="resources" class="card">
      <h2>Resources</h2>
      <ul>
        <li>To add a sound chime when advancing beads, place a file named <code>chime.mp3</code> in the same folder or edit <code>script.js</code> to use a different file.</li>
        <li>To change the exact wording, edit the prayers object in <code>script.js</code> or the prayer paragraphs in <code>index.html</code>.</li>
      </ul>
    </section>
  </main>

  <footer class="site-footer" role="contentinfo">
    <div class="container">
      <small>© Chaplet of Our Lady of Champion — Template. Customize as you like.</small>
    </div>
  </footer>

  <script src="script.js" defer></script>
</body>
</html>
