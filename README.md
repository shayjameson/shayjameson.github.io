* {
  box-sizing: border-box;
}

:root {
  --bg: #120f1d;
  --bg-2: #1d1730;
  --panel: rgba(22, 18, 33, 0.7);
  --panel-strong: rgba(28, 22, 41, 0.94);
  --border: rgba(255, 255, 255, 0.12);
  --text: #f5f1ff;
  --muted: #d8cfe9;
  --pink: #ff5ea8;
  --purple: #8d7dff;
  --cyan: #50d8ff;
  --yellow: #ffd166;
  --green: #7ef2c8;
  --shadow: 0 25px 65px rgba(0, 0, 0, 0.25);
}

html {
  scroll-behavior: smooth;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: "DM Sans", sans-serif;
  background:
    radial-gradient(circle at top left, rgba(141, 125, 255, 0.35), transparent 30%),
    radial-gradient(circle at bottom right, rgba(255, 94, 168, 0.3), transparent 25%),
    linear-gradient(135deg, var(--bg), var(--bg-2));
  color: var(--text);
}

img {
  max-width: 100%;
  display: block;
}

.page-shell {
  position: relative;
  width: min(1100px, calc(100% - 32px));
  margin: 28px auto;
  padding: 20px 24px 40px;
  border: 1px solid var(--border);
  border-radius: 28px;
  background: rgba(16, 12, 24, 0.72);
  backdrop-filter: blur(18px);
  box-shadow: var(--shadow);
  overflow: hidden;
}

.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(30px);
  opacity: 0.7;
  pointer-events: none;
}

.orb-one {
  width: 220px;
  height: 220px;
  background: rgba(255, 94, 168, 0.32);
  top: -40px;
  right: 10%;
}

.orb-two {
  width: 260px;
  height: 260px;
  background: rgba(80, 216, 255, 0.24);
  bottom: 10%;
  left: -10%;
}

.orb-three {
  width: 160px;
  height: 160px;
  background: rgba(142, 125, 255, 0.18);
  bottom: 15%;
  right: 18%;
}

.site-header,
.site-main,
.site-footer {
  position: relative;
  z-index: 1;
}

.site-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 16px;
  padding: 10px 8px 28px;
}

.brand-wrap {
  display: inline-flex;
  align-items: center;
  gap: 12px;
}

.brand-mark {
  display: inline-grid;
  place-items: center;
  width: 38px;
  height: 38px;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--pink), var(--purple));
  font-weight: 700;
  color: white;
  box-shadow: 0 12px 30px rgba(255, 94, 168, 0.35);
}

.brand-name,
.site-nav a {
  color: var(--text);
  text-decoration: none;
}

.brand-name {
  font-weight: 700;
  letter-spacing: 0.02em;
}

.site-nav {
  display: inline-flex;
  align-items: center;
  gap: 18px;
  padding: 10px 16px;
  border: 1px solid var(--border);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.02);
}

.site-nav a {
  opacity: 0.8;
  font-size: 0.96rem;
}

.hero {
  display: grid;
  grid-template-columns: 1.2fr 0.8fr;
  gap: 28px;
  align-items: center;
  padding: 28px 8px 18px;
}

.eyebrow {
  margin: 0 0 16px;
  color: var(--cyan);
  text-transform: uppercase;
  letter-spacing: 0.14em;
  font-size: 0.76rem;
  font-weight: 700;
}

.hero-copy h1,
.section-heading h2 {
  margin: 0;
  font-family: "Space Grotesk", sans-serif;
  line-height: 1.02;
  letter-spacing: -0.05em;
}

.hero-copy h1 {
  max-width: 640px;
  font-size: clamp(3rem, 7vw, 5.5rem);
}

.lede {
  max-width: 560px;
  margin: 18px 0 0;
  color: var(--muted);
  font-size: 1.1rem;
  line-height: 1.7;
}

.cta-row {
  display: flex;
  flex-wrap: wrap;
  gap: 14px;
  margin-top: 28px;
}

.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-height: 48px;
  padding: 0 18px;
  border-radius: 999px;
  text-decoration: none;
  font-weight: 700;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.button:hover {
  transform: translateY(-1px);
}

