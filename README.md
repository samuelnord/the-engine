[index.html](https://github.com/user-attachments/files/26544216/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Building the Business & IT Enablement Engine — Ivoclar</title>
<link href="https://fonts.googleapis.com/css2?family=Outfit:wght@300;400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --bg: #0a0f1a;
  --bg-card-solid: #131a2b;
  --text: #f0f2f8;
  --text-mid: #b0b8cc;
  --text-dim: #8892ab;
  --amber: #f5a623;
  --amber-glow: rgba(245,166,35,0.12);
  --cyan: #3dd8e8;
  --cyan-glow: rgba(61,216,232,0.10);
  --red: #f06060;
  --red-glow: rgba(240,96,96,0.10);
  --green: #42d89a;
  --green-glow: rgba(66,216,154,0.10);
  --violet: #b094f8;
  --violet-glow: rgba(176,148,248,0.10);
  --border: rgba(255,255,255,0.06);
}
*{margin:0;padding:0;box-sizing:border-box}
body{font-family:'Outfit',sans-serif;background:var(--bg);color:var(--text);overflow:hidden;height:100vh;width:100vw}
body::before{content:'';position:fixed;inset:0;background:radial-gradient(ellipse at 20% 50%,rgba(61,216,232,0.025) 0%,transparent 60%),radial-gradient(ellipse at 80% 20%,rgba(245,166,35,0.025) 0%,transparent 50%);pointer-events:none}
.counter{position:fixed;top:28px;right:40px;font-family:'JetBrains Mono',monospace;font-size:17px;color:var(--text-dim);z-index:200;background:rgba(10,15,26,0.7);padding:6px 14px;border-radius:6px;border:1px solid var(--border);backdrop-filter:blur(8px)}
.sb{position:fixed;left:0;top:0;bottom:0;width:240px;background:rgba(10,15,26,0.95);border-right:1px solid rgba(245,166,35,0.06);z-index:150;display:flex;flex-direction:column;padding:28px 0;backdrop-filter:blur(12px);overflow-y:auto}
.sb-logo{padding:0 20px 20px;font-family:'JetBrains Mono',monospace;font-size:10px;text-transform:uppercase;letter-spacing:3px;color:var(--amber);border-bottom:1px solid rgba(245,166,35,0.08);margin-bottom:10px}
.sb-i{padding:9px 20px;font-size:12.5px;color:var(--text-dim);cursor:pointer;transition:all .25s;border-left:2px solid transparent;display:flex;align-items:center;gap:9px}
.sb-i:hover{color:var(--text);background:rgba(255,255,255,0.02)}
.sb-i.on{color:var(--amber);background:var(--amber-glow);border-left-color:var(--amber);font-weight:600}
.sb-i .n{font-family:'JetBrains Mono',monospace;font-size:9px;opacity:.4;min-width:20px}
.sb-sep{height:1px;background:var(--border);margin:8px 20px}
.prog{position:fixed;bottom:0;left:240px;right:0;height:3px;background:rgba(245,166,35,0.04);z-index:200}
.prog-fill{height:100%;background:linear-gradient(90deg,var(--amber),var(--cyan));transition:width .5s}
.sw{margin-left:240px;height:100vh;position:relative;overflow:hidden}
.sl{position:absolute;inset:0;display:flex;align-items:center;justify-content:center;padding:48px 72px;opacity:0;transform:translateY(16px);transition:opacity .5s cubic-bezier(.4,0,.2,1),transform .5s cubic-bezier(.4,0,.2,1);pointer-events:none;overflow-y:auto}
.sl.on{opacity:1;transform:translateY(0);pointer-events:all}
.si{width:100%;max-width:1200px;display:flex;flex-direction:column;justify-content:center;min-height:55vh}
.tag{font-family:'JetBrains Mono',monospace;font-size:12px;text-transform:uppercase;letter-spacing:3.5px;color:var(--amber);margin-bottom:14px;display:flex;align-items:center;gap:8px}
.tag::before{content:'';display:inline-block;width:18px;height:1px;background:var(--amber);opacity:.5}
h1{font-size:52px;font-weight:800;line-height:1.12;margin-bottom:16px;letter-spacing:-1px;color:var(--text)}
h2{font-size:40px;font-weight:800;line-height:1.18;margin-bottom:14px;letter-spacing:-.5px;color:var(--text)}
h3{font-size:20px;font-weight:400;color:var(--text-mid);line-height:1.55}
.hi{color:var(--amber)}.hc{color:var(--cyan)}.hr{color:var(--red)}.hg{color:var(--green)}.hv{color:var(--violet)}
.cen{text-align:center;align-items:center;display:flex;flex-direction:column}
.g2{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:32px}
.g3{display:grid;grid-template-columns:1fr 1fr 1fr;gap:20px;margin-top:32px}
.cd{background:var(--bg-card-solid);border:1px solid var(--border);border-radius:14px;padding:24px 22px;position:relative;overflow:hidden}
.cd::after{content:'';position:absolute;top:0;left:0;width:3px;height:100%}
.cd:nth-child(1)::after{background:var(--red)}.cd:nth-child(2)::after{background:var(--amber)}
.cd:nth-child(3)::after{background:var(--cyan)}.cd:nth-child(4)::after{background:var(--violet)}
.cd h4{font-size:16px;font-weight:600;margin-bottom:3px;color:var(--text)}
.cd p{font-size:13.5px;color:var(--text-mid);line-height:1.55}
.shift{display:flex;align-items:center;justify-content:center;gap:28px;margin-top:36px}
.shb{padding:28px 40px;border-radius:14px;text-align:center;min-width:260px}
.shb.fr{background:var(--red-glow);border:1px solid rgba(240,96,96,0.12)}
.shb.to{background:var(--green-glow);border:1px solid rgba(66,216,154,0.12)}
.shb h4{font-size:21px;font-weight:700}.shb.fr h4{color:var(--red)}.shb.to h4{color:var(--green)}
.shb p{font-size:13.5px;color:var(--text-mid);margin-top:4px}
.sha{font-size:28px;color:var(--text-dim);opacity:.3}
.rw{width:100%;height:4px;background:repeating-linear-gradient(90deg,var(--amber) 0,var(--amber) 24px,transparent 24px,transparent 40px);opacity:.15;border-radius:2px}
.fl{display:flex;margin-top:30px;position:relative}
.fl-line{position:absolute;top:24px;left:44px;right:44px;height:2px;background:linear-gradient(90deg,var(--red),var(--amber),var(--cyan),var(--green),var(--violet));opacity:.15}
.fl-s{flex:1;text-align:center;padding:0 5px;display:flex;flex-direction:column;align-items:center;gap:6px;position:relative;z-index:1}
.fl-n{width:48px;height:48px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:'JetBrains Mono',monospace;font-size:17px;font-weight:700;border:2px solid}
.fl-s:nth-child(2) .fl-n{background:var(--red-glow);border-color:var(--red);color:var(--red)}
.fl-s:nth-child(3) .fl-n{background:var(--amber-glow);border-color:var(--amber);color:var(--amber)}
.fl-s:nth-child(4) .fl-n{background:var(--cyan-glow);border-color:var(--cyan);color:var(--cyan)}
.fl-s:nth-child(5) .fl-n{background:var(--green-glow);border-color:var(--green);color:var(--green)}
.fl-s:nth-child(6) .fl-n{background:var(--violet-glow);border-color:var(--violet);color:var(--violet)}
.fl-t{font-weight:600;font-size:14px;color:var(--text)}.fl-d{font-size:12px;color:var(--text-mid);line-height:1.45}
.gov{display:flex;flex-direction:column;align-items:center;gap:10px;margin-top:24px}
.gov-r{display:flex;gap:10px;align-items:center;justify-content:center}
.gov-b{background:var(--bg-card-solid);border:1px solid var(--border);border-radius:11px;padding:14px 18px;text-align:center}
.gov-b.tw{background:linear-gradient(135deg,var(--amber-glow),var(--cyan-glow));border-color:rgba(245,166,35,0.15);min-width:260px}
.gov-b h4{font-size:14px;font-weight:600;margin-bottom:1px;color:var(--text)}.gov-b p{font-size:12px;color:var(--text-mid)}
.gov-v{width:2px;height:18px;background:rgba(255,255,255,0.45)}
.gov-h{width:16px;height:2px;background:rgba(255,255,255,0.45)}
.rm{display:flex;gap:18px;margin-top:32px}
.rm-p{flex:1;background:var(--bg-card-solid);border-radius:14px;padding:22px 20px;border:1px solid var(--border);position:relative;overflow:hidden}
.rm-p::before{content:'';position:absolute;top:0;left:0;right:0;height:3px}
.rm-p:nth-child(1)::before{background:var(--red)}.rm-p:nth-child(2)::before{background:var(--amber)}.rm-p:nth-child(3)::before{background:var(--green)}
.rm-tg{font-family:'JetBrains Mono',monospace;font-size:10px;text-transform:uppercase;letter-spacing:2px;margin-bottom:4px}
.rm-p:nth-child(1) .rm-tg{color:var(--red)}.rm-p:nth-child(2) .rm-tg{color:var(--amber)}.rm-p:nth-child(3) .rm-tg{color:var(--green)}
.rm-p h4{font-size:18px;font-weight:700;margin-bottom:8px;color:var(--text)}
.rm-p ul{list-style:none;display:flex;flex-direction:column;gap:5px}
.rm-p li{font-size:13px;color:var(--text-mid);padding-left:14px;position:relative;line-height:1.45}
.rm-p li::before{content:'>';position:absolute;left:0;opacity:.35;font-family:'JetBrains Mono',monospace;font-size:10px}
.pil{display:flex;gap:16px;margin-top:32px}
.pil-c{flex:1;background:var(--bg-card-solid);border-radius:14px;padding:22px 18px;border:1px solid var(--border);text-align:center}
.pil-c h4{font-size:15px;font-weight:600;margin-bottom:4px;color:var(--text)}
.pil-c p{font-size:13px;color:var(--text-mid);line-height:1.55}
.qt{background:var(--bg-card-solid);border-left:4px solid var(--amber);border-radius:0 12px 12px 0;padding:20px 24px;margin-top:28px;font-size:17px;font-style:italic;line-height:1.6;color:var(--text-mid)}
.tbl{width:100%;border-collapse:separate;border-spacing:0;margin-top:28px;border-radius:12px;overflow:hidden;border:1px solid var(--border)}
.tbl th{background:rgba(245,166,35,0.08);padding:11px 16px;text-align:left;font-size:12px;font-weight:600;color:var(--amber);text-transform:uppercase;letter-spacing:1px;font-family:'JetBrains Mono',monospace;border-bottom:1px solid var(--border)}
.tbl td{padding:12px 16px;font-size:13.5px;color:var(--text-mid);line-height:1.5;border-bottom:1px solid var(--border);vertical-align:top}
.tbl tr:last-child td{border-bottom:none}
.tbl td:first-child{font-weight:600;color:var(--text);white-space:nowrap}
.tbl .stop{color:var(--red);font-weight:500}.tbl .start{color:var(--green);font-weight:500}
.donut-wrap{display:flex;align-items:center;gap:44px;margin-top:32px}
.donut-legend{display:flex;flex-direction:column;gap:14px;flex:1}
.donut-item{display:flex;align-items:flex-start;gap:12px}
.donut-dot{width:13px;height:13px;border-radius:4px;flex-shrink:0;margin-top:4px}
.donut-item h4{font-size:15px;font-weight:600;color:var(--text);margin-bottom:2px}
.donut-item p{font-size:13px;color:var(--text-mid);line-height:1.5}
.sc{display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-top:30px}
.sc-c{background:var(--bg-card-solid);border-radius:14px;padding:24px;border:1px solid var(--border);display:flex;align-items:center;gap:16px}
.sc-v{font-family:'JetBrains Mono',monospace;font-size:34px;font-weight:700;flex-shrink:0}
.sc-c:nth-child(1) .sc-v{color:var(--amber)}.sc-c:nth-child(2) .sc-v{color:var(--cyan)}
.sc-c:nth-child(3) .sc-v{color:var(--green)}.sc-c:nth-child(4) .sc-v{color:var(--violet)}
.sc-c h4{font-size:15px;font-weight:600;margin-bottom:2px;color:var(--text)}
.sc-c p{font-size:12.5px;color:var(--text-mid);line-height:1.45}
.tbm-row{display:flex;gap:22px;margin-top:30px}
.tbm-box{flex:1;background:var(--bg-card-solid);border-radius:14px;padding:24px 22px;border:1px solid var(--border);position:relative;overflow:hidden}
.tbm-box::before{content:'';position:absolute;top:0;left:0;right:0;height:3px}
.tbm-box:first-child::before{background:var(--amber)}.tbm-box:last-child::before{background:var(--cyan)}
.tbm-label{font-family:'JetBrains Mono',monospace;font-size:10px;text-transform:uppercase;letter-spacing:2px;margin-bottom:8px}
.tbm-box:first-child .tbm-label{color:var(--amber)}.tbm-box:last-child .tbm-label{color:var(--cyan)}
.tbm-box h4{font-size:18px;font-weight:700;color:var(--text);margin-bottom:6px}
.tbm-box p{font-size:13.5px;color:var(--text-mid);line-height:1.55}
.tbm-example{margin-top:12px;padding:10px 14px;background:rgba(255,255,255,0.03);border-radius:8px;border:1px solid var(--border)}
.tbm-example p{font-size:12.5px;color:var(--text-mid);line-height:1.45}
.tbm-example strong{color:var(--text)}
.notes-panel{position:fixed;bottom:0;left:240px;right:0;max-height:38vh;background:rgba(8,12,22,0.97);border-top:2px solid var(--amber);z-index:300;overflow-y:auto;padding:18px 32px 22px;transform:translateY(100%);transition:transform .35s cubic-bezier(.4,0,.2,1);backdrop-filter:blur(12px)}
.notes-panel.show{transform:translateY(0)}
.notes-panel h5{font-family:'JetBrains Mono',monospace;font-size:10px;text-transform:uppercase;letter-spacing:2px;color:var(--amber);margin-bottom:10px;opacity:.7}
.notes-panel .script{font-size:16px;line-height:1.75;color:var(--text-mid);max-width:840px}
.notes-panel .script .pause{display:inline-block;font-family:'JetBrains Mono',monospace;font-size:9px;background:rgba(245,166,35,0.12);color:var(--amber);padding:2px 7px;border-radius:4px;vertical-align:middle;margin:0 3px;letter-spacing:1px}
.notes-panel .timing{font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--text-dim);margin-top:10px;opacity:.6}
.sl.on .tag{animation:fu .4s .05s both}
.sl.on h1,.sl.on h2{animation:fu .4s .1s both}
.sl.on h3{animation:fu .4s .18s both}
.sl.on .cd:nth-child(1),.sl.on .pil-c:nth-child(1){animation:fu .35s .12s both}
.sl.on .cd:nth-child(2),.sl.on .pil-c:nth-child(2){animation:fu .35s .2s both}
.sl.on .cd:nth-child(3),.sl.on .pil-c:nth-child(3){animation:fu .35s .28s both}
.sl.on .cd:nth-child(4),.sl.on .pil-c:nth-child(4){animation:fu .35s .36s both}
.sl.on .shift,.sl.on .par,.sl.on .fl,.sl.on .gov,.sl.on .rm,.sl.on .sc,.sl.on .qt,.sl.on .tbl,.sl.on .donut-wrap,.sl.on .tbm-row,.sl.on .pil,.sl.on .g2,.sl.on .g3{animation:fu .45s .15s both}
@keyframes fu{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}
.hint{position:fixed;bottom:14px;right:32px;font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--text-dim);opacity:.25;z-index:200}
.hint kbd{display:inline-block;padding:2px 6px;border:1px solid rgba(255,255,255,0.08);border-radius:3px;margin:0 1px;font-size:9px}
</style>
</head>
<body>
<div class="counter"><span id="cur">1</span> / <span id="tot">14</span></div>
<nav class="sb">
  <div class="sb-logo">Enablement Engine</div>
  <div class="sb-i" data-c="exec" onclick="go(0)"><span class="n">00</span> Executive View</div>
  <div class="sb-i" data-c="portfolio" onclick="go(1)"><span class="n">00</span> 50 / 30 / 20</div>
  <div class="sb-i" data-c="pillars" onclick="go(2)"><span class="n">00</span> 4-Pillar Strategy</div>
  <div class="sb-i" data-c="tbm" onclick="go(3)"><span class="n">00</span> TBM &amp; FinOps</div>
  <div class="sb-i" data-c="scorecard" onclick="go(4)"><span class="n">00</span> Scorecard</div>
  <div class="sb-sep"></div>
  <div class="sb-i" data-c="airport" onclick="go(5)"><span class="n">01</span> The Airport</div>
  <div class="sb-i" data-c="pareto" onclick="go(6)"><span class="n">02</span> Pareto</div>
  <div class="sb-i" data-c="engine" onclick="go(7)"><span class="n">03</span> The Engine</div>
  <div class="sb-i" data-c="d2v" onclick="go(8)"><span class="n">04</span> Demand-to-Value</div>
  <div class="sb-i" data-c="ai" onclick="go(9)"><span class="n">05</span> AI + FinOps Gate</div>
  <div class="sb-i" data-c="shadow" onclick="go(10)"><span class="n">06</span> Shadow Demand</div>
  <div class="sb-i" data-c="road" onclick="go(11)"><span class="n">07</span> 365-Day Plan</div>
  <div class="sb-i" data-c="stake" onclick="go(12)"><span class="n">08</span> Stakeholders</div>
  <div class="sb-i" data-c="close" onclick="go(13)"><span class="n">fin</span> Closing</div>
