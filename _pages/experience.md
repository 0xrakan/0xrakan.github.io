---
layout: splash
title: "Experience"
permalink: /experience/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');

body {
  background: #000;
  color: #fff;
}

#exp-particles {
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
  margin: 2.5rem 0 1rem 0;
  position: relative;
  padding-left: 1.5rem;
}

h3::before {
  content: '▸';
  position: absolute;
  left: 0;
  color: #667eea;
}

h4 {
  color: #f093fb;
  font-size: 1.2rem;
  font-weight: 600;
  margin: 1rem 0 0.5rem 0;
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
  content: '•';
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
  margin: 2.5rem 0;
}

.btn {
  display: inline-block;
  padding: 0.8rem 2rem;
  background: linear-gradient(135deg, #667eea, #764ba2);
  color: #fff;
  border-radius: 8px;
  margin: 0.5rem;
  transition: all 0.3s ease;
  text-decoration: none;
  font-weight: 600;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 25px rgba(102, 126, 234, 0.3);
  color: #fff;
}

.experience-card {
  background: rgba(255, 255, 255, 0.02);
  border-left: 3px solid #667eea;
  border-radius: 8px;
  padding: 2rem;
  margin-bottom: 2rem;
  transition: all 0.3s ease;
}

.experience-card:hover {
  background: rgba(255, 255, 255, 0.05);
  transform: translateX(10px);
  box-shadow: 0 10px 30px rgba(102, 126, 234, 0.2);
}
</style>

<canvas id="exp-particles"></canvas>

<div class="content-wrapper">
  <h1 class="page-title">Experience</h1>
  
  <div class="section">
    <h2>Professional Experience</h2>
    
    <div class="experience-card">
      <h3>Al Rajhi Bank</h3>
      <h4>Offensive Security Engineer</h4>
      <p><strong>February 2025 - August 2025 | Riyadh, Saudi Arabia</strong></p>
      <p>Executed comprehensive offensive security operations for one of the largest financial institutions in the Middle East.</p>
      
      <p><strong>Responsibilities:</strong></p>
      <ul>
        <li>Executed 100+ offensive security assessments across web applications, APIs, cloud services, and internal infrastructure</li>
        <li>Conducted 25+ penetration tests, identifying critical authentication, logic, and configuration flaws</li>
        <li>Partnered with detection and incident response teams to validate alerts and improve SIEM coverage (purple team operations)</li>
        <li>Automated testing and reporting workflows using Python and Bash</li>
        <li>Drove the remediation of 100+ security findings with engineering teams</li>
      </ul>
      
      <p><strong>Key Achievements:</strong></p>
      <ul>
        <li>Identified and remediated critical vulnerabilities in customer-facing applications</li>
        <li>Improved detection coverage through purple team exercises</li>
        <li>Developed automation tools to streamline security testing workflows</li>
      </ul>
    </div>
    
    <div class="divider"></div>
    
    <div class="experience-card">
      <h3>DePaul University</h3>
      <h4>Student Network Analyst</h4>
      <p><strong>July 2022 - June 2024 | Chicago, IL</strong></p>
      <p>Maintained enterprise network infrastructure supporting thousands of students and faculty.</p>
      
      <p><strong>Responsibilities:</strong></p>
      <ul>
        <li>Maintained enterprise network infrastructure with 99.999% uptime</li>
        <li>Deployed and managed 200+ Cisco VoIP phones and network endpoints</li>
        <li>Supported monitoring and security operations across two campuses</li>
        <li>Troubleshot network connectivity and performance issues</li>
        <li>Participated in network upgrade and maintenance projects</li>
      </ul>
    </div>
    
    <div class="divider"></div>
    
    <div class="experience-card">
      <h3>DePaul Security Daemons (CCDC Team)</h3>
      <h4>Network & Security Lead</h4>
      <p><strong>June 2021 - June 2024 | Chicago, IL</strong></p>
      <p>Led competitive cyber defense team in regional and national competitions.</p>
      
      <p><strong>Responsibilities:</strong></p>
      <ul>
        <li>Led red/blue team operations during live cyber defense competitions</li>
        <li>Operated Splunk, Security Onion, Palo Alto, and Cisco Firepower under active attack scenarios</li>
        <li>Authored incident response reports with actionable remediation recommendations</li>
        <li>Mentored team members on defensive security techniques</li>
        <li>Coordinated team response during high-pressure competition scenarios</li>
      </ul>
      
      <p><strong>Competition Results:</strong></p>
      <ul>
        <li>1st Place: Midwest CCDC Invitational (2022)</li>
        <li>2nd Place: Regional CCDC (2024)</li>
        <li>14th Place: National CCDC (2024)</li>
      </ul>
    </div>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Education</h2>
    
    <div class="experience-card">
      <h3>Carnegie Mellon University</h3>
      <h4>M.S. Information Technology (Information Security)</h4>
      <p><strong>August 2025 - May 2027 (Current) | Pittsburgh, PA</strong></p>
      <p>Specializing in offensive security, vulnerability research, and secure systems design through the Information Networking Institute (INI).</p>
      
      <p><strong>Coursework:</strong></p>
      <ul>
        <li>Advanced penetration testing</li>
        <li>Vulnerability research and exploitation</li>
        <li>Secure software development</li>
        <li>Network security architecture</li>
        <li>Applied cryptography</li>
      </ul>
    </div>
    
    <div class="experience-card">
      <h3>DePaul University</h3>
      <h4>B.S. Network Engineering and Security</h4>
      <h4>B.S. Cybersecurity</h4>
      <p><strong>September 2020 - June 2024 | Chicago, IL</strong></p>
      <p>Dual degree program covering both defensive and offensive security principles.</p>
      <p><strong>GPA: 3.85</strong></p>
      
      <p><strong>Relevant Coursework:</strong></p>
      <ul>
        <li>Penetration testing and ethical hacking</li>
        <li>Network security and monitoring</li>
        <li>Cryptography and secure communications</li>
        <li>Operating systems security</li>
        <li>Malware analysis</li>
      </ul>
    </div>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Skills & Expertise</h2>
    
    <h3>Offensive Security</h3>
    <ul>
      <li>Web application penetration testing</li>
      <li>API security testing</li>
      <li>Network penetration testing</li>
      <li>Vulnerability research and exploitation</li>
      <li>Red team operations</li>
      <li>Social engineering</li>
    </ul>
    
    <h3>Detection & Response</h3>
    <ul>
      <li>SIEM deployment and tuning (Splunk, ELK)</li>
      <li>Security monitoring and log analysis</li>
      <li>Incident detection and response</li>
      <li>Threat hunting</li>
      <li>Purple team operations</li>
    </ul>
    
    <h3>Tools & Technologies</h3>
    <ul>
      <li>Burp Suite, OWASP ZAP</li>
      <li>Metasploit, Cobalt Strike</li>
      <li>Nmap, Nessus, OpenVAS</li>
      <li>Wireshark, tcpdump</li>
      <li>Splunk, Security Onion</li>
      <li>Python, Bash, PowerShell</li>
    </ul>
    
    <h3>Networking</h3>
    <ul>
      <li>Palo Alto Networks firewalls</li>
      <li>Cisco Firepower</li>
      <li>pfSense</li>
      <li>Network segmentation and monitoring</li>
      <li>VPN and remote access security</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div style="text-align: center;">
    <a href="/cves/" class="btn">View CVE Discoveries</a>
    <a href="/certifications/" class="btn">View Certifications</a>
  </div>
</div>

<script>
const canvas = document.getElementById('exp-particles');
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
