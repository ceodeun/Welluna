[welluna.html](https://github.com/user-attachments/files/28868831/welluna.html)
# Welluna<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Welluna — Women's Wellness AI</title>
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@tabler/icons-webfont@2.44.0/tabler-icons.min.css">
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;background:#fff;color:#1a1a1a;max-width:480px;margin:0 auto}
.topbar{padding:14px 16px 10px;border-bottom:1px solid #f0e6ee;display:flex;align-items:center;gap:10px;background:#fff;position:sticky;top:0;z-index:10}
.logo{font-size:19px;font-weight:600;letter-spacing:-0.3px;color:#1a1a1a}
.logo span{color:#D4537E}
.pill{font-size:11px;padding:2px 9px;border-radius:20px;background:#FBEAF0;color:#993556}
.tabs{display:flex;border-bottom:1px solid #f0e6ee;background:#fff;position:sticky;top:53px;z-index:9}
.tab{flex:1;padding:10px 4px;font-size:13px;color:#888;border:none;background:none;cursor:pointer;border-bottom:2px solid transparent;transition:all 0.15s}
.tab.on{color:#993556;border-bottom-color:#D4537E;font-weight:500}
.pad{padding:14px 16px}
.sec-label{font-size:11px;color:#999;letter-spacing:0.06em;margin-bottom:10px;font-weight:500;text-transform:uppercase}
.card{background:#fff;border:1px solid #f0e6ee;border-radius:12px;padding:14px 16px;margin-bottom:10px}
.card-title{font-size:14px;font-weight:500;color:#1a1a1a;margin-bottom:10px;display:flex;align-items:center;gap:7px}
.hero{background:#FBEAF0;border-radius:12px;padding:18px 16px;margin-bottom:12px;display:flex;align-items:center;gap:16px}
.hero-moon{width:56px;height:56px;border-radius:50%;background:#F4C0D1;display:flex;align-items:center;justify-content:center;flex-shrink:0;font-size:26px}
.hero-phase{font-size:13px;color:#993556;font-weight:500;margin-bottom:2px}
.hero-day{font-size:24px;font-weight:600;color:#72243E}
.hero-next{font-size:12px;color:#993556;margin-top:3px}
.grid2{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:12px}
.mcard{background:#faf5f8;border-radius:8px;padding:11px 13px}
.m-lbl{font-size:11px;color:#999;margin-bottom:2px}
.m-val{font-size:16px;font-weight:500;color:#1a1a1a}
.cal-hdr{display:grid;grid-template-columns:repeat(7,1fr);gap:3px;margin-bottom:3px}
.cal-grid{display:grid;grid-template-columns:repeat(7,1fr);gap:3px}
.chd{text-align:center;font-size:11px;color:#999;padding:3px 0}
.cd{width:100%;aspect-ratio:1;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:12px;cursor:pointer;border:none;background:none;color:#888}
.cd.today{background:#FBEAF0;color:#993556;font-weight:600}
.cd.period{background:#D4537E;color:#FBEAF0}
.cd.ovul{background:#993556;color:#FBEAF0;font-weight:600}
.cd.fertile{background:#F4C0D1;color:#72243E}
.cd.pred{background:#FBEAF0;color:#993556;border:1px dashed #D4537E}
.legend{display:flex;gap:8px;flex-wrap:wrap;margin-top:10px}
.leg{display:flex;align-items:center;gap:4px;font-size:11px;color:#888}
.ldot{width:9px;height:9px;border-radius:50%;flex-shrink:0}
.chip-row{display:flex;gap:6px;flex-wrap:wrap;margin-top:8px}
.chip{padding:6px 12px;border-radius:20px;border:1px solid #f0e6ee;background:#faf5f8;font-size:12px;color:#888;cursor:pointer;transition:all 0.12s}
.chip.sel{background:#FBEAF0;border-color:#D4537E;color:#72243E}
.rrow{display:flex;align-items:center;gap:10px;margin-top:8px}
.rrow label{font-size:12px;color:#888;width:55px;flex-shrink:0}
.rrow input[type=range]{flex:1;accent-color:#D4537E}
.rrow span{font-size:12px;font-weight:500;color:#1a1a1a;min-width:28px;text-align:right}
.save-btn{width:100%;padding:13px;border-radius:10px;border:none;background:#D4537E;color:#FBEAF0;font-size:14px;font-weight:500;cursor:pointer;margin-top:14px}
.save-btn:hover{background:#993556}
.insight-card{border:1px solid #F4C0D1;border-radius:12px;padding:14px 16px;margin-bottom:10px;background:#fff}
.i-label{font-size:11px;color:#D4537E;font-weight:500;letter-spacing:0.04em;margin-bottom:5px;text-transform:uppercase}
.i-text{font-size:13px;color:#333;line-height:1.65}
.stat-row{display:flex;gap:8px;margin-bottom:12px}
.sbox{flex:1;background:#faf5f8;border-radius:8px;padding:10px 12px;text-align:center}
.sl{font-size:11px;color:#999}
.sv{font-size:16px;font-weight:500;color:#1a1a1a;margin-top:2px}
.bubble{background:#FBEAF0;border-radius:0 12px 12px 12px;padding:11px 14px;margin-bottom:10px}
.bubble p{font-size:13px;color:#72243E;line-height:1.6}
.bubble-hdr{display:flex;align-items:center;gap:7px;margin-bottom:7px}
.bdot{width:7px;height:7px;border-radius:50%;background:#D4537E}
.bname{font-size:12px;font-weight:500;color:#993556}
.user-msg{text-align:right;margin-bottom:10px}
.user-bubble{display:inline-block;background:#f5f5f5;border-radius:12px 0 12px 12px;padding:9px 13px;font-size:13px;color:#1a1a1a;max-width:85%}
.chat-input-row{display:flex;gap:8px;margin-top:8px;position:sticky;bottom:0;background:#fff;padding:10px 0 4px}
.chat-input-row input{flex:1;font-size:13px;padding:9px 13px;border:1px solid #f0e6ee;border-radius:20px;outline:none}
.chat-input-row input:focus{border-color:#D4537E}
.chat-input-row button{padding:9px 16px;border-radius:20px;border:none;background:#D4537E;color:#FBEAF0;font-size:13px;cursor:pointer;font-weight:500}
.ask-btn{width:100%;padding:11px;border-radius:10px;border:1px solid #F4C0D1;background:none;font-size:13px;cursor:pointer;color:#993556;margin-top:4px}
.ask-btn:hover{background:#FBEAF0}
#t-home,#t-log,#t-insights,#t-ai{display:none}
#t-home{display:block}
</style>
</head>
<body>

<div class="topbar">
  <div class="logo">Well<span>una</span></div>
  <div class="pill">Women's Wellness AI</div>
  <div style="margin-left:auto;font-size:12px;color:#999">Day <b style="color:#D4537E">14</b></div>
</div>

<div class="tabs">
  <button class="tab on" onclick="sw('home',this)"><i class="ti ti-home" style="font-size:15px"></i></button>
  <button class="tab" onclick="sw('log',this)">Log</button>
  <button class="tab" onclick="sw('insights',this)">Insights</button>
  <button class="tab" onclick="sw('ai',this)">AI Chat</button>
</div>

<div id="t-home">
  <div class="pad">
    <div class="hero">
      <div class="hero-moon">🌙</div>
      <div>
        <div class="hero-phase">Ovulation phase</div>
        <div class="hero-day">Day 14 of 28</div>
        <div class="hero-next">Next period in 14 days · Jun 29</div>
      </div>
    </div>
    <div class="grid2">
      <div class="mcard"><div class="m-lbl">Cycle length</div><div class="m-val">28 days</div></div>
      <div class="mcard"><div class="m-lbl">Period length</div><div class="m-val">5 days</div></div>
      <div class="mcard"><div class="m-lbl">Last period</div><div class="m-val">Jun 1</div></div>
      <div class="mcard"><div class="m-lbl">Fertile window</div><div class="m-val">Jun 10–16</div></div>
    </div>
    <div class="sec-label">June 2026</div>
    <div class="card" style="padding:12px 14px">
      <div class="cal-hdr" id="cal-hdr"></div>
      <div class="cal-grid" id="cal-body"></div>
      <div class="legend">
        <div class="leg"><div class="ldot" style="background:#D4537E"></div>Period</div>
        <div class="leg"><div class="ldot" style="background:#993556"></div>Ovulation</div>
        <div class="leg"><div class="ldot" style="background:#F4C0D1"></div>Fertile</div>
        <div class="leg"><div class="ldot" style="background:#FBEAF0;border:1px dashed #D4537E"></div>Predicted</div>
      </div>
    </div>
  </div>
</div>

<div id="t-log">
  <div class="pad">
    <div class="sec-label">Today — June 12</div>
    <div class="card">
      <div class="card-title">😊 Mood</div>
      <div class="chip-row">
        <button class="chip" onclick="tog(this)">Happy</button>
        <button class="chip sel" onclick="tog(this)">Calm</button>
        <button class="chip" onclick="tog(this)">Anxious</button>
        <button class="chip" onclick="tog(this)">Irritable</button>
        <button class="chip" onclick="tog(this)">Sad</button>
        <button class="chip" onclick="tog(this)">Energetic</button>
        <button class="chip" onclick="tog(this)">Emotional</button>
      </div>
    </div>
    <div class="card">
      <div class="card-title">🩺 Symptoms</div>
      <div class="chip-row">
        <button class="chip" onclick="tog(this)">Cramps</button>
        <button class="chip sel" onclick="tog(this)">Bloating</button>
        <button class="chip" onclick="tog(this)">Headache</button>
        <button class="chip" onclick="tog(this)">Fatigue</button>
        <button class="chip" onclick="tog(this)">Back pain</button>
        <button class="chip" onclick="tog(this)">Nausea</button>
        <button class="chip" onclick="tog(this)">Breast pain</button>
        <button class="chip" onclick="tog(this)">Acne</button>
        <button class="chip" onclick="tog(this)">Hot flashes</button>
      </div>
    </div>
    <div class="card">
      <div class="card-title">💧 Flow (if period)</div>
      <div class="chip-row">
        <button class="chip" onclick="togGroup(this)">None</button>
        <button class="chip sel" onclick="togGroup(this)">Light</button>
        <button class="chip" onclick="togGroup(this)">Medium</button>
        <button class="chip" onclick="togGroup(this)">Heavy</button>
      </div>
    </div>
    <div class="card">
      <div class="card-title">🌙 Sleep & energy</div>
      <div class="rrow"><label>Sleep</label><input type="range" min="1" max="12" value="7" step="1" oninput="document.getElementById('sl-o').textContent=this.value+'h'"><span id="sl-o">7h</span></div>
      <div class="rrow"><label>Energy</label><input type="range" min="1" max="10" value="6" step="1" oninput="document.getElementById('en-o').textContent=this.value+'/10'"><span id="en-o">6/10</span></div>
      <div class="rrow"><label>Stress</label><input type="range" min="1" max="10" value="4" step="1" oninput="document.getElementById('st-o').textContent=this.value+'/10'"><span id="st-o">4/10</span></div>
    </div>
    <button class="save-btn" onclick="alert('Logged! Welluna will update your insights tonight. 🌙')">Save today's log</button>
  </div>
</div>

<div id="t-insights">
  <div class="pad">
    <div class="sec-label">Your pattern — 3 months</div>
    <div class="stat-row">
      <div class="sbox"><div class="sl">Avg cycle</div><div class="sv">28d</div></div>
      <div class="sbox"><div class="sl">Regularity</div><div class="sv">High</div></div>
      <div class="sbox"><div class="sl">Days logged</div><div class="sv">47</div></div>
    </div>
    <div class="insight-card">
      <div class="i-label">PMS pattern detected</div>
      <div class="i-text">Bloating and fatigue consistently appear 3–5 days before your period. Try reducing sodium and increasing water intake during this window.</div>
    </div>
    <div class="insight-card">
      <div class="i-label">Sleep & mood link</div>
      <div class="i-text">Your sleep drops to ~5.5h during the luteal phase (days 15–28). Mood scores closely follow sleep quality on those days.</div>
    </div>
    <div class="insight-card">
      <div class="i-label">Energy peak</div>
      <div class="i-text">Your energy is highest around ovulation (days 12–16). Great time for high-intensity workouts or demanding work tasks.</div>
    </div>
    <div class="insight-card">
      <div class="i-label">Upcoming alert</div>
      <div class="i-text">Based on your pattern, expect mild cramping and mood dips around June 24. Welluna will remind you 2 days before.</div>
    </div>
    <button class="ask-btn" onclick="sw('ai',document.querySelectorAll('.tab')[3])">Ask Welluna AI for deeper analysis →</button>
  </div>
</div>

<div id="t-ai">
  <div class="pad">
    <div class="sec-label">Welluna AI</div>
    <div id="chat-box"></div>
    <div class="chat-input-row">
      <input type="text" id="chat-input" placeholder="Ask Welluna anything..." onkeydown="if(event.key==='Enter')sendChat()">
      <button onclick="sendChat()">Send</button>
    </div>
    <div class="chip-row" style="margin-top:10px">
      <button class="chip" onclick="quickQ('Why do I feel off today?')">Why do I feel off?</button>
      <button class="chip" onclick="quickQ('Predict my PMS this cycle')">Predict my PMS</button>
      <button class="chip" onclick="quickQ('Diet tips by cycle phase')">Cycle diet tips</button>
      <button class="chip" onclick="quickQ('Workout recommendations by phase')">Workout by phase</button>
    </div>
  </div>
</div>

<script>
const DAYS=['Sun','Mon','Tue','Wed','Thu','Fri','Sat'];
const PERIOD=[1,2,3,4,5],FERTILE=[10,11,13,14,15,16],OVUL=14,PRED=[29,30],TODAY=12;

function buildCal(){
  document.getElementById('cal-hdr').innerHTML=DAYS.map(d=>`<div class="chd">${d}</div>`).join('');
  const dow=new Date(2026,5,1).getDay();
  let cells='';
  for(let i=0;i<dow;i++)cells+=`<div></div>`;
  for(let d=1;d<=30;d++){
    let cls='cd';
    if(d===TODAY)cls+=' today';
    else if(PERIOD.includes(d))cls+=' period';
    else if(d===OVUL)cls+=' ovul';
    else if(FERTILE.includes(d))cls+=' fertile';
    else if(PRED.includes(d))cls+=' pred';
    cells+=`<button class="${cls}">${d}</button>`;
  }
  document.getElementById('cal-body').innerHTML=cells;
}

function tog(el){el.classList.toggle('sel');}
function togGroup(el){el.parentElement.querySelectorAll('.chip').forEach(c=>c.classList.remove('sel'));el.classList.add('sel');}

function sw(tab,btn){
  document.querySelectorAll('.tab').forEach(t=>t.classList.remove('on'));
  btn.classList.add('on');
  ['home','log','insights','ai'].forEach(t=>{document.getElementById('t-'+t).style.display=t===tab?'block':'none';});
  if(tab==='ai')initChat();
}

const INIT_MSGS=[
  {r:'ai',t:"Hi! I'm Welluna, your AI wellness companion. I've analysed your cycle and symptom logs. How are you feeling today? 🌸"},
  {r:'user',t:"I've been feeling more tired than usual lately."},
  {r:'ai',t:"You're on day 14 — your ovulation phase, which is usually your highest-energy window. Since fatigue isn't typical for you now, it may be linked to your 6.5h average sleep this week. Try to get 7–8h tonight. Want a tailored wind-down routine for better sleep during this phase?"},
];
const AI_REPLIES=[
  "Based on your 3-month history, that's consistent with your luteal phase pattern. Your logs show this symptom clusters around days 18–22.",
  "Your cycle data suggests this is linked to hormonal shifts. Magnesium-rich foods like spinach and dark chocolate can really help! 🍫",
  "Your next PMS window is likely June 24–28. I'd suggest reducing caffeine 3 days before and adding light yoga to your routine. 🧘‍♀️",
  "Your energy peaks around ovulation — now is a great time for HIIT or strength training if you're up for it! 💪",
  "Your sleep drops by about 1.5h before your period. A consistent wind-down routine — no screens 30 min before bed — can make a big difference. 🌙",
];
let msgs=[...INIT_MSGS],aiIdx=0,chatInited=false;

function initChat(){
  if(chatInited)return;
  chatInited=true;renderChat();
}
function renderChat(){
  const box=document.getElementById('chat-box');
  box.innerHTML=msgs.map(m=>{
    if(m.r==='ai')return`<div class="bubble"><div class="bubble-hdr"><div class="bdot"></div><div class="bname">Welluna AI</div></div><p>${m.t}</p></div>`;
    return`<div class="user-msg"><div class="user-bubble">${m.t}</div></div>`;
  }).join('');
  box.scrollTop=box.scrollHeight;
}
function sendChat(){
  const inp=document.getElementById('chat-input'),txt=inp.value.trim();
  if(!txt)return;
  msgs.push({r:'user',t:txt});inp.value='';renderChat();
  setTimeout(()=>{msgs.push({r:'ai',t:AI_REPLIES[aiIdx%AI_REPLIES.length]});aiIdx++;renderChat();},900);
}
function quickQ(q){
  sw('ai',document.querySelectorAll('.tab')[3]);
  initChat();
  document.getElementById('chat-input').value=q;sendChat();
}

buildCal();
</script>
</body>
</html>