</nav>
<div class="prog"><div class="prog-fill" id="prog"></div></div>
<div class="hint"><kbd>&larr;</kbd><kbd>&rarr;</kbd> slides · <kbd>N</kbd> notes · <kbd>F</kbd> full</div>
<div class="notes-panel" id="notes"><h5>Speaker Notes</h5><div class="script" id="scriptText"></div><div class="timing" id="scriptTime"></div></div>

<div class="sw">

<!-- ═══ INTRO BLOCK (5 slides, ~11 min) ═══ -->

<!-- 0: EXECUTIVE OVERVIEW -->
<div class="sl on" data-c="exec" data-time="~2 min" data-script="Good afternoon. Thank you for having me back. Before I go into the details, let me give you the big picture first. Ivoclar IT today works as a cost center. It takes orders, it delivers. But it does not steer. My plan is to change that. I want to turn IT into a value engine. That means three things. First, transparency — everyone sees the pipeline, what it costs, what it delivers. Second, value — we measure outcomes, not just activity. Third, AI-readiness — not more pilots, but the governance to actually scale them. And everything backed by real financials — TBM and FinOps — so we prove value in Euros, not in PowerPoint. Let me walk you through each layer.">
  <div class="si cen">
    <div class="tag">Executive Overview</div>
    <h1 style="max-width:880px">From <span class="hr">&ldquo;Cost Center&rdquo;</span><br>to <span class="hg">&ldquo;Value Engine&rdquo;</span></h1>
    <h3 style="max-width:680px">Building the Business &amp; IT Enablement Engine — my strategic concept for the first 12 months.</h3>
    <div style="display:flex;gap:18px;margin-top:42px;justify-content:center;flex-wrap:wrap">
      <div style="text-align:center;padding:16px 26px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:12px;min-width:150px"><div style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--amber);letter-spacing:1px;margin-bottom:5px">TRANSPARENCY</div><div style="font-size:13.5px;color:var(--text-mid)">See the full pipeline</div></div>
      <div style="text-align:center;padding:16px 26px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:12px;min-width:150px"><div style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--cyan);letter-spacing:1px;margin-bottom:5px">VALUE</div><div style="font-size:13.5px;color:var(--text-mid)">Measure outcomes</div></div>
      <div style="text-align:center;padding:16px 26px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:12px;min-width:150px"><div style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--green);letter-spacing:1px;margin-bottom:5px">AI-READY</div><div style="font-size:13.5px;color:var(--text-mid)">Govern, then scale</div></div>
      <div style="text-align:center;padding:16px 26px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:12px;min-width:150px"><div style="font-family:'JetBrains Mono',monospace;font-size:11px;color:var(--violet);letter-spacing:1px;margin-bottom:5px">TBM &amp; FINOPS</div><div style="font-size:13.5px;color:var(--text-mid)">Prove it in Euros</div></div>
    </div>
    <div class="rw" style="margin-top:42px;width:38%"></div>
  </div>
