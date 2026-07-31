<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes, viewport-fit=cover">
  <title>Happy Girlfriend's Day, Annie ❤️</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;0,800;1,400;1,500;1,600&family=Poppins:wght@200;300;400;500;600;700&display=swap" rel="stylesheet">
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/gsap.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.5/ScrollTrigger.min.js"></script>
  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <style>
    :root {
      --crimson: #c41e3a;
      --soft-pink: #f8c8d4;
      --teal: #5b8c8c;
      --white: #fffafb;
      --rose-gold: #b76e79;
      --light-gold: #d4a853;
      --glass-bg: rgba(255, 250, 251, 0.12);
      --glass-border: rgba(255, 255, 255, 0.25);
      --glass-shadow: 0 8px 40px rgba(0, 0, 0, 0.08);
      --font-serif: 'Playfair Display', Georgia, serif;
      --font-sans: 'Poppins', sans-serif;
    }
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    html {
      scroll-behavior: smooth;
      scrollbar-width: thin;
      scrollbar-color: #c41e3a #1a0a0d;
    }
    ::-webkit-scrollbar { width: 6px; }
    ::-webkit-scrollbar-track { background: #1a0a0d; }
    ::-webkit-scrollbar-thumb { background: #c41e3a; border-radius: 20px; }

    body {
      font-family: var(--font-sans);
      background: #0d0508;
      color: #f5e6e8;
      overflow-x: hidden;
      -webkit-tap-highlight-color: transparent;
      user-select: none;
    }

    /* Custom cursor hidden on touch devices */
    @media (hover: none) and (pointer: coarse) {
      #custom-cursor, #cursor-trail-container { display: none; }
      body { cursor: auto; }
    }

    #custom-cursor {
      position: fixed;
      pointer-events: none;
      z-index: 99999;
      width: 28px;
      height: 28px;
      border-radius: 50%;
      background: radial-gradient(circle, #ff6b8a 0%, #c41e3a 70%, transparent 72%);
      box-shadow: 0 0 25px #ff3b6e, 0 0 50px #ff3b6e55, 0 0 80px #ff174430;
      transform: translate(-50%, -50%);
      transition: width 0.2s, height 0.2s, background 0.3s;
      animation: cursorPulse 1.6s ease-in-out infinite;
    }
    #custom-cursor::after {
      content: '❤️';
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 10px;
      animation: cursorHeartBeat 0.8s ease-in-out infinite;
      opacity: 0.9;
    }
    @keyframes cursorPulse {
      0%,100% { box-shadow: 0 0 25px #ff3b6e, 0 0 50px #ff3b6e55, 0 0 80px #ff174430; }
      50% { box-shadow: 0 0 40px #ff6b8a, 0 0 70px #ff3b6e70, 0 0 110px #ff174450; }
    }
    @keyframes cursorHeartBeat {
      0%,100% { transform: translate(-50%, -50%) scale(1); }
      25% { transform: translate(-50%, -50%) scale(1.35); }
      50% { transform: translate(-50%, -50%) scale(1); }
      75% { transform: translate(-50%, -50%) scale(1.25); }
    }
    #cursor-trail-container {
      position: fixed;
      pointer-events: none;
      z-index: 99998;
      top: 0; left: 0;
      width: 100%; height: 100%;
    }
    .cursor-trail-heart {
      position: absolute;
      pointer-events: none;
      font-size: 14px;
      animation: trailFade 1.2s ease-out forwards;
      opacity: 0.9;
    }
    @keyframes trailFade {
      0% { opacity:0.9; transform:translate(0,0) scale(1) rotate(0deg); }
      100% { opacity:0; transform:translate(var(--tx),var(--ty)) scale(0.2) rotate(var(--rot)); }
    }

    #loading-screen {
      position: fixed; top:0; left:0; width:100%; height:100%;
      background: radial-gradient(ellipse at center, #1a0508 0%, #0d0204 100%);
      z-index: 100000; display:flex; flex-direction:column; align-items:center; justify-content:center;
      transition: opacity 0.8s ease, visibility 0.8s ease;
    }
    #loading-screen.hidden { opacity:0; visibility:hidden; pointer-events:none; }
    .blooming-rose { position:relative; width:80px; height:80px; }
    .rose-petal {
      position:absolute; width:35px; height:35px;
      background: radial-gradient(circle at 30% 30%, #ff6b8a, #c41e3a);
      border-radius:50% 0 50% 50%; top:50%; left:50%;
      transform-origin:center; animation:bloomPetal 2s ease-in-out infinite; opacity:0;
    }
    .rose-petal:nth-child(1){animation-delay:0s;} .rose-petal:nth-child(2){animation-delay:0.25s;}
    .rose-petal:nth-child(3){animation-delay:0.5s;} .rose-petal:nth-child(4){animation-delay:0.75s;}
    .rose-petal:nth-child(5){animation-delay:1s;} .rose-petal:nth-child(6){animation-delay:1.25s;}
    @keyframes bloomPetal {
      0%{opacity:0; transform:translate(-50%,-50%) rotate(0deg) scale(0);}
      40%{opacity:1;} 100%{opacity:0.85; transform:translate(-50%,-50%) rotate(var(--angle)) scale(1);}
    }
    .rose-center {
      position:absolute; width:18px; height:18px; background:radial-gradient(circle,#ffd700,#d4a853);
      border-radius:50%; top:50%; left:50%; transform:translate(-50%,-50%); z-index:2;
      animation:centerGlow 1.5s ease-in-out infinite;
    }
    @keyframes centerGlow {
      0%,100%{box-shadow:0 0 15px #ffd70088,0 0 30px #d4a85344;}
      50%{box-shadow:0 0 30px #ffd700bb,0 0 60px #d4a85377;}
    }
    .loading-text { margin-top:25px; font-family:var(--font-serif); font-size:1.1rem; color:#f8c8d4; letter-spacing:3px; animation:fadeInOut 2s ease-in-out infinite; }
    @keyframes fadeInOut { 0%,100%{opacity:0.4;} 50%{opacity:1;} }

    #envelope-screen {
      position:fixed; top:0; left:0; width:100%; height:100%;
      background: radial-gradient(ellipse at center, #1a0508 0%, #0d0204 100%);
      z-index:99990; display:flex; flex-direction:column; align-items:center; justify-content:center;
      transition: all 1.2s cubic-bezier(0.68,-0.55,0.27,1.55);
    }
    #envelope-screen.opened { transform:scale(1.8); opacity:0; pointer-events:none; filter:blur(20px); }
    .envelope-wrapper { position:relative; cursor:pointer; animation:floatEnvelope 3s ease-in-out infinite; }
    @keyframes floatEnvelope { 0%,100%{transform:translateY(0);} 50%{transform:translateY(-18px);} }
    .envelope-body {
      width:200px; height:130px; background:linear-gradient(145deg,#f5e6e8,#e8d0d4);
      border-radius:12px; position:relative; box-shadow:0 20px 60px rgba(180,40,60,0.35),0 0 80px rgba(255,150,170,0.2);
    }
    .envelope-flap {
      position:absolute; top:0; left:0; width:100%; height:80px;
      background:linear-gradient(180deg,#f0dce0,#e0c8cc); clip-path:polygon(0 0,50% 70%,100% 0);
      border-radius:12px 12px 0 0; transform-origin:top center;
      transition:transform 0.8s cubic-bezier(0.68,-0.3,0.27,1.3); z-index:3;
    }
    #envelope-screen.opened .envelope-flap { transform:rotateX(180deg); }
    .wax-seal {
      position:absolute; top:50%; left:50%; transform:translate(-50%,-50%);
      width:55px; height:55px; background:radial-gradient(circle at 35% 35%,#d4455a,#8b1a2b);
      border-radius:50%; z-index:5; box-shadow:0 6px 25px rgba(180,30,50,0.6),inset 0 2px 8px rgba(255,200,200,0.4);
      display:flex; align-items:center; justify-content:center; font-family:var(--font-serif);
      font-size:1.6rem; font-weight:700; color:#ffd700; animation:sealGlow 2s ease-in-out infinite;
    }
    @keyframes sealGlow { 0%,100%{box-shadow:0 6px 25px rgba(180,30,50,0.6),0 0 40px rgba(255,180,100,0.25);} 50%{box-shadow:0 6px 35px rgba(200,30,50,0.8),0 0 65px rgba(255,180,100,0.5);} }
    .envelope-tap-text { margin-top:30px; font-family:var(--font-sans); font-size:0.95rem; color:#f8c8d4; letter-spacing:4px; animation:tapPulse 1.8s ease-in-out infinite; }
    @keyframes tapPulse { 0%,100%{opacity:0.5; transform:scale(1);} 50%{opacity:1; transform:scale(1.08);} }
    .envelope-particles { position:absolute; pointer-events:none; width:100%; height:100%; top:0; left:0; }
    .envelope-particle {
      position:absolute; width:4px; height:4px; background:#ffd700; border-radius:50%;
      animation:particleDrift 4s ease-in-out infinite; opacity:0;
    }
    @keyframes particleDrift { 0%{opacity:0; transform:translateY(0) translateX(0);} 30%{opacity:0.8;} 100%{opacity:0; transform:translateY(-120px) translateX(var(--dx));} }

    #main-content { position:relative; z-index:1; opacity:0; transition:opacity 1.5s ease; }
    #main-content.visible { opacity:1; }

    #music-player {
      position:fixed; bottom:25px; right:25px; z-index:99980;
      background:var(--glass-bg); backdrop-filter:blur(20px); -webkit-backdrop-filter:blur(20px);
      border:1px solid var(--glass-border); border-radius:20px; padding:15px 20px;
      display:flex; align-items:center; gap:14px; box-shadow:var(--glass-shadow),0 0 40px rgba(180,100,120,0.2);
      transition:all 0.3s ease; max-width:380px;
    }
    .vinyl-record {
      width:55px; height:55px; border-radius:50%;
      background:conic-gradient(#1a1a1a 0% 25%,#2a2a2a 25% 50%,#1a1a1a 50% 75%,#2a2a2a 75% 100%);
      border:3px solid #444; position:relative; flex-shrink:0;
      animation:spinVinyl 3s linear infinite paused;
    }
    .vinyl-record.playing { animation-play-state:running; }
    @keyframes spinVinyl { from{transform:rotate(0deg);} to{transform:rotate(360deg);} }
    .vinyl-record::after {
      content:''; position:absolute; width:18px; height:18px;
      background:radial-gradient(circle,#c41e3a,#8b1a2b); border-radius:50%;
      top:50%; left:50%; transform:translate(-50%,-50%); border:2px solid #ffd70055;
    }
    .player-controls { display:flex; flex-direction:column; gap:6px; min-width:0; }
    .player-info { font-family:var(--font-serif); font-size:0.75rem; color:#f8c8d4; letter-spacing:1px; white-space:nowrap; overflow:hidden; text-overflow:ellipsis; }
    .player-buttons { display:flex; align-items:center; gap:10px; }
    .player-btn {
      background:rgba(255,255,255,0.15); border:1px solid rgba(255,255,255,0.3); color:#fff;
      width:32px; height:32px; border-radius:50%; cursor:pointer; font-size:13px;
      display:flex; align-items:center; justify-content:center; transition:all 0.3s ease;
    }
    .progress-bar-wrap { width:100%; height:4px; background:rgba(255,255,255,0.2); border-radius:10px; overflow:hidden; }
    .progress-bar-fill { height:100%; background:linear-gradient(90deg,#c41e3a,#ff6b8a); border-radius:10px; width:0%; }
    .volume-slider { width:60px; height:3px; -webkit-appearance:none; background:rgba(255,255,255,0.25); border-radius:10px; outline:none; }
    .volume-slider::-webkit-slider-thumb { -webkit-appearance:none; width:14px; height:14px; background:#ff6b8a; border-radius:50%; box-shadow:0 0 10px #ff3b6e; }

    .section { position:relative; min-height:100vh; display:flex; flex-direction:column; align-items:center; justify-content:center; padding:60px 20px; overflow:hidden; }
    #hero { background:radial-gradient(ellipse at 50% 40%, #1f0a10 0%, #0d0204 60%, #050102 100%); text-align:center; }
    .hero-title {
      font-family:var(--font-serif); font-size:clamp(2.4rem,6vw,5rem); font-weight:700;
      background:linear-gradient(135deg,#ff6b8a,#c41e3a,#ffd700,#ff6b8a); background-size:300% 300%;
      -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text;
      animation:gradientShift 4s ease-in-out infinite; letter-spacing:2px;
    }
    @keyframes gradientShift { 0%,100%{background-position:0% 50%;} 50%{background-position:100% 50%;} }
    .hero-subtitle { font-family:var(--font-serif); font-size:clamp(1.2rem,3vw,2rem); color:#f8c8d4; letter-spacing:3px; font-style:italic; }
    .scroll-indicator { position:absolute; bottom:40px; display:flex; flex-direction:column; align-items:center; gap:8px; animation:bounceDown 2s ease-in-out infinite; }
    @keyframes bounceDown { 0%,100%{transform:translateY(0);} 50%{transform:translateY(15px);} }
    .scroll-arrow { width:30px; height:30px; border-right:2px solid #f8c8d4; border-bottom:2px solid #f8c8d4; transform:rotate(45deg); opacity:0.7; }

    .floating-hearts-container,.petals-container,.sparkles-container { position:absolute; pointer-events:none; top:0; left:0; width:100%; height:100%; z-index:2; }
    .floating-heart { position:absolute; animation:heartRise linear forwards; opacity:0; font-size:var(--size); }
    @keyframes heartRise { 0%{opacity:0; transform:translateY(0) translateX(0) rotate(0deg) scale(0.3);} 15%{opacity:var(--op);} 85%{opacity:var(--op);} 100%{opacity:0; transform:translateY(-105vh) translateX(var(--drift)) rotate(var(--spin)) scale(1.2);} }
    .petal { position:absolute; animation:petalFall linear forwards; opacity:0; font-size:var(--size); }
    @keyframes petalFall { 0%{opacity:0; transform:translateY(-5vh) translateX(0) rotate(0deg);} 10%{opacity:0.85;} 90%{opacity:0.6;} 100%{opacity:0; transform:translateY(108vh) translateX(var(--drift)) rotate(var(--spin));} }
    .sparkle-dot { position:absolute; width:var(--size); height:var(--size); background:#ffd700; border-radius:50%; animation:sparkleTwinkle var(--dur) ease-in-out infinite; animation-delay:var(--delay); opacity:0; }
    @keyframes sparkleTwinkle { 0%,100%{opacity:0; transform:scale(0);} 50%{opacity:1; transform:scale(1);} }

    #love-counter { background:radial-gradient(ellipse at 50% 50%, #1a080d 0%, #0d0204 100%); text-align:center; }
    .counter-value { font-family:var(--font-serif); font-size:clamp(4rem,10vw,8rem); font-weight:800; background:linear-gradient(180deg,#ff6b8a 0%,#c41e3a 50%,#ffd700 100%); -webkit-background-clip:text; -webkit-text-fill-color:transparent; background-clip:text; }
    .counter-heart { font-size:3rem; animation:hugeHeartBeat 1s ease-in-out infinite; }
    @keyframes hugeHeartBeat { 0%,100%{transform:scale(1);} 30%{transform:scale(1.4);} 60%{transform:scale(1);} 80%{transform:scale(1.3);} }

    .memory-card { width:260px; background:var(--glass-bg); backdrop-filter:blur(16px); border:1px solid var(--glass-border); border-radius:24px; padding:20px; text-align:center; box-shadow:var(--glass-shadow); transition:all 0.5s; }
    .memory-frame { aspect-ratio:1; border-radius:16px; overflow:hidden; border:4px solid #c41e3a55; background:linear-gradient(135deg,#3a1020,#1a050d); display:flex; align-items:center; justify-content:center; }
    .memory-img-placeholder { width:80%; height:80%; border-radius:12px; display:flex; align-items:center; justify-content:center; font-size:4rem; background:linear-gradient(135deg,#ff6b8a33,#c41e3a22,#ffd70022); color:#ffd700; }

    .bouquet-rose { font-size:clamp(3rem,8vw,6rem); animation:roseBloom 2s ease-out forwards; opacity:0; transform:scale(0); filter:drop-shadow(0 0 20px #ff3b6e55); }
    @keyframes roseBloom { 0%{opacity:0; transform:scale(0) rotate(-30deg);} 60%{opacity:1; transform:scale(1.3) rotate(5deg);} 100%{opacity:1; transform:scale(1) rotate(0deg);} }
    .bouquet-message { font-family:var(--font-serif); font-size:clamp(1.3rem,4vw,2rem); color:#f8c8d4; letter-spacing:2px; margin-top:25px; }

    .btn-yes { padding:16px 50px; font-size:1.3rem; font-weight:600; background:linear-gradient(135deg,#c41e3a,#ff6b8a); color:#fff; border:none; border-radius:50px; cursor:pointer; box-shadow:0 8px 35px rgba(200,40,60,0.5); transition:0.3s; z-index:10; }
    .btn-no { padding:16px 50px; font-size:1.3rem; background:rgba(255,255,255,0.1); color:#ddd; border:2px solid rgba(255,255,255,0.3); border-radius:50px; cursor:pointer; transition:0.15s; }

    .reason-card { background:var(--glass-bg); backdrop-filter:blur(14px); border:1px solid var(--glass-border); border-radius:20px; padding:30px 20px; text-align:center; font-family:var(--font-serif); font-size:1.1rem; color:#f5e6e8; animation:reasonGlow 3s ease-in-out infinite; }
    @keyframes reasonGlow { 0%,100%{box-shadow:0 8px 40px rgba(0,0,0,0.08),0 0 20px rgba(200,100,130,0.1);} 50%{box-shadow:0 8px 40px rgba(0,0,0,0.08),0 0 45px rgba(200,100,130,0.35);} }

    #dream-section { background:radial-gradient(ellipse at 50% 30%,#0a0d1a 0%,#020408 70%,#000 100%); min-height:100vh; }
    .moon { position:absolute; top:8%; right:15%; width:100px; height:100px; background:radial-gradient(circle at 40% 40%,#fffde7,#ffecb3 40%,#ffe082 100%); border-radius:50%; box-shadow:0 0 60px #fffde7aa; animation:moonGlow 4s ease-in-out infinite; }
    @keyframes moonGlow { 0%,100%{box-shadow:0 0 60px #fffde7aa;} 50%{box-shadow:0 0 90px #fffde7cc;} }

    .letter-card { max-width:700px; background:linear-gradient(145deg,#fdf5e6,#f5e6d3,#fdf5e6); border-radius:16px; padding:40px 30px; box-shadow:0 20px 70px rgba(0,0,0,0.4); border:2px solid #d4a85355; color:#3a1a1a; font-family:var(--font-serif); line-height:1.9; }
    .letter-seal { position:absolute; top:-25px; left:50%; transform:translateX(-50%); width:50px; height:50px; background:radial-gradient(circle at 35% 35%,#d4455a,#8b1a2b); border-radius:50%; display:flex; align-items:center; justify-content:center; font-weight:700; font-size:1.3rem; color:#ffd700; }

    #ending-scene {
      position:fixed; top:0; left:0; width:100%; height:100%;
      background:radial-gradient(ellipse at center, #0a0d1a 0%, #000 100%);
      z-index:99995; display:flex; flex-direction:column; align-items:center; justify-content:center;
      opacity:0; visibility:hidden; pointer-events:none; transition:opacity 2s ease, visibility 2s ease;
    }
    #ending-scene.active { opacity:1; visibility:visible; pointer-events:auto; }
    .ending-close {
      position:absolute; top:25px; right:25px; font-size:2.2rem; color:#fff; background:rgba(255,255,255,0.2);
      border:none; border-radius:50%; width:50px; height:50px; cursor:pointer; display:flex; align-items:center; justify-content:center;
      backdrop-filter:blur(10px); transition:0.3s; z-index:10;
    }
    .ending-close:hover { background:rgba(255,255,255,0.4); }

    @media (max-width: 768px) {
      #music-player { bottom:10px; right:10px; padding:10px; max-width:250px; }
      .memory-card { width:200px; }
      .btn-yes,.btn-no { padding:14px 30px; font-size:1.1rem; }
    }
  </style>
</head>
<body>

<div id="custom-cursor"></div>
<div id="cursor-trail-container"></div>

<div id="loading-screen">
  <div class="blooming-rose">
    <div class="rose-petal" style="--angle:0deg;"></div>
    <div class="rose-petal" style="--angle:60deg;"></div>
    <div class="rose-petal" style="--angle:120deg;"></div>
    <div class="rose-petal" style="--angle:180deg;"></div>
    <div class="rose-petal" style="--angle:240deg;"></div>
    <div class="rose-petal" style="--angle:300deg;"></div>
    <div class="rose-center"></div>
  </div>
  <div class="loading-text">Blooming for you...</div>
</div>

<div id="envelope-screen">
  <div class="envelope-wrapper" id="envelope-wrapper">
    <div class="envelope-body">
      <div class="envelope-flap"></div>
      <div class="wax-seal">A</div>
    </div>
    <div class="envelope-particles" id="envelope-particles"></div>
  </div>
  <div class="envelope-tap-text">Tap to Open</div>
</div>

<div class="celebration-overlay" id="celebration-overlay"></div>

<div id="main-content">
  <div id="music-player">
    <div class="vinyl-record playing" id="vinyl-record"></div>
    <div class="player-controls">
      <div class="player-info">🎵 Golden Brown × Love Story</div>
      <div class="player-buttons">
        <button class="player-btn" id="btn-play-pause">⏯️</button>
        <div class="progress-bar-wrap"><div class="progress-bar-fill" id="progress-fill"></div></div>
        <input type="range" class="volume-slider" id="volume-slider" min="0" max="100" value="70">
      </div>
    </div>
  </div>

  <section class="section" id="hero">
    <div class="floating-hearts-container" id="hero-hearts"></div>
    <h1 class="hero-title" data-aos="fade-down">Happy Girlfriend's Day ❤️</h1>
    <p class="hero-subtitle" data-aos="fade-up" data-aos-delay="400">To My Dearest Annie</p>
    <div class="scroll-indicator"><span>Scroll Down</span><div class="scroll-arrow"></div></div>
  </section>

  <section class="section" id="love-counter">
    <div class="counter-label">My Love For You</div>
    <div class="counter-value" id="counter-display">0%</div>
    <div class="counter-heart">❤️‍🔥</div>
  </section>

  <section class="section" id="memory-gallery">
    <div class="memory-card" data-aos="fade-up"><div class="memory-frame"><div class="memory-img-placeholder">📸✨</div></div><p class="caption">Our First Beautiful Moment ❤️</p></div>
    <div class="memory-card" data-aos="fade-up" data-aos-delay="200"><div class="memory-frame"><div class="memory-img-placeholder">💫💖</div></div><p class="caption">Our Favorite Memory ❤️</p></div>
    <div class="memory-card" data-aos="fade-up" data-aos-delay="400"><div class="memory-frame"><div class="memory-img-placeholder">🌟💕</div></div><p class="caption">Forever In My Heart ❤️</p></div>
  </section>

  <section class="section" id="bouquet-section">
    <div class="bouquet-container" id="bouquet-roses">
      <span class="bouquet-rose">🌹</span><span class="bouquet-rose">🌹</span><span class="bouquet-rose">🌹</span>
      <span class="bouquet-rose">🌹</span><span class="bouquet-rose">🌹</span><span class="bouquet-rose">🌹</span><span class="bouquet-rose">🌹</span>
    </div>
    <p class="bouquet-message">For the most beautiful girl in my world.</p>
  </section>

  <section class="section" id="love-game">
    <p class="game-question">Will you stay with me forever? ❤️</p>
    <div class="game-buttons">
      <button class="btn-yes" id="btn-yes">YES 💕</button>
      <button class="btn-no" id="btn-no">NO 😅</button>
    </div>
    <p class="yes-message" id="yes-message" style="display:none;">I knew you'd say yes! ❤️</p>
  </section>

  <section class="section" id="love-reasons">
    <h2>Why I Love You</h2>
    <div class="reasons-grid">
      <div class="reason-card">❤️ Your beautiful smile</div>
      <div class="reason-card">💖 Your kindness</div>
      <div class="reason-card">💕 Your heart</div>
      <div class="reason-card">😊 Your laugh</div>
      <div class="reason-card">💗 Your love</div>
      <div class="reason-card">✨ Everything about you</div>
    </div>
  </section>

  <section class="section" id="dream-section">
    <div class="moon"></div>
    <div class="stars-container" id="stars-container"></div>
    <p class="dream-text">Dreaming of you<br>under the stars ✨</p>
  </section>

  <section class="section" id="final-letter">
    <div class="letter-card">
      <div class="letter-seal">A</div>
      <div class="letter-content">
        <p>Happy Girlfriend's Day, my dearest Annie. 💗✨</p>
        <p>From the very first moment you became a part of my life, everything around me started feeling brighter, warmer, and so much more meaningful…</p>
        <p>I love you endlessly, today, tomorrow, and for every tomorrow after that. ❤️</p>
        <p class="signature">— Forever yours</p>
      </div>
    </div>
  </section>
</div>

<div id="ending-scene">
  <button class="ending-close" id="close-ending" aria-label="Close">✕</button>
  <div class="ending-heart">❤️</div>
  <div class="ending-text">Forever & Always ❤️</div>
  <div class="ending-sub">Made with endless love for Annie.</div>
</div>

<script>
(function() {
  const loadingScreen = document.getElementById('loading-screen');
  const envelopeScreen = document.getElementById('envelope-screen');
  const envelopeWrapper = document.getElementById('envelope-wrapper');
  const mainContent = document.getElementById('main-content');
  const customCursor = document.getElementById('custom-cursor');
  const cursorTrail = document.getElementById('cursor-trail-container');
  const celebrationOverlay = document.getElementById('celebration-overlay');
  const btnYes = document.getElementById('btn-yes');
  const btnNo = document.getElementById('btn-no');
  const yesMessage = document.getElementById('yes-message');
  const counterDisplay = document.getElementById('counter-display');
  const vinylRecord = document.getElementById('vinyl-record');
  const btnPlayPause = document.getElementById('btn-play-pause');
  const progressFill = document.getElementById('progress-fill');
  const volumeSlider = document.getElementById('volume-slider');
  const endingScene = document.getElementById('ending-scene');
  const closeEnding = document.getElementById('close-ending');

  let envelopeOpened = false;
  let musicPlaying = true;
  let audioCtx = null;
  let musicOscillators = [];
  let musicGain = null;

  function initAudio() {
    if(!audioCtx) {
      audioCtx = new (window.AudioContext || window.webkitAudioContext)();
      musicGain = audioCtx.createGain();
      musicGain.gain.value = 0.04;
      musicGain.connect(audioCtx.destination);
      startAmbient();
    }
  }
  function startAmbient() {
    stopAmbient();
    const notes = [261.63,293.66,329.63,349.23,392.0,349.23,329.63,293.66];
    let i=0;
    function next() {
      if(!musicPlaying || !audioCtx) return;
      const osc = audioCtx.createOscillator();
      const g = audioCtx.createGain();
      osc.type='sine'; osc.frequency.value=notes[i%notes.length];
      g.gain.value=0.03; osc.connect(g); g.connect(musicGain);
      g.gain.setValueAtTime(0.03,audioCtx.currentTime);
      g.gain.exponentialRampToValueAtTime(0.001,audioCtx.currentTime+1.8);
      osc.start(); osc.stop(audioCtx.currentTime+1.9);
      musicOscillators.push(osc);
      i++; setTimeout(()=>{ if(musicPlaying) next(); },1600);
    }
    next();
    const bass = audioCtx.createOscillator(); bass.type='sine'; bass.frequency.value=65.41;
    const bg = audioCtx.createGain(); bg.gain.value=0.02; bass.connect(bg); bg.connect(musicGain);
    bass.start(); musicOscillators.push(bass);
  }
  function stopAmbient() {
    musicOscillators.forEach(o=>{try{o.stop();}catch(e){}});
    musicOscillators=[];
  }
  function setVolume(v) { if(musicGain) musicGain.gain.value = v*0.08; }

  window.addEventListener('load', ()=>{
    setTimeout(()=>{ loadingScreen.classList.add('hidden'); setTimeout(()=>loadingScreen.remove(),800); },2200);
  });

  // Envelope click
  envelopeWrapper.addEventListener('click', ()=>{
    if(envelopeOpened) return;
    envelopeOpened=true;
    initAudio();
    envelopeScreen.classList.add('opened');
    setTimeout(()=>{ mainContent.classList.add('visible'); initMain(); },900);
    setTimeout(()=>{ envelopeScreen.style.display='none'; },2000);
    for(let i=0;i<30;i++) {
      let h=document.createElement('span');
      h.textContent=['❤️','💕','💖'][Math.floor(Math.random()*3)];
      h.style.cssText=`position:fixed;z-index:99991;left:${40+Math.random()*20}%;top:${35+Math.random()*30}%;font-size:${20+Math.random()*30}px;animation:envBurst ${1+Math.random()*2}s ease-out forwards;`;
      document.body.appendChild(h); setTimeout(()=>h.remove(),2500);
    }
  });

  function initMain() {
    AOS.init({duration:1000, once:true, offset:80});
    gsap.registerPlugin(ScrollTrigger);
    startProgress();
    startFloating();
    startCounter();
    initStars();
    initFireflies();
    initShootingStars();
    setupNoButton();
    observeFinalLetter();
  }

  function startProgress() {
    let prog=0;
    setInterval(()=>{ if(musicPlaying){ prog+=0.15; if(prog>100) prog=0; progressFill.style.width=prog+'%'; } },300);
  }
  btnPlayPause.addEventListener('click',()=>{
    musicPlaying=!musicPlaying;
    if(musicPlaying){ vinylRecord.classList.add('playing'); if(audioCtx) startAmbient(); }
    else { vinylRecord.classList.remove('playing'); stopAmbient(); }
  });
  volumeSlider.addEventListener('input',()=> setVolume(volumeSlider.value/100));
  setVolume(0.7);

  function startFloating() {
    document.querySelectorAll('.floating-hearts-container').forEach(c=>{
      setInterval(()=>{
        if(!c.isConnected) return;
        let h=document.createElement('span'); h.classList.add('floating-heart');
        h.textContent=['❤️','💕','💖','💗'][Math.floor(Math.random()*4)];
        h.style.cssText=`left:${Math.random()*90}%;bottom:-30px;--size:${14+Math.random()*28}px;--op:0.7;--drift:${Math.random()*120-60}px;--spin:${Math.random()*360}deg;animation-duration:${6+Math.random()*10}s;font-size:var(--size);`;
        c.appendChild(h); setTimeout(()=>h.remove(),16000);
      },800);
    });
    document.querySelectorAll('.petals-container').forEach(c=>{
      setInterval(()=>{
        if(!c.isConnected) return;
        let p=document.createElement('span'); p.classList.add('petal');
        p.textContent=['🌹','💮','🌸'][Math.floor(Math.random()*3)];
        p.style.cssText=`left:${Math.random()*95}%;top:-30px;--size:${12+Math.random()*22}px;--drift:${Math.random()*150-75}px;--spin:${Math.random()*720}deg;animation-duration:${8+Math.random()*12}s;font-size:var(--size);`;
        c.appendChild(p); setTimeout(()=>p.remove(),20000);
      },1200);
    });
  }

  function startCounter() {
    const obs = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{ if(e.isIntersecting){ animateCounter(); obs.disconnect(); } });
    },{threshold:0.5});
    obs.observe(document.getElementById('love-counter'));
  }
  function animateCounter() {
    const target=999999999; const dur=4000; const start=performance.now();
    function upd(now){
      const p=Math.min((now-start)/dur,1); const val=Math.floor((1-Math.pow(1-p,4))*target);
      if(val>=target-1){ counterDisplay.textContent='∞'; return; }
      counterDisplay.textContent=val.toLocaleString()+'%';
      if(p<1) requestAnimationFrame(upd);
    }
    requestAnimationFrame(upd);
  }

  function initStars() {
    const c=document.getElementById('stars-container');
    for(let i=0;i<150;i++){
      let s=document.createElement('div'); s.classList.add('star-dot');
      s.style.cssText=`left:${Math.random()*100}%;top:${Math.random()*100}%;--sz:${1+Math.random()*3}px;--dur:${2+Math.random()*5}s;--delay:${Math.random()*6}s;`;
      c.appendChild(s);
    }
  }
  function initShootingStars() {
    const c=document.getElementById('stars-container');
    for(let i=0;i<6;i++){
      let ss=document.createElement('div'); ss.classList.add('shooting-star');
      ss.style.cssText=`left:${Math.random()*60}%;top:${Math.random()*40}%;--dur:${3+Math.random()*6}s;--delay:${Math.random()*10}s;`;
      c.appendChild(ss);
    }
  }
  function initFireflies() {
    const sec=document.getElementById('dream-section');
    for(let i=0;i<20;i++){
      let ff=document.createElement('div'); ff.classList.add('firefly');
      ff.style.cssText=`left:${Math.random()*90}%;top:${Math.random()*85}%;--dur:${4+Math.random()*8}s;--delay:${Math.random()*6}s;--mx:${Math.random()*80-40}px;--my:${Math.random()*80-40}px;`;
      sec.appendChild(ff);
    }
  }

  function setupNoButton() {
    function moveNo() {
      const btn = btnNo;
      const maxX = window.innerWidth - btn.offsetWidth - 20;
      const maxY = window.innerHeight - btn.offsetHeight - 20;
      btn.style.position = 'fixed';
      btn.style.left = Math.random()*maxX + 'px';
      btn.style.top = Math.random()*maxY + 'px';
      btn.style.zIndex = '99999';
    }
    btnNo.addEventListener('mouseenter', moveNo);
    btnNo.addEventListener('touchstart', (e) => { e.preventDefault(); moveNo(); });
    btnNo.addEventListener('click', (e) => {
      e.preventDefault();
      btnNo.style.transform='scale(0.3)'; btnNo.style.opacity='0.5';
      setTimeout(()=>{
        btnNo.style.transform='scale(1)'; btnNo.style.opacity='1';
        btnNo.textContent='YES 💕'; btnNo.style.background='linear-gradient(135deg,#c41e3a,#ff6b8a)';
        btnNo.style.color='#fff'; btnNo.style.border='none'; btnNo.style.boxShadow='0 8px 35px rgba(200,40,60,0.5)';
        btnNo.onclick = ()=> triggerCelebration();
      },400);
    });
  }

  btnYes.addEventListener('click', triggerCelebration);
  function triggerCelebration() {
    yesMessage.style.display='block';
    celebrationOverlay.classList.add('active');
    for(let i=0;i<200;i++){
      let p=document.createElement('div'); p.className='confetti-piece';
      p.style.cssText=`left:${Math.random()*100}%;top:-20px;background:${['#ff6b8a','#c41e3a','#ffd700'][Math.floor(Math.random()*3)]};width:${6+Math.random()*16}px;height:${6+Math.random()*16}px;animation-duration:${2+Math.random()*4}s;`;
      celebrationOverlay.appendChild(p); setTimeout(()=>p.remove(),6000);
    }
    for(let i=0;i<60;i++){
      let h=document.createElement('span'); h.textContent='❤️';
      h.style.cssText=`position:fixed;z-index:99986;left:${40+Math.random()*20}%;top:${30+Math.random()*30}%;font-size:${20+Math.random()*40}px;animation:celebHeart 2s ease-out forwards;`;
      document.body.appendChild(h); setTimeout(()=>h.remove(),3500);
    }
    setTimeout(()=> celebrationOverlay.classList.remove('active'), 5000);
    // No longer triggers ending scene automatically; it will be shown after reading the letter.
  }

  // Observe final letter to trigger ending scene
  function observeFinalLetter() {
    const letterSection = document.getElementById('final-letter');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting && entry.intersectionRatio > 0.7) {
          // User has read most of the letter, wait a bit then show ending
          setTimeout(() => {
            endingScene.classList.add('active');
            // Softly stop music after ending appears
            setTimeout(() => {
              musicPlaying = false;
              vinylRecord.classList.remove('playing');
              stopAmbient();
            }, 3000);
          }, 2000);
          observer.unobserve(letterSection);
        }
      });
    }, { threshold: 0.7 });
    observer.observe(letterSection);
  }

  // Close ending scene button
  closeEnding.addEventListener('click', () => {
    endingScene.classList.remove('active');
    // Optionally scroll back to final letter or top
    document.getElementById('final-letter').scrollIntoView({ behavior: 'smooth' });
  });

  // Easter egg A key
  document.addEventListener('keydown', (e) => {
    if(e.key.toLowerCase()==='a'){
      for(let i=0;i<150;i++){
        let h=document.createElement('span'); h.textContent=['❤️','💕','💖'][Math.floor(Math.random()*3)];
        h.style.cssText=`position:fixed;z-index:99999;left:${Math.random()*95}%;top:${Math.random()*90}%;font-size:${18+Math.random()*40}px;animation:easterEgg 4s ease-out forwards;`;
        document.body.appendChild(h); setTimeout(()=>h.remove(),5000);
      }
    }
  });

  // Cursor
  document.addEventListener('mousemove', (e)=>{
    customCursor.style.left=e.clientX+'px'; customCursor.style.top=e.clientY+'px';
    if(Math.random()<0.35){
      let t=document.createElement('span'); t.className='cursor-trail-heart'; t.textContent='❤️';
      t.style.left=e.clientX+'px'; t.style.top=e.clientY+'px';
      t.style.setProperty('--tx',(Math.random()*40-20)+'px');
      t.style.setProperty('--ty',(Math.random()*40-20)+'px');
      t.style.setProperty('--rot',(Math.random()*60-30)+'deg');
      cursorTrail.appendChild(t); setTimeout(()=>t.remove(),1300);
    }
  });
  document.addEventListener('touchmove', (e)=>{
    customCursor.style.left=e.touches[0].clientX+'px'; customCursor.style.top=e.touches[0].clientY+'px';
  });

})();
</script>
</body>
</html>
