---
layout: splash
title: "Certifications"
permalink: /certifications/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

body {
  background: #000;
  color: #fff;
}

#cert-particles {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
  pointer-events: none;
}

.content-wrapper {
  position: relative;
  z-index: 2;
  max-width: 1200px;
  margin: 0 auto;
  padding: 4rem 2rem;
  font-family: 'Inter', sans-serif;
}

.page-title {
  font-size: 3.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #667eea, #764ba2, #f093fb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 3rem;
  animation: fadeIn 1s ease-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.cert-section {
  margin-bottom: 3rem;
  animation: slideIn 0.8s ease-out;
}

@keyframes slideIn {
  from { opacity: 0; transform: translateX(-30px); }
  to { opacity: 1; transform: translateX(0); }
}

.cert-card {
  background: rgba(255, 255, 255, 0.02);
  border-left: 4px solid #764ba2;
  border-radius: 12px;
  padding: 2rem;
  margin-bottom: 2rem;
  transition: all 0.3s ease;
}

.cert-card:hover {
  background: rgba(255, 255, 255, 0.05);
  transform: translateX(10px);
  box-shadow: 0 10px 30px rgba(102, 126, 234, 0.2);
}

h2 {
  color: #667eea;
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 2rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid rgba(102, 126, 234, 0.3);
}

h3 {
  color: #764ba2;
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}

p {
  color: #ccc;
  line-height: 1.8;
  margin-bottom: 1rem;
}

ul {
  list-style: none;
  padding-left: 0;
  margin: 1rem 0;
}

li {
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
  color: #ccc;
}

li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
}

.btn {
  display: inline-block;
  padding: 1rem 2.5rem;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: #fff;
  text-decoration: none;
  border-radius: 8px;
  margin-top: 2rem;
  transition: all 0.3s ease;
  font-weight: 600;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}

.divider {
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.5), transparent);
  margin: 3rem 0;
}
</style>

<canvas id="cert-particles"></canvas>

<div class="content-wrapper">
  <h1 class="page-title">Certifications</h1>
  
  <h2>Professional Certifications</h2>
  
  <div class="cert-section">
    <div class="cert-card">
      <h3>Offensive Security Certified Professional (OSCP)</h3>
      <p>Industry-leading hands-on penetration testing certification. Demonstrates practical skills in identifying and exploiting vulnerabilities in realistic network environments.</p>
      <p><strong>Key Skills:</strong></p>
      <ul>
        <li>Network penetration testing</li>
        <li>Buffer overflow exploitation</li>
        <li>Privilege escalation (Linux & Windows)</li>
        <li>Web application attacks</li>
        <li>Active Directory exploitation</li>
      </ul>
    </div>
  </div>
  
  <div class="cert-section">
    <div class="cert-card">
      <h3>Offensive Security Defense Analyst (OSDA)</h3>
      <p>Advanced defensive security certification focusing on detection, monitoring, and incident response.</p>
      <p><strong>Key Skills:</strong></p>
      <ul>
        <li>Security monitoring and log analysis</li>
        <li>Threat hunting</li>
        <li>Incident detection and response</li>
        <li>SIEM deployment and tuning</li>
        <li>Purple team operations</li>
      </ul>
    </div>
  </div>
  
  <div class="cert-section">
    <div class="cert-card">
      <h3>Cisco Certified Network Associate (CCNA)</h3>
      <p>Fundamental networking certification covering network fundamentals, IP connectivity, and security.</p>
      <p><strong>Key Skills:</strong></p>
      <ul>
        <li>Network configuration and troubleshooting</li>
        <li>Routing and switching</li>
        <li>Network security fundamentals</li>
        <li>Cisco device management</li>
      </ul>
    </div>
  </div>
  
  <div class="cert-section">
    <div class="cert-card">
      <h3>CompTIA Security+</h3>
      <p>Foundational cybersecurity certification covering essential security concepts and best practices.</p>
      <p><strong>Key Skills:</strong></p>
      <ul>
        <li>Security concepts and terminology</li>
        <li>Risk management</li>
        <li>Cryptography</li>
        <li>Identity and access management</li>
        <li>Security operations</li>
      </ul>
    </div>
  </div>
  
  <div class="divider"></div>
  
  <h2>Continuous Learning</h2>
  <p>I maintain active engagement with the security community through:</p>
  <ul>
    <li>CTF competitions and challenges</li>
    <li>Security research and vulnerability discovery</li>
    <li>Open-source security tool development</li>
    <li>Academic coursework at Carnegie Mellon University</li>
  </ul>
  
  <a href="/about/" class="btn">Back to About</a>
</div>

<script>
const canvas = document.getElementById('cert-particles');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = document.documentElement.scrollHeight;

const particles = [];
const particleCount = 60;
const colors = ['#667eea', '#764ba2', '#f093fb'];

class Particle {
  constructor() {
    this.x = Math.random() * canvas.width;
    this.y = Math.random() * canvas.height;
    this.size = Math.random() * 2 + 1;
    this.speedX = (Math.random() - 0.5) * 0.3;
    this.speedY = (Math.random() - 0.5) * 0.3;
    this.color = colors[Math.floor(Math.random() * colors.length)];
  }
  
  update() {
    this.x += this.speedX;
    this.y += this.speedY;
    if (this.x > canvas.width || this.x < 0) this.speedX *= -1;
    if (this.y > canvas.height || this.y < 0) this.speedY *= -1;
  }
  
  draw() {
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
    ctx.fillStyle = this.color;
    ctx.fill();
  }
}

for (let i = 0; i < particleCount; i++) {
  particles.push(new Particle());
}

function animate() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  
  particles.forEach(particle => {
    particle.update();
    particle.draw();
  });
  
  for (let a = 0; a < particles.length; a++) {
    for (let b = a + 1; b < particles.length; b++) {
      const dx = particles[a].x - particles[b].x;
      const dy = particles[a].y - particles[b].y;
      const distance = Math.sqrt(dx * dx + dy * dy);
      
      if (distance < 100) {
        const opacity = (1 - distance / 100) * 0.3;
        ctx.strokeStyle = `rgba(102, 126, 234, ${opacity})`;
        ctx.lineWidth = 1;
        ctx.beginPath();
        ctx.moveTo(particles[a].x, particles[a].y);
        ctx.lineTo(particles[b].x, particles[b].y);
        ctx.stroke();
      }
    }
  }
  
  requestAnimationFrame(animate);
}

animate();

window.addEventListener('resize', () => {
  canvas.width = window.innerWidth;
  canvas.height = document.documentElement.scrollHeight;
});
</script>
