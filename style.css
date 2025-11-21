const canvas = document.getElementById("gameCanvas");
spawnTimer += dt;
powerSpawn += dt;


if (spawnTimer > 600) { spawnObstacle(); spawnTimer = 0; }
if (powerSpawn > 5000) { spawnPowerup(); powerSpawn = 0; }


movePlayers();
updateObstacles();
updatePowerups();
checkHits();


// Timers
if (p1.boost>0) p1.boost -= dt;
if (p2.boost>0) p2.boost -= dt;
if (p1.shield>0) p1.shield -= dt;
if (p2.shield>0) p2.shield -= dt;
if (p1.reversed) p1.reversedTimer -= dt;


ctx.clearRect(0,0,canvas.width,canvas.height);
drawPlayer(p1);
drawPlayer(p2);


ctx.fillStyle = "white";
obstacles.forEach(o=> ctx.fillRect(o.x,o.y,o.size,o.size));


ctx.fillStyle = "gold";
powerups.forEach(p=> ctx.fillRect(p.x,p.y,p.size,p.size));


drawHUD();


requestAnimationFrame(gameLoop);



// FIXED START BUTTON
const startBtn = document.getElementById("startBtn");
startBtn.onclick = ()=>{
document.getElementById("cover").style.display="none";
canvas.style.display="block";
bgm.volume = 0.3;
bgm.play();
playing = true;
requestAnimationFrame(gameLoop);
};