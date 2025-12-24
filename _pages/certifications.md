---
layout: splash
title: "Certifications"
permalink: /certifications/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

.page__content {
  font-family: 'Inter', sans-serif;
  position: relative;
  z-index: 2;
  max-width: 1200px;
  margin: 0 auto;
  padding: 3rem 2rem;
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

.page__title {
  font-size: 3.5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #667eea, #764ba2, #f093fb);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  margin-bottom: 2rem;
  animation: fadeIn 1s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

h2 {
  color: #667eea;
  font-weight: 700;
  margin-top: 3rem;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid rgba(102, 126, 234, 0.3);
  animation: slideIn 0.8s ease-out;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateX(-30px);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}

h3 {
  color: #764ba2;
  font-weight: 700;
  margin-top: 2rem;
  padding: 1.5rem;
  background: rgba(118, 75, 162, 0.05);
  border-left: 4px solid #764ba2;
  border-radius: 8px;
}

.page__content a {
  color: #667eea;
  text-decoration: none;
  transition: all 0.3s ease;
}

.page__content a:hover {
  color: #764ba2;
}

ul {
  list-style: none;
  padding-left: 0;
}

ul li {
  padding-left: 1.5rem;
  position: relative;
  margin-bottom: 0.5rem;
}

ul li::before {
  content: '✓';
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
}

hr {
  border: none;
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.5), transparent);
  margin: 2.5rem 0;
}

.btn {
  display: inline-block;
  padding: 0.8rem 2rem;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: #fff !important;
  border-radius: 8px;
  margin: 0.5rem;
  transition: all 0.3s ease;
  text-decoration: none;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
}
</style>

<canvas id="cert-particles"></canvas>

<div class="page__content">

## Professional Certifications

### Offensive Security Certified Professional (OSCP)
Industry-leading hands-on penetration testing certification. Demonstrates practical skills in identifying and exploiting vulnerabilities in realistic network environments.

Key Skills:
- Network penetration testing
- Buffer overflow exploitation
- Privilege escalation (Linux & Windows)
- Web application attacks
- Active Directory exploitation

---

### Offensive Security Defense Analyst (OSDA)
Advanced defensive security certification focusing on detection, monitoring, and incident response.

Key Skills:
- Security monitoring and log analysis
- Threat hunting
- Incident detection and response
- SIEM deployment and tuning
- Purple team operations

---

### Cisco Certified Network Associate (CCNA)
Fundamental networking certification covering network fundamentals, IP connectivity, and security.

Key Skills:
- Network configuration and troubleshooting
- Routing and switching
- Network security fundamentals
- Cisco device management

---

### CompTIA Security+
Foundational cybersecurity certification covering essential security concepts and best practices.

Key Skills:
- Security concepts and terminology
- Risk management
- Cryptography
- Identity and access management
- Security operations

---

## Continuous Learning

I maintain active engagement with the security community through:
- CTF competitions and challenges
- Security research and vulnerability discovery
- Open-source security tool development
- Academic coursework at Carnegie Mellon University

---

[Back to About](/about/){: .btn .btn--primary}

</div>

<script>
// Particle background
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
  
  // Connect particles
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
