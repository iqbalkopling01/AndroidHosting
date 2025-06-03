## 🔍 System Overview
- Device: Mi 11 Lite (aarch64)
- OS: Ubuntu Server via UserLand
- Web Server: Nginx (port 8080)
- Domain: Managed via Cloudflare
- Access: Cloudflare Tunnel + Zero Trust
- SSL: Provided by Cloudflare

## 🧰 System Requirements
- Hardware: Mi 11 Lite
- Software: UserLand, PuTTY, GitHub, Microsoft Word

## 🏗️ Project Stages
### 1. Preparing the Device
Install Ubuntu on Android using UserLand. Minimal terminal environment is preferred.
![Setup Step 1](images/image (1).png)
![Setup Step 2](images/image (2).png)
![Setup Step 3](images/image (3).png)
![Setup Step 4](images/image (4).png)
![Setup Step 5](images/image (5).png)
![Setup Step 6](images/image (6).png)
![Setup Step 7](images/image (7).png)
![Setup Step 8](images/image (8).png)
![Setup Step 9](images/image (9).png)
![Setup Step 10](images/image (10).png)

### 2. Server Configuration
- `sudo su` to gain root
- `apt update && upgrade`
- Install `neofetch`, `net-tools`, `nano`
- Install Nginx on port `8080`
![Server Config 1](images/image (11).png)
![Server Config 2](images/image (12).png)
![Server Config 3](images/image (13).png)
![Server Config 4](images/image (14).png)
![Server Config 5](images/image (15).png)
![Server Config 6](images/image (16).png)
![Server Config 7](images/image (17).png)
![Server Config 8](images/image (18).png)
![Server Config 9](images/image (19).png)
![Server Config 10](images/image (20).png)
### 3. Domain Setup via Cloudflare
Buy domain, register Cloudflare, set nameservers, disable DNSSEC.
![Cloudflare Setup 1](images/image (21).png)
![Cloudflare Setup 2](images/image (22).png)
![Cloudflare Setup 3](images/image (23).png)
![Cloudflare Setup 4](images/image (24).png)
![Cloudflare Setup 5](images/image (25).png)
![Cloudflare Setup 6](images/image (26).png)
![Cloudflare Setup 7](images/image (27).png)
![Cloudflare Setup 8](images/image (28).png)
![Cloudflare Setup 9](images/image (29).png)
![Cloudflare Setup 10](images/image (30).png)
### 4. Cloudflare Tunnel (Zero Trust)
Create tunnel, bind public hostname to `localhost:8080`, validate with domain.
### 5. Blog Deployment
- Create static HTML/CSS site
- Upload to GitHub
- Clone repo to `/var/www/html`
- Use `git pull` to update
## ✅ Project Outcome
### 🎯 Goals Achieved
- Static blog hosted successfully on private server
### 🔐 Security and Reliability
- Cloudflare hides real IP
- Zero Trust ensures validated access
### ⚠️ Limitations
- Android hardware limits performance
- UserLand setup is complex
### 💡 Future Recommendations
- CI/CD with GitHub Actions
- Monitoring with Prometheus/Grafana
- Web performance optimization


## 🌐 Domain
Access: [iqbalmln.my.id](http://iqbalmln.my.id)
## 📬 Contact
Open an issue or PR for suggestions/contributions.
