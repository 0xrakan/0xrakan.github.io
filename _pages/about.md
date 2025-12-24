---
layout: splash
title: "About"
permalink: /about/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

body {
  background: #000;
  color: #fff;
}

#about-particles {
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
  margin-bottom: 3rem;
  animation: fadeIn 1s ease-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

h2 {
  color: #667eea;
  font-size: 2rem;
  font-weight: 700;
  margin: 3rem 0 1.5rem 0;
  padding-bottom: 0.5rem;
  border-bottom: 2px solid rgba(102, 126, 234, 0.3);
}

h3 {
  color: #764ba2;
  font-size: 1.5rem;
  font-weight: 700;
  margin: 2rem 0 1rem 0;
}

h4 {
  color: #f093fb;
  font-size: 1.2rem;
  font-weight: 600;
  margin: 1.5rem 0 0.5rem 0;
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
  content: '▸';
  position: absolute;
  left: 0;
  color: #667eea;
  font-weight: bold;
}

a {
  color: #667eea;
  text-decoration: none;
  transition: color 0.3s ease;
}

a:hover {
  color: #764ba2;
}

.section {
  margin-bottom: 3rem;
  animation: slideIn 0.8s ease-out;
}

@keyframes slideIn {
  from { opacity: 0; transform: translateX(-30px); }
  to { opacity: 1; transform: translateX(0); }
}

.divider {
  height: 1px;
  background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.5), transparent);
  margin: 3rem 0;
}
</style>

<canvas id="about-particles"></canvas>

<div class="content-wrapper">
  <h1 class="page-title">About</h1>
  
  <div class="section">
    <h2>Summary</h2>
    <p>Offensive Security Engineer with experience in red teaming, vulnerability research, penetration testing, and purple team operations. Discovered multiple critical-severity vulnerabilities resulting in assigned CVEs. Strong background in adversary emulation, detection validation, and security automation across cloud, application, and network environments.</p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Education</h2>
    
    <h3>Carnegie Mellon University</h3>
    <p><strong>M.S. Information Technology (Information Security)</strong><br>
    Information Networking Institute (INI)<br>
    August 2025 - May 2027 (Current)<br>
    Pittsburgh, PA</p>
    
    <h3>DePaul University</h3>
    <p><strong>Bachelor of Science in Network Engineering and Security</strong><br>
    <strong>Bachelor of Science in Cybersecurity</strong><br>
    School of Computing<br>
    September 2020 - June 2024<br>
    GPA: 3.85<br>
    Chicago, IL</p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Professional Experience</h2>
    
    <h3>Al Rajhi Bank</h3>
    <h4>Offensive Security Engineer</h4>
    <p>February 2025 - August 2025 | Riyadh, Saudi Arabia</p>
    <ul>
      <li>Executed 100+ offensive security assessments across web applications, APIs, cloud services, and internal infrastructure</li>
      <li>Conducted 25+ penetration tests, identifying critical authentication, logic, and configuration flaws</li>
      <li>Partnered with detection and incident response teams to validate alerts and improve SIEM coverage (purple team operations)</li>
      <li>Automated testing and reporting workflows using Python and Bash</li>
      <li>Drove the remediation of 100+ security findings with engineering teams</li>
    </ul>
    
    <h3>DePaul University</h3>
    <h4>Student Network Analyst</h4>
    <p>July 2022 - June 2024 | Chicago, IL</p>
    <ul>
      <li>Maintained enterprise network infrastructure with 99.999% uptime</li>
      <li>Deployed and managed 200+ Cisco VoIP phones and network endpoints</li>
      <li>Supported monitoring and security operations across two campuses</li>
    </ul>
    
    <h3>DePaul Security Daemons (CCDC Team)</h3>
    <h4>Network & Security Lead</h4>
    <p>June 2021 - June 2024 | Chicago, IL</p>
    <ul>
      <li>Led red/blue team operations during live cyber defense competitions</li>
      <li>Operated Splunk, Security Onion, Palo Alto, and Cisco Firepower under active attack scenarios</li>
      <li>Authored incident response reports with actionable remediation recommendations</li>
    </ul>
    <p><strong>Achievements:</strong></p>
    <ul>
      <li>1st Place - Midwest CCDC Invitational (2022)</li>
      <li>2nd Place - Regional CCDC (2024)</li>
      <li>14th Place - National CCDC (2024)</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Vulnerability Research & Responsible Disclosure</h2>
    
    <h3>Coolify (Open-Source Cloud Platform)</h3>
    <p>Discovered and responsibly disclosed five critical-severity vulnerabilities (CVSS 9.4), resulting in assigned CVEs: CVE-2025-66209 through CVE-2025-66213.</p>
    <ul>
      <li>Coordinated disclosure via GitHub Security Advisories</li>
      <li>Collaborated with maintainers on validation, root-cause analysis, and remediation prior to public release</li>
      <li>All vulnerabilities involved command injection leading to container escape and root privilege escalation</li>
    </ul>
    <p><a href="/cves/">View detailed CVE analysis</a></p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Certifications</h2>
    <ul>
      <li>Offensive Security Certified Professional (OSCP)</li>
      <li>Offensive Security Defense Analyst (OSDA)</li>
      <li>Cisco Certified Network Associate (CCNA)</li>
      <li>CompTIA Security+ (SEC+)</li>
    </ul>
    <p><a href="/certifications/">View all certifications</a></p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Technical Skills</h2>
    
    <h3>Offensive Security</h3>
    <ul>
      <li>Web/API penetration testing</li>
      <li>Vulnerability research and exploitation</li>
      <li>Adversary emulation and red teaming</li>
      <li>Command injection and privilege escalation</li>
      <li>Container security and escape techniques</li>
    </ul>
    
    <h3>Detection & Incident Response</h3>
    <ul>
      <li>Splunk SIEM</li>
      <li>Security Onion</li>
      <li>ELK Stack</li>
      <li>Purple team operations</li>
      <li>Alert validation and tuning</li>
    </ul>
    
    <h3>Networking & Infrastructure</h3>
    <ul>
      <li>Palo Alto Networks</li>
      <li>Cisco Firepower</li>
      <li>pfSense</li>
      <li>Network segmentation and monitoring</li>
    </ul>
    
    <h3>Automation & Scripting</h3>
    <ul>
      <li>Python</li>
      <li>Bash</li>
      <li>PowerShell</li>
      <li>Security automation and tooling</li>
    </ul>
    
    <h3>Operating Systems</h3>
    <ul>
      <li>Linux (Kali, Ubuntu, Debian)</li>
      <li>Windows Server</li>
      <li>Container technologies (Docker, Kubernetes)</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Contact</h2>
    <p>
      Email: <a href="mailto:ralmutai@andrew.cmu.edu">ralmutai@andrew.cmu.edu</a><br>
      GitHub: <a href="https://github.com/0xrakan">github.com/0xrakan</a><br>
      LinkedIn: <a href="https://linkedin.com/in/rakan-almutairi-105441169">linkedin.com/in/rakan-almutairi-105441169</a>
    </p>
    <p>Currently pursuing M.S. in Information Security at Carnegie Mellon University. Open to security research collaborations and summer 2026 internship opportunities.</p>
  </div>
</div>

<script>
const canvas = document.getElementById('about-particles');
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
