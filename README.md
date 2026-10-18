

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#0b1020">
<title>DeviceGuard | Security Center</title>
<style>
:root{--bg:#0b1020;--panel:#151e33;--line:#293956;--green:#52f0b0;--muted:#b8c6dc;--white:#f5f8ff}
*{box-sizing:border-box}
body{margin:0;background:var(--bg);color:var(--white);font-family:system-ui,Arial,sans-serif;line-height:1.55}
header{padding:23px 18px;background:linear-gradient(130deg,#142b45,#102a2b);border-bottom:1px solid var(--line)}
header h1{margin:0;color:var(--green);font-size:28px}
header p{margin:5px 0 0;color:var(--muted)}
nav{display:flex;gap:8px;overflow-x:auto;padding:12px 15px;background:#10182a;position:sticky;top:0;z-index:2}
nav a{white-space:nowrap;color:var(--white);text-decoration:none;border:1px solid var(--line);border-radius:9px;padding:8px 11px;font-size:13px}
main{max-width:850px;margin:auto;padding:17px}
h2{font-size:19px;margin-top:0}
.hero{padding:22px;background:linear-gradient(140deg,#163b42,#192746);border:1px solid #31505b;border-radius:18px;margin-bottom:18px}
.hero h2{font-size:24px;margin-bottom:5px}
.muted,small{color:var(--muted)}
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(145px,1fr));gap:12px}
.card{background:var(--panel);border:1px solid var(--line);border-radius:15px;padding:17px;margin-bottom:14px;scroll-margin-top:80px}
.tile{min-height:135px}
.tile .emoji{font-size:26px}
button{background:var(--green);color:#092019;border:0;border-radius:9px;padding:11px 13px;font-weight:750;font-size:14px;cursor:pointer;margin:4px 3px 4px 0}
button.secondary{background:#263652;color:var(--white);border:1px solid #415575}
button:focus-visible,a:focus-visible,input:focus-visible{outline:2px solid white;outline-offset:3px}
.result{color:var(--green);white-space:pre-line}
label{display:block;margin:10px 0 5px}
input{width:100%;padding:12px;border-radius:9px;background:#0c1425;color:white;border:1px solid #415575}
footer{padding:20px;text-align:center;color:var(--muted)}
</style>
</head>
<body>
<header>
<h1>🛡️ DeviceGuard</h1>
<p>Personal Device & Cybersecurity Learning Center</p>
</header>
<nav aria-label="Main navigation">
<a href="#dashboard">Home</a>
<a href="#device">Device Safety</a>
<a href="#wifi">Wi-Fi</a>
<a href="#learn">Learn</a>
<a href="#quiz">Quiz</a>
</nav>
<main>
<section id="dashboard" class="hero">
<p>YOUR DIGITAL SAFETY STARTS HERE</p>
<h2>Welcome to DeviceGuard</h2>
<p>Learn to protect your devices, understand security risks, and build practical IT skills.</p>
<button onclick="document.getElementById('learn').scrollIntoView()">Start learning →</button>
</section>

<section class="grid" aria-label="Learning topics">
<div class="card tile"><div class="emoji">📱</div><h2>Device safety</h2><p class="muted">Protect your Android phone.</p><a href="#device">Explore →</a></div>
<div class="card tile"><div class="emoji">📡</div><h2>Wi-Fi security</h2><p class="muted">Understand network protection.</p><a href="#wifi">Explore →</a></div>
<div class="card tile"><div class="emoji">🔐</div><h2>Cyber lessons</h2><p class="muted">Learn common threats.</p><a href="#learn">Explore →</a></div>
<div class="card tile"><div class="emoji">📍</div><h2>Lost device</h2><p class="muted">Learn official recovery steps.</p><a href="#device">Explore →</a></div>
</section>

<section id="device" class="card">
<h2>📱 Device Safety Center</h2>
<p>Use these steps to make your Android phone safer.</p>
<button onclick="show('deviceTips','Use a strong screen lock.\\nInstall Android and app updates.\\nRemove apps you do not trust.\\nReview app location, camera and microphone permissions.\\nBack up important files.\\nNever share passwords or one-time codes.')">Show safety checklist</button>
<p id="deviceTips" class="result" aria-live="polite"></p>
<h3>Find your own lost Android phone</h3>
<p class="muted">Google's official Find Hub may show a device's location when the relevant account and device settings allow it.</p>
<button onclick="window.open('https://android.com/find','_blank','noopener')">Open Google Find Hub ↗</button>
</section>

<section id="wifi" class="card">
<h2>📡 Wi-Fi Security Lab</h2>
<p>Study these basics before changing network settings.</p>
<button onclick="show('wifiTips','WPA3 or WPA2-AES are preferred modern Wi-Fi protections.\\nUse a long, unique Wi-Fi password.\\nChange your router administrator password.\\nUpdate router firmware when available.\\nAvoid sensitive activity on untrusted networks.\\nTest only networks you own or have permission to assess.')">Show Wi-Fi lesson</button>
<p id="wifiTips" class="result" aria-live="polite"></p>
</section>

<section id="learn" class="card">
<h2>🎓 Cybersecurity Learning Hub</h2>
<h3>1. Phishing</h3>
<p>Fraudulent messages may impersonate trusted services to steal passwords or verification codes. Check the sender and open official websites directly.</p>
<h3>2. Password security</h3>
<p>Use unique passwords and a password manager. Enable two-step verification wherever possible.</p>
<h3>3. Network fundamentals</h3>
<p>Learn IP addresses, routers, DNS, HTTPS and firewalls before studying security testing.</p>
<h3>4. Ethical security testing</h3>
<p>Practice in intentionally vulnerable labs or on your own systems with permission. Never access another person's device or account without authorization.</p>
<h3>5. GPS and privacy</h3>
<p>Location accuracy depends on device settings, connectivity and available signals. A website cannot silently track a phone merely by knowing its number.</p>
</section>

<section id="quiz" class="card">
<h2>🔐 Cybersecurity Quiz</h2>
<p id="question">Question 1: Someone asks you to send them your one-time login code. What should you do?</p>
<div id="answers">
<button class="secondary" onclick="check(0)">Send the code</button>
<button class="secondary" onclick="check(1)">Keep it private</button>
<button class="secondary" onclick="check(0)">Post it online</button>
</div>
<p id="feedback" class="result" aria-live="polite"></p>
<p id="score">Score: 0 / 0</p>
<button onclick="nextQuestion()">Next question →</button>
</section>

<section class="card">
<h2>ℹ️ About DeviceGuard</h2>
<p>DeviceGuard is an educational demo. It does not scan phones, access private files, or track devices in the background.</p>
<p class="muted">Future modules can add practice labs, saved learning progress, and defensive security checklists.</p>
</section>
</main>
<footer>🛡️ DeviceGuard • Learn safely. Protect your digital life.</footer>
<script>
function show(id,text){
document.getElementById(id).textContent=text.replace(/\\n/g,'\n');
}
const questions=[
{q:"Question 1: Someone asks for your one-time login code. What should you do?",a:["Send the code","Keep it private","Post it online"],correct:1,why:"Correct! Verification codes must remain private."},
{q:"Question 2: Which is a safer Wi-Fi setting?",a:["No password","WPA2-AES or WPA3","Share the admin password publicly"],correct:1,why:"Correct! WPA2-AES or WPA3 are preferred modern protections."},
{q:"Question 3: What should you do with unexpected app files from unknown websites?",a:["Install immediately","Forward to everyone","Avoid installing until verified"],correct:2,why:"Correct! Unverified app files may contain malware."},
{q:"Question 4: Which action helps protect accounts?",a:["Reuse one password everywhere","Use unique passwords and two-step verification","Share passwords with strangers"],correct:1,why:"Correct! Unique passwords and two-step verification reduce account risk."}
];
let current=0,answered=false,score=0,attempts=0;
function renderQuestion(){
answered=false;
const q=questions[current];
document.getElementById('question').textContent=q.q;
document.getElementById('answers').innerHTML='';
q.a.forEach((label,i)=>{
const b=document.createElement('button');
b.className='secondary';b.textContent=label;
b.onclick=()=>choose(i);
document.getElementById('answers').appendChild(b);
});
document.getElementById('feedback').textContent='';
}
function choose(i){
if(answered)return;
answered=true;attempts++;
const q=questions[current];
if(i===q.correct){score++;document.getElementById('feedback').textContent=q.why;}
else{document.getElementById('feedback').textContent='Not quite. '+q.why;}
document.getElementById('score').textContent='Score: '+score+' / '+attempts;
}
function check(i){choose(i);}
function nextQuestion(){current=(current+1)%questions.length;renderQuestion();}
renderQuestion();
</script>
</body>
</html>