</div>

<!-- 1: 50/30/20 -->
<div class="sl" data-c="portfolio" data-time="~2 min" data-script="Right now, IT spending is reactive. Whoever shouts loudest gets resources. I want to change that with a clear split. Fifty percent goes to strategic value — projects that actually grow the business. Thirty percent goes to IT health — keeping things safe and modern, and that includes cleaning up unused licenses. Twenty percent goes to innovation — AI experiments in a safe sandbox. This ratio is not a fixed rule. The Demand Board reviews it every quarter. But having a target stops the drift.">
  <div class="si">
    <div class="tag">The Strategic Balance</div>
    <h2>The <span class="hi">50 / 30 / 20</span> Portfolio</h2>
    <div style="display:flex;align-items:center;gap:56px;margin-top:40px">
      <div style="flex-shrink:0;position:relative">
        <svg viewBox="0 0 260 260" width="300" height="300">
          <circle cx="130" cy="130" r="95" fill="none" stroke="rgba(255,255,255,0.03)" stroke-width="36"/>
          <circle cx="130" cy="130" r="95" fill="none" stroke="var(--amber)" stroke-width="36" stroke-dasharray="298.5 597" stroke-dashoffset="0" transform="rotate(-90 130 130)" opacity=".9"/>
          <circle cx="130" cy="130" r="95" fill="none" stroke="var(--cyan)" stroke-width="36" stroke-dasharray="179.1 597" stroke-dashoffset="-298.5" transform="rotate(-90 130 130)" opacity=".9"/>
          <circle cx="130" cy="130" r="95" fill="none" stroke="var(--green)" stroke-width="36" stroke-dasharray="119.4 597" stroke-dashoffset="-477.6" transform="rotate(-90 130 130)" opacity=".9"/>
          <text x="130" y="122" text-anchor="middle" font-family="'JetBrains Mono',monospace" font-size="32" font-weight="800" fill="var(--text)">50/30</text>
          <text x="130" y="152" text-anchor="middle" font-family="'JetBrains Mono',monospace" font-size="32" font-weight="800" fill="var(--text)">/20</text>
        </svg>
      </div>
      <div style="display:flex;flex-direction:column;gap:22px;flex:1">
        <div style="display:flex;align-items:flex-start;gap:16px">
          <div style="width:18px;height:18px;border-radius:5px;flex-shrink:0;margin-top:3px;background:var(--amber)"></div>
          <div>
            <h4 style="font-size:20px;font-weight:700;color:var(--text);margin-bottom:3px">50% — Strategic Value</h4>
            <p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Projects that grow the business</p>
            <p style="font-size:14.5px;color:var(--text-mid);line-height:1.5">CRM rollouts, digital workflows, new market enablement. This is where IT becomes a growth engine.</p>
          </div>
        </div>
        <div style="display:flex;align-items:flex-start;gap:16px">
          <div style="width:18px;height:18px;border-radius:5px;flex-shrink:0;margin-top:3px;background:var(--cyan)"></div>
          <div>
            <h4 style="font-size:20px;font-weight:700;color:var(--text);margin-bottom:3px">30% — IT Health</h4>
            <p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Keep systems safe, modern, and compliant</p>
            <p style="font-size:14.5px;color:var(--text-mid);line-height:1.5">Infrastructure, patching, and license management. Stop paying for software nobody uses.</p>
          </div>
        </div>
        <div style="display:flex;align-items:flex-start;gap:16px">
          <div style="width:18px;height:18px;border-radius:5px;flex-shrink:0;margin-top:3px;background:var(--green)"></div>
          <div>
            <h4 style="font-size:20px;font-weight:700;color:var(--text);margin-bottom:3px">20% — Innovation</h4>
            <p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Try new things in a safe space</p>
            <p style="font-size:14.5px;color:var(--text-mid);line-height:1.5">AI experiments in a secure sandbox. Structured pilots with clear gates — not open-ended R&amp;D.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

