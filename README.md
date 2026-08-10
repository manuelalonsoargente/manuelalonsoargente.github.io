<style>
  :root {
    --portal-primary: #1565c0;
    --portal-primary-dark: #0d47a1;
    --portal-secondary: #00897b;
    --portal-text: #24292f;
    --portal-muted: #57606a;
    --portal-border: #d8dee4;
    --portal-bg: #ffffff;
    --portal-card: rgba(255, 255, 255, 0.96);
    --portal-shadow: 0 10px 30px rgba(31, 35, 40, 0.10);
    --portal-shadow-hover: 0 18px 42px rgba(31, 35, 40, 0.18);
  }

  @media (prefers-color-scheme: dark) {
    :root {
      --portal-text: #f0f6fc;
      --portal-muted: #a8b3bf;
      --portal-border: #30363d;
      --portal-bg: #0d1117;
      --portal-card: rgba(22, 27, 34, 0.96);
      --portal-shadow: 0 10px 30px rgba(0, 0, 0, 0.32);
      --portal-shadow-hover: 0 18px 42px rgba(0, 0, 0, 0.5);
    }
  }

  .portal {
    max-width: 1500px;
    margin: 0 auto;
    color: var(--portal-text);
  }

  .portal * {
    box-sizing: border-box;
  }

  .portal-hero {
    position: relative;
    overflow: hidden;
    margin: 1.5rem 0 3rem;
    padding: clamp(2rem, 6vw, 4.5rem);
    border: 1px solid var(--portal-border);
    border-radius: 28px;
    background:
      radial-gradient(
        circle at top right,
        rgba(255, 255, 255, 0.24),
        transparent 32%
      ),
      linear-gradient(135deg, #0d47a1 0%, #1976d2 55%, #00897b 100%);
    box-shadow: var(--portal-shadow);
    color: white;
  }

  .portal-hero::before,
  .portal-hero::after {
    content: "";
    position: absolute;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.08);
  }

  .portal-hero::before {
    width: 260px;
    height: 260px;
    top: -130px;
    right: -70px;
  }

  .portal-hero::after {
    width: 170px;
    height: 170px;
    right: 170px;
    bottom: -110px;
  }

  .portal-hero-content {
    position: relative;
    z-index: 1;
    max-width: 1000px;
  }

  .portal-label {
    display: inline-flex;
    align-items: center;
    gap: 0.45rem;
    margin-bottom: 1rem;
    padding: 0.45rem 0.85rem;
    border: 1px solid rgba(255, 255, 255, 0.35);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.13);
    font-size: 0.85rem;
    font-weight: 700;
    letter-spacing: 0.03em;
    backdrop-filter: blur(8px);
  }

  .portal-hero h1 {
    margin: 0;
    color: white;
    font-size: clamp(2.2rem, 6vw, 4.2rem);
    line-height: 1.05;
    letter-spacing: -0.04em;
  }

  .portal-hero-subtitle {
    margin: 1rem 0 0;
    color: rgba(255, 255, 255, 0.92);
    font-size: clamp(1.05rem, 2vw, 1.3rem);
    line-height: 1.65;
  }

  .portal-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 1.8rem;
  }

  .portal-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.45rem;
    min-height: 46px;
    padding: 0.7rem 1.15rem;
    border: 1px solid rgba(255, 255, 255, 0.45);
    border-radius: 12px;
    color: white !important;
    font-weight: 700;
    text-decoration: none !important;
    transition:
      transform 0.2s ease,
      background 0.2s ease,
      box-shadow 0.2s ease;
  }

  .portal-button-primary {
    border-color: white;
    background: white;
    color: #0d47a1 !important;
  }

  .portal-button-secondary {
    background: rgba(255, 255, 255, 0.12);
    backdrop-filter: blur(8px);
  }

  .portal-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 10px 22px rgba(0, 0, 0, 0.2);
  }

  .portal-intro {
    display: grid;
    grid-template-columns: 1.4fr 0.6fr;
    gap: 1.5rem;
    margin-bottom: 3rem;
  }

  .portal-intro-card,
  .portal-info-card {
    padding: 1.6rem;
    border: 1px solid var(--portal-border);
    border-radius: 20px;
    background: var(--portal-card);
  }

  .portal-intro-card h2,
  .portal-info-card h2 {
    margin-top: 0;
  }

  .portal-intro-card p {
    margin-bottom: 0;
    color: var(--portal-muted);
    font-size: 1.05rem;
    line-height: 1.75;
  }

  .portal-info-list {
    display: grid;
    gap: 0.8rem;
    margin-top: 1rem;
  }

  .portal-info-item {
    display: flex;
    align-items: flex-start;
    gap: 0.7rem;
    color: var(--portal-muted);
  }

  .portal-info-icon {
    display: grid;
    flex: 0 0 32px;
    width: 32px;
    height: 32px;
    place-items: center;
    border-radius: 9px;
    background: rgba(21, 101, 192, 0.12);
    font-size: 1rem;
  }

  .portal-section-header {
    display: flex;
    align-items: end;
    justify-content: space-between;
    gap: 1rem;
    margin-bottom: 1.3rem;
  }

  .portal-section-header h2 {
    margin: 0;
    font-size: clamp(1.7rem, 3vw, 2.3rem);
  }

  .portal-section-header p {
    margin: 0;
    color: var(--portal-muted);
  }

  .portal-modules {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.5rem;
  }

  .portal-module-link {
    display: block;
    color: inherit !important;
    text-decoration: none !important;
  }

  .portal-module {
    position: relative;
    height: 100%;
    overflow: hidden;
    border: 1px solid var(--portal-border);
    border-radius: 22px;
    background: var(--portal-card);
    box-shadow: var(--portal-shadow);
    transition:
      transform 0.25s ease,
      box-shadow 0.25s ease,
      border-color 0.25s ease;
  }

  .portal-module:hover {
    transform: translateY(-7px);
    border-color: rgba(21, 101, 192, 0.45);
    box-shadow: var(--portal-shadow-hover);
  }

  .portal-module-image {
    position: relative;
    height: 220px;
    overflow: hidden;
    background: linear-gradient(135deg, #1976d2 0%, #00897b 100%);
  }

  .portal-module-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.45s ease;
  }

  .portal-module:hover .portal-module-image img {
    transform: scale(1.045);
  }

  .portal-module-image::after {
    content: "";
    position: absolute;
    inset: auto 0 0;
    height: 45%;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.28));
  }

  .portal-module-body {
    padding: 1.5rem;
  }

  .portal-module-top {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }

  .portal-module h3 {
    margin: 0;
    font-size: 1.55rem;
  }

  .portal-arrow {
    display: grid;
    width: 42px;
    height: 42px;
    place-items: center;
    border-radius: 50%;
    background: rgba(21, 101, 192, 0.11);
    color: var(--portal-primary);
    font-size: 1.25rem;
    transition:
      transform 0.2s ease,
      background 0.2s ease;
  }

  .portal-module:hover .portal-arrow {
    transform: translateX(4px);
    background: rgba(21, 101, 192, 0.18);
  }

  .portal-module-description {
    min-height: 3.2rem;
    margin: 0.9rem 0 1rem;
    color: var(--portal-muted);
    line-height: 1.6;
  }

  .portal-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
  }

  .portal-tag {
    padding: 0.32rem 0.65rem;
    border: 1px solid var(--portal-border);
    border-radius: 999px;
    background: rgba(21, 101, 192, 0.07);
    color: var(--portal-muted);
    font-size: 0.78rem;
    font-weight: 650;
  }

  .portal-footer {
    margin: 3.5rem 0 1.5rem;
    padding-top: 1.5rem;
    border-top: 1px solid var(--portal-border);
    color: var(--portal-muted);
    text-align: center;
    font-size: 0.9rem;
  }

  @media (max-width: 820px) {
    .portal-intro,
    .portal-modules {
      grid-template-columns: 1fr;
    }

    .portal-section-header {
      display: block;
    }

    .portal-section-header p {
      margin-top: 0.5rem;
    }
  }

  @media (max-width: 520px) {
    .portal-hero {
      padding: 2rem 1.3rem;
      border-radius: 20px;
    }

    .portal-actions {
      display: grid;
    }

    .portal-button {
      width: 100%;
    }

    .portal-module-image {
      height: 175px;
    }

    .portal-intro-card,
    .portal-info-card,
    .portal-module-body {
      padding: 1.2rem;
    }
  }
