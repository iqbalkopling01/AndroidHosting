## HOW TO: Create your OWN Hosting by your ANDROID PHONE!
You think hosting service is expensive?? Actually, yes it is lol. But i'll provide you some cheap

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
![Setup Step 1](s/1.png)
![Setup Step 2](s/2.png)
![Setup Step 3](s/3.png)
![Setup Step 4](s/4.png)
![Setup Step 5](s/5.png)
![Setup Step 6](s/6.png)
![Setup Step 7](s/7.png)
![Setup Step 8](s/8.png)
![Setup Step 9](s/9.png)
![Setup Step 10](s/10.png)

### 2. Server Configuration
- `sudo su` to gain root
- `apt update && upgrade`
- Install `neofetch`, `net-tools`, `nano`
- Install Nginx on port `8080`
![Server Config 1](s/11.png)
![Server Config 2](s/12.png)
![Server Config 3](s/13.png)
![Server Config 4](s/14.png)
![Server Config 5](s/15.png)
![Server Config 6](s/16.png)
![Server Config 7](s/17.png)
![Server Config 8](s/18.png)
![Server Config 9](s/19.png)
![Server Config 10](s/20.png)

### 3. Domain Setup via Cloudflare
Buy domain, register Cloudflare, set nameservers, disable DNSSEC.
![Cloudflare Setup 1](s/21.png)
![Cloudflare Setup 2](s/22.png)
![Cloudflare Setup 3](s/23.png)
![Cloudflare Setup 4](s/24.png)
![Cloudflare Setup 5](s/25.png)
![Cloudflare Setup 6](s/26.png)
![Cloudflare Setup 7](s/27.png)
![Cloudflare Setup 8](s/28.png)
![Cloudflare Setup 9](s/29.png)
![Cloudflare Setup 10](s/30.png)

### 4. Cloudflare Tunnel (Zero Trust)
Create tunnel, bind public hostname to `localhost:8080`, validate with domain.

### 5. Blog Deployment
- Create static HTML/CSS site
- Upload to GitHub
- Clone repo to `/var/www/html`
- Use `git pull` to update
- 
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