<!-- 2: 4-PILLAR TABLE -->
<div class="sl" data-c="pillars" data-time="~2.5 min" data-script="Here is the strategy in simple language. Four pillars, each one solving a real problem from the case study. Demand — we stop hallway requests. One Front Door, one way in. Priority — we stop the loudest voice from winning. We use a scoring system instead. AI — we stop the unsecured hype. We build a sandbox-to-scale funnel. Process — we stop digitizing the mess. Global Process Owners have to approve the workflow before we automate anything. Four problems, four answers.">
  <div class="si">
    <div class="tag">The 4-Pillar Strategy</div>
    <h2><span class="hr">Why</span> · <span class="hg">What</span> · <span class="hi">How</span></h2>
    <table class="tbl">
      <thead><tr><th style="width:90px">Pillar</th><th style="width:180px;color:var(--red)">Stop this (Why)</th><th style="color:var(--green)">Start this (What)</th><th style="width:180px;color:var(--amber)">How</th></tr></thead>
      <tbody>
        <tr><td>Demand</td><td><span class="stop">Hallway requests</span></td><td><span class="start">One &ldquo;Front Door&rdquo;</span> — every request enters the same way</td><td>Intake form + triage SLA</td></tr>
        <tr><td>Priority</td><td><span class="stop">&ldquo;Loudest voice wins&rdquo;</span></td><td><span class="start">Value-scoring system</span> — impact, effort, strategy fit</td><td>Bi-weekly Demand Board</td></tr>
        <tr><td>AI</td><td><span class="stop">Unsecured hype</span></td><td><span class="start">Sandbox-to-Scale funnel</span> — prove data readiness + ROI</td><td>AI Scorecard + Review Board</td></tr>
        <tr><td>Process</td><td><span class="stop">&ldquo;Digitizing the mess&rdquo;</span></td><td><span class="start">GPOs approve first</span> — standardize, then automate</td><td>GPO Council + process gates</td></tr>
      </tbody>
    </table>
  </div>
</div>

<!-- 3: TBM & FINOPS -->
<div class="sl" data-c="tbm" data-time="~2.5 min" data-script="None of this means anything if we cannot show the money. That is where TBM and FinOps come in. Two views on the same question — where does the money go, and is it worth it? The macro view is TBM — Technology Business Management. We take every Euro spent on IT and map it to the business unit it supports. So we can answer things like: what does IT cost for dental product development? Today, IT costs are a black box. TBM opens it. The micro view is FinOps. Think of it like a bakery. You do not just know your total costs — you know what it costs to make one croissant. We apply the same thinking to AI. Cost per AI-generated summary? Twelve cents. Manual cost? Four fifty. Scale it. Cost per AI quality check? Eight twenty. Manual cost? Three. Do not scale it. Simple math. Together, TBM and FinOps are the financial cockpit of the Enablement Engine.">
  <div class="si">
    <div class="tag">The Financial Engine</div>
    <h2><span class="hi">TBM</span> &amp; <span class="hc">FinOps</span> — prove value in Euros</h2>
    <h3>Two views on one question: where does the money go, and is it worth it?</h3>
    <div class="tbm-row">
      <div class="tbm-box"><div class="tbm-label">Macro View — TBM</div><h4>Where every Euro goes</h4><p>Map IT costs to business units. No more black-box budgets.</p><div class="tbm-example"><p><strong>Example:</strong> &ldquo;IT cost for dental product dev = CHF 2.4M/year — split by infrastructure, apps, and people.&rdquo;</p></div></div>
      <div class="tbm-box"><div class="tbm-label">Micro View — FinOps</div><h4>The cost of one croissant</h4><p>Know the unit cost of every IT service and AI action. Compare it to the manual alternative.</p><div class="tbm-example"><p><strong>AI example:</strong> One AI-written summary costs 12 cents. Doing it by hand costs 4.50. That saves money — scale it. One AI quality check costs 8.20. Doing it by hand costs 3. That loses money — stop it.</p></div></div>
    </div>
    <div class="qt" style="margin-top:22px;border-left-color:var(--cyan)">&ldquo;TBM tells the board where the money goes. FinOps tells the teams whether it is worth spending.&rdquo;</div>
  </div>
