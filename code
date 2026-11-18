<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>THE YOUNG PRODIGIES — Quiet Luxury Atelier | Kumasi &amp; Global</title>

  <!-- Google Fonts: Cormorant Garamond (Luxury Editorial Serif) & Plus Jakarta Sans (Clean Modernist Sans) -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Plus+Jakarta+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />

  <!-- Paystack Inline JS SDK -->
  <script src="https://js.paystack.co/v1/inline.js"></script>

  <style>
    :root {
      --bg-bone: #F8F6F2;
      --bg-ivory: #FFFFFF;
      --bg-sand: #EFECE6;
      --ink-obsidian: #121110;
      --ink-charcoal: #2D2A27;
      --ink-muted: #767068;
      --gold-asante: #B5945B;
      --gold-soft: rgba(181, 148, 91, 0.16);
      --border-hairline: rgba(18, 17, 16, 0.10);
      --border-strong: rgba(18, 17, 16, 0.24);
      --font-serif: 'Cormorant Garamond', Georgia, serif;
      --font-sans: 'Plus Jakarta Sans', -apple-system, BlinkMacSystemFont, sans-serif;
      --ease-luxury: cubic-bezier(0.22, 1, 0.36, 1);
      --ease-curtain: cubic-bezier(0.77, 0, 0.175, 1);
      --nav-height: 76px;
    }

    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      font-size: 16px;
      background-color: var(--bg-bone);
      color: var(--ink-obsidian);
      -webkit-font-smoothing: antialiased;
    }

    body {
      font-family: var(--font-sans);
      background-color: var(--bg-bone);
      color: var(--ink-obsidian);
      line-height: 1.6;
      overflow-x: hidden;
    }

    body.no-scroll {
      overflow: hidden;
    }

    img, video {
      display: block;
      max-width: 100%;
    }

    button, input, select, textarea {
      font-family: inherit;
      color: inherit;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    /* ==================== WELCOME CURTAIN FEATURE ==================== */
    .welcome-overlay {
      position: fixed;
      inset: 0;
      z-index: 9999;
      background: #0D0C0B;
      color: #F8F6F2;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
      transition: transform 1.15s var(--ease-curtain), opacity 0.9s ease;
    }

    .welcome-overlay.is-dismissed {
      transform: translateY(-100%);
      pointer-events: none;
    }

    .welcome-overlay.is-hidden {
      display: none;
    }

    /* Floating Ambient Orbs & Silk Shimmer */
    .welcome-orb {
      position: absolute;
      border-radius: 50%;
      filter: blur(80px);
      opacity: 0.45;
      pointer-events: none;
      will-change: transform;
    }

    .welcome-orb--1 {
      width: 46vw;
      height: 46vw;
      max-width: 560px;
      max-height: 560px;
      background: radial-gradient(circle, rgba(181, 148, 91, 0.52) 0%, rgba(181, 148, 91, 0) 72%);
      top: -12%;
      left: -8%;
      animation: floatOrbOne 12s ease-in-out infinite alternate;
    }

    .welcome-orb--2 {
      width: 40vw;
      height: 40vw;
      max-width: 480px;
      max-height: 480px;
      background: radial-gradient(circle, rgba(160, 128, 86, 0.34) 0%, rgba(18, 17, 16, 0) 70%);
      bottom: -14%;
      right: -6%;
      animation: floatOrbTwo 14s ease-in-out infinite alternate;
    }

    .welcome-grid-lines {
      position: absolute;
      inset: 0;
      background-image: linear-gradient(to right, rgba(248, 246, 242, 0.03) 1px, transparent 1px),
                        linear-gradient(to bottom, rgba(248, 246, 242, 0.03) 1px, transparent 1px);
      background-size: 96px 96px;
      mask-image: radial-gradient(circle at center, black 35%, transparent 80%);
      pointer-events: none;
    }

    .welcome-content {
      position: relative;
      z-index: 2;
      text-align: center;
      padding: 2rem;
      max-width: 780px;
    }

    .welcome-monogram {
      width: 74px;
      height: 74px;
      margin: 0 auto 2rem;
      border: 1px solid rgba(181, 148, 91, 0.55);
      border-radius: 50%;
      display: grid;
      place-items: center;
      font-family: var(--font-serif);
      font-size: 1.35rem;
      letter-spacing: 0.2em;
      color: var(--gold-asante);
      animation: floatGentle 4.8s ease-in-out infinite, fadeRise 1s var(--ease-luxury) both;
      box-shadow: 0 0 40px rgba(181, 148, 91, 0.14);
    }

    .welcome-kicker {
      font-size: 0.72rem;
      letter-spacing: 0.34em;
      text-transform: uppercase;
      color: var(--gold-asante);
      margin-bottom: 1.2rem;
      animation: fadeRise 1s 0.18s var(--ease-luxury) both;
    }

    .welcome-title {
      font-family: var(--font-serif);
      font-weight: 300;
      font-size: clamp(2.8rem, 7vw, 5.4rem);
      line-height: 1.03;
      letter-spacing: 0.04em;
      margin-bottom: 1.35rem;
      animation: fadeRise 1.1s 0.32s var(--ease-luxury) both, floatTitle 6.5s 1.2s ease-in-out infinite;
    }

    .welcome-title em {
      font-style: italic;
      color: #E7D8BE;
    }

    .welcome-sub {
      font-size: 0.96rem;
      font-weight: 300;
      color: rgba(248, 246, 242, 0.72);
      max-width: 480px;
      margin: 0 auto 2.6rem;
      animation: fadeRise 1.1s 0.48s var(--ease-luxury) both;
    }

    .welcome-actions {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 1.1rem;
      animation: fadeRise 1.1s 0.64s var(--ease-luxury) both;
    }

    .btn-enter {
      position: relative;
      overflow: hidden;
      background: transparent;
      color: #F8F6F2;
      border: 1px solid rgba(248, 246, 242, 0.38);
      padding: 1.05rem 2.9rem;
      font-size: 0.76rem;
      letter-spacing: 0.28em;
      text-transform: uppercase;
      cursor: pointer;
      transition: border-color 0.4s ease, color 0.4s ease, transform 0.4s var(--ease-luxury);
      animation: floatGentle 5.5s 1s ease-in-out infinite;
    }

    .btn-enter::before {
      content: '';
      position: absolute;
      inset: 0;
      background: var(--gold-asante);
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.55s var(--ease-luxury);
      z-index: -1;
    }

    .btn-enter:hover {
      border-color: var(--gold-asante);
      color: #0D0C0B;
      transform: translateY(-2px);
    }

    .btn-enter:hover::before {
      transform: scaleX(1);
    }

    .welcome-meta {
      font-size: 0.7rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: rgba(248, 246, 242, 0.45);
    }

    @keyframes floatOrbOne {
      0% { transform: translate(0, 0) scale(1); }
      100% { transform: translate(12vw, 8vh) scale(1.15); }
    }

    @keyframes floatOrbTwo {
      0% { transform: translate(0, 0) scale(1); }
      100% { transform: translate(-10vw, -10vh) scale(1.18); }
    }

    @keyframes floatGentle {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-8px); }
    }

    @keyframes floatTitle {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-5px); }
    }

    @keyframes fadeRise {
      from {
        opacity: 0;
        transform: translateY(24px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* ==================== NAVIGATION ==================== */
    .site-header {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      height: var(--nav-height);
      z-index: 900;
      background: rgba(248, 246, 242, 0.86);
      backdrop-filter: blur(16px);
      -webkit-backdrop-filter: blur(16px);
      border-bottom: 1px solid var(--border-hairline);
      transition: background 0.4s ease, border-color 0.4s ease;
    }

    .site-header.is-hero-overlay {
      background: rgba(18, 17, 16, 0.34);
      border-bottom-color: rgba(255, 255, 255, 0.14);
      color: #F8F6F2;
    }

    .nav-inner {
      max-width: 1440px;
      height: 100%;
      margin: 0 auto;
      padding: 0 clamp(1.25rem, 4vw, 3.5rem);
      display: grid;
      grid-template-columns: 1fr auto 1fr;
      align-items: center;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 2.2rem;
    }

    .nav-link {
      background: none;
      border: none;
      cursor: pointer;
      font-size: 0.72rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      font-weight: 500;
      position: relative;
      padding: 0.35rem 0;
      opacity: 0.74;
      transition: opacity 0.3s ease;
    }

    .nav-link::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: 0;
      width: 100%;
      height: 1px;
      background: currentColor;
      transform: scaleX(0);
      transform-origin: right;
      transition: transform 0.4s var(--ease-luxury);
    }

    .nav-link:hover,
    .nav-link.is-active {
      opacity: 1;
    }

    .nav-link.is-active::after,
    .nav-link:hover::after {
      transform: scaleX(1);
      transform-origin: left;
    }

    .brand-mark {
      background: none;
      border: none;
      cursor: pointer;
      text-align: center;
      font-family: var(--font-serif);
      font-size: clamp(1.15rem, 2.2vw, 1.55rem);
      font-weight: 500;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      white-space: nowrap;
    }

    .brand-mark span {
      display: block;
      font-family: var(--font-sans);
      font-size: 0.56rem;
      letter-spacing: 0.34em;
      opacity: 0.65;
      margin-top: 1px;
    }

    .nav-utilities {
      display: flex;
      align-items: center;
      justify-content: flex-end;
      gap: 1.6rem;
    }

    .currency-pill {
      font-size: 0.68rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      padding: 0.35rem 0.7rem;
      border: 1px solid currentColor;
      border-radius: 999px;
      opacity: 0.72;
    }

    .bag-trigger {
      background: none;
      border: none;
      cursor: pointer;
      display: flex;
      align-items: center;
      gap: 0.55rem;
      font-size: 0.72rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      font-weight: 500;
    }

    .bag-count {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-width: 22px;
      height: 22px;
      padding: 0 6px;
      border-radius: 999px;
      background: var(--gold-asante);
      color: #FFFFFF;
      font-size: 0.68rem;
      font-weight: 600;
    }

    .mobile-menu-btn {
      display: none;
      background: none;
      border: none;
      cursor: pointer;
      font-size: 0.74rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
    }

    .mobile-drawer {
      position: fixed;
      inset: 0;
      z-index: 950;
      background: var(--ink-obsidian);
      color: var(--bg-bone);
      display: flex;
      flex-direction: column;
      justify-content: center;
      padding: 2.5rem;
      gap: 1.5rem;
      transform: translateX(-100%);
      transition: transform 0.55s var(--ease-luxury);
    }

    .mobile-drawer.is-open {
      transform: translateX(0);
    }

    .mobile-drawer-close {
      position: absolute;
      top: 1.6rem;
      right: 1.6rem;
      background: none;
      border: none;
      color: var(--bg-bone);
      font-size: 0.75rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      cursor: pointer;
    }

    .mobile-drawer-link {
      background: none;
      border: none;
      color: var(--bg-bone);
      text-align: left;
      font-family: var(--font-serif);
      font-size: 2.4rem;
      font-weight: 300;
      cursor: pointer;
    }

    /* ==================== PAGE VIEWS ==================== */
    .page-view {
      display: none;
      animation: pageFade 0.6s var(--ease-luxury) both;
    }

    .page-view.is-active {
      display: block;
    }

    @keyframes pageFade {
      from { opacity: 0; transform: translateY(10px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .container {
      max-width: 1440px;
      margin: 0 auto;
      padding: 0 clamp(1.25rem, 4vw, 3.5rem);
    }

    .section-pad {
      padding: clamp(4.5rem, 8vw, 7.5rem) 0;
    }

    .eyebrow {
      font-size: 0.7rem;
      letter-spacing: 0.28em;
      text-transform: uppercase;
      color: var(--gold-asante);
      font-weight: 600;
      margin-bottom: 0.9rem;
      display: block;
    }

    .heading-xl {
      font-family: var(--font-serif);
      font-weight: 300;
      font-size: clamp(2.4rem, 5vw, 4.4rem);
      line-height: 1.06;
      letter-spacing: -0.01em;
    }

    .heading-lg {
      font-family: var(--font-serif);
      font-weight: 300;
      font-size: clamp(1.9rem, 3.6vw, 3.1rem);
      line-height: 1.12;
    }

    .heading-md {
      font-family: var(--font-serif);
      font-weight: 400;
      font-size: clamp(1.35rem, 2.2vw, 1.85rem);
      line-height: 1.2;
    }

    /* ==================== BUTTONS ==================== */
    .btn-primary {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.6rem;
      background: var(--ink-obsidian);
      color: var(--bg-bone);
      border: 1px solid var(--ink-obsidian);
      padding: 0.95rem 2.2rem;
      font-size: 0.72rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      cursor: pointer;
      transition: background 0.35s ease, color 0.35s ease, transform 0.35s var(--ease-luxury);
    }

    .btn-primary:hover {
      background: var(--gold-asante);
      border-color: var(--gold-asante);
      color: #FFFFFF;
      transform: translateY(-1px);
    }

    .btn-outline {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.6rem;
      background: transparent;
      color: inherit;
      border: 1px solid currentColor;
      padding: 0.95rem 2.2rem;
      font-size: 0.72rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.35s var(--ease-luxury);
    }

    .btn-outline:hover {
      background: var(--ink-obsidian);
      border-color: var(--ink-obsidian);
      color: var(--bg-bone);
    }

    /* ==================== HOME: VIDEO-FIRST EXPERIENCE ==================== */
    .hero-video-section {
      position: relative;
      height: 100svh;
      min-height: 620px;
      background: #141210;
      color: #F8F6F2;
      overflow: hidden;
      display: flex;
      align-items: flex-end;
    }

    .hero-video-el {
      position: absolute;
      inset: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
      filter: contrast(1.04) brightness(0.76);
      transform: scale(1.02);
    }

    .hero-scrim {
      position: absolute;
      inset: 0;
      background: linear-gradient(
        to top,
        rgba(12, 11, 10, 0.84) 0%,
        rgba(12, 11, 10, 0.28) 45%,
        rgba(12, 11, 10, 0.42) 100%
      );
      pointer-events: none;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      width: 100%;
      padding-bottom: clamp(3rem, 7vh, 5.5rem);
    }

    .hero-flex {
      display: flex;
      flex-wrap: wrap;
      align-items: flex-end;
      justify-content: space-between;
      gap: 2rem;
    }

    .hero-copy {
      max-width: 680px;
    }

    .hero-copy p {
      margin-top: 1.1rem;
      color: rgba(248, 246, 242, 0.82);
      font-weight: 300;
      max-width: 480px;
      font-size: 0.98rem;
    }

    .hero-ctas {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      margin-top: 2rem;
    }

    .btn-hero-light {
      background: #F8F6F2;
      color: #121110;
      border: 1px solid #F8F6F2;
      padding: 0.95rem 2.2rem;
      font-size: 0.72rem;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.35s var(--ease-luxury);
    }

    .btn-hero-light:hover {
      background: var(--gold-asante);
      border-color: var(--gold-asante);
      color: #FFFFFF;
    }

    .video-control-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: rgba(18, 17, 16, 0.55);
      backdrop-filter: blur(10px);
      border: 1px solid rgba(248, 246, 242, 0.28);
      color: #F8F6F2;
      padding: 0.65rem 1.15rem;
      border-radius: 999px;
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      cursor: pointer;
      transition: border-color 0.3s ease;
    }

    .video-control-pill:hover {
      border-color: var(--gold-asante);
    }

    .live-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: var(--gold-asante);
      animation: pulseDot 2s infinite;
    }

    @keyframes pulseDot {
      0%, 100% { opacity: 1; transform: scale(1); }
      50% { opacity: 0.4; transform: scale(0.75); }
    }

    /* Editorial Video Triptych on Home */
    .section-head-row {
      display: flex;
      flex-wrap: wrap;
      align-items: flex-end;
      justify-content: space-between;
      gap: 1.5rem;
      margin-bottom: 3rem;
      border-bottom: 1px solid var(--border-hairline);
      padding-bottom: 1.6rem;
    }

    .video-triptych {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 1.75rem;
    }

    .video-card {
      position: relative;
      cursor: pointer;
      group: true;
    }

    .video-frame {
      position: relative;
      aspect-ratio: 3 / 4;
      overflow: hidden;
      background: #1C1A18;
    }

    .video-frame video {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.9s var(--ease-luxury), filter 0.6s ease;
    }

    .video-card:hover .video-frame video {
      transform: scale(1.04);
    }

    .video-badge {
      position: absolute;
      top: 1rem;
      left: 1rem;
      background: rgba(18, 17, 16, 0.62);
      backdrop-filter: blur(8px);
      color: #F8F6F2;
      font-size: 0.62rem;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      padding: 0.35rem 0.75rem;
    }

    .video-card-meta {
      display: flex;
      align-items: baseline;
      justify-content: space-between;
      padding-top: 1rem;
    }

    .video-card-title {
      font-family: var(--font-serif);
      font-size: 1.45rem;
      font-weight: 400;
    }

    .video-card-link {
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--ink-muted);
      transition: color 0.3s ease;
    }

    .video-card:hover .video-card-link {
      color: var(--gold-asante);
    }

    /* Split Film Manifesto Section on Home */
    .split-atelier {
      display: grid;
      grid-template-columns: 1.05fr 0.95fr;
      gap: clamp(2rem, 5vw, 5.5rem);
      align-items: center;
    }

    .split-video-box {
      position: relative;
      aspect-ratio: 4 / 5;
      overflow: hidden;
      background: #181614;
    }

    .split-video-box video {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .split-text p {
      color: var(--ink-charcoal);
      font-weight: 300;
      margin: 1.5rem 0 2.2rem;
      font-size: 1.02rem;
      max-width: 500px;
    }

    /* Delivery & Payment Assurance Ribbon */
    .assurance-strip {
      background: var(--ink-obsidian);
      color: var(--bg-bone);
      padding: 2.6rem 0;
    }

    .assurance-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 2rem;
    }

    .assurance-item h4 {
      font-family: var(--font-serif);
      font-size: 1.25rem;
      font-weight: 400;
      color: #E7D8BE;
      margin-bottom: 0.35rem;
    }

    .assurance-item p {
      font-size: 0.8rem;
      color: rgba(248, 246, 242, 0.7);
      font-weight: 300;
    }

    /* ==================== PRODUCT GRID (HOME PREVIEW & SHOP) ==================== */
    .product-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 2rem 1.5rem;
    }

    .product-card {
      display: flex;
      flex-direction: column;
    }

    .product-media {
      position: relative;
      aspect-ratio: 3 / 4;
      overflow: hidden;
      background: var(--bg-sand);
      cursor: pointer;
    }

    .product-media img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.85s var(--ease-luxury);
    }

    .product-card:hover .product-media img {
      transform: scale(1.05);
    }

    .product-quick-bar {
      position: absolute;
      left: 0.75rem;
      right: 0.75rem;
      bottom: 0.75rem;
      background: rgba(255, 255, 255, 0.94);
      backdrop-filter: blur(8px);
      padding: 0.65rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      opacity: 0;
      transform: translateY(10px);
      transition: all 0.35s var(--ease-luxury);
    }

    .product-card:hover .product-quick-bar {
      opacity: 1;
      transform: translateY(0);
    }

    .quick-size-btn {
      background: none;
      border: 1px solid transparent;
      font-size: 0.68rem;
      letter-spacing: 0.08em;
      padding: 0.28rem 0.45rem;
      cursor: pointer;
      transition: border-color 0.25s ease, background 0.25s ease;
    }

    .quick-size-btn:hover {
      border-color: var(--ink-obsidian);
      background: var(--ink-obsidian);
      color: #FFFFFF;
    }

    .product-info {
      padding-top: 0.95rem;
      display: flex;
      justify-content: space-between;
      align-items: flex-start;
      gap: 0.75rem;
    }

    .product-title {
      font-family: var(--font-serif);
      font-size: 1.2rem;
      font-weight: 400;
      cursor: pointer;
    }

    .product-material {
      font-size: 0.74rem;
      color: var(--ink-muted);
      margin-top: 0.15rem;
    }

    .product-price {
      font-size: 0.84rem;
      font-weight: 500;
      white-space: nowrap;
      letter-spacing: 0.04em;
    }

    /* ==================== SHOP PAGE CONTROLS ==================== */
    .page-banner {
      padding-top: calc(var(--nav-height) + clamp(3.5rem, 7vw, 5.5rem));
      padding-bottom: 2.8rem;
      border-bottom: 1px solid var(--border-hairline);
    }

    .shop-toolbar {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      gap: 1.25rem;
      padding: 1.8rem 0 2.5rem;
    }

    .filter-pills {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .filter-pill {
      background: transparent;
      border: 1px solid var(--border-hairline);
      padding: 0.55rem 1.2rem;
      font-size: 0.7rem;
      letter-spacing: 0.16em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.25s ease;
    }

    .filter-pill.is-active,
    .filter-pill:hover {
      background: var(--ink-obsidian);
      border-color: var(--ink-obsidian);
      color: var(--bg-bone);
    }

    .sort-select {
      background: transparent;
      border: 1px solid var(--border-hairline);
      padding: 0.55rem 1rem;
      font-size: 0.72rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: pointer;
    }

    /* ==================== LOOKBOOK PAGE ==================== */
    .lookbook-grid {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      gap: 2.5rem 1.75rem;
      padding: 3.5rem 0 6rem;
    }

    .look-item {
      position: relative;
    }

    .look-item--wide {
      grid-column: span 8;
    }

    .look-item--tall {
      grid-column: span 4;
    }

    .look-item--half {
      grid-column: span 6;
    }

    .look-img-wrap {
      position: relative;
      overflow: hidden;
      background: var(--bg-sand);
      aspect-ratio: 4 / 5;
    }

    .look-item--wide .look-img-wrap {
      aspect-ratio: 16 / 10;
    }

    .look-img-wrap img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 1s var(--ease-luxury);
    }

    .look-item:hover .look-img-wrap img {
      transform: scale(1.03);
    }

    .look-caption {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 1rem;
      gap: 1rem;
    }

    .look-caption h3 {
      font-family: var(--font-serif);
      font-size: 1.4rem;
      font-weight: 400;
    }

    .look-caption span {
      font-size: 0.72rem;
      color: var(--ink-muted);
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .shop-look-btn {
      background: none;
      border: none;
      border-bottom: 1px solid var(--ink-obsidian);
      padding-bottom: 2px;
      font-size: 0.7rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      cursor: pointer;
      white-space: nowrap;
    }

    .shop-look-btn:hover {
      color: var(--gold-asante);
      border-color: var(--gold-asante);
    }

    /* ==================== ABOUT US PAGE ==================== */
    .about-hero {
      padding-top: calc(var(--nav-height) + clamp(4rem, 8vw, 6.5rem));
      padding-bottom: clamp(3rem, 6vw, 5rem);
    }

    .about-lead {
      font-family: var(--font-serif);
      font-size: clamp(1.5rem, 2.8vw, 2.35rem);
      font-weight: 300;
      line-height: 1.38;
      max-width: 960px;
      margin-top: 1.5rem;
      color: var(--ink-charcoal);
    }

    .about-banner-img {
      margin-top: 3rem;
      aspect-ratio: 21 / 9;
      overflow: hidden;
      background: var(--bg-sand);
    }

    .about-banner-img img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .about-pillars {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2.5rem;
      border-top: 1px solid var(--border-hairline);
      border-bottom: 1px solid var(--border-hairline);
      padding: 4rem 0;
    }

    .pillar-num {
      font-family: var(--font-serif);
      font-size: 1.1rem;
      color: var(--gold-asante);
      margin-bottom: 1rem;
      display: block;
    }

    .pillar-card h3 {
      font-family: var(--font-serif);
      font-size: 1.8rem;
      font-weight: 400;
      margin-bottom: 0.85rem;
    }

    .pillar-card p {
      font-size: 0.92rem;
      color: var(--ink-charcoal);
      font-weight: 300;
      line-height: 1.75;
    }

    .about-story-block {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: clamp(2rem, 5vw, 5rem);
      align-items: center;
      padding: 5rem 0;
    }

    .about-story-block.is-reversed .about-story-media {
      order: 2;
    }

    .about-story-media {
      aspect-ratio: 4 / 5;
      overflow: hidden;
      background: var(--bg-sand);
    }

    .about-story-media img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .about-story-copy p {
      color: var(--ink-charcoal);
      font-weight: 300;
      line-height: 1.85;
      margin-top: 1.25rem;
      font-size: 0.98rem;
    }

    .ethics-stats {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 2rem;
      background: var(--bg-sand);
      padding: clamp(2.5rem, 5vw, 4.5rem);
      margin-bottom: 5rem;
    }

    .stat-item strong {
      display: block;
      font-family: var(--font-serif);
      font-size: clamp(2.2rem, 4vw, 3.2rem);
      font-weight: 300;
      color: var(--ink-obsidian);
      line-height: 1.1;
    }

    .stat-item span {
      display: block;
      font-size: 0.76rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--ink-muted);
      margin-top: 0.5rem;
    }

    /* ==================== MODALS & CART/CHECKOUT DRAWER ==================== */
    .drawer-backdrop {
      position: fixed;
      inset: 0;
      background: rgba(12, 11, 10, 0.55);
      backdrop-filter: blur(4px);
      z-index: 1100;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.4s ease;
    }

    .drawer-backdrop.is-open {
      opacity: 1;
      pointer-events: auto;
    }

    .cart-drawer {
      position: fixed;
      top: 0;
      right: 0;
      bottom: 0;
      width: 100%;
      max-width: 490px;
      background: var(--bg-ivory);
      z-index: 1200;
      display: flex;
      flex-direction: column;
      transform: translateX(100%);
      transition: transform 0.5s var(--ease-luxury);
      box-shadow: -20px 0 60px rgba(0, 0, 0, 0.16);
    }

    .cart-drawer.is-open {
      transform: translateX(0);
    }

    .cart-header {
      padding: 1.4rem 1.8rem;
      border-bottom: 1px solid var(--border-hairline);
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .cart-header h3 {
      font-family: var(--font-serif);
      font-size: 1.55rem;
      font-weight: 400;
    }

    .close-icon-btn {
      background: none;
      border: none;
      font-size: 1.5rem;
      line-height: 1;
      cursor: pointer;
      padding: 0.25rem;
      color: var(--ink-obsidian);
    }

    .cart-body {
      flex: 1;
      overflow-y: auto;
      padding: 1.5rem 1.8rem;
    }

    .cart-empty {
      text-align: center;
      padding: 4rem 1rem;
      color: var(--ink-muted);
    }

    .cart-item {
      display: grid;
      grid-template-columns: 76px 1fr;
      gap: 1rem;
      padding-bottom: 1.25rem;
      margin-bottom: 1.25rem;
      border-bottom: 1px solid var(--border-hairline);
    }

    .cart-item img {
      width: 76px;
      height: 98px;
      object-fit: cover;
      background: var(--bg-sand);
    }

    .cart-item-top {
      display: flex;
      justify-content: space-between;
      gap: 0.5rem;
    }

    .cart-item-title {
      font-family: var(--font-serif);
      font-size: 1.12rem;
    }

    .cart-item-meta {
      font-size: 0.74rem;
      color: var(--ink-muted);
      margin-top: 0.2rem;
    }

    .cart-item-controls {
      display: flex;
      align-items: center;
      justify-content: space-between;
      margin-top: 0.85rem;
    }

    .qty-stepper {
      display: inline-flex;
      align-items: center;
      border: 1px solid var(--border-hairline);
    }

    .qty-stepper button {
      background: none;
      border: none;
      width: 28px;
      height: 28px;
      cursor: pointer;
      font-size: 0.9rem;
    }

    .qty-stepper span {
      min-width: 26px;
      text-align: center;
      font-size: 0.78rem;
    }

    .remove-item-btn {
      background: none;
      border: none;
      font-size: 0.7rem;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--ink-muted);
      cursor: pointer;
      text-decoration: underline;
    }

    /* Checkout Section inside Cart Drawer */
    .checkout-panel {
      margin-top: 1.2rem;
    }

    .checkout-label {
      display: block;
      font-size: 0.68rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--ink-muted);
      margin-bottom: 0.55rem;
      font-weight: 600;
    }

    .delivery-options {
      display: grid;
      gap: 0.6rem;
      margin-bottom: 1.35rem;
    }

    .delivery-option {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.85rem 1rem;
      border: 1px solid var(--border-hairline);
      cursor: pointer;
      transition: border-color 0.25s ease, background 0.25s ease;
    }

    .delivery-option.is-selected {
      border-color: var(--ink-obsidian);
      background: var(--bg-bone);
    }

    .delivery-option input {
      margin-right: 0.65rem;
      accent-color: var(--ink-obsidian);
    }

    .delivery-option-title {
      font-size: 0.82rem;
      font-weight: 500;
    }

    .delivery-option-sub {
      display: block;
      font-size: 0.7rem;
      color: var(--ink-muted);
    }

    .delivery-option-fee {
      font-size: 0.82rem;
      font-weight: 600;
      white-space: nowrap;
    }

    .form-grid {
      display: grid;
      gap: 0.75rem;
      margin-bottom: 1.25rem;
    }

    .form-input {
      width: 100%;
      padding: 0.78rem 0.9rem;
      border: 1px solid var(--border-hairline);
      background: var(--bg-ivory);
      font-size: 0.84rem;
      outline: none;
      transition: border-color 0.25s ease;
    }

    .form-input:focus {
      border-color: var(--ink-obsidian);
    }

    .payment-methods {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.6rem;
      margin-bottom: 1rem;
    }

    .pay-method-btn {
      padding: 0.75rem 0.6rem;
      border: 1px solid var(--border-hairline);
      background: var(--bg-ivory);
      font-size: 0.72rem;
      letter-spacing: 0.06em;
      text-align: center;
      cursor: pointer;
      transition: all 0.25s ease;
    }

    .pay-method-btn.is-selected {
      border-color: var(--ink-obsidian);
      background: var(--ink-obsidian);
      color: #FFFFFF;
    }

    .paystack-trust-note {
      font-size: 0.72rem;
      color: var(--ink-muted);
      background: var(--bg-bone);
      padding: 0.65rem 0.85rem;
      border-left: 2px solid var(--gold-asante);
      margin-bottom: 1rem;
    }

    .cart-footer {
      padding: 1.25rem 1.8rem 1.6rem;
      border-top: 1px solid var(--border-hairline);
      background: var(--bg-bone);
    }

    .summary-row {
      display: flex;
      justify-content: space-between;
      font-size: 0.84rem;
      margin-bottom: 0.45rem;
      color: var(--ink-charcoal);
    }

    .summary-row.is-total {
      font-size: 1.05rem;
      font-weight: 600;
      color: var(--ink-obsidian);
      padding-top: 0.6rem;
      margin-top: 0.4rem;
      border-top: 1px solid var(--border-hairline);
      margin-bottom: 1rem;
    }

    /* Quick View Modal */
    .modal-overlay {
      position: fixed;
      inset: 0;
      z-index: 1300;
      background: rgba(12, 11, 10, 0.65);
      backdrop-filter: blur(6px);
      display: none;
      align-items: center;
      justify-content: center;
      padding: 1.25rem;
    }

    .modal-overlay.is-open {
      display: flex;
    }

    .quickview-box {
      background: var(--bg-ivory);
      max-width: 880px;
      width: 100%;
      max-height: 90vh;
      overflow-y: auto;
      display: grid;
      grid-template-columns: 1fr 1fr;
      position: relative;
      animation: fadeRise 0.35s var(--ease-luxury) both;
    }

    .quickview-media {
      background: var(--bg-sand);
      aspect-ratio: 3 / 4;
    }

    .quickview-media img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }

    .quickview-details {
      padding: 2.5rem;
      display: flex;
      flex-direction: column;
      justify-content: center;
    }

    .size-selector {
      display: flex;
      flex-wrap: wrap;
      gap: 0.5rem;
      margin: 1.2rem 0 1.8rem;
    }

    .size-pill {
      min-width: 44px;
      height: 40px;
      border: 1px solid var(--border-hairline);
      background: transparent;
      font-size: 0.76rem;
      cursor: pointer;
      transition: all 0.25s ease;
    }

    .size-pill.is-selected {
      background: var(--ink-obsidian);
      border-color: var(--ink-obsidian);
      color: #FFFFFF;
    }

    /* Order Receipt Modal */
    .receipt-box {
      background: var(--bg-ivory);
      max-width: 520px;
      width: 100%;
      padding: 2.6rem;
      text-align: center;
      position: relative;
    }

    .receipt-badge {
      width: 56px;
      height: 56px;
      border-radius: 50%;
      background: var(--gold-soft);
      color: var(--gold-asante);
      display: grid;
      place-items: center;
      margin: 0 auto 1.25rem;
      font-size: 1.4rem;
    }

    /* Toast Notification */
    .toast {
      position: fixed;
      bottom: 1.75rem;
      left: 50%;
      transform: translateX(-50%) translateY(20px);
      background: var(--ink-obsidian);
      color: var(--bg-bone);
      padding: 0.85rem 1.5rem;
      font-size: 0.76rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      z-index: 1500;
      opacity: 0;
      pointer-events: none;
      transition: all 0.35s var(--ease-luxury);
    }

    .toast.is-visible {
      opacity: 1;
      transform: translateX(-50%) translateY(0);
    }

    /* ==================== FOOTER ==================== */
    .site-footer {
      background: #121110;
      color: #F8F6F2;
      padding: 4.5rem 0 2.5rem;
      border-top: 1px solid rgba(255, 255, 255, 0.08);
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1.5fr 1fr 1fr 1.2fr;
      gap: 3rem;
      padding-bottom: 3.5rem;
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    }

    .footer-col h5 {
      font-size: 0.68rem;
      letter-spacing: 0.24em;
      text-transform: uppercase;
      color: var(--gold-asante);
      margin-bottom: 1.2rem;
    }

    .footer-col ul {
      list-style: none;
      display: grid;
      gap: 0.65rem;
    }

    .footer-col button,
    .footer-col a {
      background: none;
      border: none;
      color: rgba(248, 246, 242, 0.72);
      font-size: 0.85rem;
      cursor: pointer;
      text-align: left;
      transition: color 0.25s ease;
    }

    .footer-col button:hover,
    .footer-col a:hover {
      color: #FFFFFF;
    }

    .footer-bottom {
      padding-top: 1.8rem;
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 1rem;
      font-size: 0.74rem;
      color: rgba(248, 246, 242, 0.5);
    }

    /* ==================== RESPONSIVE ==================== */
    @media (max-width: 1080px) {
      .product-grid {
        grid-template-columns: repeat(2, 1fr);
      }
      .assurance-grid {
        grid-template-columns: repeat(2, 1fr);
      }
      .footer-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 860px) {
      .nav-links {
        display: none;
      }
      .mobile-menu-btn {
        display: inline-block;
      }
      .currency-pill {
        display: none;
      }
      .video-triptych,
      .split-atelier,
      .about-pillars,
      .about-story-block,
      .ethics-stats,
      .quickview-box {
        grid-template-columns: 1fr;
      }
      .about-story-block.is-reversed .about-story-media {
        order: 0;
      }
      .look-item--wide,
      .look-item--tall,
      .look-item--half {
        grid-column: span 12;
      }
      .footer-grid {
        grid-template-columns: 1fr;
      }
    }
  </style>
