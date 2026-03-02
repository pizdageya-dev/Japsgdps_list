<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Game Levels</title>
<style>
body{margin:0;font-family:Arial;background:#111;color:white;overflow:hidden;}
.cube{position:fixed;width:20px;height:20px;background:orange;animation:float 10s linear infinite;opacity:0.3;z-index:0;}
@keyframes float{0%{transform:translateY(100vh) rotate(0deg);}100%{transform:translateY(-100vh) rotate(360deg);}}
.tabs{display:flex;background:#000;border-bottom:3px solid orange;position:relative;z-index:1;}
.tab-button{flex:1;padding:15px;background:none;border:none;color:orange;font-weight:bold;cursor:pointer;}
.tab-button.active{background:orange;color:black;}
.tab-content{display:none;padding:20px;}
.tab-content.active{display:block;}
.level{background:#1a1a1a;padding:15px;margin:10px 0;border-left:5px solid orange;cursor:pointer;transition:0.3s;}
.level:hover{background:#222;}
.top1{background:gold;color:black;font-weight:bold;}
.top2{background:silver;color:black;font-weight:bold;}
.top3{background:#cd7f32;color:black;font-weight:bold;}
.description-box{background:#1a1a1a;border:2px solid orange;padding:15px;margin-top:10px;display:none;}
h2{color:orange;}
</style>
</head>
<body>

<h2 style="padding:20px">Game Levels</h2>
<div class="tabs">
<button class="tab-button active" onclick="openTab('demon',this)">Demon List</button>
<button class="tab-button" onclick="openTab('pemon',this)">Pemon List</button>
<button class="tab-button" onclick="openTab('challenge',this)">Challenge List</button>
</div>

<!-- DEMON LIST -->
<div id="demon" class="tab-content active">
  <div class="level top1" onclick="showDesc('Least Wanted')">1. Least Wanted</div>
  <div class="level top2" onclick="showDesc('Lava Powder')">2. Lava Powder</div>
  <div class="level top3" onclick="showDesc('Upsite Down')">3. Upsite Down</div>
  <div class="level" onclick="showDesc('Insane Processing')">4. Insane Processing</div>
  <div class="level" onclick="showDesc('Shittty Aftermath')">5. Shittty Aftermath</div>
  <div class="level" onclick="showDesc('Silent Darknest')">6. Silent Darknest</div>
  <div class="level" onclick="showDesc('Rays of Sun')">7. Rays of Sun</div>
  <div class="level" onclick="showDesc('aaAAaAaaAA')">8. aaAAaAaaAA</div>
  <div class="level" onclick="showDesc('KOCMOC')">9. KOCMOC</div>
  <div class="level" onclick="showDesc('Voce Na Mira')">10. Voce Na Mira</div>
</div>

<!-- PEMONS LIST -->
<div id="pemon" class="tab-content">
  <div class="level" onclick="showDesc('Orange Pulse')">1. Orange Pulse</div>
  <div class="level" onclick="showDesc('Cyber Rush')">2. Cyber Rush</div>
  <div class="level" onclick="showDesc('Plasma Run')">3. Plasma Run</div>
  <div class="level" onclick="showDesc('Neon Strike')">4. Neon Strike</div>
  <div class="level" onclick="showDesc('Speed Vortex')">5. Speed Vortex</div>
  <div class="level" onclick="showDesc('Toxic Dash')">6. Toxic Dash</div>
  <div class="level" onclick="showDesc('Rapid Wave')">7. Rapid Wave</div>
  <div class="level" onclick="showDesc('Flash Reactor')">8. Flash Reactor</div>
  <div class="level" onclick="showDesc('Power Grid')">9. Power Grid</div>
  <div class="level" onclick="showDesc('Storm Dash')">10. Storm Dash</div>
</div>

<!-- CHALLENGE LIST -->
<div id="challenge" class="tab-content">
  <div class="level" onclick="showDesc('Mini Wave Spam')">1. Mini Wave Spam</div>
  <div class="level" onclick="showDesc('Straight Fly 100%')">2. Straight Fly 100%</div>
  <div class="level" onclick="showDesc('Invisible Blocks')">3. Invisible Blocks</div>
  <div class="level" onclick="showDesc('Speed Trial')">4. Speed Trial</div>
  <div class="level" onclick="showDesc('Tight Corridor')">5. Tight Corridor</div>
  <div class="level" onclick="showDesc('Double Click Timing')">6. Double Click Timing</div>
  <div class="level" onclick="showDesc('Micro Cube')">7. Micro Cube</div>
  <div class="level" onclick="showDesc('Memory Path')">8. Memory Path</div>
  <div class="level" onclick="showDesc('Gravity Chaos')">9. Gravity Chaos</div>
  <div class="level" onclick="showDesc('Final Reaction')">10. Final Reaction</div>
</div>

<div id="descriptionBox" class="description-box"></div>

<script>
function openTab(tabName, btn){
  document.querySelectorAll('.tab-button').forEach(b=>b.classList.remove('active'));
  btn.classList.add('active');
  document.querySelectorAll('.tab-content').forEach(c=>c.classList.remove('active'));
  document.getElementById(tabName).classList.add('active');
  document.getElementById('descriptionBox').style.display='none';
}

function randomName(){
  const names=['ShadowX','WaveGod','CubeMaster','DarkPlayer','NeonDash','TopClick','SpeedPro','UltraWave','SilentX','FireDash'];
  return names[Math.floor(Math.random()*names.length)];
}

function showDesc(levelName){
  const box=document.getElementById('descriptionBox');
  box.style.display='block';
  box.innerHTML=`<strong>Level:</strong> ${levelName}<br>
                   <strong>ID:</strong> ${Math.floor(100000+Math.random()*900000)}<br>
                   <strong>Created by:</strong> ${randomName()}<br>
                   <strong>Verified by:</strong> ${randomName()}`;
}

// Фоновые кубики
for(let i=0;i<30;i++){
  let cube=document.createElement('div');
  cube.className='cube';
  cube.style.left=Math.random()*100+'vw';
  cube.style.top=Math.random()*100+'vh';
  cube.style.background=Math.random()>0.5?'orange':'#ff6600';
  cube.style.animationDuration=(5+Math.random()*10)+'s';
  document.body.appendChild(cube);
}
</script>

</body>
</html>