</div>

<!-- 4: SCORECARD -->
<div class="sl" data-c="scorecard" data-time="~2 min" data-script="Four KPIs that tell us if the engine works. Cost recovery — fifteen percent saving by cleaning up unused licenses. That is the fastest win. Decision speed — thirty percent faster from idea to yes or no. AI efficiency — if AI costs more than doing it by hand, we do not scale it. If the AI croissant is more expensive, we do not scale. Portfolio balance — every quarter we check if we are spending in the right places. Four numbers. Board-level clarity. Now let me show you how we build this — I will use a picture.">
  <div class="si">
    <div class="tag">The Success Scorecard</div>
    <h2>Four numbers that <span class="hi">matter</span></h2>
    <div class="sc">
      <div class="sc-c"><div style="text-align:center;flex-shrink:0;min-width:80px"><div class="sc-v" style="color:var(--amber)">15%</div><div style="font-size:10px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;margin-top:2px">saved</div></div><div><h4>Cost Recovery</h4><p>We find software nobody uses and stop paying for it. Target: save 15% of license costs in year one.</p></div></div>
      <div class="sc-c"><div style="text-align:center;flex-shrink:0;min-width:80px"><div class="sc-v" style="color:var(--cyan)">&ndash;30%</div><div style="font-size:10px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;margin-top:2px">faster</div></div><div><h4>Decision Speed</h4><p>Today people wait weeks for an answer. Target: cut that waiting time by 30%.</p></div></div>
      <div class="sc-c"><div style="text-align:center;flex-shrink:0;min-width:80px"><div class="sc-v" style="color:var(--green)">&lt; 1x</div><div style="font-size:10px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;margin-top:2px">vs. manual</div></div><div><h4>AI Efficiency</h4><p>Every AI solution must cost less than doing the same job by hand. If not, we do not scale it.</p></div></div>
      <div class="sc-c"><div style="text-align:center;flex-shrink:0;min-width:80px"><div class="sc-v" style="color:var(--violet)">50/30/20</div><div style="font-size:10px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;margin-top:2px">ratio</div></div><div><h4>Portfolio Balance</h4><p>50% growth, 30% health, 20% innovation. We check every quarter if the split is still right.</p></div></div>
    </div>
    <div class="rw" style="margin-top:34px;width:32%"></div>
  </div>
</div>

<!-- ═══ DEEP DIVE (8 slides, ~17 min) ═══ -->

<!-- 5: THE AIRPORT + PAIN POINTS -->
<div class="sl" data-c="airport" data-time="~2 min" data-script="Let me paint a picture. Imagine Ivoclar IT is a busy international airport. Planes — your IT requests — landing from everywhere. Pilots calling different numbers, landing on side runways, sometimes not even announcing. There is no single control tower. That is today. IT delivers — but it does not steer. What is broken? Four things. No flight control — requests through side channels. Blocked runway — loudest voice lands first. Rogue test flights — AI hype without rules. Terminal chaos — every process works differently. These four are not separate. They form a chain.">
  <div class="si">
    <div class="tag">The Metaphor</div>
    <h1>IT is a busy airport — <span class="hr">no control tower</span></h1>
    <div class="g2" style="margin-top:28px">
      <div class="cd"><h4>No Flight Control — Intake Chaos</h4><p>Requests through side channels. No single front door.</p></div>
      <div class="cd"><h4>Blocked Runway — Prioritization Jam</h4><p>Too many planes. Loudest voice lands first. IT maintenance pushed away.</p></div>
      <div class="cd"><h4>Rogue Test Flights — AI Hype</h4><p>Many AI pilots, no rulebook. Nobody knows which are safe to scale.</p></div>
      <div class="cd"><h4>Terminal Chaos — Process Fragmentation</h4><p>Every terminal works differently. Wasting time and blocking capacity.</p></div>
    </div>
  </div>
</div>

