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

Open the app and choose Ubuntu 

![Setup Step 1](s/1.png)

Give the permission needed

![Setup Step 2](s/2.png)
![Setup Step 3](s/3.png)

Choose minimal environtment

![Setup Step 4](s/4.png)

Choose Terminal GUI only so that the server would run smoothly even just running on an android mobile phone

![Setup Step 5](s/5.png)
![Setup Step 6](s/6.png)

Wait till the process done. Once the process done, the terminal screen will appear.

![Setup Step 7](s/7.png)

### 2. Server Configuration
First, type sudo su to gain the highest previllege on the server.

![Setup Step 8](s/8.png)

Netx, update the password on your server by typing passwd. Type your password 2 times.

![Setup Step 9](s/9.png)

Before beginning any installs, update and upgrade the repository if you haven't already. 

sudo apt update && apt upgrade -y	

![Setup Step 10](s/10.png)!
[Setup Step 10](s/10.png)

Next, install neofetch to verified the version of operating system used.

apt install neofetch -y

![Server Config 1](s/11.png)

Verify the installation by typing neofetch

![Server Config 2](s/12.png)

Install net-tools to check device’s IP address. (Author was already installed net-tools)

apt install net-tools -y

![Server Config 3](s/13.png)

Check device’s IP address using ifconfig. Numbers after ‘inet’ is the device’s IP. Write or just remember it. It will be used later.

![Server Config 4](s/14.png)

Configuring The Web Server: Web server used on this project is Nginx. 

apt install nginx -y 

![Server Config 5](s/15.png)

Next, verify the status of nginx (at first, it will show that nginx is not running, but it’s not a problem because nginx is not started yet). Nginx need more configuration and text editor choosen is nano.

service nginx status
apt install nano -y

![Server Config 6](s/16.png)

Next configuration for nginx is changing the default port to 8080. To do this, use command below.

nano /etc/nginx/sites-available/default

![Server Config 7](s/17.png)

Change “80” to 8080. Click CTRL+X, then press Y, and press Enter button on keyboard to exit from nano and back to terminal.
Next, restart nginx service. Once it’s done restarting, it will show [OK].

service nginx restart

![Server Config 8](s/18.png)

Verify the service by accessing device’s IP:8080 on browser. 
Example: 192.168.1.2:8080

![Server Config 9](s/19.png)

The web server is already working. Next, for changing the welcoming page. Go to default web page’s directory by using comand below.

cd /var/www/html 

![Server Config 10](s/20.png)

There will be a default file: index.nginx-debian.html. Remove it by command below.

rm -r index.nginx-debian.html

![Cloudflare Setup 1](s/21.png)
![Cloudflare Setup 2](s/22.png)

### 3. Domain Setup via Cloudflare
Buy domain, register Cloudflare, set nameservers, disable DNSSEC.

**3.1 Get The Domain.**
Author bouught a cheap domain on idcloudhost.com. 

**3.2 Create Cloudflare Account**
Go to cloudflare.com

![Cloudflare Setup 3](s/23.png)

Click Log In and Simply just click Continue with Google and finish the entire process.

![Cloudflare Setup 4](s/24.png)

**3.3	Add Domain to Cloudflare**
Picture below is page that will show up after you created an account. Type your domain to available field, choose the Quick scan option, and click continue.

![Cloudflare Setup 5](s/25.png)

Choose the most suit plan and confirm plan (Author choose the free plan).

![Cloudflare Setup 6](s/26.png)

Next, click continue to activation

![Cloudflare Setup 7](s/27.png)

Pay attention to any information that showed on the page.

![Cloudflare Setup 8](s/28.png)

Log in to your domain registrar (Author is using idcloudhost) to turn off DNSSEC and update nameservers.

![Cloudflare Setup 9](s/29.png)

Choose your domain and click the three dots after ‘status’.

![Cloudflare Setup 10](s/30.png)

Choose “Manage Nameservers”.

![Cloudflare Setup 11](s/31.png)

Choose “Use Custom Nameservers” and change the first two default value (given by domain registrar. Example: Sindoro.cloudhost.com) by name server given by cloudflare. Scroll a little bit and click Change Nameservers.

![Cloudflare Setup 12](s/32.png)

Next, choose Manage DNSSec and make sure there is no DNSSec records found.

![Cloudflare Setup 13](s/33.png)

![Cloudflare Setup 14](s/34.png)


Next, press previous button and choose manage DNS and change the default value (given by domain registrar. Example: Sindoro.cloudhost.com) by name server that given by cloudflare (the same domain that you put on Nameserver). 

![Cloudflare Setup 15](s/35.png)

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
