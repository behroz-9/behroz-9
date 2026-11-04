<img src="tomar_pic_link_ba_path.png" alt="Profile Picture" width="100%"/>

<p align="center">
  <a href="https://komarev.com/ghpvc/?username=behroz-9">
    <img src="https://komarev.com/ghpvc/?username=behroz-9&label=Profile%20views&color=00FFFF&style=flat-square" alt="behroz-9's profile views" />
  </a>
</p>

<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&pause=1000&color=00FFFF&center=true&vCenter=true&width=700&lines=Welcome+to+my+GitHub+Profile!;Hi%2C+I'm+Muhammad+Behrouz+%F0%9F%91%8B;Full+Stack+Web+Developer;" alt="Typing SVG" />
</h1>

## 📌 About Me
- Hi, I'm Muhammad Behrouz, and I am currently pursuing my academic studies at the A Level tier. Driven by curiosity and a strong passion for technology, I love diving into everything from Full-Stack Web Development and software prototyping to interactive application design. I am currently exploring new projects, open to collaborations, and continuously sharpening my technical skills.

<p align="center">
  <a href="https://www.linkedin.com/">
    <img src="https://raw.githubusercontent.com/gauravghongde/social-icons/master/SVG/Color/LinkedIN.svg" alt="LinkedIn" width="40" />
  </a>
  <a href="https://github.com/behroz-9">
    <img src="https://raw.githubusercontent.com/gauravghongde/social-icons/master/SVG/Color/GitHub.svg" alt="GitHub" width="40" />
  </a>
  <a href="mailto:behrouz@example.com">
    <img src="https://raw.githubusercontent.com/gauravghongde/social-icons/master/SVG/Color/Gmail.svg" alt="Gmail" width="40" />
  </a>
</p>

<hr>

## 🚀 Current Endeavors & Recent Work
- ⚛️ **Full-Stack Development:** Building real-time web applications and interactive platforms using modern technologies like Node.js, Express.js, Socket.io, and Tailwind CSS.
- 🎨 **UI/UX Design & Prototyping:** Crafting responsive layouts, dark maroon gradient aesthetics, and interactive user interfaces with smooth user experiences.
- 🛠️ **Software Engineering:** Experimenting with database configurations (SQLite3, Supabase) and deploying applications via GitHub to cloud platforms like Vercel and Render.
  
<hr>

