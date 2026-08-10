<style>
  :root {
    --portal-primary: #1565c0;
    --portal-primary-dark: #0d47a1;
    --portal-accent: #00897b;
    --portal-gold: #ffd54f;
    --portal-text: #24292f;
    --portal-muted: #57606a;
    --portal-border: #d8dee4;
    --portal-bg: #ffffff;
    --portal-card: rgba(255, 255, 255, 0.96);
    --portal-shadow: 0 10px 30px rgba(31, 35, 40, 0.10);
    --portal-shadow-hover: 0 18px 42px rgba(31, 35, 40, 0.18);
    --portal-font: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
      "Helvetica Neue", Arial, sans-serif;
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

  @media (prefers-reduced-motion: reduce) {
    .portal * {
      transition: none !important;
      animation: none !important;
    }
  }

  .portal {
    max-width: 1200px;
    margin: 0 auto;
    padding: clamp(1rem, 2.5vw, 2rem);
    border: 1px solid var(--portal-border);
    border-radius: 28px;
    background: var(--portal-bg);
    color: var(--portal-text);
    font-family: var(--portal-font);
  }

  .portal *,
  .portal *::before,
  .portal *::after {
    box-sizing: border-box;
  }

  .portal h2,
  .portal h3 {
    border-bottom: 0 !important;
    color: var(--portal-text);
    font-weight: 700;
  }

  .portal a {
    color: inherit;
  }

  .portal [id] {
    scroll-margin-top: 2.5rem;
  }

  .portal :focus-visible {
    outline: 3px solid var(--portal-primary);
    outline-offset: 2px;
  }

  html {
    scroll-behavior: smooth;
  }

  @media (prefers-reduced-motion: reduce) {
    html {
      scroll-behavior: auto;
    }
  }

  .portal-topbar {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 1.5rem;
    padding-bottom: 1.2rem;
    margin-bottom: 2.5rem;
    border-bottom: 1px solid var(--portal-border);
  }

  .portal-brand {
    display: flex;
    align-items: center;
    gap: 0.8rem;
    color: var(--portal-text) !important;
    text-decoration: none !important;
  }

  .portal-brand-mark {
    display: grid;
    width: 44px;
    height: 44px;
    place-items: center;
    border-radius: 12px;
    background: linear-gradient(135deg, var(--portal-primary) 0%, var(--portal-accent) 100%);
    color: #fff !important;
    font-size: 1.15rem;
    font-weight: 800;
    box-shadow: var(--portal-shadow);
  }

  .portal-brand-text strong {
    display: block;
    font-size: 1rem;
    line-height: 1.2;
  }

  .portal-brand-text small {
    display: block;
    margin-top: 0.1rem;
    color: var(--portal-muted);
    font-size: 0.78rem;
  }

  .portal-nav {
    display: flex;
    align-items: center;
    gap: 1.25rem;
  }

  .portal-nav a {
    color: var(--portal-text) !important;
    text-decoration: none !important;
    font-size: 0.95rem;
    font-weight: 600;
    transition: color 0.2s ease;
  }

  .portal-nav a:hover {
    color: var(--portal-primary) !important;
  }

  .portal-social {
    display: flex;
    gap: 0.5rem;
  }

  .portal-social a {
    display: grid;
    width: 38px;
    height: 38px;
    place-items: center;
    border: 1px solid var(--portal-border);
    border-radius: 10px;
    color: var(--portal-text) !important;
    transition:
      transform 0.2s ease,
      background 0.2s ease,
      color 0.2s ease,
      border-color 0.2s ease;
  }

  .portal-social a:hover {
    transform: translateY(-2px);
    border-color: var(--portal-primary);
    background: var(--portal-primary);
    color: #fff !important;
  }

  .portal-hero {
    position: relative;
    overflow: hidden;
    margin-bottom: 3rem;
    padding: clamp(2.2rem, 6vw, 4.5rem) clamp(1.4rem, 5vw, 4rem);
    border-radius: 28px;
    background:
      radial-gradient(circle at top right, rgba(255, 255, 255, 0.24), transparent 34%),
      linear-gradient(135deg, #0d47a1 0%, #1976d2 55%, #00897b 100%);
    box-shadow: var(--portal-shadow);
    color: #fff;
  }

  .portal-hero::before {
    content: "";
    position: absolute;
    inset: 0;
    background-image:
      linear-gradient(rgba(255, 255, 255, 0.06) 1px, transparent 1px),
      linear-gradient(90deg, rgba(255, 255, 255, 0.06) 1px, transparent 1px);
    background-size: 46px 46px;
    -webkit-mask-image: radial-gradient(ellipse at 72% 28%, #000 0%, transparent 72%);
    mask-image: radial-gradient(ellipse at 72% 28%, #000 0%, transparent 72%);
  }

  .portal-hero::after {
    content: "";
    position: absolute;
    width: 320px;
    height: 320px;
    border-radius: 50%;
    right: -110px;
    bottom: -150px;
    background: rgba(255, 255, 255, 0.08);
  }

  .portal-hero-content {
    position: relative;
    z-index: 1;
    max-width: 900px;
  }

  .portal-badge {
    display: inline-flex;
    align-items: center;
    gap: 0.5rem;
    padding: 0.5rem 0.95rem;
    border: 1px solid rgba(255, 255, 255, 0.35);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.12);
    color: rgba(255, 255, 255, 0.95);
    font-size: 0.82rem;
    font-weight: 700;
    letter-spacing: 0.04em;
    backdrop-filter: blur(8px);
  }

  .portal-hero h1 {
    margin: 1.2rem 0 0;
    color: #fff !important;
    font-size: clamp(2.4rem, 7vw, 4.4rem);
    line-height: 1.05;
    font-weight: 800;
    letter-spacing: -0.03em;
  }

  .portal-hero-accent {
    background: linear-gradient(90deg, var(--portal-gold) 0%, #ffb74d 100%);
    -webkit-background-clip: text;
    background-clip: text;
    -webkit-text-fill-color: transparent;
    color: transparent;
  }

  .portal-hero-subtitle {
    margin: 1.1rem 0 0;
    max-width: 56ch;
    color: rgba(255, 255, 255, 0.92);
    font-size: clamp(1.05rem, 1.8vw, 1.25rem);
    line-height: 1.7;
  }

  .portal-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.8rem;
    margin-top: 2rem;
  }

  .portal-button {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    min-height: 48px;
    padding: 0.75rem 1.4rem;
    border: 1px solid rgba(255, 255, 255, 0.45);
    border-radius: 12px;
    font-weight: 700;
    text-decoration: none !important;
    transition:
      transform 0.2s ease,
      background 0.2s ease,
      box-shadow 0.2s ease;
  }

  .portal-button-primary {
    border-color: #fff;
    background: #fff;
    color: #0d47a1 !important;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.18);
  }

  .portal-button-secondary {
    background: rgba(255, 255, 255, 0.12);
    color: #fff !important;
    backdrop-filter: blur(8px);
  }

  .portal-button:hover {
    transform: translateY(-3px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.24);
  }

  .portal-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
    margin-top: 2.2rem;
  }

  .portal-tech span {
    padding: 0.35rem 0.75rem;
    border: 1px solid rgba(255, 255, 255, 0.28);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.08);
    color: rgba(255, 255, 255, 0.9);
    font-size: 0.78rem;
    font-weight: 600;
    letter-spacing: 0.03em;
  }

  .portal-intro {
    display: grid;
    grid-template-columns: 1.35fr 0.65fr;
    gap: 1.5rem;
    margin-bottom: 3.5rem;
  }

  .portal-card {
    padding: 1.8rem;
    border: 1px solid var(--portal-border);
    border-radius: 20px;
    background: var(--portal-card);
    box-shadow: var(--portal-shadow);
  }

  .portal-card h2 {
    margin: 0 0 0.8rem;
    font-size: 1.35rem;
  }

  .portal-intro-card p {
    margin: 0;
    color: var(--portal-muted);
    font-size: 1.02rem;
    line-height: 1.8;
  }

  .portal-info-list {
    display: grid;
    gap: 1rem;
    margin-top: 1.1rem;
  }

  .portal-info-item {
    display: flex;
    align-items: flex-start;
    gap: 0.8rem;
    color: var(--portal-muted);
    font-size: 0.95rem;
    line-height: 1.5;
  }

  .portal-info-icon {
    display: grid;
    flex: 0 0 40px;
    width: 40px;
    height: 40px;
    place-items: center;
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(21, 101, 192, 0.12), rgba(0, 137, 123, 0.12));
    color: var(--portal-primary);
  }

  .portal-features {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 1rem;
    margin-bottom: 3.5rem;
  }

  .portal-feature {
    padding: 1.4rem;
    border: 1px solid var(--portal-border);
    border-radius: 16px;
    background: var(--portal-card);
    transition:
      transform 0.2s ease,
      border-color 0.2s ease,
      box-shadow 0.2s ease;
  }

  .portal-feature:hover {
    transform: translateY(-4px);
    border-color: rgba(21, 101, 192, 0.4);
    box-shadow: var(--portal-shadow);
  }

  .portal-feature-icon {
    display: grid;
    width: 44px;
    height: 44px;
    place-items: center;
    margin-bottom: 1rem;
    border-radius: 12px;
    background: linear-gradient(135deg, rgba(21, 101, 192, 0.12), rgba(0, 137, 123, 0.12));
    color: var(--portal-primary);
  }

  .portal-feature h3 {
    margin: 0 0 0.4rem;
    font-size: 1.02rem;
  }

  .portal-feature p {
    margin: 0;
    color: var(--portal-muted);
    font-size: 0.9rem;
    line-height: 1.6;
  }

  .portal-section-header {
    display: flex;
    align-items: end;
    justify-content: space-between;
    gap: 1rem;
    margin-bottom: 1.4rem;
  }

  .portal-eyebrow {
    margin: 0 0 0.35rem;
    color: var(--portal-primary);
    font-size: 0.8rem;
    font-weight: 800;
    letter-spacing: 0.1em;
    text-transform: uppercase;
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
    height: 100%;
    color: inherit !important;
    text-decoration: none !important;
  }

  .portal-module {
    --module-accent: var(--portal-primary);
    display: flex;
    flex-direction: column;
    height: 100%;
    overflow: hidden;
    border: 1px solid var(--portal-border);
    border-radius: 22px;
    background: var(--portal-card);
    box-shadow: var(--portal-shadow);
    transition:
      transform 0.25s ease,
      border-color 0.25s ease,
      box-shadow 0.25s ease;
  }

  .portal-module:hover {
    transform: translateY(-7px);
    border-color: rgba(21, 101, 192, 0.45);
    border-color: color-mix(in srgb, var(--module-accent) 45%, var(--portal-border));
    box-shadow: var(--portal-shadow-hover);
  }

  .portal-module-image {
    position: relative;
    height: 200px;
    overflow: hidden;
    background: linear-gradient(135deg, var(--module-accent) 0%, var(--portal-accent) 100%);
  }

  .portal-module-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: transform 0.5s ease;
  }

  .portal-module:hover .portal-module-image img {
    transform: scale(1.06);
  }

  .portal-module-image::after {
    content: "";
    position: absolute;
    inset: 0;
    background: linear-gradient(180deg, transparent 32%, rgba(0, 0, 0, 0.4));
  }

  .portal-module-overlay {
    position: absolute;
    z-index: 1;
    inset: auto 0 0;
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    gap: 1rem;
    padding: 1.1rem 1.4rem;
  }

  .portal-module-acronym {
    margin: 0;
    color: #fff;
    font-size: 2.5rem;
    line-height: 1;
    font-weight: 800;
    letter-spacing: 0.02em;
    text-shadow: 0 2px 14px rgba(0, 0, 0, 0.35);
  }

  .portal-module-chip {
    padding: 0.35rem 0.7rem;
    border: 1px solid rgba(255, 255, 255, 0.35);
    border-radius: 999px;
    background: rgba(255, 255, 255, 0.16);
    color: #fff;
    font-size: 0.75rem;
    font-weight: 700;
    backdrop-filter: blur(6px);
  }

  .portal-module-body {
    display: flex;
    flex-direction: column;
    flex: 1;
    padding: 1.4rem 1.5rem 1.5rem;
  }

  .portal-module-body h3 {
    margin: 0 0 0.8rem;
    font-size: 1.25rem;
    line-height: 1.3;
  }

  .portal-module-description {
    margin: 0 0 1.1rem;
    color: var(--portal-muted);
    font-size: 0.95rem;
    line-height: 1.65;
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

  .portal-module-foot {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: auto;
    padding-top: 1.15rem;
    border-top: 1px solid var(--portal-border);
  }

  .portal-module-foot span {
    display: inline-flex;
    align-items: center;
    gap: 0.45rem;
    color: var(--module-accent);
    font-size: 0.92rem;
    font-weight: 700;
    transition: gap 0.2s ease;
  }

  .portal-module:hover .portal-module-foot span {
    gap: 0.7rem;
  }

  .portal-cta {
    position: relative;
    overflow: hidden;
    margin: 3.5rem 0;
    padding: clamp(2rem, 5vw, 3.2rem);
    border-radius: 24px;
    background: linear-gradient(135deg, #0d47a1 0%, #1976d2 60%, #00897b 100%);
    box-shadow: var(--portal-shadow);
    color: #fff;
    text-align: center;
  }

  .portal-cta h2 {
    margin: 0 0 0.7rem;
    color: #fff !important;
    font-size: clamp(1.6rem, 4vw, 2.4rem);
  }

  .portal-cta p {
    margin: 0 auto 1.7rem;
    max-width: 52ch;
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.7;
  }

  .portal-cta-actions {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 0.8rem;
  }

  .portal-cta .portal-button {
    min-width: 180px;
  }

  .portal-cta .portal-button-secondary svg {
    margin-right: 0.2rem;
  }

  .portal-footer {
    display: grid;
    grid-template-columns: 1.4fr 1fr 1fr;
    gap: 2rem;
    padding-top: 2.5rem;
    border-top: 1px solid var(--portal-border);
  }

  .portal-footer h4 {
    margin: 0 0 0.9rem;
    color: var(--portal-text);
    font-size: 0.82rem;
    font-weight: 800;
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  .portal-footer p {
    margin: 0;
    color: var(--portal-muted);
    font-size: 0.9rem;
    line-height: 1.7;
  }

  .portal-footer ul {
    display: grid;
    gap: 0.55rem;
    margin: 0;
    padding: 0;
    list-style: none;
  }

  .portal-footer a {
    color: var(--portal-muted) !important;
    text-decoration: none !important;
    font-size: 0.92rem;
    transition: color 0.2s ease;
  }

  .portal-footer a:hover {
    color: var(--portal-primary) !important;
  }

  .portal-footer-bottom {
    grid-column: 1 / -1;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
    padding-top: 1.2rem;
    border-top: 1px solid var(--portal-border);
    color: var(--portal-muted);
    font-size: 0.85rem;
  }

  .portal-footer-bottom .portal-social a {
    width: 34px;
    height: 34px;
  }

  @media (max-width: 1000px) {
    .portal-intro {
      grid-template-columns: 1fr;
    }

    .portal-features {
      grid-template-columns: repeat(2, 1fr);
    }

    .portal-footer {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media (max-width: 760px) {
    .portal-modules {
      grid-template-columns: 1fr;
    }

    .portal-nav {
      display: none;
    }

    .portal-footer {
      grid-template-columns: 1fr;
    }

    .portal-footer-bottom {
      flex-direction: column;
      align-items: flex-start;
    }
  }

  @media (max-width: 540px) {
    .portal-hero {
      padding: 2rem 1.3rem;
      border-radius: 20px;
    }

    .portal-features {
      grid-template-columns: 1fr;
    }

    .portal-actions {
      display: grid;
    }

    .portal-button {
      width: 100%;
    }

    .portal-module-image {
      height: 170px;
    }

    .portal-module-acronym {
      font-size: 1.9rem;
    }

    .portal-card {
      padding: 1.3rem;
    }

    .portal-section-header {
      display: block;
    }

    .portal-section-header p {
      margin-top: 0.5rem;
    }
  }
</style>

<div class="portal">

  <header class="portal-topbar">

    <a class="portal-brand" href="#inici" aria-label="Inici del portal">
      <span class="portal-brand-mark" aria-hidden="true">M</span>
      <span class="portal-brand-text">
        <strong>Portal de recursos formatius</strong>
        <small>Formació Professional · Informàtica</small>
      </span>
    </a>

    <nav class="portal-nav" aria-label="Navegació principal">
      <a href="#inici">Inici</a>
      <a href="#moduls">Mòduls</a>
      <a href="#contacte">Contacte</a>
    </nav>

    <div class="portal-social">
      <a href="https://github.com/manuelalonsoargente" target="_blank" rel="noopener" aria-label="GitHub">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
          <path d="M12 .5C5.7.5.5 5.7.5 12c0 5.1 3.3 9.4 7.9 10.9.6.1.8-.3.8-.6v-2c-3.2.7-3.9-1.5-3.9-1.5-.5-1.3-1.3-1.7-1.3-1.7-1-.7.1-.7.1-.7 1.2.1 1.8 1.2 1.8 1.2 1 1.8 2.7 1.3 3.4 1 .1-.8.4-1.3.7-1.6-2.6-.3-5.3-1.3-5.3-5.7 0-1.3.4-2.3 1.2-3.1-.1-.3-.5-1.5.1-3.1 0 0 1-.3 3.2 1.2a11 11 0 0 1 5.8 0C17.9 5.3 18.9 5.6 18.9 5.6c.6 1.6.2 2.8.1 3.1.8.8 1.2 1.8 1.2 3.1 0 4.4-2.7 5.4-5.3 5.7.4.4.8 1.1.8 2.2v3.3c0 .3.2.7.8.6a11.5 11.5 0 0 0 7.9-10.9C23.5 5.7 18.3.5 12 .5z"></path>
        </svg>
      </a>
      <a href="https://www.linkedin.com/in/manuel-alonso-argente-10a7111a/" target="_blank" rel="noopener" aria-label="LinkedIn">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 1 1 0-4.124 2.062 2.062 0 0 1 0 4.124zM7.119 20.452H3.555V9h3.564v11.452z"></path>
        </svg>
      </a>
    </div>

  </header>

  <section class="portal-hero" id="inici">

    <div class="portal-hero-content">

      <span class="portal-badge">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
          <path d="M22 10 12 5 2 10l10 5 10-5z"></path>
          <path d="M6 12v5c0 1.7 2.7 3 6 3s6-1.3 6-3v-5"></path>
          <path d="M22 10v6"></path>
        </svg>
        CFGS · Desenvolupament d'Aplicacions Web
      </span>

      <h1>Portal de recursos <span class="portal-hero-accent">formatius</span></h1>

      <p class="portal-hero-subtitle">
        Materials, teoria, exemples i activitats dels mòduls de 1r del cicle
        de Desenvolupament d'Aplicacions Web, amb accés directe a cada assignatura.
      </p>

      <div class="portal-actions">
        <a href="./LLMSGI" class="portal-button portal-button-primary">
          Accedir a LMSGI
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <line x1="5" y1="12" x2="19" y2="12"></line>
            <polyline points="12 5 19 12 12 19"></polyline>
          </svg>
        </a>

        <a href="./BBDD" class="portal-button portal-button-secondary">
          Accedir a BBDD
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
            <line x1="5" y1="12" x2="19" y2="12"></line>
            <polyline points="12 5 19 12 12 19"></polyline>
          </svg>
        </a>
      </div>

      <div class="portal-tech" aria-label="Tecnologies principals">
        <span>HTML</span>
        <span>CSS</span>
        <span>JavaScript</span>
        <span>XML</span>
        <span>JSON</span>
        <span>SQL</span>
        <span>NoSQL</span>
      </div>

    </div>
  </section>

  <section class="portal-intro">

    <div class="portal-card portal-intro-card">
      <h2>Benvinguda</h2>
      <p>
        Sóc <strong>Manuel Alonso Argente</strong>, professor de
        <strong>Formació Professional</strong> a l'IES Mestre Ramon Esteve
        de Catadau. Aquest portal centralitza els materials, exemples,
        activitats i recursos dels mòduls que impartisc, amb accés directe
        a cada assignatura.
      </p>
    </div>

    <aside class="portal-card portal-info-card" aria-label="Informació">
      <h2>Informació</h2>

      <div class="portal-info-list">

        <div class="portal-info-item">
          <span class="portal-info-icon" aria-hidden="true">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M3 21h18"></path>
              <path d="M5 21V7l7-4 7 4v14"></path>
              <path d="M9 9h1.01"></path>
              <path d="M9 13h1.01"></path>
              <path d="M9 17h1.01"></path>
              <path d="M14 9h1.01"></path>
              <path d="M14 13h1.01"></path>
              <path d="M14 17h1.01"></path>
            </svg>
          </span>
          <span>
            <strong>Centre</strong><br>
            IES Mestre Ramon Esteve
          </span>
        </div>

        <div class="portal-info-item">
          <span class="portal-info-icon" aria-hidden="true">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M22 10 12 5 2 10l10 5 10-5z"></path>
              <path d="M6 12v5c0 1.7 2.7 3 6 3s6-1.3 6-3v-5"></path>
              <path d="M22 10v6"></path>
            </svg>
          </span>
          <span>
            <strong>Cicle</strong><br>
            CFGS · Desenvolupament d'Aplicacions Web
          </span>
        </div>

        <div class="portal-info-item">
          <span class="portal-info-icon" aria-hidden="true">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <rect x="3" y="4" width="18" height="18" rx="2"></rect>
              <line x1="16" y1="2" x2="16" y2="6"></line>
              <line x1="8" y1="2" x2="8" y2="6"></line>
              <line x1="3" y1="10" x2="21" y2="10"></line>
            </svg>
          </span>
          <span>
            <strong>Curs</strong><br>
            Primer
          </span>
        </div>

        <div class="portal-info-item">
          <span class="portal-info-icon" aria-hidden="true">
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M2 4h6a4 4 0 0 1 4 4v12a3 3 0 0 0-3-3H2z"></path>
              <path d="M22 4h-6a4 4 0 0 0-4 4v12a3 3 0 0 1 3-3h7z"></path>
            </svg>
          </span>
          <span>
            <strong>Continguts</strong><br>
            Teoria, exemples i activitats
          </span>
        </div>

      </div>
    </aside>

  </section>

  <section class="portal-features" aria-label="Com es treballa">

    <div class="portal-feature">
      <span class="portal-feature-icon" aria-hidden="true">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M9 18h6"></path>
          <path d="M10 22h4"></path>
          <path d="M12 2a7 7 0 0 0-4 12.7c.8.6 1 1.3 1 2.3h6c0-1 .2-1.7 1-2.3A7 7 0 0 0 12 2z"></path>
        </svg>
      </span>
      <h3>Teoria</h3>
      <p>Documents, apunts i esquemes de cada unitat formativa.</p>
    </div>

    <div class="portal-feature">
      <span class="portal-feature-icon" aria-hidden="true">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <polyline points="16 18 22 12 16 6"></polyline>
          <polyline points="8 6 2 12 8 18"></polyline>
        </svg>
      </span>
      <h3>Exemples</h3>
      <p>Casos resolts per aplicar els conceptes a situacions reals.</p>
    </div>

    <div class="portal-feature">
      <span class="portal-feature-icon" aria-hidden="true">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <rect x="8" y="2" width="8" height="4" rx="1"></rect>
          <path d="M16 4h2a2 2 0 0 1 2 2v14a2 2 0 0 1-2 2H6a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2h2"></path>
          <line x1="9" y1="12" x2="15" y2="12"></line>
          <line x1="9" y1="16" x2="13" y2="16"></line>
        </svg>
      </span>
      <h3>Activitats</h3>
      <p>Pràctiques i exercicis per consolidar i repassar els continguts.</p>
    </div>

    <div class="portal-feature">
      <span class="portal-feature-icon" aria-hidden="true">
        <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M22 19a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h5l2 3h9a2 2 0 0 1 2 2z"></path>
        </svg>
      </span>
      <h3>Recursos</h3>
      <p>Enllaços i materials complementaris per ampliar coneixements.</p>
    </div>

  </section>

  <section id="moduls">

    <div class="portal-section-header">
      <div>
        <p class="portal-eyebrow">Continguts</p>
        <h2>Mòduls formatius</h2>
      </div>
      <p>Selecciona un mòdul per accedir als seus continguts.</p>
    </div>

    <div class="portal-modules">

      <a href="./LLMSGI" class="portal-module-link">
        <article class="portal-module" style="--module-accent: var(--portal-primary)">

          <div class="portal-module-image">
            <img
              src="./img/LMSGI.png"
              alt="Llenguatges de Marques i Sistemes de Gestió d'Informació"
              onerror="this.remove()"
            >
            <div class="portal-module-overlay">
              <p class="portal-module-acronym">LMSGI</p>
              <span class="portal-module-chip">1r DAW</span>
            </div>
          </div>

          <div class="portal-module-body">
            <h3>Llenguatges de Marques i Sistemes de Gestió d'Informació</h3>

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

            <div class="portal-module-foot">
              <span>
                Veure continguts
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                  <line x1="5" y1="12" x2="19" y2="12"></line>
                  <polyline points="12 5 19 12 12 19"></polyline>
                </svg>
              </span>
            </div>
          </div>
        </article>
      </a>

      <a href="./BBDD" class="portal-module-link">
        <article class="portal-module" style="--module-accent: var(--portal-accent)">

          <div class="portal-module-image">
            <img
              src="./img/BBDD.png"
              alt="Bases de Dades"
              onerror="this.remove()"
            >
            <div class="portal-module-overlay">
              <p class="portal-module-acronym">BBDD</p>
              <span class="portal-module-chip">1r DAW</span>
            </div>
          </div>

          <div class="portal-module-body">
            <h3>Bases de Dades</h3>

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

            <div class="portal-module-foot">
              <span>
                Veure continguts
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true">
                  <line x1="5" y1="12" x2="19" y2="12"></line>
                  <polyline points="12 5 19 12 12 19"></polyline>
                </svg>
              </span>
            </div>
          </div>
        </article>
      </a>

    </div>
  </section>

  <section class="portal-cta" id="contacte">

    <h2>Preguntes o suggeriments?</h2>
    <p>
      Si vols consultar algun contingut o tens qualsevol dubte sobre els
      mòduls, pots contactar amb mi a través de les xarxes.
    </p>

    <div class="portal-cta-actions">
      <a href="#moduls" class="portal-button portal-button-primary">
        Accedir als mòduls
      </a>

      <a href="https://github.com/manuelalonsoargente" target="_blank" rel="noopener" class="portal-button portal-button-secondary">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
          <path d="M12 .5C5.7.5.5 5.7.5 12c0 5.1 3.3 9.4 7.9 10.9.6.1.8-.3.8-.6v-2c-3.2.7-3.9-1.5-3.9-1.5-.5-1.3-1.3-1.7-1.3-1.7-1-.7.1-.7.1-.7 1.2.1 1.8 1.2 1.8 1.2 1 1.8 2.7 1.3 3.4 1 .1-.8.4-1.3.7-1.6-2.6-.3-5.3-1.3-5.3-5.7 0-1.3.4-2.3 1.2-3.1-.1-.3-.5-1.5.1-3.1 0 0 1-.3 3.2 1.2a11 11 0 0 1 5.8 0C17.9 5.3 18.9 5.6 18.9 5.6c.6 1.6.2 2.8.1 3.1.8.8 1.2 1.8 1.2 3.1 0 4.4-2.7 5.4-5.3 5.7.4.4.8 1.1.8 2.2v3.3c0 .3.2.7.8.6a11.5 11.5 0 0 0 7.9-10.9C23.5 5.7 18.3.5 12 .5z"></path>
        </svg>
        GitHub
      </a>

      <a href="https://www.linkedin.com/in/manuel-alonso-argente-10a7111a/" target="_blank" rel="noopener" class="portal-button portal-button-secondary">
        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 1 1 0-4.124 2.062 2.062 0 0 1 0 4.124zM7.119 20.452H3.555V9h3.564v11.452z"></path>
        </svg>
        LinkedIn
      </a>
    </div>

  </section>

  <footer class="portal-footer">

    <div>
      <h4>Sobre el portal</h4>
      <p>
        Recursos formatius dels mòduls de 1r del cicle de Desenvolupament
        d'Aplicacions Web a l'IES Mestre Ramon Esteve de Catadau.
      </p>
    </div>

    <div>
      <h4>Navegació</h4>
      <ul>
        <li><a href="#inici">Inici</a></li>
        <li><a href="#moduls">Mòduls</a></li>
        <li><a href="#contacte">Contacte</a></li>
      </ul>
    </div>

    <div>
      <h4>Mòduls</h4>
      <ul>
        <li><a href="./LLMSGI">Llenguatges de Marques i Sistemes de Gestió d'Informació</a></li>
        <li><a href="./BBDD">Bases de Dades</a></li>
      </ul>
    </div>

    <div class="portal-footer-bottom">
      <span>&copy; 2026 Manuel Alonso Argente · IES Mestre Ramon Esteve</span>
      <div class="portal-social">
        <a href="https://github.com/manuelalonsoargente" target="_blank" rel="noopener" aria-label="GitHub">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M12 .5C5.7.5.5 5.7.5 12c0 5.1 3.3 9.4 7.9 10.9.6.1.8-.3.8-.6v-2c-3.2.7-3.9-1.5-3.9-1.5-.5-1.3-1.3-1.7-1.3-1.7-1-.7.1-.7.1-.7 1.2.1 1.8 1.2 1.8 1.2 1 1.8 2.7 1.3 3.4 1 .1-.8.4-1.3.7-1.6-2.6-.3-5.3-1.3-5.3-5.7 0-1.3.4-2.3 1.2-3.1-.1-.3-.5-1.5.1-3.1 0 0 1-.3 3.2 1.2a11 11 0 0 1 5.8 0C17.9 5.3 18.9 5.6 18.9 5.6c.6 1.6.2 2.8.1 3.1.8.8 1.2 1.8 1.2 3.1 0 4.4-2.7 5.4-5.3 5.7.4.4.8 1.1.8 2.2v3.3c0 .3.2.7.8.6a11.5 11.5 0 0 0 7.9-10.9C23.5 5.7 18.3.5 12 .5z"></path>
          </svg>
        </a>
        <a href="https://www.linkedin.com/in/manuel-alonso-argente-10a7111a/" target="_blank" rel="noopener" aria-label="LinkedIn">
          <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="currentColor" aria-hidden="true">
            <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 1 1 0-4.124 2.062 2.062 0 0 1 0 4.124zM7.119 20.452H3.555V9h3.564v11.452z"></path>
          </svg>
        </a>
      </div>
    </div>

  </footer>

</div>