.button.primary {
  background: linear-gradient(135deg, var(--pink), var(--purple));
  color: white;
  box-shadow: 0 16px 30px rgba(255, 94, 168, 0.28);
}

.button.ghost {
  border: 1px solid var(--border);
  color: var(--text);
  background: rgba(255, 255, 255, 0.02);
}

.hero-visual {
  position: relative;
  display: grid;
  justify-items: center;
  min-height: 420px;
}

.card {
  background: linear-gradient(180deg, rgba(255,255,255,0.08), rgba(255,255,255,0.02));
  border: 1px solid var(--border);
  border-radius: 24px;
  box-shadow: var(--shadow);
}

.card-large {
  width: min(100%, 350px);
  padding: 26px 24px;
  transform: rotate(6deg);
  margin-top: 28px;
}

.card-small {
  width: 220px;
  padding: 18px;
  transform: translate(-70px, -30px) rotate(-8deg);
}

.tag,
.project-badge,
.tiny-label {
  display: inline-block;
  padding: 7px 10px;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.tag {
  background: rgba(126, 242, 200, 0.14);
  color: var(--green);
}

.card-large h2 {
  margin: 18px 0 18px;
  font-size: clamp(2rem, 3vw, 2.8rem);
  font-family: "Space Grotesk", sans-serif;
}

.mini-chart {
  display: grid;
  grid-template-columns: repeat(5, minmax(0, 1fr));
  gap: 10px;
  align-items: end;
  min-height: 120px;
}

.mini-chart span {
  display: block;
  border-radius: 999px 999px 0 0;
  background: linear-gradient(180deg, var(--cyan), var(--purple));
}

.mini-chart span:nth-child(1) { height: 28%; }
.mini-chart span:nth-child(2) { height: 42%; }
.mini-chart span:nth-child(3) { height: 70%; }
.mini-chart span:nth-child(4) { height: 62%; }
.mini-chart span:nth-child(5) { height: 88%; }

.tiny-label {
  background: rgba(255, 209, 102, 0.15);
  color: var(--yellow);
}

.dot-grid {
  margin-top: 12px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
}

.dot-grid span {
  width: 50px;
  height: 50px;
  border-radius: 16px;
  background: linear-gradient(135deg, rgba(255,94,168,.9), rgba(80,216,255,.72));
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
  padding: 18px 8px 8px;
}

.info-card {
  padding: 22px 18px;
  border: 1px solid var(--border);
  border-radius: 20px;
  background: rgba(255, 255, 255, 0.025);
}

.accent-pink { box-shadow: inset 0 0 0 1px rgba(255, 94, 168, 0.15); }
.accent-yellow { box-shadow: inset 0 0 0 1px rgba(255, 209, 102, 0.18); }
.accent-purple { box-shadow: inset 0 0 0 1px rgba(141, 125, 255, 0.16); }

.card-kicker {
  margin: 0 0 12px;
  color: var(--muted);
  font-weight: 700;
}

.info-card h3 {
  margin: 0 0 10px;
  font-size: 1.35rem;
}

.info-card p:last-child {
  margin: 0;
  color: var(--muted);
  line-height: 1.7;
}

.showcase {
  padding: 42px 8px 0;
}

.section-heading {
  margin-bottom: 18px;
}

.section-heading h2 {
  font-size: clamp(2.2rem, 5vw, 3.5rem);
}

.project-list {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 18px;
}

.project-card {
  padding: 22px 20px;
  border-radius: 22px;
  border: 1px solid var(--border);
  background: rgba(255,255,255,0.03);
}

.project-badge {
  background: rgba(141, 125, 255, 0.14);
  color: #d9d0ff;
}

.project-card h3 {
  margin: 18px 0 10px;
  font-size: 1.5rem;
}

.project-card p {
  margin: 0;
  color: var(--muted);
  line-height: 1.7;
}

.site-footer {
  padding: 36px 8px 0;
  color: var(--muted);
  text-align: center;
}

@media (max-width: 800px) {
  .hero,
  .info-grid,
  .project-list {
    grid-template-columns: 1fr;
  }

  .site-header {
    flex-direction: column;
    align-items: flex-start;
  }

  .site-nav {
    width: 100%;
    justify-content: space-between;
  }

  .hero-visual {
    display: block;
  }

  .card-small {
    margin-top: 14px;
    transform: none;
  }
}
