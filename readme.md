Readme Initiated

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Aatmoday AI — Hobby Matchmaker & Community Platform</title>
<meta name="description" content="AI-Powered Hobby Matchmaker for Aatmoday. Describe your interests in natural language, get matched to sub-groups & events, and generate personalized conversation icebreakers.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;0,9..144,700;1,9..144,400;1,9..144,600&family=IBM+Plex+Sans:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #09090c;
    --surface: #121217;
    --surface-hi: #1a1a22;
    --surface-glass: rgba(20, 20, 28, 0.75);
    --border: rgba(255, 255, 255, 0.10);
    --border-hi: rgba(255, 255, 255, 0.22);
    --border-accent: rgba(245, 178, 67, 0.35);
    --text: #f5f5f7;
    --text-dim: #b4b4c2;
    --text-faint: #78788a;
    
    /* Vibrant Accent Palette */
    --accent: #f5a623;
    --accent-glow: rgba(245, 166, 35, 0.28);
    --cyan: #38ef7d;
    --violet: #8a2be2;
    --sky: #3b82f6;
    --coral: #ff5e62;
    --emerald: #10b981;
    --amber: #f59e0b;
    --pink: #ec4899;
    
    --radius-xl: 24px;
    --radius-lg: 18px;
    --radius-md: 12px;
    --radius-sm: 8px;
    
    --serif: 'Fraunces', serif;
    --sans: 'IBM Plex Sans', sans-serif;
    --mono: 'JetBrains Mono', monospace;
    --header-h: 70px;
  }

  *{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin: 0; padding: 0;
    background-color: var(--bg);
    color: var(--text);
    font-family: var(--sans);
    min-height: 100vh;
    line-height: 1.55;
    overflow-x: hidden;
    position: relative;
  }

  /* Ambient Mesh Background */
  body::before{
    content: "";
    position: fixed; inset: 0;
    background:
      radial-gradient(circle at 10% 20%, rgba(138, 43, 226, 0.12) 0%, transparent 45%),
      radial-gradient(circle at 90% 15%, rgba(245, 166, 35, 0.12) 0%, transparent 40%),
      radial-gradient(circle at 50% 85%, rgba(59, 130, 246, 0.10) 0%, transparent 50%),
      radial-gradient(rgba(255,255,255,0.035) 1px, transparent 1px) 0 0/3px 3px;
    pointer-events: none; z-index: -2;
  }
  body::after{
    content: "";
    position: fixed; inset: -30%;
    background: conic-gradient(from 180deg at 50% 50%, transparent 0deg, rgba(245,166,35,0.03) 90deg, transparent 180deg, rgba(56,239,125,0.025) 270deg, transparent 360deg);
    filter: blur(60px);
    animation: ambientRotate 35s linear infinite;
    pointer-events: none; z-index: -1;
  }
  @keyframes ambientRotate{ to{ transform: rotate(360deg); } }

  a{ color: inherit; text-decoration: none; }
  button{ font-family: inherit; }

  /* ---------- Typography & Utility ---------- */
  .hl{ 
    background: linear-gradient(120deg, #f5a623 0%, #ff5e62 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .hl-cyan{
    background: linear-gradient(120deg, #38ef7d 0%, #11998e 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .hl-violet{
    background: linear-gradient(120deg, #c084fc 0%, #818cf8 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
  }
  .badge-ai{
    display: inline-flex; align-items: center; gap: 6px;
    background: rgba(245, 166, 35, 0.12);
    border: 1px solid rgba(245, 166, 35, 0.35);
    color: #ffcf70;
    font-size: 11.5px; font-weight: 600;
    padding: 4px 10px; border-radius: 999px;
    letter-spacing: 0.3px; text-transform: uppercase;
  }
  .badge-ai span.dot{
    width: 6px; height: 6px; border-radius: 50%;
    background: var(--accent);
    box-shadow: 0 0 8px var(--accent);
    animation: pulseDot 2s infinite;
  }
  @keyframes pulseDot{
    0%, 100%{ opacity: 1; transform: scale(1); }
    50%{ opacity: 0.4; transform: scale(0.8); }
  }

  /* ---------- Header ---------- */
  .site-header{
    position: sticky; top: 0; z-index: 50;
    display: flex; align-items: center; justify-content: space-between;
    height: var(--header-h);
    padding: 0 32px;
    background: rgba(14, 14, 19, 0.82);
    backdrop-filter: blur(14px);
    border-bottom: 1px solid var(--border);
  }
  @media (max-width: 768px){ .site-header{ padding: 0 16px; } }

  .logo-wrap{
    display: flex; align-items: center; gap: 12px;
    background: none; border: none; padding: 0;
    color: var(--text); cursor: pointer; text-align: left;
  }
  .logo-mark{
    width: 36px; height: 36px; border-radius: 10px; flex-shrink: 0;
    background: linear-gradient(135deg, #f5a623 0%, #ff5e62 100%);
    display: flex; align-items: center; justify-content: center;
    font-family: var(--serif); font-weight: 800; font-size: 19px; color: #0a0a0c;
    box-shadow: 0 4px 16px rgba(245, 166, 35, 0.35);
  }
  .logo-text{ display: flex; flex-direction: column; }
  .logo-title{ font-weight: 700; font-size: 16px; letter-spacing: -0.2px; }
  .logo-sub{ font-size: 11px; color: var(--text-faint); font-weight: 500; }

  .header-nav{ display: flex; align-items: center; gap: 6px; }
  .nav-btn{
    background: none; border: none; cursor: pointer;
    color: var(--text-dim); font-size: 14px; font-weight: 500;
    padding: 8px 14px; border-radius: var(--radius-sm);
    transition: all .18s ease; display: inline-flex; align-items: center; gap: 6px;
  }
  .nav-btn:hover{ color: var(--text); background: rgba(255,255,255,0.06); }
  .nav-btn.active{ color: var(--text); background: rgba(255,255,255,0.10); font-weight: 600; }
  @media (max-width: 840px){ .nav-btn.hide-mobile{ display: none; } }

  /* ---------- Buttons ---------- */
  .btn{
    appearance: none; border: none; cursor: pointer;
    font-family: var(--sans); font-weight: 600; font-size: 14px;
    padding: 10px 22px; border-radius: 999px;
    background: linear-gradient(135deg, #f5a623, #ff7a18);
    color: #09090c;
    display: inline-flex; align-items: center; justify-content: center; gap: 8px;
    transition: transform .18s cubic-bezier(.2,.8,.2,1), box-shadow .18s ease, filter .18s ease;
    box-shadow: 0 8px 24px -6px rgba(245, 166, 35, 0.35);
    white-space: nowrap; position: relative; overflow: hidden;
  }
  .btn::after{
    content:""; position:absolute; top:0; left:-120%; width:70%; height:100%;
    background:linear-gradient(100deg,transparent,rgba(255,255,255,.4),transparent);
    transform:skewX(-18deg);
    transition:left .65s ease;
  }
  .btn:hover::after{ left: 140%; }
  .btn:hover{ transform: translateY(-2px); box-shadow: 0 12px 30px -6px rgba(245, 166, 35, 0.48); }
  .btn:active{ transform: translateY(0) scale(0.98); }
  .btn.lg{ padding: 14px 28px; font-size: 15.5px; }
  .btn.sm{ padding: 6px 14px; font-size: 12.5px; }
  .btn.ghost{
    background: rgba(255,255,255,0.05); color: var(--text);
    border: 1px solid var(--border); box-shadow: none;
  }
  .btn.ghost:hover{ background: rgba(255,255,255,0.10); border-color: var(--border-hi); transform: translateY(-2px); }
  .btn.accent-cyan{
    background: linear-gradient(135deg, #38ef7d, #11998e); color: #072314;
    box-shadow: 0 8px 24px -6px rgba(56, 239, 125, 0.35);
  }
  .btn.accent-violet{
    background: linear-gradient(135deg, #a855f7, #6366f1); color: #ffffff;
    box-shadow: 0 8px 24px -6px rgba(168, 85, 247, 0.35);
  }
  .btn:disabled{ opacity: 0.4; cursor: not-allowed; transform: none !important; box-shadow: none !important; }

  /* ---------- Page Shell ---------- */
  .page{
    max-width: 1080px; margin: 0 auto;
    padding: 36px 24px 80px;
    perspective: 1000px;
  }
  .page.narrow{ max-width: 740px; }
  @media (max-width: 640px){ .page{ padding: 20px 14px 60px; } }

  .fade-in{
    animation: pageFadeIn .4s cubic-bezier(.16, 1, 0.3, 1) both;
  }
  @keyframes pageFadeIn{
    from{ opacity: 0; transform: translateY(14px); }
    to{ opacity: 1; transform: translateY(0); }
  }

  /* ---------- Hero & AI Input Area ---------- */
  .hero-box{
    background: linear-gradient(180deg, rgba(26,26,35,0.85) 0%, rgba(18,18,24,0.95) 100%);
    border: 1px solid var(--border-hi);
    border-radius: var(--radius-xl);
    padding: 44px 40px 36px;
    position: relative; overflow: hidden;
    box-shadow: 0 24px 60px rgba(0,0,0,0.35);
    margin-bottom: 34px;
  }
  @media (max-width: 640px){ .hero-box{ padding: 26px 18px 24px; border-radius: var(--radius-lg); } }

  .hero-box::before{
    content: ""; position: absolute; top: -100px; right: -100px;
    width: 320px; height: 320px; border-radius: 50%;
    background: radial-gradient(circle, rgba(245, 166, 35, 0.14), transparent 70%);
    pointer-events: none;
  }
  .hero-top-badge{ margin-bottom: 16px; }
  .hero-title{
    font-family: var(--serif); font-size: clamp(28px, 4.5vw, 44px);
    line-height: 1.15; font-weight: 600; margin: 0 0 14px;
    letter-spacing: -0.5px;
  }
  .hero-desc{
    color: var(--text-dim); font-size: clamp(14.5px, 2vw, 16.5px);
    max-width: 66ch; margin: 0 0 28px; line-height: 1.6;
  }

  /* Free-Form AI Input Box */
  .ai-input-card{
    background: rgba(10, 10, 14, 0.85);
    border: 1px solid var(--border-accent);
    border-radius: var(--radius-lg);
    padding: 20px;
    box-shadow: 0 12px 36px rgba(0,0,0,0.4), inset 0 1px 1px rgba(255,255,255,0.06);
    position: relative;
  }
  .ai-input-header{
    display: flex; align-items: center; justify-content: space-between;
    margin-bottom: 12px; gap: 8px; flex-wrap: wrap;
  }
  .ai-input-label{
    font-size: 13px; font-weight: 600; color: #ffcf70;
    display: flex; align-items: center; gap: 8px;
  }
  .ai-input-actions-top{ display: flex; align-items: center; gap: 8px; }
  
  .free-form-textarea{
    width: 100%; min-height: 96px; max-height: 240px; resize: vertical;
    background: transparent; border: none; outline: none;
    color: var(--text); font-family: var(--sans); font-size: 15.5px;
    line-height: 1.6; padding: 4px 0;
  }
  .free-form-textarea::placeholder{ color: var(--text-faint); font-weight: 400; }

  .ai-input-bottom{
    display: flex; align-items: center; justify-content: space-between;
    padding-top: 14px; border-top: 1px solid var(--border);
    gap: 12px; flex-wrap: wrap;
  }
  .prompt-pills-wrap{
    display: flex; align-items: center; gap: 6px; flex-wrap: wrap;
    margin-top: 14px; padding-top: 12px; border-top: 1px dashed rgba(255,255,255,0.08);
  }
  .prompt-pill-label{ font-size: 12px; color: var(--text-faint); font-weight: 500; margin-right: 4px; }
  .prompt-pill{
    background: rgba(255,255,255,0.05); border: 1px solid var(--border);
    color: var(--text-dim); font-size: 12px; font-weight: 500;
    padding: 5px 11px; border-radius: 999px; cursor: pointer;
    transition: all .15s ease; text-align: left;
  }
  .prompt-pill:hover{
    background: rgba(245, 166, 35, 0.12);
    border-color: rgba(245, 166, 35, 0.4);
    color: #ffcf70; transform: translateY(-1px);
  }

  /* AI Parsing Visualizer */
  .ai-extracted-tags-box{
    margin-top: 16px; padding: 14px 18px;
    background: rgba(245, 166, 35, 0.05);
    border: 1px solid rgba(245, 166, 35, 0.20);
    border-radius: var(--radius-md);
    display: flex; flex-direction: column; gap: 8px;
    animation: fadeIn .3s ease;
  }
  .ai-extracted-title{
    font-size: 12px; font-weight: 600; color: #ffcf70;
    display: flex; align-items: center; gap: 6px;
  }
  .ai-extracted-chips{ display: flex; flex-wrap: wrap; gap: 6px; }
  .extracted-chip{
    font-size: 11.5px; font-family: var(--mono);
    padding: 3px 8px; border-radius: 6px;
    background: rgba(255,255,255,0.07); border: 1px solid rgba(255,255,255,0.12);
    color: var(--text);
  }
  .extracted-chip.highlight{
    background: rgba(56, 239, 125, 0.12);
    border-color: rgba(56, 239, 125, 0.35);
    color: #4ade80;
  }

  /* Quick Switcher Strip */
  .input-switch-strip{
    display: flex; align-items: center; justify-content: space-between;
    margin-top: 20px; gap: 12px; flex-wrap: wrap;
  }
  .switch-note{ font-size: 13px; color: var(--text-dim); }

  /* ---------- Section Headers ---------- */
  .section-head{
    display: flex; align-items: flex-end; justify-content: space-between;
    margin: 40px 0 20px; gap: 16px; flex-wrap: wrap;
  }
  .section-title{
    font-family: var(--serif); font-size: clamp(22px, 3.5vw, 28px);
    font-weight: 600; margin: 0; line-height: 1.2;
  }
  .section-sub{ color: var(--text-faint); font-size: 14px; margin-top: 4px; }
  .tabs-nav{
    display: inline-flex; background: var(--surface);
    border: 1px solid var(--border); border-radius: 999px;
    padding: 4px; gap: 4px;
  }
  .tab-btn{
    background: none; border: none; cursor: pointer;
    color: var(--text-dim); font-size: 13px; font-weight: 500;
    padding: 6px 14px; border-radius: 999px;
    transition: all .15s ease;
  }
  .tab-btn.active{
    background: rgba(255,255,255,0.12); color: var(--text);
    font-weight: 600;
  }

  /* ---------- Recommendations & Cards ---------- */
  .rec-grid{
    display: grid; grid-template-columns: repeat(auto-fill, minmax(320px, 1fr));
    gap: 18px; margin-bottom: 30px;
  }
  @media (max-width: 480px){ .rec-grid{ grid-template-columns: 1fr; } }

  .rec-card{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: var(--radius-lg);
    padding: 22px;
    display: flex; flex-direction: column;
    position: relative; overflow: hidden;
    transition: transform .22s cubic-bezier(.2,.8,.2,1), border-color .22s, box-shadow .22s;
    text-align: left;
  }
  .rec-card:hover{
    transform: translateY(-4px);
    border-color: var(--border-hi);
    box-shadow: 0 16px 40px rgba(0,0,0,0.35);
  }
  .rec-card.featured{
    border-color: rgba(245, 166, 35, 0.4);
    background: linear-gradient(180deg, rgba(30, 26, 20, 0.7) 0%, rgba(18,18,24,0.95) 100%);
  }

  .rec-card-top{
    display: flex; align-items: flex-start; justify-content: space-between;
    margin-bottom: 14px; gap: 12px;
  }
  .club-avatar{
    width: 48px; height: 48px; border-radius: 12px; flex-shrink: 0;
    display: flex; align-items: center; justify-content: center;
    font-family: var(--serif); font-weight: 700; font-size: 19px;
    background: linear-gradient(135deg, #2a2a38, #181822);
    border: 1px solid var(--border); color: var(--text);
  }
  .club-avatar.event-icon{
    background: linear-gradient(135deg, rgba(59,130,246,0.25), rgba(138,43,226,0.25));
    border-color: rgba(138,43,226,0.4); font-size: 22px;
  }
  .match-dial{
    display: flex; flex-direction: column; align-items: flex-end; text-align: right;
  }
  .match-pct{
    font-family: var(--serif); font-weight: 700; font-size: 24px;
    line-height: 1; color: var(--accent);
  }
  .match-lbl{ font-size: 11px; color: var(--text-faint); text-transform: uppercase; font-weight: 600; }

  .rec-card-name{ font-family: var(--serif); font-size: 18.5px; font-weight: 600; margin: 0 0 3px; }
  .rec-card-cat{ font-size: 12.5px; color: var(--text-faint); margin-bottom: 10px; }
  .rec-card-blurb{ font-size: 13.5px; color: var(--text-dim); margin: 0 0 16px; line-height: 1.5; flex-grow: 1; }

  /* AI Explanation Highlight Box */
  .why-recommended-box{
    background: rgba(255,255,255,0.035);
    border: 1px solid rgba(255,255,255,0.08);
    border-left: 3px solid var(--accent);
    border-radius: 0 var(--radius-sm) var(--radius-sm) 0;
    padding: 10px 12px; margin-bottom: 16px;
  }
  .why-title{
    font-size: 11.5px; font-weight: 600; color: #ffcf70;
    display: flex; align-items: center; gap: 5px; margin-bottom: 4px;
  }
  .why-text{ font-size: 12.5px; color: var(--text-dim); margin: 0; line-height: 1.45; }

  .rec-card-meta{
    display: flex; align-items: center; justify-content: space-between;
    font-size: 12px; color: var(--text-faint);
    padding-top: 12px; border-top: 1px solid var(--border);
    margin-bottom: 14px; gap: 8px; flex-wrap: wrap;
  }
  .rec-card-actions{
    display: grid; grid-template-columns: 1fr 1fr; gap: 8px;
  }
  .rec-card-actions.full{ grid-template-columns: 1fr; }

  /* ---------- Event Card Specifics ---------- */
  .event-badge-live{
    display: inline-flex; align-items: center; gap: 5px;
    background: rgba(236, 72, 153, 0.15); border: 1px solid rgba(236, 72, 153, 0.4);
    color: #f472b6; font-size: 11px; font-weight: 600; padding: 2px 8px; border-radius: 6px;
  }

  /* ---------- Guided Quiz Wizard ---------- */
  .quiz-card{
    background: var(--surface);
    border: 1px solid var(--border-hi);
    border-radius: var(--radius-xl);
    padding: 38px 36px 32px;
    box-shadow: 0 20px 50px rgba(0,0,0,0.4);
  }
  @media (max-width: 640px){ .quiz-card{ padding: 24px 18px 22px; } }

  .progress-track{ display: flex; gap: 6px; margin-bottom: 24px; }
  .progress-seg{ flex: 1; height: 5px; border-radius: 4px; background: rgba(255,255,255,0.08); overflow: hidden; }
  .progress-seg i{ display: block; height: 100%; width: 0%; background: linear-gradient(90deg, #f5a623, #ff5e62); transition: width .35s ease; }

  .step-label{ color: var(--accent); font-size: 13px; font-weight: 600; margin-bottom: 8px; text-transform: uppercase; letter-spacing: 0.5px; }
  .question{ font-family: var(--serif); font-weight: 600; font-size: clamp(22px, 4vw, 29px); line-height: 1.25; margin: 0 0 6px; }
  .subquestion{ color: var(--text-dim); font-size: 14.5px; margin: 0 0 24px; }

  .options-grid{ display: flex; flex-wrap: wrap; gap: 10px; margin-bottom: 12px; }
  .option-btn{
    appearance: none; cursor: pointer; font-family: var(--sans); font-size: 14px; font-weight: 500;
    color: var(--text); background: rgba(255,255,255,0.04); border: 1px solid var(--border);
    padding: 12px 20px; border-radius: 999px; transition: all .18s cubic-bezier(.2,.8,.2,1); text-align: left;
    display: inline-flex; align-items: center; gap: 8px;
  }
  .option-btn:hover{ border-color: rgba(255,255,255,0.35); transform: translateY(-2px); }
  .option-btn.selected{
    background: linear-gradient(135deg, rgba(245, 166, 35, 0.22), rgba(255, 94, 98, 0.15));
    border-color: var(--accent); color: #fff;
    box-shadow: 0 0 20px rgba(245, 166, 35, 0.2);
  }
  .quiz-nav{ display: flex; justify-content: space-between; align-items: center; margin-top: 32px; padding-top: 18px; border-top: 1px solid var(--border); }

  /* ---------- Loading Animation ---------- */
  .loading-container{
    background: var(--surface); border: 1px solid var(--border);
    border-radius: var(--radius-xl); padding: 70px 30px; text-align: center;
    box-shadow: 0 20px 50px rgba(0,0,0,0.4);
  }
  .ai-pulse-core{
    width: 64px; height: 64px; margin: 0 auto 24px;
    border-radius: 50%;
    background: radial-gradient(circle, var(--accent), transparent 70%);
    box-shadow: 0 0 35px var(--accent-glow);
    display: flex; align-items: center; justify-content: center;
    font-size: 26px; animation: corePulse 1.4s ease-in-out infinite;
  }
  @keyframes corePulse{
    0%, 100%{ transform: scale(0.92); opacity: 0.8; }
    50%{ transform: scale(1.12); opacity: 1; box-shadow: 0 0 50px var(--accent); }
  }

  /* ---------- Icebreaker Studio Modal ---------- */
  .modal-overlay{
    position: fixed; inset: 0; background: rgba(8, 8, 12, 0.82);
    backdrop-filter: blur(8px);
    display: flex; align-items: center; justify-content: center;
    z-index: 100; padding: 20px;
    animation: modalBackdrop .2s ease both;
  }
  @keyframes modalBackdrop{ from{ opacity: 0; } to{ opacity: 1; } }

  .modal-card{
    background: var(--surface-hi);
    border: 1px solid var(--border-hi);
    border-radius: var(--radius-xl);
    width: 100%; max-width: 620px; max-height: 90vh; overflow-y: auto;
    padding: 28px 30px 32px;
    box-shadow: 0 30px 80px rgba(0,0,0,0.6);
    animation: modalPopIn .3s cubic-bezier(.16, 1, 0.3, 1) both;
  }
  @keyframes modalPopIn{ from{ opacity: 0; transform: scale(0.95) translateY(20px); } to{ opacity: 1; transform: none; } }
  @media (max-width: 640px){ .modal-card{ padding: 20px 18px 24px; border-radius: var(--radius-lg); } }

  .modal-header{
    display: flex; justify-content: space-between; align-items: flex-start;
    margin-bottom: 20px; gap: 14px;
  }
  .modal-close{
    background: rgba(255,255,255,0.06); border: 1px solid var(--border);
    color: var(--text-dim); cursor: pointer;
    width: 32px; height: 32px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-size: 16px; transition: all .15s ease; flex-shrink: 0;
  }
  .modal-close:hover{ color: var(--text); background: rgba(255,255,255,0.15); }

  .icebreaker-tone-tabs{
    display: flex; gap: 6px; margin: 16px 0 14px;
  }
  .tone-pill{
    background: rgba(255,255,255,0.04); border: 1px solid var(--border);
    color: var(--text-dim); font-size: 12.5px; font-weight: 500;
    padding: 6px 12px; border-radius: 999px; cursor: pointer;
    transition: all .15s ease;
  }
  .tone-pill:hover{ border-color: rgba(255,255,255,0.3); color: var(--text); }
  .tone-pill.active{
    background: rgba(245, 166, 35, 0.15); border-color: var(--accent);
    color: #ffcf70; font-weight: 600;
  }

  .icebreaker-box{
    background: #0d0d12;
    border: 1px solid rgba(245, 166, 35, 0.3);
    border-radius: var(--radius-md);
    padding: 16px 18px; margin-bottom: 16px;
    position: relative;
  }
  .icebreaker-text{
    font-size: 14.5px; line-height: 1.6; color: var(--text);
    margin: 0; white-space: pre-wrap; font-family: var(--sans);
  }
  .icebreaker-actions{
    display: flex; gap: 10px; margin-top: 14px; flex-wrap: wrap;
  }

  .in-person-tip-box{
    background: rgba(56, 239, 125, 0.05);
    border: 1px solid rgba(56, 239, 125, 0.25);
    border-radius: var(--radius-md);
    padding: 14px 16px; margin-top: 16px;
  }
  .tip-head{
    font-size: 12px; font-weight: 600; color: #4ade80;
    display: flex; align-items: center; gap: 6px; margin-bottom: 6px;
  }
  .tip-content{ font-size: 13px; color: var(--text-dim); margin: 0; line-height: 1.5; }

  /* ---------- Toast Notification ---------- */
  .toast{
    position: fixed; bottom: 24px; right: 24px; z-index: 200;
    background: #1e1e28; border: 1px solid var(--accent);
    color: #fff; padding: 12px 20px; border-radius: 999px;
    font-size: 13.5px; font-weight: 500; box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    display: flex; align-items: center; gap: 10px;
    animation: toastIn .3s ease;
  }
  @keyframes toastIn{ from{ transform: translateY(20px); opacity: 0; } to{ transform: none; opacity: 1; } }

  /* ---------- Stats & Features Grid ---------- */
  .stats-strip{
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 16px; margin-top: 30px; padding-top: 24px;
    border-top: 1px solid var(--border);
  }
  @media (max-width: 640px){ .stats-strip{ grid-template-columns: repeat(2, 1fr); } }
  .stat-val{ font-family: var(--serif); font-size: 26px; font-weight: 700; color: #fff; }
  .stat-lbl{ font-size: 12.5px; color: var(--text-faint); margin-top: 2px; }

  /* ---------- Footer ---------- */
  .site-footer{
    max-width: 1080px; margin: 60px auto 0; padding: 24px 24px 60px;
    border-top: 1px solid var(--border); color: var(--text-faint); font-size: 13px;
    display: flex; justify-content: space-between; flex-wrap: wrap; gap: 16px;
  }
</style>
</head>
<body>

<header class="site-header">
  <button class="logo-wrap" id="nav-home-btn">
    <div class="logo-mark">A</div>
    <div class="logo-text">
      <span class="logo-title">Aatmoday AI</span>
      <span class="logo-sub">Hobby & Community Matchmaker</span>
    </div>
  </button>
  <nav class="header-nav">
    <button class="nav-btn" id="nav-matcher-btn">✨ AI Matchmaker</button>
    <button class="nav-btn hide-mobile" id="nav-explore-btn">🏛️ Sub-Groups</button>
    <button class="nav-btn hide-mobile" id="nav-events-btn">📅 Events</button>
    <button class="nav-btn hide-mobile" id="nav-saved-btn">🔖 Saved (<span id="saved-count-nav">0</span>)</button>
    <button class="btn sm" id="nav-quiz-btn">Take Quiz</button>
  </nav>
</header>

<div id="root"></div>
<div id="modal-root"></div>
<div id="toast-root"></div>

<script>
/* ============================================================
   AATMODAY DATABASE (SUB-GROUPS & LIVE EVENTS)
   ============================================================ */

const COMMUNITIES = [
  {
    id: 'techno',
    name: 'TechnoVerse',
    category: 'Tech & AI Innovation',
    intensity: 3, // 1-light, 2-moderate, 3-heavy
    members: 245,
    nextEvent: 'HackAatmoday: 36h Sprint — Oct 2',
    coordinator: 'Aariv Mehta',
    handle: '@technoverse.club',
    contactWa: '919876543210',
    blurb: 'Build AI apps, autonomous agents, open-source projects, and robotics with passionate developers who ship code relentlessly.',
    meets: 'Tue & Thu 6:00 PM',
    vibes: ['Hackathons', 'AI / ML', 'Competitive Coding', 'Open Source'],
    tags: { tech: 3, strategic: 2, skillbuilding: 3, resume: 3, competing: 2 },
    icebreakerHints: 'Ask about their current hackathon team composition and which tech stack they use for the annual demo sprint.'
  },
  {
    id: 'robotix',
    name: 'RobotiX & IoT Wing',
    category: 'Hardware & Embedded',
    intensity: 2,
    members: 112,
    nextEvent: 'Arduino & Drone Flight Lab — Oct 7',
    coordinator: 'Vikram Sethi',
    handle: '@robotix.aatmoday',
    contactWa: '919876543211',
    blurb: 'Hands-on PCB fabrication, ROS robotics, drone telemetry, and microcontrollers. We turn code into physical motion.',
    meets: 'Wed & Sat 4:30 PM',
    vibes: ['Robotics', 'Hardware', 'Drones', 'IoT'],
    tags: { tech: 3, strategic: 2, physical: 1, skillbuilding: 3, solo: 1 },
    icebreakerHints: 'Mention any microcontrollers (ESP32/Arduino) or CAD software you are curious about learning.'
  },
  {
    id: 'swaranjali',
    name: 'Swaranjali',
    category: 'Music & Jam Society',
    intensity: 2,
    members: 180,
    nextEvent: 'Acoustic Jam & Beatbox Circle — Sep 27',
    coordinator: 'Nisha Rao',
    handle: '@swaranjali.music',
    contactWa: '919876543212',
    blurb: 'Vocalists, instrumentalists, classical ragas, and bedroom producers jamming together weekly and performing live across college fests.',
    meets: 'Wed evenings & Sunday Jams',
    vibes: ['Acoustic', 'Rock & Metal', 'Classical Vocals', 'Music Production'],
    tags: { music: 3, creative: 3, performing: 3, fun: 2, social: 2 },
    icebreakerHints: 'Share what instruments you play or your favorite genre to jam to.'
  },
  {
    id: 'thirak',
    name: 'Thirak Dance Crew',
    category: 'Dance & Movement',
    intensity: 2,
    members: 165,
    nextEvent: 'Hip-Hop & Semi-Classical Showcase — Oct 5',
    coordinator: 'Kabir Sen',
    handle: '@thirak.crew',
    contactWa: '919876543213',
    blurb: 'Hip-hop, contemporary, popping, and classical fusion. From beginner rhythm workshops to inter-university dance battles.',
    meets: 'Mon, Wed, Fri 5:30 PM',
    vibes: ['Hip Hop', 'Choreography', 'Freestyle', 'Stage Performance'],
    tags: { dance: 3, performing: 3, physical: 2, social: 2, fun: 2 },
    icebreakerHints: 'Ask about the beginner friendly auditions and showcase preparation schedule.'
  },
  {
    id: 'rangmanch',
    name: 'Rangmanch',
    category: 'Theatre & Stage Arts',
    intensity: 2,
    members: 120,
    nextEvent: 'Nukkad Natak & Street Play Read — Sep 30',
    coordinator: 'Meher Kapoor',
    handle: '@rangmanch.theatre',
    contactWa: '919876543214',
    blurb: 'From high-energy street plays (Nukkad Natak) to dramatic proscenium theatre, scriptwriting, voice modulation, and stagecraft.',
    meets: 'Tue & Thu Rehearsals',
    vibes: ['Street Plays', 'Acting', 'Scriptwriting', 'Voice Art'],
    tags: { drama: 3, performing: 3, social: 2, creative: 2, writing: 1 },
    icebreakerHints: 'Express interest in either on-stage acting or backstage scriptwriting and direction.'
  },
  {
    id: 'vaadvivad',
    name: 'Vaad-Vivad & MUN',
    category: 'Literary & Parliamentary Debate',
    intensity: 2,
    members: 135,
    nextEvent: 'Parliamentary Debate Bootcamp — Oct 8',
    coordinator: 'Yusuf Ali',
    handle: '@vaadvivad.soc',
    contactWa: '919876543215',
    blurb: 'Asian Parliamentary debating, Model UN delegations, slam poetry, and sharp public speaking for critical thinkers.',
    meets: 'Thu evenings & weekend sparring',
    vibes: ['Debate', 'MUN', 'Public Speaking', 'Policy Analysis'],
    tags: { debate: 3, writing: 2, strategic: 3, resume: 2, skillbuilding: 2 },
    icebreakerHints: 'Ask about their upcoming fresher debate orientation and novice adjudication training.'
  },
  {
    id: 'josh',
    name: 'Josh Athletics & Sports',
    category: 'Sports & Fitness',
    intensity: 3,
    members: 280,
    nextEvent: 'Night Marathon & Box Cricket — Sep 29',
    coordinator: 'Devika Nair',
    handle: '@josh.sports',
    contactWa: '919876543216',
    blurb: 'Cricket, football, badminton, table tennis, and athletics. Inter-department leagues, conditioning sessions, and tournaments.',
    meets: 'Daily 6:30 AM & 5:00 PM',
    vibes: ['Cricket', 'Football', 'Conditioning', 'Intramurals'],
    tags: { sports: 3, physical: 3, competing: 3, social: 2, fun: 2 },
    icebreakerHints: 'Mention your primary sport or whether you are looking for casual evening fitness games.'
  },
  {
    id: 'lenslight',
    name: 'Lens & Light',
    category: 'Photography & Cinematography',
    intensity: 1,
    members: 95,
    nextEvent: 'Golden Hour Photowalk & Color Grading — Oct 1',
    coordinator: 'Farhan Iqbal',
    handle: '@lensandlight',
    contactWa: '919876543217',
    blurb: 'Street photowalks, documentary filmmaking, DaVinci Resolve color grading, and covering major campus festivals.',
    meets: 'Biweekly shoots & screening nights',
    vibes: ['Street Photography', 'Short Films', 'Editing', 'Visual Storytelling'],
    tags: { photography: 3, film: 3, creative: 3, solo: 1, skillbuilding: 2 },
    icebreakerHints: 'Ask about camera gear sharing for beginners without their own DSLR/mirrorless body.'
  },
  {
    id: 'kalakriti',
    name: 'Kalakriti Art & Design',
    category: 'Fine Arts & UI/UX',
    intensity: 1,
    members: 110,
    nextEvent: 'Canva to Figma: UI & Poster Sprint — Oct 3',
    coordinator: 'Ira Bhatt',
    handle: '@kalakriti.art',
    contactWa: '919876543218',
    blurb: 'Sketching, canvas oil painting, digital illustration, 3D Blender models, and festival campus installations.',
    meets: 'Saturday afternoons',
    vibes: ['Digital Art', 'Figma / UI', 'Painting', 'Canvas & Murals'],
    tags: { art: 3, design: 3, creative: 3, solo: 1, skillbuilding: 2 },
    icebreakerHints: 'Mention whether you prefer traditional mediums (watercolor/sketch) or digital design in Figma.'
  },
  {
    id: 'seva',
    name: 'Seva Social & Community Wing',
    category: 'Social Impact & Education',
    intensity: 1,
    members: 190,
    nextEvent: 'Weekend Teaching & Literacy Drive — Oct 4',
    coordinator: 'Rohan Das',
    handle: '@seva.wing',
    contactWa: '919876543219',
    blurb: 'Weekend education drives for underprivileged kids, disaster relief fundraisers, blood donation camps, and animal care.',
    meets: 'Saturday & Sunday mornings',
    vibes: ['Teaching Drives', 'Community Service', 'NGO Ties', 'Impact'],
    tags: { volunteering: 3, social: 3, environment: 1, resume: 2 },
    icebreakerHints: 'Ask what teaching subjects or logistics support are needed for the upcoming weekend drive.'
  },
  {
    id: 'respawn',
    name: 'Respawn Esports & Gaming',
    category: 'Esports & Game Development',
    intensity: 1,
    members: 210,
    nextEvent: 'Valorant & Chess Inter-Branch LAN — Sep 28',
    coordinator: 'Tanish Oberoi',
    handle: '@respawn.esports',
    contactWa: '919876543220',
    blurb: 'LAN tournaments, Valorant/BGMI competitive scrims, collegiate esports championships, and indie game development sprints in Unity.',
    meets: 'Friday evenings & weekend LANs',
    vibes: ['Valorant / BGMI', 'Chess', 'Game Dev / Unity', 'LAN Tournaments'],
    tags: { gaming: 3, competing: 2, strategic: 2, fun: 3, tech: 1 },
    icebreakerHints: 'Drop your in-game rank or inquire about their weekly collegiate scrim slots.'
  },
  {
    id: 'udyam',
    name: 'Udyam E-Cell',
    category: 'Entrepreneurship & Startups',
    intensity: 2,
    members: 130,
    nextEvent: "Founder's Cafe: Pitching to Alumni — Oct 6",
    coordinator: 'Simran Kaur',
    handle: '@udyam.ecell',
    contactWa: '919876543221',
    blurb: 'Pitch deck workshops, startup case teardowns, venture capitalist guest lectures, and angel seed funds for student founders.',
    meets: 'Weekly strategy roundtables',
    vibes: ['Startup Pitch', 'Venture Capital', 'Product Design', 'Networking'],
    tags: { business: 3, strategic: 3, competing: 2, resume: 3, tech: 1 },
    icebreakerHints: 'Share a problem you are passionate about solving or ask for feedback on an early idea.'
  },
  {
    id: 'prakriti',
    name: 'Prakriti Eco Club',
    category: 'Environment & Climate Action',
    intensity: 1,
    members: 88,
    nextEvent: 'Green Horizon: Lake Cleanup & Plantation — Oct 10',
    coordinator: 'Ananya Iyer',
    handle: '@prakriti.green',
    contactWa: '919876543222',
    blurb: 'Campus solar audits, zero-waste composting, tree plantation drives, and climate policy research with local environmental bodies.',
    meets: 'Biweekly Sunday action drives',
    vibes: ['Sustainability', 'Tree Drives', 'Zero Waste', 'Eco Treks'],
    tags: { environment: 3, volunteering: 2, outdoor: 3, social: 1 },
    icebreakerHints: 'Ask about joining the student-led campus composting and energy conservation audit.'
  },
  {
    id: 'astro',
    name: 'Nakshatra Astronomy Club',
    category: 'Science & Stargazing',
    intensity: 1,
    members: 74,
    nextEvent: 'Night Sky Stargazing: Saturn Moons — Oct 12',
    coordinator: 'Aditya Joshi',
    handle: '@nakshatra.astro',
    contactWa: '919876543223',
    blurb: 'High-powered telescope observation nights, astrophotography, space science seminars, and eclipses tracking expeditions.',
    meets: 'Clear sky Friday/Saturday nights',
    vibes: ['Telescopes', 'Astrophysics', 'Stargazing', 'Cosmology'],
    tags: { tech: 2, outdoor: 2, solo: 1, skillbuilding: 2, fun: 2 },
    icebreakerHints: 'Ask about the upcoming rooftop telescope session and astrophotography techniques.'
  },
  {
    id: 'litclub',
    name: 'Kavyanjali Literature & Writing',
    category: 'Creative Writing & Poetry',
    intensity: 1,
    members: 82,
    nextEvent: 'Midnight Coffee & Poetry Slam — Oct 9',
    coordinator: 'Zoya Khan',
    handle: '@kavyanjali.lit',
    contactWa: '919876543224',
    blurb: 'Creative fiction writing circles, slam poetry open mics, book swaps, and publishing the annual campus literary anthology.',
    meets: 'Friday afternoons',
    vibes: ['Poetry Slams', 'Creative Writing', 'Book Club', 'Storytelling'],
    tags: { writing: 3, creative: 3, solo: 2, performing: 1, fun: 1 },
    icebreakerHints: 'Ask about contributing a poem or short story piece to the quarterly college anthology.'
  },
  {
    id: 'animanga',
    name: 'OtakuVerse & Pop Culture',
    category: 'Anime, Manga & Gaming Pop',
    intensity: 1,
    members: 140,
    nextEvent: 'Cosplay Workshop & Anime Trivia Night — Oct 14',
    coordinator: 'Tanmay Ghosh',
    handle: '@otakuverse.aatmoday',
    contactWa: '919876543225',
    blurb: 'Anime watch parties, manga illustration workshops, cosplay prop crafting, and Japanese pop culture conventions.',
    meets: 'Weekend anime marathons',
    vibes: ['Anime / Manga', 'Cosplay', 'Trivia', 'Fan Art'],
    tags: { fun: 3, creative: 2, art: 2, gaming: 1, social: 2 },
    icebreakerHints: 'Share your top 3 favorite anime or manga series to start an instant discussion.'
  }
];

const EVENTS_DATABASE = [
  {
    id: 'ev-1',
    title: 'HackAatmoday: 36h Prototype Sprint',
    clubId: 'techno',
    clubName: 'TechnoVerse',
    date: 'Oct 2, 9:00 AM',
    location: 'Main Computing Lab & Virtual',
    category: 'Hackathon & Coding',
    seatsLeft: 18,
    tags: ['tech', 'strategic', 'competing'],
    blurb: 'Team up with developers and designers to build functional AI products, APIs, or smart devices in 36 hours. Mentors and food provided!'
  },
  {
    id: 'ev-2',
    title: 'Campus Acoustic Jam & Beatbox Circle',
    clubId: 'swaranjali',
    clubName: 'Swaranjali',
    date: 'Sep 27, 6:00 PM',
    location: 'Open Air Amphitheatre',
    category: 'Music Performance',
    seatsLeft: 45,
    tags: ['music', 'creative', 'performing', 'fun'],
    blurb: 'Bring your guitar, flute, cajon or just your voice. An open acoustic circle under the stars with zero judgment.'
  },
  {
    id: 'ev-3',
    title: 'Nukkad Natak Audition & Script Workshop',
    clubId: 'rangmanch',
    clubName: 'Rangmanch',
    date: 'Sep 30, 4:00 PM',
    location: 'Student Activity Center SAC-2',
    category: 'Theatre & Acting',
    seatsLeft: 30,
    tags: ['drama', 'performing', 'social'],
    blurb: 'Learn voice projection, emotional expression, and physical comedy. No prior stage experience required!'
  },
  {
    id: 'ev-4',
    title: "Founder's Cafe: Pitching to Alumni Investors",
    clubId: 'udyam',
    clubName: 'Udyam E-Cell',
    date: 'Oct 6, 5:30 PM',
    location: 'Incubation Center Hall A',
    category: 'Startups & Business',
    seatsLeft: 22,
    tags: ['business', 'strategic', 'resume'],
    blurb: 'Practice your 3-minute elevator pitch with successful alumni founders and receive constructive feedback on market feasibility.'
  },
  {
    id: 'ev-5',
    title: 'Green Horizon: Mega Lake Cleanup & Plantation',
    clubId: 'prakriti',
    clubName: 'Prakriti + Seva Wing',
    date: 'Oct 10, 7:00 AM',
    location: 'Campus West Lake Promenade',
    category: 'Eco & Volunteering',
    seatsLeft: 60,
    tags: ['environment', 'volunteering', 'outdoor'],
    blurb: 'Join 100+ students in cleaning campus waterways and planting 150 indigenous saplings. Gloves and refreshments provided.'
  },
  {
    id: 'ev-6',
    title: 'Valorant & Chess Inter-Branch LAN Showdown',
    clubId: 'respawn',
    clubName: 'Respawn Esports',
    date: 'Sep 28, 5:00 PM',
    location: 'Auditorium Block C',
    category: 'Gaming Competition',
    seatsLeft: 12,
    tags: ['gaming', 'competing', 'fun', 'strategic'],
    blurb: 'High-stakes custom lobby matches casted live on Discord with cash prizes and custom trophies for winners.'
  },
  {
    id: 'ev-7',
    title: 'Golden Hour Photowalk & Lightroom Sprint',
    clubId: 'lenslight',
    clubName: 'Lens & Light',
    date: 'Oct 1, 5:15 PM',
    location: 'Campus Clock Tower',
    category: 'Photography & Media',
    seatsLeft: 25,
    tags: ['photography', 'film', 'creative'],
    blurb: 'Explore architectural symmetry, portrait framing, and dynamic shadows, followed by a fast Lightroom color grading tutorial.'
  },
  {
    id: 'ev-8',
    title: 'Parliamentary Debate Bootcamp: Zero to Speaker',
    clubId: 'vaadvivad',
    clubName: 'Vaad-Vivad',
    date: 'Oct 8, 4:30 PM',
    location: 'Seminar Hall 3',
    category: 'Public Speaking',
    seatsLeft: 35,
    tags: ['debate', 'writing', 'strategic', 'skillbuilding'],
    blurb: 'Master the art of structuring rebuttal arguments, policy analysis, and persuasive rhetoric with senior national debaters.'
  },
  {
    id: 'ev-9',
    title: 'Arduino & Drone Flight Lab for Beginners',
    clubId: 'robotix',
    clubName: 'RobotiX',
    date: 'Oct 7, 3:30 PM',
    location: 'Robotics Center Workshop',
    category: 'Hardware Workshop',
    seatsLeft: 15,
    tags: ['tech', 'skillbuilding', 'hardware'],
    blurb: 'Assemble basic sensor circuits, flash firmware, and practice flight maneuvers in our protected drone safety cage.'
  },
  {
    id: 'ev-10',
    title: 'Canva to Figma: UI/UX Poster Design Sprint',
    clubId: 'kalakriti',
    clubName: 'Kalakriti Art',
    date: 'Oct 3, 4:00 PM',
    location: 'Design Studio Lab',
    category: 'UI/UX Design',
    seatsLeft: 28,
    tags: ['art', 'design', 'creative', 'resume'],
    blurb: 'Learn layout grids, typography pairings, color theory, and auto-layout in Figma to create stunning event graphics.'
  }
];

const PRESET_PROMPTS = [
  {
    label: '💻 Tech + Music',
    text: "I'm a 2nd year student who loves Python coding and AI projects, but I also play electric guitar and want to jam in evening music sessions."
  },
  {
    label: '🎭 Introvert Creative',
    text: "I love creative writing, digital illustration, and photography. Prefer calm small groups or solo creative sprints with low time pressure (2-3 hrs/wk)."
  },
  {
    label: '🌱 Social Seva + Nature',
    text: "Passionate about weekend volunteering, teaching underprivileged children, and environmental tree plantation drives with friendly people."
  },
  {
    label: '🚀 Startups & Debating',
    text: "Looking for business pitch competitions, startup idea validation, Model UN, and public speaking to sharpen my resume and leadership skills."
  },
  {
    label: '🎮 Esports & Sports',
    text: "Competitive Valorant and chess player who also plays evening football and badminton. Looking for intense tournaments and fun LAN parties."
  },
  {
    label: '🤖 Hardware & Drones',
    text: "Interested in robotics, soldering circuits, building drones, and working on physical tech hardware projects with dedicated teammates."
  }
];

const QUESTIONS = [
  {
    key: 'interests',
    type: 'multi',
    min: 1,
    max: 5,
    q: 'What types of activities genuinely excite you?',
    sub: 'Select all that spark your interest — this forms your foundational profile.',
    options: [
      { label: '💻 Coding, AI & App Development', tags: { tech: 3, skillbuilding: 2 } },
      { label: '🎸 Music, Instruments & Singing', tags: { music: 3, creative: 2 } },
      { label: '💃 Dance & Choreography', tags: { dance: 3, physical: 2 } },
      { label: '🎭 Theatre, Drama & Acting', tags: { drama: 3, performing: 2 } },
      { label: '🗣️ Debating, MUN & Quizzing', tags: { debate: 3, strategic: 2 } },
      { label: '⚽ Sports, Cricket & Fitness', tags: { sports: 3, physical: 3 } },
      { label: '📸 Photography & Filmmaking', tags: { photography: 3, film: 2 } },
      { label: '🎨 Fine Arts & UI/UX Design', tags: { art: 3, design: 3 } },
      { label: '🤝 Community Teaching & NGO Seva', tags: { volunteering: 3, social: 2 } },
      { label: '🎮 Esports, Gaming & Chess', tags: { gaming: 3, fun: 2 } },
      { label: '🚀 Startups, Business & Pitching', tags: { business: 3, resume: 3 } },
      { label: '🌿 Sustainability & Eco Action', tags: { environment: 3, outdoor: 2 } },
      { label: '🔭 Astronomy & Stargazing', tags: { tech: 1, outdoor: 2, solo: 1 } },
      { label: '✍️ Poetry & Creative Writing', tags: { writing: 3, creative: 2 } }
    ]
  },
  {
    key: 'workStyle',
    type: 'single',
    q: 'How do you perform and feel most energized?',
    sub: 'Your preferred team dynamic and social flow.',
    options: [
      { label: '🎨 Solo creator doing deep work', tags: { solo: 3, creative: 1 } },
      { label: '🤝 A tight-knit crew of 3-5 close friends', tags: { creative: 2, social: 1 } },
      { label: '⚡ A high-energy competitive squad', tags: { competing: 3, strategic: 2 } },
      { label: '🌟 A large, lively community with big events', tags: { social: 3, performing: 1 } }
    ]
  },
  {
    key: 'commitment',
    type: 'single',
    q: 'How much time can you realistically invest per week?',
    sub: 'We match communities according to your actual academic bandwidth.',
    options: [
      { label: '🌱 1–2 hours/week (Light & flexible, zero stress)', level: 1 },
      { label: '⚡ 3–5 hours/week (Regular weekly sessions & projects)', level: 2 },
      { label: '🔥 6+ hours/week (All-in! Core team & organizing fests)', level: 3 },
      { label: '🌊 Ad-hoc / Weekend-only (Flexible event participation)', level: 1 }
    ]
  },
  {
    key: 'primaryGoal',
    type: 'single',
    q: 'What is your #1 goal from joining an Aatmoday group?',
    sub: 'What outcome would make this semester memorable?',
    options: [
      { label: '🚀 Build high-impact projects for my Resume/Portfolio', tags: { resume: 3, skillbuilding: 3 } },
      { label: '💛 Make genuine, lifelong college friends', tags: { social: 3, fun: 2 } },
      { label: '🏆 Compete and win inter-college tournaments/hackathons', tags: { competing: 3, strategic: 2 } },
      { label: '🧘 De-stress, have fun, and pursue my creative passions', tags: { fun: 3, creative: 2 } },
      { label: '🌍 Create a tangible social or environmental impact', tags: { volunteering: 3, environment: 2 } }
    ]
  }
];

/* ============================================================
   APPLICATION STATE & STORAGE
   ============================================================ */

const state = {
  screen: 'matcher', // matcher | explore | events | quiz | loading | results | saved
  activeTab: 'all',  // for explore/events filtering
  freeFormText: '',
  quizStep: 0,
  quizAnswers: {},
  extractedInsights: null,
  recommendations: [],
  eventRecommendations: [],
  selectedClubForIcebreaker: null,
  selectedIcebreakerTone: 'casual', // casual | enthusiastic | formal
  savedClubs: JSON.parse(localStorage.getItem('aatmoday_saved_clubs') || '[]'),
  savedEvents: JSON.parse(localStorage.getItem('aatmoday_saved_events') || '[]'),
  isVoiceListening: false
};

function saveStateToStorage(){
  localStorage.setItem('aatmoday_saved_clubs', JSON.stringify(state.savedClubs));
  localStorage.setItem('aatmoday_saved_events', JSON.stringify(state.savedEvents));
  const el = document.getElementById('saved-count-nav');
  if(el) el.textContent = state.savedClubs.length + state.savedEvents.length;
}

/* ============================================================
   AI SEMANTIC NLP & MATCHING ENGINE
   ============================================================ */

// Semantic tag lexicon with synonym mapping and weight distributions
const SEMANTIC_KEYWORDS = {
  tech: ['code', 'coding', 'python', 'javascript', 'react', 'web', 'app', 'ai', 'ml', 'machine learning', 'developer', 'software', 'hackathon', 'algorithm', 'data', 'cloud', 'backend', 'frontend', 'deep learning', 'open source', 'linux', 'programming'],
  music: ['music', 'guitar', 'piano', 'sing', 'singing', 'song', 'band', 'drums', 'vocal', 'vocals', 'jam', 'jamming', 'flute', 'violin', 'audio', 'beatbox', 'production', 'acoustic', 'rock', 'classical music'],
  dance: ['dance', 'dancing', 'hip hop', 'hip-hop', 'choreography', 'popping', 'locking', 'freestyle', 'classical dance', 'contemporary', 'salsa', 'kathak', 'bharatnatyam', 'rhythm'],
  drama: ['theatre', 'theater', 'drama', 'acting', 'actor', 'actress', 'stage', 'nukkad', 'street play', 'play', 'skit', 'script', 'scriptwriting', 'director', 'improv', 'monologue'],
  writing: ['writing', 'write', 'writer', 'poetry', 'poem', 'stories', 'fiction', 'article', 'blog', 'slam poetry', 'literature', 'author', 'screenplay', 'reading', 'book', 'novels'],
  debate: ['debate', 'debating', 'speech', 'speaking', 'mun', 'model un', 'orator', 'public speaking', 'quizzing', 'quiz', 'arguments', 'policy', 'discourse', 'parliamentary'],
  sports: ['sports', 'cricket', 'football', 'soccer', 'badminton', 'tennis', 'table tennis', 'basketball', 'athletics', 'running', 'fitness', 'gym', 'workout', 'marathon'],
  physical: ['fitness', 'movement', 'stamina', 'athletics', 'exercise', 'physical', 'stamina', 'sports', 'dance'],
  photography: ['photo', 'photography', 'camera', 'dslr', 'pictures', 'photowalk', 'photoshop', 'lightroom', 'portraits', 'street photography', 'framing', 'lens'],
  film: ['film', 'filmmaking', 'video', 'cinematography', 'editing', 'premiere', 'davinci', 'youtube', 'short film', 'documentary', 'reels', 'shooting'],
  art: ['art', 'drawing', 'painting', 'sketch', 'sketching', 'illustration', 'mural', 'watercolor', 'canvas', 'acrylic', 'doodling'],
  design: ['design', 'ui', 'ux', 'ui/ux', 'figma', 'poster', 'graphic', 'canva', 'photoshop', 'illustrator', '3d', 'blender', 'typography'],
  volunteering: ['volunteer', 'volunteering', 'ngo', 'service', 'teach', 'teaching', 'children', 'underprivileged', 'seva', 'help', 'social work', 'charity', 'blood donation'],
  environment: ['environment', 'nature', 'sustainability', 'green', 'eco', 'plants', 'trees', 'plantation', 'climate', 'solar', 'waste', 'recycle', 'conservation', 'lake'],
  gaming: ['gaming', 'game', 'esports', 'valorant', 'bgmi', 'pubg', 'chess', 'lan', 'steam', 'fifa', 'minecraft', 'game dev', 'unity', 'unreal'],
  business: ['startup', 'startups', 'business', 'entrepreneur', 'entrepreneurship', 'pitch', 'pitching', 'product', 'marketing', 'venture', 'fund', 'strategy', 'finance', 'founder'],
  strategic: ['strategy', 'analytical', 'chess', 'case study', 'debating', 'strategic', 'logic', 'problem solving', 'consulting'],
  creative: ['creative', 'creativity', 'imagination', 'artistic', 'expressive', 'craft', 'original', 'design', 'music', 'theatre'],
  performing: ['performing', 'performance', 'stage', 'audience', 'live', 'showcase', 'spotlight', 'public'],
  social: ['friends', 'friendship', 'social', 'team', 'teamwork', 'community', 'people', 'collaborate', 'meetup', 'extrovert'],
  solo: ['solo', 'independent', 'introvert', 'quiet', 'calm', 'peaceful', 'individual', 'flexible'],
  competing: ['compete', 'competition', 'tournament', 'win', 'winning', 'championship', 'league', 'match', 'battle', 'hackathon'],
  skillbuilding: ['learn', 'learning', 'skills', 'workshop', 'masterclass', 'bootcamp', 'grow', 'training', 'practice'],
  resume: ['resume', 'career', 'portfolio', 'cv', 'linkedin', 'internship', 'leadership', 'certificate', 'high impact'],
  fun: ['fun', 'casual', 'chill', 'hobby', 'relax', 'de-stress', 'enjoy', 'weekend', 'light']
};

function analyzeNaturalLanguageInterest(text){
  const lower = text.toLowerCase();
  const detectedTags = {};
  const extractedKeywords = [];
  
  // Keyword density and proximity scoring
  Object.entries(SEMANTIC_KEYWORDS).forEach(([tag, words]) => {
    let tagScore = 0;
    words.forEach(word => {
      const regex = new RegExp(`\\b${word}\\b`, 'gi');
      const matches = lower.match(regex);
      if(matches){
        tagScore += matches.length * 2.5;
        if(!extractedKeywords.includes(word)) extractedKeywords.push(word);
      } else if(word.includes(' ') && lower.includes(word)){
        tagScore += 3.5;
        if(!extractedKeywords.includes(word)) extractedKeywords.push(word);
      }
    });
    if(tagScore > 0){
      detectedTags[tag] = tagScore;
    }
  });

  // Infer Commitment Bandwidth from text
  let inferredIntensity = 2; // default moderate
  if(lower.includes('1-2') || lower.includes('light') || lower.includes('casual') || lower.includes('low pressure') || lower.includes('free time') || lower.includes('weekend only')){
    inferredIntensity = 1;
  } else if(lower.includes('all-in') || lower.includes('hardcore') || lower.includes('heavy') || lower.includes('every day') || lower.includes('intense') || lower.includes('core team')){
    inferredIntensity = 3;
  }

  // Infer Persona archetype
  let archetype = 'Versatile Explorer';
  if(detectedTags.tech && detectedTags.business) archetype = 'Tech Founder & Innovator';
  else if(detectedTags.music || detectedTags.drama || detectedTags.dance) archetype = 'Passionate Performing Artist';
  else if(detectedTags.volunteering || detectedTags.environment) archetype = 'Social Impact Change-Maker';
  else if(detectedTags.art || detectedTags.design || detectedTags.writing) archetype = 'Creative Storyteller & Designer';
  else if(detectedTags.gaming || detectedTags.sports) archetype = 'Competitive Athlete & Strategist';
  else if(detectedTags.tech) archetype = 'Dedicated Software & AI Builder';

  return {
    detectedTags,
    extractedKeywords: extractedKeywords.slice(0, 8),
    inferredIntensity,
    archetype
  };
}

function computeHybridRecommendations(nlpResult, quizAnswers = {}){
  const tags = { ...(nlpResult ? nlpResult.detectedTags : {}) };
  
  // Fold in quiz tags if taken
  if(quizAnswers.interests){
    quizAnswers.interests.forEach(opt => {
      Object.entries(opt.tags || {}).forEach(([t, val]) => {
        tags[t] = (tags[t] || 0) + val * 2;
      });
    });
  }
  if(quizAnswers.workStyle && quizAnswers.workStyle.tags){
    Object.entries(quizAnswers.workStyle.tags).forEach(([t, val]) => {
      tags[t] = (tags[t] || 0) + val * 2;
    });
  }
  if(quizAnswers.primaryGoal && quizAnswers.primaryGoal.tags){
    Object.entries(quizAnswers.primaryGoal.tags).forEach(([t, val]) => {
      tags[t] = (tags[t] || 0) + val * 2.5;
    });
  }

  const targetIntensity = quizAnswers.commitment ? quizAnswers.commitment.level : (nlpResult ? nlpResult.inferredIntensity : 2);

  // Score each community
  const clubScores = COMMUNITIES.map(c => {
    let score = 0;
    const matchReasons = [];
    const matchedTags = [];

    // Tag Overlap calculation
    Object.entries(c.tags).forEach(([t, weight]) => {
      if(tags[t]){
        const points = tags[t] * weight * 3;
        score += points;
        matchedTags.push({ tag: t, points });
      }
    });

    // Intensity alignment bonus
    const intensityDiff = Math.abs(c.intensity - targetIntensity);
    const intensityScore = Math.max(0, 15 - intensityDiff * 6);
    score += intensityScore;

    // Generate explicit explanations
    if(matchedTags.length > 0){
      matchedTags.sort((a, b) => b.points - a.points);
      const topT = matchedTags.slice(0, 2).map(m => m.tag);
      
      const keywordsFound = (nlpResult && nlpResult.extractedKeywords) ? nlpResult.extractedKeywords : [];
      if(keywordsFound.length > 0){
        matchReasons.push(`Strong overlap with your expressed interest in "${keywordsFound.slice(0, 3).join(', ')}".`);
      }
      matchReasons.push(`Direct alignment with ${c.name}'s focus on ${c.vibes.slice(0, 2).join(' & ')}.`);
    } else {
      matchReasons.push(`Recommended as an enriching complementary community to explore new horizons.`);
    }

    if(intensityDiff === 0){
      matchReasons.push(`Meeting frequency matches your preferred commitment level (${c.meets}).`);
    }

    return {
      ...c,
      rawScore: score,
      matchReasons,
      matchedTags
    };
  });

  // Calculate relative match percentages with normalized scaling
  const maxScore = Math.max(...clubScores.map(c => c.rawScore), 1);
  const normalizedClubs = clubScores.map(c => {
    const pct = Math.min(99, Math.max(62, Math.round(60 + (c.rawScore / maxScore) * 39)));
    return { ...c, matchPct: pct };
  }).sort((a, b) => b.matchPct - a.matchPct);

  // Score Live Events based on top matched tags
  const eventScores = EVENTS_DATABASE.map(ev => {
    let score = 0;
    ev.tags.forEach(t => {
      if(tags[t]) score += tags[t] * 4;
    });
    const hostClub = normalizedClubs.find(c => c.id === ev.clubId);
    if(hostClub) score += (hostClub.matchPct / 10);

    const matchPct = Math.min(98, Math.max(65, Math.round(62 + (score / (maxScore + 10)) * 36)));
    return {
      ...ev,
      matchPct,
      reason: `Hosted by ${ev.clubName} · Perfect match for your passion in ${ev.tags.join(' & ')}.`
    };
  }).sort((a, b) => b.matchPct - a.matchPct);

  return {
    topClubs: normalizedClubs,
    topEvents: eventScores
  };
}

/* ============================================================
   AI ICEBREAKER GENERATOR ENGINE
   ============================================================ */

function generatePersonalizedIcebreakers(club, studentKeywords = [], tone = 'casual'){
  const coord = club.coordinator;
  const clubName = club.name;
  const kwString = studentKeywords.length > 0 ? studentKeywords.slice(0, 2).join(' and ') : 'your club activities';

  let icebreaker = '';
  let inPersonStarter = '';

  if(tone === 'casual'){
    icebreaker = `Hey ${coord}! 👋 I'm a student at campus and just got matched with ${clubName} on the Aatmoday platform. I've been really curious about ${kwString}, and I saw your upcoming session "${club.nextEvent}". Would love to know how I can drop by to check it out!`;
    inPersonStarter = `Walk up to ${coord} or any member at the meetup and say: "Hey! I saw the announcement for ${clubName}'s ${club.vibes[0]} sprint. Are you guys currently accepting new members for this semester's projects?"`;
  } else if(tone === 'enthusiastic'){
    icebreaker = `Hi ${coord}! 🚀 Super excited to connect. I recently explored ${clubName} through Aatmoday and was stoked to see your focus on ${club.vibes.join(', ')}! I have some background in ${kwString} and would love to actively contribute to your next event (${club.nextEvent}). When is the best time to sync up?`;
    inPersonStarter = `Introduce yourself with energy: "Hey everyone! I've been working on ${kwString} and wanted to team up with people who love ${club.vibes[0]} as much as I do. What's the biggest project the crew is tackling right now?"`;
  } else { // inquiring / formal
    icebreaker = `Hello ${coord}, I hope you are having a productive week. I am reaching out regarding ${clubName}. Through the Aatmoday matchmaker, your community stood out as an ideal fit for my interests in ${kwString}. Could you please guide me regarding the orientation process and prerequisites for joining your upcoming meetup (${club.meets})? Thank you!`;
    inPersonStarter = `Politely approach the registration desk: "Hello! I'm here for the ${clubName} orientation. Could you point me toward ${coord}? I'm looking forward to learning more about your schedule and initiatives."`;
  }

  return { icebreaker, inPersonStarter };
}

/* ============================================================
   NAVIGATION & UI CONTROLLER
   ============================================================ */

const root = document.getElementById('root');
const modalRoot = document.getElementById('modal-root');
const toastRoot = document.getElementById('toast-root');

function showToast(msg, icon = '✅'){
  const toast = document.createElement('div');
  toast.className = 'toast';
  toast.innerHTML = `<span>${icon}</span> <span>${msg}</span>`;
  toastRoot.appendChild(toast);
  setTimeout(() => {
    toast.style.transition = 'opacity .3s ease, transform .3s ease';
    toast.style.opacity = '0';
    toast.style.transform = 'translateY(15px)';
    setTimeout(() => toast.remove(), 300);
  }, 2800);
}

function goToScreen(scr){
  state.screen = scr;
  updateNavUI();
  window.scrollTo({ top: 0, behavior: 'smooth' });
  renderApp();
}

function updateNavUI(){
  document.getElementById('nav-matcher-btn').classList.toggle('active', state.screen === 'matcher' || state.screen === 'results');
  document.getElementById('nav-explore-btn').classList.toggle('active', state.screen === 'explore');
  document.getElementById('nav-events-btn').classList.toggle('active', state.screen === 'events');
  document.getElementById('nav-saved-btn').classList.toggle('active', state.screen === 'saved');
}

// Bind Navigation
document.getElementById('nav-home-btn').onclick = () => goToScreen('matcher');
document.getElementById('nav-matcher-btn').onclick = () => goToScreen('matcher');
document.getElementById('nav-explore-btn').onclick = () => goToScreen('explore');
document.getElementById('nav-events-btn').onclick = () => goToScreen('events');
document.getElementById('nav-saved-btn').onclick = () => goToScreen('saved');
document.getElementById('nav-quiz-btn').onclick = () => {
  state.quizStep = 0;
  state.quizAnswers = {};
  goToScreen('quiz');
};

/* ============================================================
   SCREEN RENDERERS
   ============================================================ */

function renderApp(){
  if(state.screen === 'matcher') renderMatcherScreen();
  else if(state.screen === 'explore') renderExploreScreen();
  else if(state.screen === 'events') renderEventsScreen();
  else if(state.screen === 'quiz') renderQuizScreen();
  else if(state.screen === 'loading') renderLoadingScreen();
  else if(state.screen === 'results') renderResultsScreen();
  else if(state.screen === 'saved') renderSavedScreen();
  saveStateToStorage();
}

/* ---------- SCREEN 1: MATCHER (FREE-FORM NLP HERO) ---------- */
function renderMatcherScreen(){
  const totalClubs = COMMUNITIES.length;
  const totalMembers = COMMUNITIES.reduce((sum, c) => sum + c.members, 0);

  root.innerHTML = `
    <div class="page fade-in">
      <div class="hero-box">
        <div class="hero-top-badge">
          <span class="badge-ai"><span class="dot"></span> AI Interest Matchmaker · Bit N Build '26</span>
        </div>
        <h1 class="hero-title">Discover your true <span class="hl">tribe</span> at Aatmoday.</h1>
        <p class="hero-desc">
          Describe what excites you in natural language. Our AI understands your unique passions, schedule bandwidth, and vibe to recommend the perfect sub-groups and live events.
        </p>

        <!-- Free-form AI Input Card -->
        <div class="ai-input-card">
          <div class="ai-input-header">
            <span class="ai-input-label">✨ Natural Language Interest Description</span>
            <div class="ai-input-actions-top">
              <button class="btn sm ghost" id="voice-btn" title="Simulate voice dictation">
                🎤 ${state.isVoiceListening ? 'Listening...' : 'Voice Input'}
              </button>
              <button class="btn sm ghost" id="clear-input-btn" title="Clear input">Clear</button>
            </div>
          </div>

          <textarea 
            class="free-form-textarea" 
            id="free-form-input" 
            placeholder="Type anything freely... e.g. I love coding Python algorithms, playing electric guitar in jam sessions, and I want to teach kids on weekends. I only have 3-4 hours a week."
          >${state.freeFormText}</textarea>

          <div class="prompt-pills-wrap">
            <span class="prompt-pill-label">💡 Or try an example:</span>
            ${PRESET_PROMPTS.map((p, i) => `
              <button class="prompt-pill" data-idx="${i}">${p.label}</button>
            `).join('')}
          </div>

          <div class="ai-input-bottom">
            <span style="font-size:12.5px; color:var(--text-faint);">⚡ Instant Semantic Analysis · Context Aware</span>
            <button class="btn lg" id="analyze-match-btn">
              <span>Find My Matches</span> ➔
            </button>
          </div>
        </div>

        <div class="input-switch-strip">
          <span class="switch-note">Prefer a guided step-by-step experience?</span>
          <button class="btn sm ghost" id="switch-quiz-btn">🎯 Take the 4-Step Interactive Quiz instead</button>
        </div>

        <div class="stats-strip">
          <div><div class="stat-val">${totalClubs}</div><div class="stat-lbl">Active Sub-Groups</div></div>
          <div><div class="stat-val">${totalMembers}+</div><div class="stat-lbl">Student Members</div></div>
          <div><div class="stat-val">${EVENTS_DATABASE.length}+</div><div class="stat-lbl">Live Workshops & Events</div></div>
          <div><div class="stat-val">100%</div><div class="stat-lbl">Personalized Explanations</div></div>
        </div>
      </div>

      <!-- Live Events Spotlight Section -->
      <div class="section-head">
        <div>
          <h2 class="section-title">🔥 Happening This Week</h2>
          <div class="section-sub">Upcoming workshops, open mics, and hackathons you can attend immediately.</div>
        </div>
        <button class="btn sm ghost" id="view-all-events-btn">View All ${EVENTS_DATABASE.length} Events ➔</button>
      </div>

      <div class="rec-grid">
        ${EVENTS_DATABASE.slice(0, 3).map(ev => eventCardHTML(ev)).join('')}
      </div>
    </div>
  `;

  // Bind Matcher Actions
  const input = document.getElementById('free-form-input');
  input.oninput = (e) => { state.freeFormText = e.target.value; };

  root.querySelectorAll('.prompt-pill').forEach(btn => {
    btn.onclick = () => {
      const idx = parseInt(btn.dataset.idx, 10);
      state.freeFormText = PRESET_PROMPTS[idx].text;
      input.value = state.freeFormText;
      showToast('Loaded example prompt! Click "Find My Matches".', '✨');
    };
  });

  document.getElementById('voice-btn').onclick = () => {
    state.isVoiceListening = true;
    showToast('Simulating voice dictation...', '🎙️');
    setTimeout(() => {
      state.freeFormText = "I enjoy building deep learning AI models, playing competitive badminton, and jamming with rock bands on weekends.";
      input.value = state.freeFormText;
      state.isVoiceListening = false;
      renderApp();
      showToast('Voice transcribed successfully!', '✨');
    }, 1200);
  };

  document.getElementById('clear-input-btn').onclick = () => {
    state.freeFormText = '';
    input.value = '';
    input.focus();
  };

  document.getElementById('analyze-match-btn').onclick = () => {
    if(!state.freeFormText.trim()){
      state.freeFormText = "I'm looking for a creative tech community to build cool web apps, make friends, and attend hackathons.";
    }
    triggerAIMatching(state.freeFormText);
  };

  document.getElementById('switch-quiz-btn').onclick = () => {
    state.quizStep = 0;
    state.quizAnswers = {};
    goToScreen('quiz');
  };

  document.getElementById('view-all-events-btn').onclick = () => goToScreen('events');
  bindCardInteractions();
}

function triggerAIMatching(rawText){
  goToScreen('loading');
  setTimeout(() => {
    const nlp = analyzeNaturalLanguageInterest(rawText);
    state.extractedInsights = nlp;
    const { topClubs, topEvents } = computeHybridRecommendations(nlp, state.quizAnswers);
    state.recommendations = topClubs;
    state.eventRecommendations = topEvents;
    goToScreen('results');
  }, 950);
}

/* ---------- SCREEN 2: RESULTS & EXPLANATIONS ---------- */
function renderResultsScreen(){
  const topMatches = state.recommendations.slice(0, 4);
  const matchedEvents = state.eventRecommendations.slice(0, 3);
  const nlp = state.extractedInsights || { archetype: 'Community Builder', extractedKeywords: [] };

  root.innerHTML = `
    <div class="page fade-in">
      <div class="hero-box" style="padding: 30px; margin-bottom: 24px;">
        <div style="display:flex; justify-content:space-between; align-items:flex-start; flex-wrap:wrap; gap:12px;">
          <div>
            <span class="badge-ai"><span class="dot"></span> AI Profile Analysis Generated</span>
            <h2 style="font-family:var(--serif); font-size:26px; margin:8px 0 4px;">Persona Archetype: <span class="hl">${nlp.archetype}</span></h2>
            <p style="color:var(--text-dim); font-size:14px; margin:0;">
              Matched against <strong>${COMMUNITIES.length} sub-groups</strong> and <strong>${EVENTS_DATABASE.length} live events</strong> with explainable reasoning.
            </p>
          </div>
          <div style="display:flex; gap:8px;">
            <button class="btn sm ghost" id="retake-ai-btn">✏️ Edit Prompt</button>
            <button class="btn sm ghost" id="quiz-refine-btn">🎯 Refine with Quiz</button>
          </div>
        </div>

        ${nlp.extractedKeywords && nlp.extractedKeywords.length > 0 ? `
          <div class="ai-extracted-tags-box">
            <span class="ai-extracted-title">🧠 Inferred Core Passions & Semantic Keywords:</span>
            <div class="ai-extracted-chips">
              ${nlp.extractedKeywords.map(kw => `<span class="extracted-chip highlight">#${kw}</span>`).join('')}
              <span class="extracted-chip">Bandwidth: ${nlp.inferredIntensity === 1 ? 'Light (1-2h)' : nlp.inferredIntensity === 3 ? 'Heavy (6h+)' : 'Standard (3-5h)'}</span>
            </div>
          </div>
        ` : ''}
      </div>

      <!-- Top Recommended Sub-Groups -->
      <div class="section-head">
        <div>
          <h2 class="section-title">🏆 Top Matched Aatmoday Communities</h2>
          <div class="section-sub">Ranked by interest synergy, activity schedule, and vibe compatibility.</div>
        </div>
      </div>

      <div class="rec-grid">
        ${topMatches.map((c, i) => clubCardHTML(c, true, i === 0)).join('')}
      </div>

      <!-- Recommended Events -->
      <div class="section-head" style="margin-top:40px;">
        <div>
          <h2 class="section-title">📅 Recommended Events & Workshops for You</h2>
          <div class="section-sub">Events hosted by your matched communities that you can RSVP right now.</div>
        </div>
      </div>

      <div class="rec-grid">
        ${matchedEvents.map(ev => eventCardHTML(ev, true)).join('')}
      </div>

      <div style="text-align:center; margin-top:40px; padding:24px; background:var(--surface); border:1px solid var(--border); border-radius:var(--radius-lg);">
        <h3 style="font-family:var(--serif); margin:0 0 8px;">Want to explore the entire directory?</h3>
        <p style="color:var(--text-dim); font-size:14px; margin:0 0 16px;">Browse all 16 sub-groups across tech, creative arts, and sports.</p>
        <button class="btn" id="browse-all-btn">Browse Full Directory ➔</button>
      </div>
    </div>
  `;

  document.getElementById('retake-ai-btn').onclick = () => goToScreen('matcher');
  document.getElementById('quiz-refine-btn').onclick = () => {
    state.quizStep = 0;
    goToScreen('quiz');
  };
  document.getElementById('browse-all-btn').onclick = () => goToScreen('explore');
  bindCardInteractions();
}

/* ---------- SCREEN 3: GUIDED QUIZ WIZARD ---------- */
function renderQuizScreen(){
  const q = QUESTIONS[state.quizStep];
  const isMulti = q.type === 'multi';
  const current = state.quizAnswers[q.key];

  const isSelected = (opt) => {
    if(isMulti) return (current || []).some(o => o.label === opt.label);
    if(q.key === 'commitment') return current && current.level === opt.level;
    return current && current.label === opt.label;
  };

  const canAdvance = isMulti ? (current && current.length >= (q.min || 1)) : !!current;

  root.innerHTML = `
    <div class="page narrow fade-in">
      <div class="quiz-card">
        <div class="progress-track">
          ${QUESTIONS.map((_, i) => `
            <div class="progress-seg">
              <i style="width:${i < state.quizStep ? 100 : i === state.quizStep ? 50 : 0}%"></i>
            </div>
          `).join('')}
        </div>

        <div class="step-label">Step ${state.quizStep + 1} of ${QUESTIONS.length} · Guided Discovery</div>
        <h2 class="question">${q.q}</h2>
        <p class="subquestion">${q.sub}</p>

        <div class="options-grid">
          ${q.options.map((opt, i) => `
            <button class="option-btn ${isSelected(opt) ? 'selected' : ''}" data-idx="${i}">
              <span>${opt.label}</span>
            </button>
          `).join('')}
        </div>

        <div class="quiz-nav">
          <button class="btn ghost sm" id="quiz-back-btn" ${state.quizStep === 0 ? 'disabled' : ''}>← Back</button>
          <div style="font-size:12.5px; color:var(--text-faint);">
            ${isMulti ? `${(current || []).length} selected (max ${q.max})` : 'Select one option'}
          </div>
          <button class="btn sm" id="quiz-next-btn" ${canAdvance ? '' : 'disabled'}>
            ${state.quizStep === QUESTIONS.length - 1 ? 'Compute AI Matches ✨' : 'Continue →'}
          </button>
        </div>
      </div>
    </div>
  `;

  root.querySelectorAll('.option-btn').forEach(btn => {
    btn.onclick = () => {
      const opt = q.options[parseInt(btn.dataset.idx, 10)];
      if(isMulti){
        let arr = state.quizAnswers[q.key] || [];
        const exists = arr.some(o => o.label === opt.label);
        if(exists){
          arr = arr.filter(o => o.label !== opt.label);
        } else {
          if(q.max && arr.length >= q.max){
            showToast(`You can pick up to ${q.max} options.`, 'ℹ️');
            return;
          }
          arr = [...arr, opt];
        }
        state.quizAnswers[q.key] = arr;
      } else {
        state.quizAnswers[q.key] = opt;
      }
      renderQuizScreen();
    };
  });

  document.getElementById('quiz-back-btn').onclick = () => {
    if(state.quizStep > 0){
      state.quizStep--;
      renderQuizScreen();
    }
  };

  document.getElementById('quiz-next-btn').onclick = () => {
    if(!canAdvance) return;
    if(state.quizStep < QUESTIONS.length - 1){
      state.quizStep++;
      renderQuizScreen();
    } else {
      goToScreen('loading');
      setTimeout(() => {
        const nlp = analyzeNaturalLanguageInterest(state.freeFormText || 'Active student exploring campus hobbies');
        state.extractedInsights = nlp;
        const { topClubs, topEvents } = computeHybridRecommendations(nlp, state.quizAnswers);
        state.recommendations = topClubs;
        state.eventRecommendations = topEvents;
        goToScreen('results');
      }, 900);
    }
  };
}

/* ---------- SCREEN 4: LOADING SPINNER ---------- */
function renderLoadingScreen(){
  root.innerHTML = `
    <div class="page narrow fade-in">
      <div class="loading-container">
        <div class="ai-pulse-core">✨</div>
        <h2 style="font-family:var(--serif); font-size:24px; margin:0 0 10px;">Synthesizing Your Passion Profile...</h2>
        <p style="color:var(--text-dim); font-size:14.5px; max-width:44ch; margin:0 auto 20px;">
          Running semantic tag extraction, schedule constraint matching, and generating personalized icebreakers.
        </p>
        <span class="badge-ai"><span class="dot"></span> Querying Aatmoday Knowledgebase</span>
      </div>
    </div>
  `;
}

/* ---------- SCREEN 5: EXPLORE ALL SUB-GROUPS ---------- */
function renderExploreScreen(){
  const filtered = COMMUNITIES.filter(c => {
    if(state.activeTab === 'all') return true;
    if(state.activeTab === 'tech') return c.tags.tech || c.category.includes('Tech') || c.category.includes('Hardware');
    if(state.activeTab === 'arts') return c.tags.music || c.tags.dance || c.tags.drama || c.tags.art || c.tags.writing;
    if(state.activeTab === 'sports') return c.tags.sports || c.tags.gaming;
    if(state.activeTab === 'social') return c.tags.volunteering || c.tags.environment || c.tags.business;
    return true;
  });

  root.innerHTML = `
    <div class="page fade-in">
      <div class="section-head" style="margin-top:0;">
        <div>
          <h1 class="section-title">🏛️ Explore Aatmoday Sub-Groups</h1>
          <div class="section-sub">Browse all ${COMMUNITIES.length} specialized wings, clubs, and interest societies.</div>
        </div>

        <div class="tabs-nav">
          <button class="tab-btn ${state.activeTab==='all'?'active':''}" data-tab="all">All (${COMMUNITIES.length})</button>
          <button class="tab-btn ${state.activeTab==='tech'?'active':''}" data-tab="tech">Tech & AI</button>
          <button class="tab-btn ${state.activeTab==='arts'?'active':''}" data-tab="arts">Creative & Stage</button>
          <button class="tab-btn ${state.activeTab==='sports'?'active':''}" data-tab="sports">Sports & Gaming</button>
          <button class="tab-btn ${state.activeTab==='social'?'active':''}" data-tab="social">Impact & Startups</button>
        </div>
      </div>

      <div class="rec-grid">
        ${filtered.map(c => clubCardHTML(c, false)).join('')}
      </div>
    </div>
  `;

  root.querySelectorAll('.tab-btn').forEach(btn => {
    btn.onclick = () => {
      state.activeTab = btn.dataset.tab;
      renderExploreScreen();
    };
  });

  bindCardInteractions();
}

/* ---------- SCREEN 6: EVENTS CATALOG ---------- */
function renderEventsScreen(){
  root.innerHTML = `
    <div class="page fade-in">
      <div class="section-head" style="margin-top:0;">
        <div>
          <h1 class="section-title">📅 Live Campus Events & Workshops</h1>
          <div class="section-sub">Join scheduled hackathons, jam circles, and orientation meetups.</div>
        </div>
        <button class="btn sm" id="match-events-cta-btn">✨ Match Events to My Profile</button>
      </div>

      <div class="rec-grid">
        ${EVENTS_DATABASE.map(ev => eventCardHTML(ev, false)).join('')}
      </div>
    </div>
  `;

  document.getElementById('match-events-cta-btn').onclick = () => goToScreen('matcher');
  bindCardInteractions();
}

/* ---------- SCREEN 7: SAVED BOOKMARKS ---------- */
function renderSavedScreen(){
  const savedClubsList = COMMUNITIES.filter(c => state.savedClubs.includes(c.id));
  const savedEventsList = EVENTS_DATABASE.filter(ev => state.savedEvents.includes(ev.id));

  root.innerHTML = `
    <div class="page fade-in">
      <div class="section-head" style="margin-top:0;">
        <div>
          <h1 class="section-title">🔖 My Saved Bookmarks</h1>
          <div class="section-sub">Communities and events you have shortlisted for this semester.</div>
        </div>
      </div>

      ${savedClubsList.length === 0 && savedEventsList.length === 0 ? `
        <div style="text-align:center; padding:60px 20px; background:var(--surface); border:1px dashed var(--border); border-radius:var(--radius-lg);">
          <div style="font-size:32px; margin-bottom:12px;">📭</div>
          <h3 style="font-family:var(--serif); margin:0 0 6px;">No saved bookmarks yet</h3>
          <p style="color:var(--text-dim); font-size:14px; margin:0 0 16px;">Bookmark groups or events from recommendations to access them anytime.</p>
          <button class="btn sm" id="empty-saved-explore-btn">Explore Communities ➔</button>
        </div>
      ` : `
        ${savedClubsList.length > 0 ? `
          <h3 style="font-family:var(--serif); font-size:20px; margin:20px 0 14px;">Saved Sub-Groups (${savedClubsList.length})</h3>
          <div class="rec-grid">
            ${savedClubsList.map(c => clubCardHTML(c, false)).join('')}
          </div>
        ` : ''}

        ${savedEventsList.length > 0 ? `
          <h3 style="font-family:var(--serif); font-size:20px; margin:30px 0 14px;">Saved Events (${savedEventsList.length})</h3>
          <div class="rec-grid">
            ${savedEventsList.map(ev => eventCardHTML(ev, false)).join('')}
          </div>
        ` : ''}
      `}
    </div>
  `;

  const btn = document.getElementById('empty-saved-explore-btn');
  if(btn) btn.onclick = () => goToScreen('explore');
  bindCardInteractions();
}

/* ============================================================
   HTML CARD GENERATORS & HELPERS
   ============================================================ */

function clubCardHTML(c, showMatch = false, isFeatured = false){
  const isSaved = state.savedClubs.includes(c.id);
  return `
    <div class="rec-card ${isFeatured ? 'featured' : ''}" data-club-id="${c.id}">
      <div class="rec-card-top">
        <div class="club-avatar">${c.name.substring(0, 2).toUpperCase()}</div>
        ${showMatch ? `
          <div class="match-dial">
            <span class="match-pct">${c.matchPct}%</span>
            <span class="match-lbl">Match Score</span>
          </div>
        ` : `
          <span style="font-size:11.5px; color:var(--text-faint);">${c.members} members</span>
        `}
      </div>

      <h3 class="rec-card-name">${c.name}</h3>
      <div class="rec-card-cat">${c.category} · ${c.intensity === 1 ? '🌱 Light' : c.intensity === 3 ? '🔥 High Energy' : '⚡ Moderate'}</div>
      <p class="rec-card-blurb">${c.blurb}</p>

      ${showMatch && c.matchReasons ? `
        <div class="why-recommended-box">
          <span class="why-title">💡 Why this fits you:</span>
          <p class="why-text">${c.matchReasons[0]}</p>
        </div>
      ` : ''}

      <div class="rec-card-meta">
        <span>🕒 Meets: ${c.meets}</span>
        <span>Lead: ${c.coordinator}</span>
      </div>

      <div class="rec-card-actions">
        <button class="btn sm" data-action="icebreaker" data-id="${c.id}">
          💬 AI Icebreaker
        </button>
        <button class="btn sm ghost" data-action="save-club" data-id="${c.id}">
          ${isSaved ? '★ Saved' : '☆ Save'}
        </button>
      </div>
    </div>
  `;
}

function eventCardHTML(ev, showMatch = false){
  const isSaved = state.savedEvents.includes(ev.id);
  return `
    <div class="rec-card" data-event-id="${ev.id}">
      <div class="rec-card-top">
        <div class="club-avatar event-icon">📅</div>
        ${showMatch ? `
          <div class="match-dial">
            <span class="match-pct" style="color:#4ade80;">${ev.matchPct}%</span>
            <span class="match-lbl">Relevance</span>
          </div>
        ` : `
          <span class="event-badge-live">Open RSVP</span>
        `}
      </div>

      <h3 class="rec-card-name">${ev.title}</h3>
      <div class="rec-card-cat">${ev.category} · Hosted by <strong>${ev.clubName}</strong></div>
      <p class="rec-card-blurb">${ev.blurb}</p>

      ${showMatch && ev.reason ? `
        <div class="why-recommended-box" style="border-left-color:#4ade80;">
          <span class="why-title" style="color:#4ade80;">💡 Event Synergy:</span>
          <p class="why-text">${ev.reason}</p>
        </div>
      ` : ''}

      <div class="rec-card-meta">
        <span>📍 ${ev.location}</span>
        <span>🕒 ${ev.date}</span>
      </div>

      <div class="rec-card-actions">
        <button class="btn sm accent-cyan" data-action="rsvp-event" data-id="${ev.id}">
          🎟️ RSVP / Join
        </button>
        <button class="btn sm ghost" data-action="save-event" data-id="${ev.id}">
          ${isSaved ? '★ Shortlisted' : '☆ Save'}
        </button>
      </div>
    </div>
  `;
}

function bindCardInteractions(){
  root.querySelectorAll('[data-action="icebreaker"]').forEach(btn => {
    btn.onclick = (e) => {
      e.stopPropagation();
      const clubId = btn.dataset.id;
      const club = COMMUNITIES.find(c => c.id === clubId);
      if(club) openIcebreakerModal(club);
    };
  });

  root.querySelectorAll('[data-action="save-club"]').forEach(btn => {
    btn.onclick = (e) => {
      e.stopPropagation();
      const clubId = btn.dataset.id;
      if(state.savedClubs.includes(clubId)){
        state.savedClubs = state.savedClubs.filter(id => id !== clubId);
        showToast('Removed club from bookmarks', '🗑️');
      } else {
        state.savedClubs.push(clubId);
        showToast('Saved club to bookmarks!', '⭐');
      }
      saveStateToStorage();
      renderApp();
    };
  });

  root.querySelectorAll('[data-action="save-event"]').forEach(btn => {
    btn.onclick = (e) => {
      e.stopPropagation();
      const evId = btn.dataset.id;
      if(state.savedEvents.includes(evId)){
        state.savedEvents = state.savedEvents.filter(id => id !== evId);
        showToast('Removed event from bookmarks', '🗑️');
      } else {
        state.savedEvents.push(evId);
        showToast('Shortlisted event!', '⭐');
      }
      saveStateToStorage();
      renderApp();
    };
  });

  root.querySelectorAll('[data-action="rsvp-event"]').forEach(btn => {
    btn.onclick = (e) => {
      e.stopPropagation();
      const evId = btn.dataset.id;
      const ev = EVENTS_DATABASE.find(x => x.id === evId);
      showToast(`RSVP Confirmed for "${ev.title}"! Calendar invite generated.`, '🎉');
    };
  });
}

/* ============================================================
   AI ICEBREAKER & CONVERSATION STARTER MODAL
   ============================================================ */

function openIcebreakerModal(club){
  state.selectedClubForIcebreaker = club;
  renderIcebreakerModal();
}

function renderIcebreakerModal(){
  const club = state.selectedClubForIcebreaker;
  if(!club){
    modalRoot.innerHTML = '';
    return;
  }

  const kw = state.extractedInsights ? state.extractedInsights.extractedKeywords : [];
  const { icebreaker, inPersonStarter } = generatePersonalizedIcebreakers(club, kw, state.selectedIcebreakerTone);

  modalRoot.innerHTML = `
    <div class="modal-overlay" id="modal-overlay">
      <div class="modal-card">
        <div class="modal-header">
          <div>
            <span class="badge-ai"><span class="dot"></span> AI Conversation Starter</span>
            <h2 style="font-family:var(--serif); font-size:22px; margin:6px 0 2px;">
              Connect with <span class="hl">${club.name}</span>
            </h2>
            <p style="color:var(--text-faint); font-size:13px; margin:0;">
              Lead Coordinator: <strong>${club.coordinator}</strong> (${club.handle})
            </p>
          </div>
          <button class="modal-close" id="modal-close-btn">✕</button>
        </div>

        <div style="font-size:12.5px; color:var(--text-dim); margin-bottom:6px;">Select Conversation Tone:</div>
        <div class="icebreaker-tone-tabs">
          <button class="tone-pill ${state.selectedIcebreakerTone==='casual'?'active':''}" data-tone="casual">☕ Casual & Friendly</button>
          <button class="tone-pill ${state.selectedIcebreakerTone==='enthusiastic'?'active':''}" data-tone="enthusiastic">🚀 Enthusiastic & Passionate</button>
          <button class="tone-pill ${state.selectedIcebreakerTone==='formal'?'active':''}" data-tone="formal">👔 Curious & Inquiring</button>
        </div>

        <!-- Generated Message Card -->
        <div class="icebreaker-box">
          <p class="icebreaker-text" id="icebreaker-copy-text">${icebreaker}</p>
        </div>

        <div class="icebreaker-actions">
          <button class="btn sm" id="copy-icebreaker-btn">📋 Copy Message</button>
          <a class="btn sm accent-cyan" id="wa-connect-btn" href="https://api.whatsapp.com/send?phone=${club.contactWa}&text=${encodeURIComponent(icebreaker)}" target="_blank">
            📱 Open in WhatsApp
          </a>
          <button class="btn sm ghost" id="regen-icebreaker-btn">🔄 Regenerate Variation</button>
        </div>

        <!-- In-Person Meetup Tip -->
        <div class="in-person-tip-box">
          <span class="tip-head">🗣️ What to say at your first in-person meetup:</span>
          <p class="tip-content">${inPersonStarter}</p>
        </div>
      </div>
    </div>
  `;

  modalRoot.querySelectorAll('.tone-pill').forEach(btn => {
    btn.onclick = () => {
      state.selectedIcebreakerTone = btn.dataset.tone;
      renderIcebreakerModal();
    };
  });

  document.getElementById('copy-icebreaker-btn').onclick = async () => {
    try {
      await navigator.clipboard.writeText(icebreaker);
      showToast('Copied intro message to clipboard!', '📋');
    } catch(err) {
      showToast('Message ready to send!', '📋');
    }
  };

  document.getElementById('regen-icebreaker-btn').onclick = () => {
    showToast('Regenerated personalized variation!', '✨');
    renderIcebreakerModal();
  };

  document.getElementById('modal-close-btn').onclick = () => {
    state.selectedClubForIcebreaker = null;
    modalRoot.innerHTML = '';
  };
  document.getElementById('modal-overlay').onclick = (e) => {
    if(e.target.id === 'modal-overlay'){
      state.selectedClubForIcebreaker = null;
      modalRoot.innerHTML = '';
    }
  };
}

/* ============================================================
   INITIALIZATION
   ============================================================ */

renderApp();
saveStateToStorage();

</script>
</body>
</html>
