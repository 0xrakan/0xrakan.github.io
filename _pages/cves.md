---
layout: splash
title: "CVE Discoveries"
permalink: /cves/
---

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;900&display=swap');

body {
  background: #000;
  color: #fff;
}

#cve-particles {
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
  background: linear-gradient(135deg, #ff0080, #ff8c00, #40e0d0);
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
  color: #ff0080;
  font-size: 2rem;
  font-weight: 700;
  margin: 3rem 0 1.5rem 0;
  padding: 1.5rem;
  background: rgba(255, 0, 128, 0.05);
  border-left: 4px solid #ff0080;
  border-radius: 8px;
}

h3 {
  color: #ff8c00;
  font-size: 1.5rem;
  font-weight: 700;
  margin: 2rem 0 1rem 0;
}

h4 {
  color: #40e0d0;
  font-size: 1.2rem;
  font-weight: 600;
  margin: 1.5rem 0 0.5rem 0;
}

p {
  color: #ccc;
  line-height: 1.8;
  margin-bottom: 1rem;
}

.cve-meta {
  background: rgba(255, 255, 255, 0.02);
  padding: 1rem;
  border-radius: 8px;
  margin: 1rem 0;
  border-left: 3px solid #667eea;
}

.cve-meta p {
  margin: 0.5rem 0;
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
  color: #ff0080;
}

table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
  margin: 2rem 0;
  background: rgba(255, 255, 255, 0.02);
  border-radius: 12px;
  overflow: hidden;
}

thead {
  background: linear-gradient(135deg, rgba(102, 126, 234, 0.2), rgba(118, 75, 162, 0.2));
}

th {
  padding: 1rem;
  text-align: left;
  font-weight: 700;
  color: #667eea;
  border-bottom: 2px solid rgba(102, 126, 234, 0.3);
}