## 🦇 Play Mini Batman Game!
<div align="center">
  <p><b>Press Space or Tap to Jump over obstacles as Batman! 🎮</b></p>
  
  <canvas id="batmanGame" width="600" height="150" style="background:#111; border: 2px solid #00FFFF; border-radius: 8px;"></canvas>

  <script>
    const canvas = document.getElementById("batmanGame");
    const ctx = canvas.getContext("2d");

    let batman = { x: 50, y: 100, width: 25, height: 35, dy: 0, jumpPower: -10, gravity: 0.6, grounded: true };
    let obstacle = { x: 600, y: 105, width: 20, height: 30, speed: 5 };
    let score = 0;
    let isGameOver = false;

    document.addEventListener("keydown", function(e) {
      if (e.code === "Space") {
        e.preventDefault();
        jump();
      }
    });

    canvas.addEventListener("click", function() {
      jump();
    });

    function jump() {
      if (batman.grounded && !isGameOver) {
        batman.dy = batman.jumpPower;
        batman.grounded = false;
      } else if (isGameOver) {
        resetGame();
      }
    }

    function resetGame() {
      score = 0;
      obstacle.x = 600;
      obstacle.speed = 5;
      isGameOver = false;
      loop();
    }

    function update() {
      if (isGameOver) return;

      // Gravity mechanics
      batman.dy += batman.gravity;
      batman.y += batman.dy;

      if (batman.y > 100) {
        batman.y = 100;
        batman.dy = 0;
        batman.grounded = true;
      }

      // Obstacle movement
      obstacle.x -= obstacle.speed;
      if (obstacle.x < -20) {
        obstacle.x = 600;
        score++;
        if (score % 5 === 0) obstacle.speed += 0.5; // Increase difficulty
      }

      // Collision detection
      if (
        batman.x < obstacle.x + obstacle.width &&
        batman.x + batman.width > obstacle.x &&
        batman.y < obstacle.y + obstacle.height &&
        batman.y + batman.height > obstacle.y
      ) {
        isGameOver = true;
      }
    }

    function draw() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);

      // Draw ground line
      ctx.strokeStyle = "#00FFFF";
      ctx.lineWidth = 2;
      ctx.beginPath();
      ctx.moveTo(0, 136);
      ctx.lineTo(600, 136);
      ctx.stroke();

      // Draw Batman (Dark Silhouette with Cape style)
      ctx.fillStyle = "#00FFFF";
      ctx.fillRect(batman.x, batman.y, batman.width, batman.height);
      ctx.fillStyle = "#111";
      ctx.fillRect(batman.x + 5, batman.y + 5, 15, 10); // Visor cutout style

      // Draw Obstacle (Joker/Riddler style hazard block)
      ctx.fillStyle = "#FF5555";
      ctx.fillRect(obstacle.x, obstacle.y, obstacle.width, obstacle.height);

      // Draw Score
      ctx.fillStyle = "#FFFFFF";
      ctx.font = "14px monospace";
      ctx.fillText("Score: " + score, 20, 25);

      if (isGameOver) {
        ctx.fillStyle = "rgba(0, 0, 0, 0.75)";
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        ctx.fillStyle = "#FF5555";
        ctx.font = "bold 20px monospace";
        ctx.fillText("GAME OVER - CLICK OR SPACE TO RESTART", 80, 75);
      }
    }

    function loop() {
      update();
      draw();
      if (!isGameOver) {
        requestAnimationFrame(loop);
      }
    }

    loop();
  </script>
</div>

<hr>

## 🧠 My Focus Areas
- 🌐 **Web Development**
- 💻 **Full-Stack Architecture**
- ⚡ **Real-Time Communication**
- 🎨 **UI/UX Customization**

<hr>

## 🔥 Languages & Frameworks & Tools & Abilities 
<p align="center">
  <img src="https://skillicons.dev/icons?i=html,css,tailwind,js,ts,nodejs,express,react,git,github,vscode" />
</p>

<hr>

## 🗂️ Featured Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>💬 Cappuccino</h3>
      <br/>
      <b>📝 Description:</b><br/>
      A real-time web communication platform featuring authentication gates, search functionality, private direct messaging, and real-time database subscription handling.
      <br/><br/>
      <b>💻 Technologies Used:</b><br/>
      <code>JavaScript</code> <code>Node.js</code> <code>Express.js</code> <code>Socket.io</code> <code>Tailwind CSS</code> <code>Supabase</code>
      <br/><br/>
    </td>
    <td width="50%" valign="top">
      <h3>🎬 The Hujaifa</h3>
      <br/>
      <b>📝 Description:</b><br/>
      A Netflix-inspired portfolio web application incorporating dynamic modals, video presentation links, and structured project indexes.
      <br/><br/>
      <b>💻 Technologies Used:</b><br/>
      <code>HTML</code> <code>CSS</code> <code>JavaScript</code> <code>Tailwind CSS</code>
      <br/><br/>
    </td>
  </tr>
</table>

<hr>

## 📊 GitHub Stats
<p align="center">
    <img
        src="./assets/github-stats.svg"
        alt="GitHub Profile Stats"
        width="900"
    />
</p> 

<hr>

<div align="center">
  <img src="https://user-images.githubusercontent.com/74038190/212744287-14f66c13-5458-40dc-9244-8ff533fc8f4a.gif" alt="Bottom Line" width="100%" />
</div>