<!-- 6: PARETO -->
<div class="sl" data-c="pareto" data-time="~2 min" data-script="Now — not all four problems are equal. As a project manager, my first instinct is Pareto. Where does the pain actually sit? Look at this. Intake and the missing front door — that is thirty-eight percent of the problem. Portfolio prioritization — twenty-seven percent. Together, that is sixty-five percent. Add AI governance at twenty, and you are at eighty-five. The point is: if you fix just the first two — intake and prioritization — you solve about eighty percent of the chaos. The other two become much easier once the core engine is running. So my approach is simple: build the control tower first. Then the flight plan. Then the test programs. Do not try to fix everything at once.">
  <div class="si">
    <div class="tag">The Law of the Vital Few</div>
    <h2>Pareto: <span class="hi">fix these two first</span></h2>
    <div style="display:flex;gap:36px;align-items:flex-end;margin-top:32px">
      <div style="flex:1.3;display:flex;align-items:flex-end;gap:12px;height:280px;padding-bottom:28px;border-bottom:2px solid var(--border);position:relative">
        <div style="position:absolute;left:0;top:0;bottom:28px;width:2px;background:var(--border)"></div>
        <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative">
          <div style="font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:700;color:var(--red)">38%</div>
          <div style="width:100%;max-width:68px;height:228px;border-radius:5px 5px 0 0;background:linear-gradient(180deg,var(--red),rgba(240,96,96,0.35))"></div>
          <div style="font-size:10px;color:var(--text-dim);text-align:center;font-family:'JetBrains Mono',monospace;line-height:1.3;position:absolute;bottom:-24px;white-space:nowrap">Intake &amp;<br>Front Door</div>
        </div>
        <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative">
          <div style="font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:700;color:var(--amber)">27%</div>
          <div style="width:100%;max-width:68px;height:162px;border-radius:5px 5px 0 0;background:linear-gradient(180deg,var(--amber),rgba(245,166,35,0.35))"></div>
          <div style="font-size:10px;color:var(--text-dim);text-align:center;font-family:'JetBrains Mono',monospace;line-height:1.3;position:absolute;bottom:-24px;white-space:nowrap">Portfolio<br>Prioritization</div>
        </div>
        <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative">
          <div style="font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:700;color:var(--cyan)">20%</div>
          <div style="width:100%;max-width:68px;height:120px;border-radius:5px 5px 0 0;background:linear-gradient(180deg,var(--cyan),rgba(61,216,232,0.35))"></div>
          <div style="font-size:10px;color:var(--text-dim);text-align:center;font-family:'JetBrains Mono',monospace;line-height:1.3;position:absolute;bottom:-24px;white-space:nowrap">AI<br>Governance</div>
        </div>
        <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative">
          <div style="font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:700;color:var(--violet)">10%</div>
          <div style="width:100%;max-width:68px;height:60px;border-radius:5px 5px 0 0;background:linear-gradient(180deg,var(--violet),rgba(176,148,248,0.35))"></div>
          <div style="font-size:10px;color:var(--text-dim);text-align:center;font-family:'JetBrains Mono',monospace;line-height:1.3;position:absolute;bottom:-24px;white-space:nowrap">Process<br>Standards</div>
        </div>
        <div style="flex:1;display:flex;flex-direction:column;align-items:center;gap:5px;position:relative">
          <div style="font-family:'JetBrains Mono',monospace;font-size:13px;font-weight:700;color:var(--text-dim)">5%</div>
          <div style="width:100%;max-width:68px;height:30px;border-radius:5px 5px 0 0;background:linear-gradient(180deg,rgba(255,255,255,0.25),rgba(255,255,255,0.08))"></div>
          <div style="font-size:10px;color:var(--text-dim);text-align:center;font-family:'JetBrains Mono',monospace;line-height:1.3;position:absolute;bottom:-24px;white-space:nowrap">Other</div>
        </div>
        <svg style="position:absolute;top:0;left:0;right:0;bottom:28px;pointer-events:none" viewBox="0 0 500 210" preserveAspectRatio="none"><polyline points="50,131 150,69 250,27 350,6 450,0" fill="none" stroke="var(--amber)" stroke-width="2.5" stroke-linecap="round" opacity=".55"/><line x1="0" y1="42" x2="500" y2="42" stroke="var(--amber)" stroke-width="1" stroke-dasharray="6,4" opacity=".15"/><text x="505" y="46" fill="var(--amber)" font-size="11" font-family="JetBrains Mono" opacity=".45">80%</text></svg>
      </div>
      <div style="flex:.7;padding-bottom:28px">
        <div style="font-size:88px;font-weight:800;line-height:1;background:linear-gradient(135deg,var(--amber),var(--red));-webkit-background-clip:text;-webkit-text-fill-color:transparent;background-clip:text">80%</div>
        <div style="font-size:20px;font-weight:700;margin-top:6px;color:var(--text)">of chaos solved by <span class="hi">2 levers</span></div>
        <div style="font-size:15px;color:var(--text-mid);line-height:1.6;margin-top:10px"><strong style="color:var(--text)">Fix intake + prioritization first.</strong> Everything else gets easier once the core engine runs.</div>
        <div style="margin-top:14px;padding:12px 16px;background:var(--amber-glow);border-radius:9px;border:1px solid rgba(245,166,35,0.08);font-size:15px;color:var(--text-mid)"><strong style="color:var(--amber)">My approach:</strong><br>Build the control tower first. Then flight plan. Then test programs.</div>
      </div>
    </div>
  </div>
</div>

<!-- 7: THE ENGINE — CONTROL TOWER + GOVERNANCE -->
<div class="sl" data-c="engine" data-time="~3 min" data-script="So here is the engine. Component A — the control tower. Today, requests come through dozens of channels. The first thing I would do is create one Front Door. One place where every IT request goes. Like filing a flight plan before you take off. Behind that, a triage function. Small requests get fast-tracked. Bigger ones go to the Demand Board for proper scoring. Now, who uses this system? At the bottom you see three groups. Business partners — the departments who need IT. IT delivery — the teams who build and run things. And the GPOs — that stands for Global Process Owners. These are the people who own the end-to-end business processes, like order-to-cash or product lifecycle. They define how work should flow before we automate it. All three groups submit their requests through the same Front Door. Then governance decides the order. IT Steering Committee quarterly for the big strategic calls. Demand Board bi-weekly — that is where real prioritization happens. AI Review Board monthly for use cases that need a data readiness check. Everyone sees the same flight board. No shortcuts, no side channels. And here is what makes this different from a regular org chart — every decision these boards make is backed by telemetry. Real data. Usage metrics. Cost per service. Adoption rates. Performance trends. No more gut feeling. No more loudest voice. The data decides.">
  <div class="si">
    <div class="tag">A — The Control Tower &amp; Governance</div>
    <h2>One <span class="hi">&ldquo;Front Door&rdquo;</span> — lean governance behind it</h2>
    <div class="gov">
      <div style="display:flex;gap:10px;justify-content:center;align-items:center">
        <div class="gov-b" style="flex:1;max-width:200px;border-color:rgba(240,96,96,0.15)"><h4 style="color:var(--text)">Business Partners</h4><p>Departments that need IT</p></div>
        <div class="gov-h"></div>
        <div class="gov-b" style="flex:1;max-width:200px;border-color:rgba(61,216,232,0.15)"><h4 style="color:var(--text)">IT Delivery</h4><p>Teams who build &amp; run</p></div>
        <div class="gov-h"></div>
        <div class="gov-b" style="flex:1;max-width:200px;border-color:rgba(66,216,154,0.15)"><h4 style="color:var(--text)">GPOs</h4><p>Global Process Owners — own how work flows</p></div>
      </div>
      <div style="display:flex;align-items:center;justify-content:center;gap:6px"><div class="gov-v"></div></div>
      <div style="text-align:center;font-size:12px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;letter-spacing:1px">ALL REQUESTS GO THROUGH</div>
      <div style="display:flex;align-items:center;justify-content:center;gap:6px"><div class="gov-v"></div></div>
      <div class="gov-b tw" style="padding:16px 30px;min-width:360px"><h4 style="font-size:16px">Front Door &amp; Triage</h4><p>Single intake — one way in, no side channels</p></div>
      <div style="display:flex;align-items:center;justify-content:center;gap:6px"><div class="gov-v"></div></div>
      <div style="text-align:center;font-size:12px;color:var(--text-dim);font-family:'JetBrains Mono',monospace;letter-spacing:1px">GOVERNANCE DECIDES THE ORDER</div>
      <div style="display:flex;align-items:center;justify-content:center;gap:6px"><div class="gov-v"></div></div>
      <div style="display:flex;gap:10px;justify-content:center;align-items:center">
        <div class="gov-b" style="flex:1;max-width:220px"><h4>IT Steering</h4><p>Big strategic calls — Quarterly</p></div>
        <div class="gov-h"></div>
        <div class="gov-b" style="flex:1;max-width:220px"><h4>Demand Board</h4><p>Prioritize &amp; trade-off — Bi-weekly</p></div>
        <div class="gov-h"></div>
        <div class="gov-b" style="flex:1;max-width:220px"><h4>AI Review Board</h4><p>Data readiness check — Monthly</p></div>
      </div>
    </div>
    <div style="margin-top:20px;padding:16px 20px;background:linear-gradient(135deg,var(--cyan-glow),var(--amber-glow));border:1px solid rgba(61,216,232,0.12);border-radius:12px;display:flex;align-items:center;gap:20px">
      <div style="font-family:'JetBrains Mono',monospace;font-size:11px;text-transform:uppercase;letter-spacing:2px;color:var(--cyan);white-space:nowrap;flex-shrink:0">Telemetry-Driven</div>
      <div style="width:2px;height:28px;background:rgba(255,255,255,0.1);flex-shrink:0"></div>
      <div style="font-size:14px;color:var(--text-mid);line-height:1.5">Every board decision is backed by <strong style="color:var(--text)">real data</strong> — usage metrics, cost-per-service, adoption rates, and performance trends. No more gut feeling. No more loudest voice. The telemetry decides.</div>
    </div>
  </div>
