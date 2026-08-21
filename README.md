# ShadowXLab — Connected Career Simulator
**Website**: [cybercareer.shadowxlab.com](https://cybercareer.shadowxlab.com)

A web platform simulating an end-to-end cybersecurity career workflow across five professional roles using a single connected enterprise case (**FinBank Customer Portal**).

---

## 🚀 Features

- **Connected Case Chain**: 
  1. **Ethical Hacking**: Discovery, Nmap port scan, service inspection, Wappalyzer fingerprinting, Nikto scanning, Gobuster directory enumeration, Web enumeration.
  2. **VAPT**: Burp Suite Repeater simulation, OWASP ZAP active scanner, BOLA vulnerability verification (`VULN-001`).
  3. **Controlled Attack**: Metasploit (`msfconsole`) attack simulation, Wireshark packet capture telemetry.
  4. **SOC Investigation**: Splunk ES security posture, Threat Intelligence IOC lookup (VirusTotal/AbuseIPDB style), alert correlation, true/false positive classification, containment actions (`INC-1042`).
  5. **GRC / Risk Assessment**: Quantitative risk calculation (Inherent vs Residual), NIST CSF 2.0 (`PR.AA-05`) & ISO 27001 (`A.8.3`) mapping, treatment plan (`RISK-001`).
- **Dynamic Capability Engine**: Computes candidate competency across Technical Reasoning, Investigation, Evidence Handling, Risk Thinking, Decision Quality, and Communication.
- **Role Matching & Readiness**: Evaluates readiness against 10 real-world job roles (SOC L1/L2, Junior VAPT Analyst, GRC Analyst, Blue Team Analyst, etc.).
- **Personalized 4-Month Roadmap**: Targets individual gap areas with recommended labs and milestones.
- **Career Toolkit**: Instant generation of resume bullet points, customized LinkedIn summary, and interview prep checklist.
- **Gamification & Persistence**: Built-in XP, ranking system (Trainee to Principal Analyst), badges shelf, and full LocalStorage state preservation.
- **Theme Support**: Seamless Dark/Light theme toggle.

---

## 🌐 Custom Domain & Deployment Setup

### Domain: `cybercareer.shadowxlab.com`

#### Option 1: GitHub Pages (Recommended)
1. Initialize/Push this repository to GitHub:
   ```bash
   git remote add origin https://github.com/<your-username-or-org>/cybercareer.git
   git push -u origin main
   ```
2. In your GitHub repository:
   - Go to **Settings** > **Pages**
   - Source: Deploy from branch `main` / `root`
   - Custom domain: `cybercareer.shadowxlab.com`
   - Check **Enforce HTTPS**
3. In your DNS provider (Cloudflare / GoDaddy / Namecheap for `shadowxlab.com`):
   - Add a `CNAME` record:
     - **Name / Host**: `cybercareer`
     - **Target**: `<your-username-or-org>.github.io`
     - **Proxy**: DNS only or Proxied (if using Cloudflare)

#### Option 2: Cloudflare Pages / Vercel / Netlify
- Point root directory to `/` and deploy directly from GitHub or static upload.
- Assign custom domain `cybercareer.shadowxlab.com`.

---

## 💻 Local Development / Preview

To test or run locally on your machine:

### Using Python:
```bash
python -m http.server 3000
```
Then open `http://localhost:3000`

### Using Node.js (npx):
```bash
npm start
```
or
```bash
npx serve . -l 3000
```

### Using Windows Batch Launcher:
Double-click `start_server.bat` in this folder.