</style>

<div class="portal">

  <section class="portal-hero">
    <div class="portal-hero-content">

      <div class="portal-label">
        Formació Professional · Informàtica
      </div>

      <h1>Portal de recursos</h1>

      <p class="portal-hero-subtitle">
        Recursos, continguts i activitats per als mòduls del cicle de
        <strong>Desenvolupament d’Aplicacions Web</strong>.
      </p>

      <div class="portal-actions">
        <a href="./LLMSGI" class="portal-button portal-button-primary">
          Accedir a LMSGI →
        </a>

        <a href="./BBDD" class="portal-button portal-button-secondary">
          Accedir a BBDD →
        </a>
      </div>

    </div>
  </section>

  <section class="portal-intro">

    <div class="portal-intro-card">
      <h2>Benvinguda</h2>

      <p>
        Sóc <strong>Manuel Alonso Argente</strong>, professor de
        <strong>Formació Professional</strong> a l’IES Mestre Ramon Esteve
        de Catadau. Aquesta pàgina centralitza els materials, exemples,
        activitats i recursos dels diferents mòduls que impartisc.
      </p>
    </div>

    <aside class="portal-info-card">
      <h2>Informació</h2>

      <div class="portal-info-list">

        <div class="portal-info-item">
          <span class="portal-info-icon">🏫</span>
          <span>
            <strong>Centre</strong><br>
            IES Mestre Ramon Esteve
          </span>
        </div>

        <div class="portal-info-item">
          <span class="portal-info-icon">🎓</span>
          <span>
            <strong>Cicle</strong><br>
            Desenvolupament d’Aplicacions Web
          </span>
        </div>

        <div class="portal-info-item">
          <span class="portal-info-icon">📚</span>
          <span>
            <strong>Continguts</strong><br>
            Teoria, exemples i activitats
          </span>
        </div>

      </div>
    </aside>

  </section>

  <section>

    <div class="portal-section-header">
      <div>
        <h2>Mòduls formatius</h2>
        <p>Selecciona un mòdul per accedir als seus continguts.</p>
      </div>
    </div>

    <div class="portal-modules">

      <a href="./LLMSGI" class="portal-module-link">
        <article class="portal-module">

          <div class="portal-module-image">
            <img
              src="./img/LMSGI.png"
              alt="Llenguatges de Marques i Sistemes de Gestió d’Informació"
              onerror="this.remove()"
            >
          </div>

          <div class="portal-module-body">

            <div class="portal-module-top">
              <h3>LMSGI</h3>
              <span class="portal-arrow">→</span>
            </div>

            <p class="portal-module-description">
              Llenguatges de marques, desenvolupament web, estructuració
              de dades, validació i publicació de continguts.
            </p>

            <div class="portal-tags">
              <span class="portal-tag">HTML</span>
              <span class="portal-tag">CSS</span>
              <span class="portal-tag">JavaScript</span>
              <span class="portal-tag">XML</span>
              <span class="portal-tag">JSON</span>
            </div>

          </div>
        </article>
      </a>

      <a href="./BBDD" class="portal-module-link">
        <article class="portal-module">

          <div class="portal-module-image">
            <img
              src="./img/BBDD.png"
              alt="Bases de Dades"
              onerror="this.remove()"
            >
          </div>

          <div class="portal-module-body">

            <div class="portal-module-top">
              <h3>BBDD</h3>
              <span class="portal-arrow">→</span>
            </div>

            <p class="portal-module-description">
              Disseny de bases de dades, model relacional, llenguatge SQL,
              consultes, claus, relacions i gestió de la informació.
            </p>

            <div class="portal-tags">
              <span class="portal-tag">Model ER</span>
              <span class="portal-tag">Model relacional</span>
              <span class="portal-tag">SQL</span>
              <span class="portal-tag">MySQL</span>
              <span class="portal-tag">NoSQL</span>
            </div>

          </div>
        </article>
      </a>

    </div>
  </section>

  <footer class="portal-footer">
    Manuel Alonso Argente · Formació Professional · IES Mestre Ramon Esteve
  </footer>

</div>