</div>

<!-- 7: DEMAND-TO-VALUE -->
<div class="sl" data-c="d2v" data-time="~2.5 min" data-script="Component B — the flight plan. Six steps from idea to value. One, intake through the Front Door. Two, triage — small stuff gets fast-tracked. Three, a lightweight business case. I really mean lightweight — three questions: what is the expected outcome? How do we measure it? Who owns the benefit? That is it. Four, the Demand Board decides the priority. Five, execution with a clear business owner — not just IT alone. And six — this is the one most companies skip — value check after go-live. Did we actually deliver what we said we would? A flight is not successful because it took off. It is successful because passengers arrived on time.">
  <div class="si">
    <div class="tag">B — The Flight Plan: Demand-to-Value</div>
    <h2>From idea to <span class="hi">measurable value</span></h2>
    <div class="fl">
      <div class="fl-line"></div>
      <div class="fl-s"><div class="fl-n">1</div><div class="fl-t">Intake</div><div class="fl-d">One Front Door</div></div>
      <div class="fl-s"><div class="fl-n">2</div><div class="fl-t">Triage</div><div class="fl-d">Fast-track or escalate</div></div>
      <div class="fl-s"><div class="fl-n">3</div><div class="fl-t">Biz Case</div><div class="fl-d">Outcome + measure + owner</div></div>
      <div class="fl-s"><div class="fl-n">4</div><div class="fl-t">Priority</div><div class="fl-d">Demand Board decides</div></div>
      <div class="fl-s"><div class="fl-n">5</div><div class="fl-t">Delivery</div><div class="fl-d">Agile with biz owner</div></div>
      <div class="fl-s"><div class="fl-n">6</div><div class="fl-t">Value Check</div><div class="fl-d">Did passengers arrive?</div></div>
    </div>
    <div class="qt">&ldquo;A flight is not successful because it took off — it is successful because passengers arrived on time.&rdquo;</div>
  </div>
</div>

<!-- 8: AI + FINOPS GATE -->
<div class="sl" data-c="ai" data-time="~2 min" data-script="Component C — AI orchestration. Or as I call it, the test flight program. The problem is not that Ivoclar has too few AI ideas. It is that there is no structure to evaluate them. My approach: first, an AI scorecard. Same language as every other project — value, effort, risk — but with one extra gate: data readiness. Because the best AI idea is useless if the data is not there. Second, non-negotiable guardrails. Data security, architecture standards, clear ownership. Third, a sandbox. Let people experiment safely — but with a clear path from pilot to MVP to production. And fourth, the FinOps gate. Before any AI scales, we check the unit cost. Does it save more money than it costs to run? Simple math. If not, we do not scale. AI competes in the same portfolio as classic IT. One flight board, one language.">
  <div class="si">
    <div class="tag">C — AI Orchestration + FinOps Gate</div>
    <h2>Enable <span class="hc">AI</span> — with guardrails and <span class="hi">unit economics</span></h2>
    <div class="pil">
      <div class="pil-c"><h4>AI Scorecard</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">A simple checklist for every AI idea</p><p>Is it useful? Is it doable? Is the data ready? If not all three — it waits.</p></div>
      <div class="pil-c"><h4>Guardrails</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">The safety rules nobody can skip</p><p>Data must be secure. Architecture must be approved. Someone must own it.</p></div>
      <div class="pil-c"><h4>Sandbox-to-Scale</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Try small before you go big</p><p>Test it safely first. If it works, grow it step by step. Pilot &rarr; MVP &rarr; Production.</p></div>
      <div class="pil-c"><h4>FinOps Gate</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">The money check before we scale</p><p>Does this AI save more than it costs to run? If yes, scale. If no, stop.</p></div>
    </div>
  </div>
</div>

<!-- 9: SHADOW DEMAND -->
<div class="sl" data-c="shadow" data-time="~2 min" data-script="Now — one challenge I want to address head-on. In a global organization, not all demand comes from Schaan. Some comes from Latin America, Asia, other regions — where the local team reports to the regional CEO, not to headquarters IT. I call these private jets. They land on side runways, outside the system. Someone buys a tool, starts an AI subscription — not because they want to break rules, but because it is faster. You cannot stop this by building walls. You have to make the official route faster and easier than bypassing it. Three things. A fast clearance lane for low-risk requests. The radar sweep — a subscription inventory so you see what is already flying. And procurement integration so shadow tools get caught at renewal time. The principle: make the tower so good that everyone wants to use it.">
  <div class="si">
    <div class="tag">Shadow Demand: The Global Challenge</div>
    <h2><span class="hv">Private jets</span> landing outside the system</h2>
    <h3>People bypass IT because the official way is too slow. So we make the official way faster.</h3>
    <div class="g2" style="margin-top:24px">
      <div class="cd"><h4>Fast Clearance Lane</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Make the official way quicker than the workaround</p><p>Regional IT partners can approve small, low-risk requests on the spot — no need to wait for headquarters.</p></div>
      <div class="cd"><h4>Turn On the Radar</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">See what tools people are already using</p><p>We run a regular check of all subscriptions and software across regions. No blame — just visibility.</p></div>
      <div class="cd"><h4>Procurement Integration</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Catch shadow tools when the bill comes in</p><p>Finance flags unknown subscriptions at renewal time. Every tool needs an owner and a place in the portfolio.</p></div>
      <div class="cd"><h4>Delegated Control Towers</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Local people who follow global rules</p><p>Each region gets an enablement lead who can act fast — but within the same framework as everyone else.</p></div>
    </div>
  </div>
</div>