</head>
<body>

  <!-- ==================== STYLISH FLOATING WELCOME FEATURE ==================== -->
  <div id="welcomeOverlay" class="welcome-overlay" role="dialog" aria-label="Welcome to The Young Prodigies">
    <div class="welcome-orb welcome-orb--1"></div>
    <div class="welcome-orb welcome-orb--2"></div>
    <div class="welcome-grid-lines"></div>

    <div class="welcome-content">
      <div class="welcome-monogram">TYP</div>
      <p class="welcome-kicker">Kumasi &bull; Accra &bull; Global</p>
      <h1 class="welcome-title">The Young <em>Prodigies</em></h1>
      <p class="welcome-sub">
        Architectural silhouettes cut in quiet homage to Ghanaian heritage. Crafted in small batches for the next vanguard.
      </p>
      <div class="welcome-actions">
        <button id="enterAtelierBtn" class="btn-enter" type="button">Enter The Atelier</button>
        <span class="welcome-meta">Collection 04 &bull; Ashanti Monolith &bull; Priced in GH&#8373;</span>
      </div>
    </div>
  </div>

  <!-- ==================== HEADER NAVIGATION ==================== -->
  <header id="siteHeader" class="site-header is-hero-overlay">
    <div class="nav-inner">
      <div>
        <button id="mobileMenuBtn" class="mobile-menu-btn" type="button">Menu</button>
        <nav class="nav-links" aria-label="Primary Navigation">
          <button class="nav-link is-active" data-route="home" type="button">Home</button>
          <button class="nav-link" data-route="lookbook" type="button">Lookbook</button>
          <button class="nav-link" data-route="shop" type="button">Shop</button>
          <button class="nav-link" data-route="about" type="button">About Us</button>
        </nav>
      </div>

      <button class="brand-mark" data-route="home" type="button">
        The Young Prodigies
        <span>Kumasi Atelier</span>
      </button>

      <div class="nav-utilities">
        <span class="currency-pill">GH&#8373; GHS</span>
        <button id="openBagBtn" class="bag-trigger" type="button">
          Bag <span id="navBagCount" class="bag-count">0</span>
        </button>
      </div>
    </div>
  </header>

  <!-- Mobile Navigation Drawer -->
  <div id="mobileDrawer" class="mobile-drawer" aria-hidden="true">
    <button id="closeMobileDrawer" class="mobile-drawer-close" type="button">Close &times;</button>
    <button class="mobile-drawer-link" data-route="home" type="button">Home</button>
    <button class="mobile-drawer-link" data-route="lookbook" type="button">Lookbook</button>
    <button class="mobile-drawer-link" data-route="shop" type="button">Shop</button>
    <button class="mobile-drawer-link" data-route="about" type="button">About Us</button>
  </div>

  <main>
    <!-- ==================== PAGE 1: HOME (VIDEO-FIRST) ==================== -->
    <section id="view-home" class="page-view is-active">
      <!-- Hero Full-Bleed Fashion Film -->
      <div class="hero-video-section">
        <video
          id="heroVideo"
          class="hero-video-el"
          autoplay
          muted
          loop
          playsinline
          poster="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=1600&q=80"
        >
          <source src="https://assets.mixkit.co/videos/preview/mixkit-taking-photos-from-different-angles-of-a-model-34421-large.mp4" type="video/mp4" />
        </video>
        <div class="hero-scrim"></div>

        <div class="hero-content">
          <div class="container hero-flex">
            <div class="hero-copy">
              <span class="eyebrow">Collection 04 &bull; Autumn / Winter Film</span>
              <h2 class="heading-xl">Ashanti Monolith</h2>
              <p>
                Fluid tailoring, heavyweight organic cottons, and understated regal proportions. Designed in Kumasi for global presence.
              </p>
              <div class="hero-ctas">
                <button class="btn-hero-light" data-route="shop" type="button">Shop Collection</button>
                <button class="btn-outline" data-route="lookbook" type="button" style="color:#F8F6F2;border-color:rgba(248,246,242,0.5);">
                  View Lookbook
                </button>
              </div>
            </div>

            <button id="toggleHeroVideoBtn" class="video-control-pill" type="button">
              <span class="live-dot"></span>
              <span id="heroVideoStateText">Film Playing &bull; Pause</span>
            </button>
          </div>
        </div>
      </div>

      <!-- Video Triptych: Motion Replacing Static Pictures -->
      <section class="section-pad">
        <div class="container">
          <div class="section-head-row">
            <div>
              <span class="eyebrow">Atelier In Motion</span>
              <h2 class="heading-lg">Three Studies in Silhouette</h2>
            </div>
            <button class="btn-outline" data-route="shop" type="button">Explore All Pieces</button>
          </div>

          <div class="video-triptych">
            <article class="video-card" data-shop-filter="Tailoring">
              <div class="video-frame">
                <span class="video-badge">Film 01 &bull; Tailoring</span>
                <video
                  autoplay
                  muted
                  loop
                  playsinline
                  poster="https://images.unsplash.com/photo-1594938298603-c8148c4dae35?auto=format&fit=crop&w=900&q=80"
                >
                  <source src="https://assets.mixkit.co/videos/preview/mixkit-fashion-cold-looking-woman-concept-video-39874-large.mp4" type="video/mp4" />
                </video>
              </div>
              <div class="video-card-meta">
                <h3 class="video-card-title">Structured Linen</h3>
                <span class="video-card-link">Shop Tailoring &rarr;</span>
              </div>
            </article>

            <article class="video-card" data-shop-filter="Dresses & Sets">
              <div class="video-frame">
                <span class="video-badge">Film 02 &bull; Evening</span>
                <video
                  autoplay
                  muted
                  loop
                  playsinline
                  poster="https://images.unsplash.com/photo-1549439602-43ebca2327af?auto=format&fit=crop&w=900&q=80"
                >
                  <source src="https://assets.mixkit.co/videos/preview/mixkit-woman-modeling-a-short-black-dress-805-large.mp4" type="video/mp4" />
                </video>
              </div>
              <div class="video-card-meta">
                <h3 class="video-card-title">Obsidian Drape</h3>
                <span class="video-card-link">Shop Sets &rarr;</span>
              </div>
            </article>

            <article class="video-card" data-shop-filter="Outerwear">
              <div class="video-frame">
                <span class="video-badge">Film 03 &bull; Movement</span>
                <video
                  autoplay
                  muted
                  loop
                  playsinline
                  poster="https://images.unsplash.com/photo-1561365452-adb940139ffa?auto=format&fit=crop&w=900&q=80"
                >
                  <source src="https://assets.mixkit.co/videos/preview/mixkit-man-dancing-under-changing-lights-1240-large.mp4" type="video/mp4" />
                </video>
              </div>
              <div class="video-card-meta">
                <h3 class="video-card-title">Nocturne Layering</h3>
                <span class="video-card-link">Shop Outerwear &rarr;</span>
              </div>
            </article>
          </div>
        </div>
      </section>

      <!-- Curated Pieces Preview -->
      <section class="section-pad" style="background: var(--bg-ivory); border-top: 1px solid var(--border-hairline); border-bottom: 1px solid var(--border-hairline);">
        <div class="container">
          <div class="section-head-row">
            <div>
              <span class="eyebrow">Capsule Release</span>
              <h2 class="heading-lg">Signature Editions</h2>
            </div>
            <button class="btn-outline" data-route="shop" type="button">View Full Catalog</button>
          </div>
          <div id="homeFeaturedGrid" class="product-grid"></div>
        </div>
      </section>

      <!-- Split Film Manifesto -->
      <section class="section-pad">
        <div class="container">
          <div class="split-atelier">
            <div class="split-video-box">
              <video
                autoplay
                muted
                loop
                playsinline
                poster="https://images.unsplash.com/photo-1524504259109-ddd837233694?auto=format&fit=crop&w=900&q=80"
              >
                <source src="https://assets.mixkit.co/videos/preview/mixkit-portrait-of-a-fashion-woman-with-silver-makeup-39875-large.mp4" type="video/mp4" />
              </video>
            </div>
            <div class="split-text">
              <span class="eyebrow">The House Manifesto</span>
              <h2 class="heading-lg">Discipline Over Noise. Heritage Without Literalism.</h2>
              <p>
                Born in Kumasi, The Young Prodigies translates centuries of Asante craftsmanship and regal poise into razor-clean modern garments. Every seam is deliberate; every fabric is selected for breathability, weight, and permanence.
              </p>
              <button class="btn-primary" data-route="about" type="button">Read Our Story</button>
            </div>
          </div>
        </div>
      </section>

      <!-- Delivery & Paystack Assurance Ribbon -->
      <div class="assurance-strip">
        <div class="container assurance-grid">
          <div class="assurance-item">
            <h4>Kumasi Express — GH&#8373; 20</h4>
            <p>Dedicated doorstep dispatch across Kumasi &amp; Ashanti Region within 24–48 hours.</p>
          </div>
          <div class="assurance-item">
            <h4>Nationwide — GH&#8373; 40</h4>
            <p>Insured courier delivery to Accra, Takoradi, Tamale, Cape Coast &amp; beyond.</p>
          </div>
          <div class="assurance-item">
            <h4>Mobile Money &amp; Cards</h4>
            <p>Pay securely in GH&#8373; via MTN MoMo, Telecel Cash, AT Money &amp; Debit Cards on Paystack.</p>
          </div>
          <div class="assurance-item">
            <h4>Ethical Small-Batch</h4>
            <p>Cut and finished by fairly compensated master tailors in our Kumasi studio.</p>
          </div>
        </div>
      </div>
    </section>

    <!-- ==================== PAGE 2: LOOKBOOK ==================== -->
    <section id="view-lookbook" class="page-view">
      <div class="page-banner">
        <div class="container">
          <span class="eyebrow">Editorial Archive &bull; Collection 04</span>
          <h1 class="heading-xl">The Ashanti Monolith Lookbook</h1>
          <p style="max-width: 580px; margin-top: 1rem; color: var(--ink-charcoal); font-weight: 300;">
            Photographed between brutalist concrete studies and warm red-earth light. Select any frame to inspect and shop the featured garments directly.
          </p>
        </div>
      </div>

      <div class="container">
        <div id="lookbookGrid" class="lookbook-grid"></div>
      </div>
    </section>

    <!-- ==================== PAGE 3: SHOP ==================== -->
    <section id="view-shop" class="page-view">
      <div class="page-banner">
        <div class="container">
          <span class="eyebrow">Atelier Storefront &bull; Priced in Ghana Cedis (GH&#8373;)</span>
          <h1 class="heading-xl">Ready-To-Wear &amp; Objects</h1>
        </div>
      </div>

      <div class="container">
        <div class="shop-toolbar">
          <div id="shopFilterPills" class="filter-pills">
            <button class="filter-pill is-active" data-cat="All" type="button">All</button>
            <button class="filter-pill" data-cat="Tailoring" type="button">Tailoring</button>
            <button class="filter-pill" data-cat="Outerwear" type="button">Outerwear</button>
            <button class="filter-pill" data-cat="Shirting & Knitwear" type="button">Shirting &amp; Knitwear</button>
            <button class="filter-pill" data-cat="Dresses & Sets" type="button">Dresses &amp; Sets</button>
            <button class="filter-pill" data-cat="Accessories" type="button">Accessories</button>
          </div>

          <select id="shopSortSelect" class="sort-select" aria-label="Sort products">
            <option value="featured">Sort: Featured</option>
            <option value="price-asc">Price: Low to High</option>
            <option value="price-desc">Price: High to Low</option>
          </select>
        </div>

        <div id="shopProductGrid" class="product-grid" style="padding-bottom: 6rem;"></div>
      </div>
    </section>

    <!-- ==================== PAGE 4: ABOUT US ==================== -->
    <section id="view-about" class="page-view">
      <div class="about-hero">
        <div class="container">
          <span class="eyebrow">Our House &bull; Founded in Kumasi</span>
          <h1 class="heading-xl">The Young Prodigies</h1>
          <p class="about-lead">
            We exist at the intersection of West African cultural sovereignity and quiet modernist architecture—creating heirloom garments for minds that refuse to shout to be heard.
          </p>

          <div class="about-banner-img">
            <img src="https://images.unsplash.com/photo-1550928431-ee0ec6db30d3?auto=format&fit=crop&w=1600&q=85" alt="The Young Prodigies Atelier Craftsmanship" />
          </div>
        </div>
      </div>

      <!-- Core Philosophy Pillars -->
      <div class="container">
        <div class="about-pillars">
          <div class="pillar-card">
            <span class="pillar-num">01 &bull; Core Philosophy</span>
            <h3>Architectural Restraint</h3>
            <p>
              True luxury needs no excess. We strip away ornamental clutter so proportion, lapel balance, shoulder structure, and the natural fall of cloth speak with quiet authority.
            </p>
          </div>
          <div class="pillar-card">
            <span class="pillar-num">02 &bull; Heritage Code</span>
            <h3>Ancestral Poise, Modern Cut</h3>
            <p>
              Rather than reproducing traditional motifs literally, we encode Kumasi's royal textile discipline into subtle interior bindings, hand-loomed trims, and burnished brass closures.
            </p>
          </div>
          <div class="pillar-card">
            <span class="pillar-num">03 &bull; Permanence</span>
            <h3>Seasonless Longevity</h3>
            <p>
              Every garment is engineered to age gracefully across decades, not weeks. We release deliberate, numbered capsules rather than chasing disposable fashion calendars.
            </p>
          </div>
        </div>

        <!-- Inspiration Story -->
        <div class="about-story-block">
          <div class="about-story-media">
            <img src="https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=1000&q=85" alt="Inspiration behind The Young Prodigies collections" />
          </div>
          <div class="about-story-copy">
            <span class="eyebrow">Inspiration Behind The Collections</span>
            <h2 class="heading-lg">Red Earth, Brutalist Light &amp; Royal Geometry</h2>
            <p>
              Every collection begins in Kumasi—watching early morning mist lift over warm terracotta streets, studying the deliberate symmetry of carved Asante stools, and observing how contemporary African youth carry themselves across Accra, London, and New York.
            </p>
            <p>
              Our silhouettes balance tropical breathability with sculptural weight. Loose, air-catching trousers meet sharply tailored cropped jackets; raw bone linens are juxtaposed against deep obsidian twill, echoing the contrast between sunlit stone and quiet shadow.
            </p>
          </div>
        </div>

        <!-- Materials & Ethical Production -->
        <div class="about-story-block is-reversed">
          <div class="about-story-media">
            <img src="https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=1000&q=85" alt="High quality organic fabrics and ethical tailoring" />
          </div>
          <div class="about-story-copy">
            <span class="eyebrow">Materials &amp; Ethical Practices</span>
            <h2 class="heading-lg">Honest Cloth. Dignified Hands.</h2>
            <p>
              Quality starts long before the first scissor cut. We partner with certified mills and regional weavers for long-staple organic cottons, breathable flax linens, deadstock suiting wools, and vegetable-tanned leathers finished without harsh toxic dyes.
            </p>
            <p>
              Inside our Kumasi workshop, every tailor is a named artisan—not an anonymous line worker. We pay above-living studio wages, maintain humane daylight studio hours, and mentor young Ghanaian patternmakers ("The Prodigies") in bespoke construction and zero-waste cutting.
            </p>
          </div>
        </div>

        <!-- Atelier Numbers -->
        <div class="ethics-stats">
          <div class="stat-item">
            <strong>100%</strong>
            <span>Natural &amp; Deadstock Luxury Fibers</span>
          </div>
          <div class="stat-item">
            <strong>50 Pieces</strong>
            <span>Maximum Run Per Numbered Edition</span>
          </div>
          <div class="stat-item">
            <strong>Kumasi</strong>
            <span>Designed, Patterned &amp; Finished Locally</span>
          </div>
        </div>
      </div>
    </section>
  </main>

  <!-- ==================== FOOTER ==================== -->
  <footer class="site-footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-col">
          <h4 style="font-family: var(--font-serif); font-size: 1.55rem; font-weight: 400; letter-spacing: 0.14em; text-transform: uppercase;">
            The Young Prodigies
          </h4>
          <p style="font-size: 0.85rem; color: rgba(248,246,242,0.68); margin-top: 0.9rem; max-width: 310px; font-weight: 300;">
            Minimalist luxury fashion house rooted in Kumasi, Ghana. Crafted for modern permanence.
          </p>
          <button id="replayWelcomeBtn" class="btn-outline" type="button" style="margin-top: 1.4rem; padding: 0.6rem 1.2rem; font-size: 0.65rem; border-color: rgba(248,246,242,0.3); color: #F8F6F2;">
            Replay Welcome Experience
          </button>
        </div>

        <div class="footer-col">
          <h5>Navigation</h5>
          <ul>
            <li><button data-route="home" type="button">Home</button></li>
            <li><button data-route="lookbook" type="button">Lookbook</button></li>
            <li><button data-route="shop" type="button">Shop Collection</button></li>
            <li><button data-route="about" type="button">About Us</button></li>
          </ul>
        </div>

        <div class="footer-col">
          <h5>Delivery &amp; Payments</h5>
          <ul>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">Kumasi Delivery: GH&#8373; 20</span></li>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">Outside Kumasi: GH&#8373; 40</span></li>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">MTN MoMo &bull; Telecel &bull; AT Money</span></li>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">Visa &amp; Mastercard via Paystack</span></li>
          </ul>
        </div>

        <div class="footer-col">
          <h5>Atelier Contact</h5>
          <ul>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">Ahodwo, Kumasi, Ashanti Region</span></li>
            <li><a href="mailto:concierge@theyoungprodigies.com">concierge@theyoungprodigies.com</a></li>
            <li><span style="font-size:0.84rem;color:rgba(248,246,242,0.72);">Private Appointments Available</span></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <span>&copy; 2026 The Young Prodigies. All Rights Reserved.</span>
        <span>All Prices in Ghana Cedis (GH&#8373;) &bull; Powered by Paystack Ghana</span>
      </div>
    </div>
  </footer>

  <!-- ==================== SHOPPING BAG & PAYSTACK CHECKOUT DRAWER ==================== -->
  <div id="drawerBackdrop" class="drawer-backdrop"></div>
  <aside id="cartDrawer" class="cart-drawer" aria-label="Shopping Bag and Checkout">
    <div class="cart-header">
      <h3>Your Atelier Bag</h3>
      <button id="closeBagBtn" class="close-icon-btn" type="button" aria-label="Close bag">&times;</button>
    </div>

    <div class="cart-body">
      <div id="cartItemsContainer"></div>

      <div id="checkoutPanel" class="checkout-panel" style="display: none;">
        <span class="checkout-label">1. Select Delivery Zone</span>
        <div class="delivery-options">
          <label class="delivery-option is-selected" data-zone="kumasi">
            <div>
              <input type="radio" name="deliveryZone" value="kumasi" checked />
              <span class="delivery-option-title">Within Kumasi (Ashanti Region)</span>
              <span class="delivery-option-sub">1–2 business days &bull; Dedicated rider</span>
            </div>
            <span class="delivery-option-fee">GH&#8373; 20.00</span>
          </label>

          <label class="delivery-option" data-zone="outside">
            <div>
              <input type="radio" name="deliveryZone" value="outside" />
              <span class="delivery-option-title">Outside Kumasi (Nationwide)</span>
              <span class="delivery-option-sub">Accra, Takoradi, Tamale &amp; all regions</span>
            </div>
            <span class="delivery-option-fee">GH&#8373; 40.00</span>
          </label>
        </div>

        <span class="checkout-label">2. Client &amp; Dispatch Details</span>
        <form id="checkoutForm" class="form-grid" onsubmit="return false;">
          <input id="custName" class="form-input" type="text" placeholder="Full Name *" required />
          <input id="custEmail" class="form-input" type="email" placeholder="Email Address (for Paystack receipt) *" required />
          <input id="custPhone" class="form-input" type="tel" placeholder="Phone / MoMo Number (e.g. 024 000 0000) *" required />
          <input id="custAddress" class="form-input" type="text" placeholder="Delivery Address &amp; City / Landmark *" required />
        </form>

        <span class="checkout-label">3. Preferred Paystack Channel</span>
        <div class="payment-methods">
          <button type="button" class="pay-method-btn is-selected" data-channel="mobile_money">
            Mobile Money<br /><small style="opacity:0.75;">MTN / Telecel / AT</small>
          </button>
          <button type="button" class="pay-method-btn" data-channel="card">
            Debit / Credit Card<br /><small style="opacity:0.75;">Visa &amp; Mastercard</small>
          </button>
        </div>

        <div class="paystack-trust-note">
          Encrypted checkout in <strong>Ghana Cedis (GH&#8373;)</strong> processed directly through your Paystack merchant account.
        </div>
      </div>
    </div>

    <div id="cartFooter" class="cart-footer" style="display: none;">
      <div class="summary-row">
        <span>Subtotal</span>
        <span id="summarySubtotal">GH&#8373; 0.00</span>
      </div>
      <div class="summary-row">
        <span id="summaryDeliveryLabel">Delivery (Kumasi)</span>
        <span id="summaryDelivery">GH&#8373; 20.00</span>
      </div>
      <div class="summary-row is-total">
        <span>Total Due</span>
        <span id="summaryTotal">GH&#8373; 0.00</span>
      </div>
      <button id="payWithPaystackBtn" class="btn-primary" type="button" style="width: 100%;">
        Pay Securely via Paystack
      </button>
    </div>
  </aside>

  <!-- ==================== PRODUCT QUICK VIEW MODAL ==================== -->
  <div id="quickViewModal" class="modal-overlay" role="dialog" aria-modal="true">
    <div class="quickview-box">
      <button id="closeQuickViewBtn" class="close-icon-btn" type="button" style="position:absolute;top:1rem;right:1.25rem;z-index:2;">&times;</button>
      <div class="quickview-media">
        <img id="qvImage" src="" alt="" />
      </div>
      <div class="quickview-details">
        <span id="qvCategory" class="eyebrow"></span>
        <h2 id="qvTitle" class="heading-lg" style="font-size:2.1rem;"></h2>
        <p id="qvPrice" style="font-size:1.1rem;font-weight:500;margin-top:0.4rem;"></p>
        <p id="qvDesc" style="font-size:0.88rem;color:var(--ink-charcoal);font-weight:300;margin-top:1rem;line-height:1.7;"></p>
        <p id="qvMaterial" style="font-size:0.74rem;color:var(--ink-muted);margin-top:0.8rem;letter-spacing:0.06em;text-transform:uppercase;"></p>

        <div style="margin-top:1.4rem;">
          <span class="checkout-label" style="margin-bottom:0.2rem;">Select Size</span>
          <div id="qvSizes" class="size-selector">
            <button type="button" class="size-pill" data-size="XS">XS</button>
            <button type="button" class="size-pill" data-size="S">S</button>
            <button type="button" class="size-pill is-selected" data-size="M">M</button>
            <button type="button" class="size-pill" data-size="L">L</button>
            <button type="button" class="size-pill" data-size="XL">XL</button>
          </div>
        </div>

        <button id="qvAddToBagBtn" class="btn-primary" type="button" style="width:100%;">Add To Bag</button>
      </div>
    </div>
  </div>

  <!-- ==================== ORDER CONFIRMATION RECEIPT MODAL ==================== -->
  <div id="receiptModal" class="modal-overlay" role="dialog" aria-modal="true">
    <div class="receipt-box">
      <div class="receipt-badge">&#10003;</div>
      <span class="eyebrow">Order Confirmed</span>
      <h2 class="heading-lg" style="font-size:2rem;">Thank You for Joining The Prodigies</h2>
      <p id="receiptMessage" style="font-size:0.9rem;color:var(--ink-charcoal);margin:1rem 0 1.5rem;font-weight:300;"></p>
      <div id="receiptDetails" style="background:var(--bg-bone);padding:1rem;text-align:left;font-size:0.8rem;margin-bottom:1.6rem;line-height:1.8;"></div>
      <button id="closeReceiptBtn" class="btn-primary" type="button" style="width:100%;">Continue Exploring</button>
    </div>
  </div>

  <!-- Toast Notification -->
  <div id="toast" class="toast"></div>

  <script>
    /* ============================================================================
       PAYSTACK CONFIGURATION
       ----------------------------------------------------------------------------
       Replace the placeholder key below with your LIVE or TEST Paystack Public Key
       from your Paystack Dashboard (Settings -> API Keys & Webhooks).
       Example: const PAYSTACK_PUBLIC_KEY = 'pk_live_xxxxxxxxxxxxxxxxxxxxxxxxxxxx';
       ============================================================================ */
    const PAYSTACK_PUBLIC_KEY = 'pk_test_YOUR_PAYSTACK_PUBLIC_KEY';

    const DELIVERY_FEES = {
      kumasi: 20,
      outside: 40
    };

    /* ==================== CATALOG DATA (PRICED IN GH₵) ==================== */
    const PRODUCTS = [
      {
        id: 'typ-01',
        title: 'Asante Structured Linen Blazer',
        category: 'Tailoring',
        price: 1450,
        material: '100% Organic Flax Linen • Horn Buttons',
        desc: 'Single-breasted architectural blazer with clean dropped shoulders, half-canvas chest construction, and discreet hand-loomed interior piping.',
        img: 'https://images.unsplash.com/photo-1594938298603-c8148c4dae35?auto=format&fit=crop&w=900&q=85',
        featured: true
      },
      {
        id: 'typ-02',
        title: 'Monolith Wide-Leg Trouser',
        category: 'Tailoring',
        price: 890,
        material: 'Heavyweight Cotton Twill • Kumasi Cut',
        desc: 'Double-pleated tailored trousers offering generous drape and effortless airflow in warm climates while holding a sharp vertical crease.',
        img: 'https://images.unsplash.com/photo-1541099649105-f69ad21f3246?auto=format&fit=crop&w=900&q=85',
        featured: true
      },
      {
        id: 'typ-03',
        title: 'Sovereign Ivory Silk Midi Dress',
        category: 'Dresses & Sets',
        price: 1620,
        material: '100% Mulberry Silk Crepe',
        desc: 'Bias-cut ivory silhouette designed to skim the form without restriction, finished with French seams and subtle back key-hole closure.',
        img: 'https://images.unsplash.com/photo-1617551307578-7f5160d6615e?auto=format&fit=crop&w=900&q=85',
        featured: true
      },
      {
        id: 'typ-04',
        title: 'Adinkra Minimalist Overcoat',
        category: 'Outerwear',
        price: 1980,
        material: 'Brushed Wool-Cotton Blend',
        desc: 'Longline minimalist coat featuring concealed placket buttons, deep welt pockets, and subtle embossed emblem lining.',
        img: 'https://images.unsplash.com/photo-1561365452-adb940139ffa?auto=format&fit=crop&w=900&q=85',
        featured: true
      },
      {
        id: 'typ-05',
        title: 'Atelier Crisp Poplin Shirt',
        category: 'Shirting & Knitwear',
        price: 680,
        material: 'Long-Staple Ghanaian Cotton',
        desc: 'Boxy studio shirting cut from crisp high-twist cotton poplin with elongated cuffs and mother-of-pearl hardware.',
        img: 'https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=900&q=85',
        featured: false
      },
      {
        id: 'typ-06',
        title: 'Obaatan Sculpted Two-Piece Set',
        category: 'Dresses & Sets',
        price: 1550,
        material: 'Textured Viscose-Linen Weave',
        desc: 'Coordinated sleeveless structured vest and fluid column skirt crafted for gallery openings and evening ceremonies.',
        img: 'https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=900&q=85',
        featured: false
      },
      {
        id: 'typ-07',
        title: 'Nocturne Evening Slip Gown',
        category: 'Dresses & Sets',
        price: 1790,
        material: 'Matte Cupro Silk',
        desc: 'Fluid obsidian evening gown with an architectural asymmetric neckline and whisper-soft movement.',
        img: 'https://images.unsplash.com/photo-1549439602-43ebca2327af?auto=format&fit=crop&w=900&q=85',
        featured: false
      },
      {
        id: 'typ-08',
        title: 'Prodigy Minimalist Leather Runners',
        category: 'Accessories',
        price: 1250,
        material: 'Vegetable-Tanned Calfskin',
        desc: 'Hand-lasted minimalist footwear stripped of loud branding, balanced on a tonal sculpted rubber sole.',
        img: 'https://images.unsplash.com/photo-1491553895911-0055eca6402d?auto=format&fit=crop&w=900&q=85',
        featured: false
      }
    ];

    const LOOKBOOK_FRAMES = [
      {
        layout: 'look-item--wide',
        title: 'Look 01 — The Monolith Blazer',
        subtitle: 'Collection 04 • Kumasi Concrete Study',
        img: 'https://images.unsplash.com/photo-1539109136881-3be0616acf4b?auto=format&fit=crop&w=1400&q=85',
        productId: 'typ-06'
      },
      {
        layout: 'look-item--tall',
        title: 'Look 02 — Bone Linen Tailoring',
        subtitle: 'Collection 04 • Light & Proportion',
        img: 'https://images.unsplash.com/photo-1594938298603-c8148c4dae35?auto=format&fit=crop&w=900&q=85',
        productId: 'typ-01'
      },
      {
        layout: 'look-item--half',
        title: 'Look 03 — Quiet Ivory Drape',
        subtitle: 'Collection 04 • Mulberry Silk Study',
        img: 'https://images.unsplash.com/photo-1617551307578-7f5160d6615e?auto=format&fit=crop&w=1000&q=85',
        productId: 'typ-03'
      },
      {
        layout: 'look-item--half',
        title: 'Look 04 — Studio Poplin Uniform',
        subtitle: 'Collection 04 • Ghanaian Cotton',
        img: 'https://images.unsplash.com/photo-1602810318383-e386cc2a3ccf?auto=format&fit=crop&w=1000&q=85',
        productId: 'typ-05'
      },
      {
        layout: 'look-item--tall',
        title: 'Look 05 — Nocturne Overcoat',
        subtitle: 'Collection 04 • Evening Form',
        img: 'https://images.unsplash.com/photo-1561365452-adb940139ffa?auto=format&fit=crop&w=900&q=85',
        productId: 'typ-04'
      },
      {
        layout: 'look-item--wide',
        title: 'Look 06 — Atelier Evening Silhouette',
        subtitle: 'Collection 04 • Cupro Silk',
        img: 'https://images.unsplash.com/photo-1549439602-43ebca2327af?auto=format&fit=crop&w=1400&q=85',
        productId: 'typ-07'
      }
    ];

    /* ==================== STATE ==================== */
    const state = {
      route: 'home',
      shopCategory: 'All',
      shopSort: 'featured',
      cart: JSON.parse(localStorage.getItem('typ_cart_v1') || '[]'),
      deliveryZone: 'kumasi',
      paymentChannel: 'mobile_money',
      activeQuickViewProduct: null,
      selectedQvSize: 'M'
    };

    const formatGHS = (amount) => `GH₵ ${Number(amount).toLocaleString('en-GH', { minimumFractionDigits: 2, maximumFractionDigits: 2 })}`;

    /* ==================== WELCOME FEATURE LOGIC ==================== */
    const welcomeOverlay = document.getElementById('welcomeOverlay');
    const enterAtelierBtn = document.getElementById('enterAtelierBtn');
    const replayWelcomeBtn = document.getElementById('replayWelcomeBtn');

    function dismissWelcome() {
      welcomeOverlay.classList.add('is-dismissed');
      document.body.classList.remove('no-scroll');
      sessionStorage.setItem('typ_welcomed', 'true');
      setTimeout(() => {
        welcomeOverlay.classList.add('is-hidden');
      }, 1150);
    }

    function showWelcome() {
      welcomeOverlay.classList.remove('is-hidden', 'is-dismissed');
      document.body.classList.add('no-scroll');
    }

    if (sessionStorage.getItem('typ_welcomed') === 'true') {
      welcomeOverlay.classList.add('is-hidden');
    } else {
      document.body.classList.add('no-scroll');
    }

    enterAtelierBtn.addEventListener('click', dismissWelcome);
    replayWelcomeBtn.addEventListener('click', () => {
      window.scrollTo({ top: 0, behavior: 'instant' });
      showWelcome();
    });

    /* ==================== ROUTING & NAVIGATION ==================== */
    const siteHeader = document.getElementById('siteHeader');
    const mobileDrawer = document.getElementById('mobileDrawer');

    function updateHeaderStyle() {
      if (state.route === 'home' && window.scrollY < window.innerHeight * 0.65) {
        siteHeader.classList.add('is-hero-overlay');
      } else {
        siteHeader.classList.remove('is-hero-overlay');
      }
    }

    window.addEventListener('scroll', updateHeaderStyle, { passive: true });

    function navigateTo(route, filterCat = null) {
      if (!['home', 'lookbook', 'shop', 'about'].includes(route)) route = 'home';
      state.route = route;

      if (filterCat) {
        state.shopCategory = filterCat;
        syncFilterPills();
        renderShopGrid();
      }

      document.querySelectorAll('.page-view').forEach((v) => v.classList.remove('is-active'));
      document.getElementById(`view-${route}`).classList.add('is-active');

      document.querySelectorAll('.nav-link').forEach((btn) => {
        btn.classList.toggle('is-active', btn.dataset.route === route);
      });

      mobileDrawer.classList.remove('is-open');
      window.location.hash = route;
      window.scrollTo({ top: 0, behavior: 'smooth' });
      updateHeaderStyle();
    }

    document.querySelectorAll('[data-route]').forEach((el) => {
      el.addEventListener('click', () => navigateTo(el.dataset.route));
    });

    document.querySelectorAll('[data-shop-filter]').forEach((el) => {
      el.addEventListener('click', () => navigateTo('shop', el.dataset.shopFilter));
    });

    document.getElementById('mobileMenuBtn').addEventListener('click', () => mobileDrawer.classList.add('is-open'));
    document.getElementById('closeMobileDrawer').addEventListener('click', () => mobileDrawer.classList.remove('is-open'));

    /* Hero Video Play/Pause Toggle */
    const heroVideo = document.getElementById('heroVideo');
    const toggleHeroVideoBtn = document.getElementById('toggleHeroVideoBtn');
    const heroVideoStateText = document.getElementById('heroVideoStateText');

    toggleHeroVideoBtn.addEventListener('click', () => {
      if (heroVideo.paused) {
        heroVideo.play();
        heroVideoStateText.textContent = 'Film Playing • Pause';
      } else {
        heroVideo.pause();
        heroVideoStateText.textContent = 'Film Paused • Play';
      }
    });

    /* ==================== RENDERING PRODUCTS & LOOKBOOK ==================== */
    function createProductCardHTML(product) {
      return `
        <article class="product-card">
          <div class="product-media" onclick="openQuickView('${product.id}')">
            <img src="${product.img}" alt="${product.title}" loading="lazy" />
            <div class="product-quick-bar" onclick="event.stopPropagation()">
              <span style="font-size:0.62rem;letter-spacing:0.14em;text-transform:uppercase;color:var(--ink-muted);">Quick Add:</span>
              <div>
                ${['S', 'M', 'L', 'XL'].map((s) => `
                  <button class="quick-size-btn" type="button" onclick="addToCart('${product.id}', '${s}')">${s}</button>
                `).join('')}
              </div>
            </div>
          </div>
          <div class="product-info">
            <div>
              <h3 class="product-title" onclick="openQuickView('${product.id}')">${product.title}</h3>
              <p class="product-material">${product.material}</p>
            </div>
            <span class="product-price">${formatGHS(product.price)}</span>
          </div>
        </article>
      `;
    }

    function renderHomeFeatured() {
      const container = document.getElementById('homeFeaturedGrid');
      const featured = PRODUCTS.filter((p) => p.featured);
      container.innerHTML = featured.map(createProductCardHTML).join('');
    }

    function renderShopGrid() {
      const container = document.getElementById('shopProductGrid');
      let list = state.shopCategory === 'All'
        ? [...PRODUCTS]
        : PRODUCTS.filter((p) => p.category === state.shopCategory);

      if (state.shopSort === 'price-asc') {
        list.sort((a, b) => a.price - b.price);
      } else if (state.shopSort === 'price-desc') {
        list.sort((a, b) => b.price - a.price);
      }

      container.innerHTML = list.map(createProductCardHTML).join('');
    }

    function syncFilterPills() {
      document.querySelectorAll('#shopFilterPills .filter-pill').forEach((pill) => {
        pill.classList.toggle('is-active', pill.dataset.cat === state.shopCategory);
      });
    }

    document.querySelectorAll('#shopFilterPills .filter-pill').forEach((pill) => {
      pill.addEventListener('click', () => {
        state.shopCategory = pill.dataset.cat;
        syncFilterPills();
        renderShopGrid();
      });
    });

    document.getElementById('shopSortSelect').addEventListener('change', (e) => {
      state.shopSort = e.target.value;
      renderShopGrid();
    });

    function renderLookbook() {
      const container = document.getElementById('lookbookGrid');
      container.innerHTML = LOOKBOOK_FRAMES.map((frame) => `
        <article class="look-item ${frame.layout}">
          <div class="look-img-wrap">
            <img src="${frame.img}" alt="${frame.title}" loading="lazy" />
          </div>
          <div class="look-caption">
            <div>
              <h3>${frame.title}</h3>
              <span>${frame.subtitle}</span>
            </div>
            <button class="shop-look-btn" type="button" onclick="openQuickView('${frame.productId}')">
              Shop This Look
            </button>
          </div>
        </article>
      `).join('');
    }

    /* ==================== QUICK VIEW MODAL ==================== */
    const quickViewModal = document.getElementById('quickViewModal');

    window.openQuickView = function(productId) {
      const product = PRODUCTS.find((p) => p.id === productId);
      if (!product) return;

      state.activeQuickViewProduct = product;
      state.selectedQvSize = 'M';

      document.getElementById('qvImage').src = product.img;
      document.getElementById('qvImage').alt = product.title;
      document.getElementById('qvCategory').textContent = product.category;
      document.getElementById('qvTitle').textContent = product.title;
      document.getElementById('qvPrice').textContent = formatGHS(product.price);
      document.getElementById('qvDesc').textContent = product.desc;
      document.getElementById('qvMaterial').textContent = product.material;

      document.querySelectorAll('#qvSizes .size-pill').forEach((btn) => {
        btn.classList.toggle('is-selected', btn.dataset.size === 'M');
      });

      quickViewModal.classList.add('is-open');
    };

    document.querySelectorAll('#qvSizes .size-pill').forEach((btn) => {
      btn.addEventListener('click', () => {
        state.selectedQvSize = btn.dataset.size;
        document.querySelectorAll('#qvSizes .size-pill').forEach((b) => {
          b.classList.toggle('is-selected', b === btn);
        });
      });
    });

    document.getElementById('qvAddToBagBtn').addEventListener('click', () => {
      if (state.activeQuickViewProduct) {
        addToCart(state.activeQuickViewProduct.id, state.selectedQvSize);
        quickViewModal.classList.remove('is-open');
      }
    });

    document.getElementById('closeQuickViewBtn').addEventListener('click', () => {
      quickViewModal.classList.remove('is-open');
    });

    /* ==================== CART & DELIVERY LOGIC ==================== */
    const cartDrawer = document.getElementById('cartDrawer');
    const drawerBackdrop = document.getElementById('drawerBackdrop');

    function openBag() {
      cartDrawer.classList.add('is-open');
      drawerBackdrop.classList.add('is-open');
    }

    function closeBag() {
      cartDrawer.classList.remove('is-open');
      drawerBackdrop.classList.remove('is-open');
    }

    document.getElementById('openBagBtn').addEventListener('click', openBag);
    document.getElementById('closeBagBtn').addEventListener('click', closeBag);
    drawerBackdrop.addEventListener('click', closeBag);

    function showToast(msg) {
      const toast = document.getElementById('toast');
      toast.textContent = msg;
      toast.classList.add('is-visible');
      clearTimeout(window.__toastTimer);
      window.__toastTimer = setTimeout(() => toast.classList.remove('is-visible'), 2800);
    }

    function saveCart() {
      localStorage.setItem('typ_cart_v1', JSON.stringify(state.cart));
      renderCart();
    }

    window.addToCart = function(productId, size = 'M') {
      const product = PRODUCTS.find((p) => p.id === productId);
      if (!product) return;

      const existing = state.cart.find((item) => item.id === productId && item.size === size);
      if (existing) {
        existing.qty += 1;
      } else {
        state.cart.push({
          id: product.id,
          title: product.title,
          price: product.price,
          img: product.img,
          size,
          qty: 1
        });
      }

      saveCart();
      showToast(`Added ${product.title} (${size})`);
      openBag();
    };

    window.updateQty = function(index, delta) {
      state.cart[index].qty += delta;
      if (state.cart[index].qty <= 0) {
        state.cart.splice(index, 1);
      }
      saveCart();
    };

    window.removeCartItem = function(index) {
      state.cart.splice(index, 1);
      saveCart();
    };

    function getCartTotals() {
      const subtotal = state.cart.reduce((sum, item) => sum + item.price * item.qty, 0);
      const delivery = state.cart.length > 0 ? DELIVERY_FEES[state.deliveryZone] : 0;
      return { subtotal, delivery, total: subtotal + delivery };
    }

    function renderCart() {
      const totalCount = state.cart.reduce((sum, item) => sum + item.qty, 0);
      document.getElementById('navBagCount').textContent = totalCount;

      const itemsContainer = document.getElementById('cartItemsContainer');
      const checkoutPanel = document.getElementById('checkoutPanel');
      const cartFooter = document.getElementById('cartFooter');

      if (state.cart.length === 0) {
        itemsContainer.innerHTML = `
          <div class="cart-empty">
            <p style="font-family:var(--font-serif);font-size:1.5rem;color:var(--ink-obsidian);margin-bottom:0.5rem;">Your bag is empty</p>
            <p style="font-size:0.84rem;margin-bottom:1.5rem;">Explore our Kumasi-crafted silhouettes to begin.</p>
            <button class="btn-outline" type="button" onclick="closeBagAndShop()">Browse Shop</button>
          </div>
        `;
        checkoutPanel.style.display = 'none';
        cartFooter.style.display = 'none';
        return;
      }

      itemsContainer.innerHTML = state.cart.map((item, idx) => `
        <div class="cart-item">
          <img src="${item.img}" alt="${item.title}" />
          <div>
            <div class="cart-item-top">
              <span class="cart-item-title">${item.title}</span>
              <span style="font-size:0.82rem;font-weight:500;">${formatGHS(item.price * item.qty)}</span>
            </div>
            <div class="cart-item-meta">Size: ${item.size} &bull; ${formatGHS(item.price)} each</div>
            <div class="cart-item-controls">
              <div class="qty-stepper">
                <button type="button" onclick="updateQty(${idx}, -1)">&minus;</button>
                <span>${item.qty}</span>
                <button type="button" onclick="updateQty(${idx}, 1)">+</button>
              </div>
              <button class="remove-item-btn" type="button" onclick="removeCartItem(${idx})">Remove</button>
            </div>
          </div>
        </div>
      `).join('');

      checkoutPanel.style.display = 'block';
      cartFooter.style.display = 'block';

      const { subtotal, delivery, total } = getCartTotals();
      document.getElementById('summarySubtotal').textContent = formatGHS(subtotal);
      document.getElementById('summaryDeliveryLabel').textContent =
        state.deliveryZone === 'kumasi' ? 'Delivery (Within Kumasi)' : 'Delivery (Outside Kumasi)';
      document.getElementById('summaryDelivery').textContent = formatGHS(delivery);
      document.getElementById('summaryTotal').textContent = formatGHS(total);
    }

    window.closeBagAndShop = function() {
      closeBag();
      navigateTo('shop');
    };

    /* Delivery Zone Switching (GH₵ 20 Kumasi vs GH₵ 40 Outside Kumasi) */
    document.querySelectorAll('.delivery-option').forEach((option) => {
      option.addEventListener('click', () => {
        state.deliveryZone = option.dataset.zone;
        document.querySelectorAll('.delivery-option').forEach((el) => {
          const isMatch = el.dataset.zone === state.deliveryZone;
          el.classList.toggle('is-selected', isMatch);
          el.querySelector('input').checked = isMatch;
        });
        renderCart();
      });
    });

    /* Payment Channel Switching (Mobile Money vs Debit Card) */
    document.querySelectorAll('.pay-method-btn').forEach((btn) => {
      btn.addEventListener('click', () => {
        state.paymentChannel = btn.dataset.channel;
        document.querySelectorAll('.pay-method-btn').forEach((b) => {
          b.classList.toggle('is-selected', b === btn);
        });
      });
    });

    /* ==================== PAYSTACK CHECKOUT INTEGRATION ==================== */
    function showOrderReceipt(reference, isSimulated) {
      const name = document.getElementById('custName').value.trim();
      const email = document.getElementById('custEmail').value.trim();
      const phone = document.getElementById('custPhone').value.trim();
      const address = document.getElementById('custAddress').value.trim();
      const { subtotal, delivery, total } = getCartTotals();

      document.getElementById('receiptMessage').textContent = isSimulated
        ? `Demo Checkout Complete! Once you paste your Paystack Public Key into index.html, this exact button launches the live Paystack Mobile Money & Card popup.`
        : `Your payment via Paystack has been authorized. Our Kumasi studio is preparing your pieces.`;

      document.getElementById('receiptDetails').innerHTML = `
        <strong>Reference:</strong> ${reference}<br />
        <strong>Client:</strong> ${name} (${phone})<br />
        <strong>Email:</strong> ${email}<br />
        <strong>Delivery Zone:</strong> ${state.deliveryZone === 'kumasi' ? 'Within Kumasi (GH₵ 20)' : 'Outside Kumasi (GH₵ 40)'}<br />
        <strong>Address:</strong> ${address}<br />
        <strong>Channel:</strong> ${state.paymentChannel === 'mobile_money' ? 'Mobile Money (Paystack)' : 'Debit / Credit Card (Paystack)'}<br />
        <strong>Subtotal:</strong> ${formatGHS(subtotal)} &bull; <strong>Delivery:</strong> ${formatGHS(delivery)}<br />
        <strong>Total Paid:</strong> ${formatGHS(total)}
      `;

      state.cart = [];
      saveCart();
      closeBag();
      document.getElementById('receiptModal').classList.add('is-open');
    }

    document.getElementById('closeReceiptBtn').addEventListener('click', () => {
      document.getElementById('receiptModal').classList.remove('is-open');
    });

    document.getElementById('payWithPaystackBtn').addEventListener('click', () => {
      if (state.cart.length === 0) return;

      const name = document.getElementById('custName').value.trim();
      const email = document.getElementById('custEmail').value.trim();
      const phone = document.getElementById('custPhone').value.trim();
      const address = document.getElementById('custAddress').value.trim();

      if (!name || !email || !phone || !address) {
        showToast('Please complete your name, email, phone & delivery address');
        return;
      }

      const { subtotal, delivery, total } = getCartTotals();
      const amountInPesewas = Math.round(total * 100);
      const ref = 'TYP-' + Date.now() + '-' + Math.floor(Math.random() * 1000);

      // If placeholder key hasn't been replaced yet, run clean demo confirmation
      if (!PAYSTACK_PUBLIC_KEY || PAYSTACK_PUBLIC_KEY.includes('YOUR_PAYSTACK_PUBLIC_KEY') || typeof PaystackPop === 'undefined') {
        showOrderReceipt(ref + '-TEST', true);
        return;
      }

      // Live Paystack Inline Popup (Supports Mobile Money & Debit Cards in GHS)
      const channels = state.paymentChannel === 'mobile_money'
        ? ['mobile_money', 'card']
        : ['card', 'mobile_money'];

      const handler = PaystackPop.setup({
        key: PAYSTACK_PUBLIC_KEY,
        email: email,
        amount: amountInPesewas,
        currency: 'GHS',
        ref: ref,
        channels: channels,
        metadata: {
          custom_fields: [
            { display_name: 'Client Name', variable_name: 'client_name', value: name },
            { display_name: 'Phone / MoMo Number', variable_name: 'phone_number', value: phone },
            { display_name: 'Delivery Zone', variable_name: 'delivery_zone', value: state.deliveryZone === 'kumasi' ? 'Kumasi (GHS 20)' : 'Outside Kumasi (GHS 40)' },
            { display_name: 'Delivery Address', variable_name: 'delivery_address', value: address },
            { display_name: 'Items', variable_name: 'order_items', value: state.cart.map(i => `${i.title} (${i.size}) x${i.qty}`).join(', ') },
            { display_name: 'Subtotal GHS', variable_name: 'subtotal_ghs', value: subtotal },
            { display_name: 'Delivery GHS', variable_name: 'delivery_ghs', value: delivery }
          ]
        },
        callback: function(response) {
          showOrderReceipt(response.reference, false);
        },
        onClose: function() {
          showToast('Paystack checkout closed');
        }
      });

      handler.openIframe();
    });

    /* ==================== INITIALIZATION ==================== */
    (function init() {
      renderHomeFeatured();
      renderShopGrid();
      renderLookbook();
      renderCart();

      const hashRoute = window.location.hash.replace('#', '');
      if (['home', 'lookbook', 'shop', 'about'].includes(hashRoute)) {
        navigateTo(hashRoute);
      } else {
        updateHeaderStyle();
      }
    })();
  </script>
</body>
</html>