td {
  padding: 1rem;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

tr:hover {
  background: rgba(102, 126, 234, 0.1);
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
  background: linear-gradient(90deg, transparent, rgba(255, 0, 128, 0.5), transparent);
  margin: 3rem 0;
}
</style>

<canvas id="cve-particles"></canvas>

<div class="content-wrapper">
  <h1 class="page-title">CVE Discoveries</h1>
  
  <div class="section">
    <h2>Overview</h2>
    <p>I discovered and responsibly disclosed five critical-severity vulnerabilities (CVSS 9.4) in Coolify, a popular open-source cloud deployment platform. All vulnerabilities involve authenticated command injection that allows users to achieve container escape and root-level code execution on managed servers.</p>
    <p><strong>Public Disclosure:</strong> <a href="https://github.com/0xrakan/coolify-cve-2025-66209-66213" target="_blank">GitHub Repository</a></p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE-2025-66213</h2>
    <h3>Authenticated Remote Code Execution via Command Injection in File Storage Directory Mount Path</h3>
    
    <div class="cve-meta">
      <p><strong>CVSS Score:</strong> 9.4 (Critical)</p>
      <p><strong>GHSA ID:</strong> <a href="https://github.com/coollabsio/coolify/security/advisories/GHSA-cj2c-9jx8-j427" target="_blank">GHSA-cj2c-9jx8-j427</a></p>
      <p><strong>CWE:</strong> CWE-78 (OS Command Injection)</p>
      <p><strong>CVE.org:</strong> <a href="https://www.cve.org/CVERecord?id=CVE-2025-66213" target="_blank">CVE-2025-66213</a></p>
    </div>
    
    <h4>Description</h4>
    <p>An authenticated command injection vulnerability in the File Storage Directory Mount Path functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. The file_storage_directory_source parameter is passed directly to shell commands without proper sanitization, enabling full remote code execution on the host system.</p>
    
    <h4>Impact</h4>
    <ul>
      <li>Arbitrary command execution as root</li>
      <li>Container escape</li>
      <li>Full host system compromise</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE-2025-66212</h2>
    <h3>Authenticated Remote Code Execution via Command Injection in Dynamic Proxy Configuration Filename</h3>
    
    <div class="cve-meta">
      <p><strong>CVSS Score:</strong> 9.4 (Critical)</p>
      <p><strong>GHSA ID:</strong> <a href="https://github.com/coollabsio/coolify/security/advisories/GHSA-q7rg-2j7p-83gp" target="_blank">GHSA-q7rg-2j7p-83gp</a></p>
      <p><strong>CWE:</strong> CWE-78 (OS Command Injection)</p>
      <p><strong>CVE.org:</strong> <a href="https://www.cve.org/CVERecord?id=CVE-2025-66212" target="_blank">CVE-2025-66212</a></p>
    </div>
    
    <h4>Description</h4>
    <p>An authenticated command injection vulnerability in the Dynamic Proxy Configuration Filename handling allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Proxy configuration filenames are passed to shell commands without proper escaping, enabling full remote code execution.</p>
    
    <h4>Impact</h4>
    <ul>
      <li>Arbitrary command execution as root</li>
      <li>Container escape</li>
      <li>Full host system compromise</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE-2025-66211</h2>
    <h3>Authenticated Remote Code Execution via Command Injection in PostgreSQL Init Script Filename</h3>
    
    <div class="cve-meta">
      <p><strong>CVSS Score:</strong> 9.4 (Critical)</p>
      <p><strong>GHSA ID:</strong> <a href="https://github.com/coollabsio/coolify/security/advisories/GHSA-24mp-fc9q-c884" target="_blank">GHSA-24mp-fc9q-c884</a></p>
      <p><strong>CWE:</strong> CWE-78 (OS Command Injection)</p>
      <p><strong>CVE.org:</strong> <a href="https://www.cve.org/CVERecord?id=CVE-2025-66211" target="_blank">CVE-2025-66211</a></p>
    </div>
    
    <h4>Description</h4>
    <p>An authenticated command injection vulnerability in PostgreSQL Init Script Filename handling allows users with application/service management permissions to execute arbitrary commands as root on managed servers. PostgreSQL initialization script filenames are passed to shell commands without proper validation, enabling full remote code execution.</p>
    
    <h4>Impact</h4>
    <ul>
      <li>Arbitrary command execution as root</li>
      <li>Container escape</li>
      <li>Full host system compromise</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE-2025-66209</h2>
    <h3>Authenticated Remote Code Execution via Command Injection in Database Backup</h3>
    
    <div class="cve-meta">
      <p><strong>CVSS Score:</strong> 9.4 (Critical)</p>
      <p><strong>GHSA ID:</strong> <a href="https://github.com/coollabsio/coolify/security/advisories/GHSA-vm5p-43qh-7pmq" target="_blank">GHSA-vm5p-43qh-7pmq</a></p>
      <p><strong>CWE:</strong> CWE-78 (OS Command Injection)</p>
      <p><strong>CVE.org:</strong> <a href="https://www.cve.org/CVERecord?id=CVE-2025-66209" target="_blank">CVE-2025-66209</a></p>
    </div>
    
    <h4>Description</h4>
    <p>An authenticated command injection vulnerability in the Database Backup functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Database names used in backup operations are passed directly to shell commands without sanitization, enabling full remote code execution.</p>
    
    <h4>Impact</h4>
    <ul>
      <li>Arbitrary command execution as root</li>
      <li>Container escape</li>
      <li>Full host system compromise</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE-2025-66210</h2>
    <h3>Authenticated Remote Code Execution via Command Injection in Database Import</h3>
    
    <div class="cve-meta">
      <p><strong>CVSS Score:</strong> 9.4 (Critical)</p>
      <p><strong>GHSA ID:</strong> <a href="https://github.com/coollabsio/coolify/security/advisories/GHSA-q33h-22xm-4cgh" target="_blank">GHSA-q33h-22xm-4cgh</a></p>
      <p><strong>CWE:</strong> CWE-78 (OS Command Injection)</p>
      <p><strong>CVE.org:</strong> <a href="https://www.cve.org/CVERecord?id=CVE-2025-66210" target="_blank">CVE-2025-66210</a></p>
    </div>
    
    <h4>Description</h4>
    <p>An authenticated command injection vulnerability in the Database Import functionality allows users with application/service management permissions to execute arbitrary commands as root on managed servers. Database names used in import operations are passed directly to shell commands without sanitization, enabling full remote code execution.</p>
    
    <h4>Impact</h4>
    <ul>
      <li>Arbitrary command execution as root</li>
      <li>Container escape</li>
      <li>Full host system compromise</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Technical Analysis</h2>
    
    <h3>Root Cause</h3>
    <p>All five vulnerabilities stem from insufficient input validation and sanitization of user-controlled parameters that are subsequently passed to shell commands. The affected functionality processes database names, file paths, and configuration filenames without proper escaping, allowing shell metacharacters to be injected and executed.</p>
    
    <h3>Attack Vector</h3>
    <p>Since Coolify runs with elevated privileges to manage Docker containers and host system operations, successful exploitation of any of these vulnerabilities leads to command execution as the root user on the host system, effectively achieving container escape and complete host compromise.</p>
    
    <h3>Proof of Concept</h3>
    <p>Technical details and proof-of-concept exploits are being withheld to allow users additional time to upgrade. All vulnerabilities have been patched in v4.0.0-beta.451.</p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Remediation</h2>
    <p>Upgrade to Coolify v4.0.0-beta.451 or later immediately.</p>
    <p>The Coolify development team has implemented comprehensive input validation and shell argument escaping across all affected functionality to prevent command injection attacks.</p>
    <p><strong>Fix Pull Request:</strong> <a href="https://github.com/coollabsio/coolify/pull/7375" target="_blank">coollabsio/coolify#7375</a></p>
    <p><strong>Fixed Release:</strong> <a href="https://github.com/coollabsio/coolify/releases/tag/v4.0.0-beta.451" target="_blank">v4.0.0-beta.451</a></p>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>Disclosure Timeline</h2>
    <ul>
      <li>November 2025: Vulnerabilities discovered and reported to maintainer</li>
      <li>December 2025: CVE IDs assigned by GitHub Security</li>
      <li>December 3, 2025: Fixes released in v4.0.0-beta.451</li>
      <li>December 21, 2025: Public disclosure</li>
      <li>December 23, 2025: CVEs officially published to CVE.org</li>
    </ul>
  </div>
  
  <div class="divider"></div>
  
  <div class="section">
    <h2>CVE Registry</h2>
    <table>
      <thead>
        <tr>
          <th>CVE ID</th>
          <th>CVE.org Link</th>
          <th>GHSA ID</th>
          <th>Component</th>
          <th>Status</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>CVE-2025-66213</td>
          <td><a href="https://www.cve.org/CVERecord?id=CVE-2025-66213" target="_blank">View</a></td>
          <td>GHSA-cj2c-9jx8-j427</td>
          <td>File Storage Directory Mount Path</td>
          <td>Patched</td>
        </tr>
        <tr>
          <td>CVE-2025-66212</td>
          <td><a href="https://www.cve.org/CVERecord?id=CVE-2025-66212" target="_blank">View</a></td>
          <td>GHSA-q7rg-2j7p-83gp</td>
          <td>Dynamic Proxy Configuration Filename</td>
          <td>Patched</td>
        </tr>
        <tr>
          <td>CVE-2025-66211</td>
          <td><a href="https://www.cve.org/CVERecord?id=CVE-2025-66211" target="_blank">View</a></td>
          <td>GHSA-24mp-fc9q-c884</td>
          <td>PostgreSQL Init Script Filename</td>
          <td>Patched</td>
        </tr>
        <tr>
          <td>CVE-2025-66209</td>
          <td><a href="https://www.cve.org/CVERecord?id=CVE-2025-66209" target="_blank">View</a></td>
          <td>GHSA-vm5p-43qh-7pmq</td>
          <td>Database Backup</td>
          <td>Patched</td>
        </tr>
        <tr>
          <td>CVE-2025-66210</td>
          <td><a href="https://www.cve.org/CVERecord?id=CVE-2025-66210" target="_blank">View</a></td>
          <td>GHSA-q33h-22xm-4cgh</td>
          <td>Database Import</td>
          <td>Patched</td>
        </tr>
      </tbody>
    </table>
    <p><strong>Credit:</strong> Discovered and reported by Rakan Almutairi (@0xrakan)<br>
    <strong>Fixed by:</strong> Coolify development team (@andrasbacsi)</p>
    <p>All CVEs are now officially published in the MITRE CVE database and available on CVE.org.</p>
  </div>
</div>

<script>
const canvas = document.getElementById('cve-particles');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = document.documentElement.scrollHeight;

const particles = [];
const particleCount = 50;
const colors = ['#ff0080', '#ff8c00', '#40e0d0'];

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
  
  requestAnimationFrame(animate);
}

animate();

window.addEventListener('resize', () => {
  canvas.width = window.innerWidth;
  canvas.height = document.documentElement.scrollHeight;
});
</script>