<!-- 11: 365-DAY PLAN + QUICK WINS -->
<div class="sl" data-c="road" data-time="~3 min" data-script="Three hundred and sixty-five days. Three phases. Phase one, day one to sixty: I listen. Stakeholder interviews. Pain mapping. I map where every IT Euro goes today — that is TBM cost-mapping. We take the IT budget and connect every line to a business unit. So instead of one big number, you see: this much goes to dental, this much to adhesives, this much to infrastructure. No changes yet — just building the picture and building relationships. Phase two, day sixty-one to one hundred thirty: launch and win. Front Door goes live, portfolio reset, radar sweep. Demand Board starts bi-weekly. Phase three, day one hundred thirty-one to three hundred sixty-five: stabilize, embed, grow. Governance matures. AI pilots through gates. We build a FinOps practice and gamify results — teams that save or create the most value get recognized. By day three sixty-five, we deliver the fifty-thirty-twenty portfolio view to the board.">
  <div class="si">
    <div class="tag">365-Day Plan + Quick Wins</div>
    <h2><span class="hi">Listen &rarr; Launch &rarr; Stabilize</span></h2>
    <div class="rm">
      <div class="rm-p"><div class="rm-tg">Day 1 – 60</div><h4>Listen</h4><ul><li>Stakeholder interviews &amp; pain mapping</li><li>As-is: portfolio, processes, AI landscape</li><li>Identify shadow demand patterns</li><li>TBM cost-mapping: connect every IT Euro to a business unit</li><li>Build relationships before systems</li></ul></div>
      <div class="rm-p"><div class="rm-tg">Day 61 – 130</div><h4>Launch + 3 Quick Wins</h4><ul><li>Front Door portal (48h acknowledge)</li><li>Portfolio reset: continue / pause / stop</li><li>Radar sweep: subscriptions &amp; shadow IT</li><li>Start bi-weekly Demand Board</li><li>First TBM dashboard: where every Euro goes</li></ul></div>
      <div class="rm-p"><div class="rm-tg">Day 131 – 365</div><h4>Stabilize, Embed &amp; Grow</h4><ul><li>Mature governance model</li><li>First AI pilots through proper gates</li><li>Build a FinOps practice: track unit costs</li><li>Gamify results — reward teams that save or create value</li><li>50/30/20 portfolio view to board</li></ul></div>
    </div>
  </div>
</div>

<!-- 11: STAKEHOLDERS -->
<div class="sl" data-c="stake" data-time="~1.5 min" data-script="One more thing before I close. The best engine in the world does not work if people do not use it. For business partners — co-creation, not orders from IT. I want departments to feel like co-designers, not customers. For the IT team — and I say this deliberately — I want to orchestrate, not dictate. Mike, Simon, their teams — they are the experts. My role is to enable them. Communication: regular, transparent. When wins happen, make them visible. And my change philosophy — this is very much who I am: small steps, visible results. Pull, not push. Convince through impact, not through presentations.">
  <div class="si">
    <div class="tag">Taking People on the Journey</div>
    <h2>How I work with <span class="hv">stakeholders</span></h2>
    <div class="g2">
      <div class="cd"><h4>Business Partners</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">They are co-designers, not customers</p><p>I involve departments from the start. They help shape the system, so they actually want to use it. If people feel heard, they show up.</p></div>
      <div class="cd"><h4>IT Team</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">I enable experts — I do not replace them</p><p>The existing teams are the experts. I bring structure and clarity — they bring the knowledge. My role is to support them, not to step on their toes.</p></div>
      <div class="cd"><h4>Communication</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">When something works, everyone should know</p><p>Regular updates, no surprises. When the Front Door cuts response time, we share that story — upward to leadership, sideways to peers.</p></div>
      <div class="cd"><h4>Change Philosophy</h4><p style="font-size:12px;color:var(--text-dim);margin-bottom:4px">Small wins build trust faster than big plans</p><p>I do not force change on people. I show results first, then they want to join. Pull, not push. That is how I have always worked.</p></div>
    </div>
  </div>
</div>

<!-- 12: CLOSING -->
<div class="sl" data-c="close" data-time="~1.5 min" data-script="Let me close where I started. Ivoclar's IT challenge is not technology. It is not budget. It is a missing operating system. Unmanaged demand, unclear decision rights, inconsistent execution — that creates low transparency and low value perception. The case study asked me to build the Business and IT Enablement Engine. That is exactly what I have laid out. An engine that connects demand, decisions, delivery, and value. Governance that works across regions. Financial transparency through TBM and FinOps. A portfolio balanced at fifty-thirty-twenty. And KPIs that are simple enough for anyone to understand. The airport was busy. The planes were flying. What was missing was the engine that makes it all work together. I would like to build it. Thank you. Happy to take your questions.">
  <div class="si cen">
    <div class="tag">The Enablement Engine — assembled</div>
    <h1 style="font-size:44px;max-width:860px">From <span class="hr">&ldquo;loudest voice wins&rdquo;</span><br>to <span class="hg">&ldquo;whoever creates value<br>gets priority&rdquo;</span></h1>
    <div style="font-size:21px;font-weight:300;font-style:italic;color:var(--text-mid);margin-top:10px">That is the Enablement Engine.</div>
    <div style="margin-top:38px;display:flex;gap:20px;justify-content:center;flex-wrap:wrap">
      <div style="text-align:center;padding:12px 20px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:10px"><div style="font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--amber);letter-spacing:1px;margin-bottom:3px">ENGINE CORE</div><div style="font-size:12.5px;color:var(--text-mid)">Front Door + Governance</div></div>
      <div style="text-align:center;padding:12px 20px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:10px"><div style="font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--cyan);letter-spacing:1px;margin-bottom:3px">PROCESS</div><div style="font-size:12.5px;color:var(--text-mid)">Demand-to-Value</div></div>
      <div style="text-align:center;padding:12px 20px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:10px"><div style="font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--green);letter-spacing:1px;margin-bottom:3px">INNOVATION</div><div style="font-size:12.5px;color:var(--text-mid)">Sandbox-to-Scale</div></div>
      <div style="text-align:center;padding:12px 20px;background:var(--bg-card-solid);border:1px solid var(--border);border-radius:10px"><div style="font-family:'JetBrains Mono',monospace;font-size:10px;color:var(--violet);letter-spacing:1px;margin-bottom:3px">FINANCIAL</div><div style="font-size:12.5px;color:var(--text-mid)">TBM + FinOps</div></div>
    </div>
    <div class="rw" style="margin-top:38px;width:38%"></div>
  </div>
</div>

</div>
<script>
const S=document.querySelectorAll('.sl'),I=document.querySelectorAll('.sb-i'),P=document.getElementById('prog'),C=document.getElementById('cur'),T=document.getElementById('tot'),NP=document.getElementById('notes'),ST=document.getElementById('scriptText'),STM=document.getElementById('scriptTime');
let c=0,notesOn=false;T.textContent=S.length;
function go(n){if(n<0||n>=S.length||n===c)return;S[c].classList.remove('on');S[n].classList.add('on');c=n;C.textContent=c+1;P.style.width=(c/(S.length-1)*100)+'%';const ch=S[c].dataset.c;I.forEach(i=>i.classList.toggle('on',i.dataset.c===ch));ST.innerHTML=S[c].dataset.script||'<em style="color:var(--text-dim)">No notes.</em>';STM.textContent=S[c].dataset.time||'';}
document.addEventListener('keydown',e=>{if(e.key==='ArrowRight'||e.key===' '){e.preventDefault();go(c+1)}else if(e.key==='ArrowLeft'){e.preventDefault();go(c-1)}else if(e.key==='f'||e.key==='F'){document.documentElement.requestFullscreen?.()}else if(e.key==='n'||e.key==='N'){notesOn=!notesOn;NP.classList.toggle('show',notesOn);}});
let tx=0;document.addEventListener('touchstart',e=>{tx=e.touches[0].clientX});document.addEventListener('touchend',e=>{const d=tx-e.changedTouches[0].clientX;if(Math.abs(d)>60)go(d>0?c+1:c-1);});
go(0);
</script>
</body>
</html>
