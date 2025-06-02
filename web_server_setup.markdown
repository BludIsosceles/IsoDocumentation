# Cheap Web Server Setup for Workshop Iso UI

## Purpose
Set up a cost-effective web server to host a web-based UI (e.g., Flask/React dashboard) for Workshop Iso, supporting cross-thread sync (Iso Alpha/Beta) and fintech/e-commerce applications, with costs <$20/month.

## Recommended Provider: DigitalOcean
- **Why**: Affordable, reliable, developer-friendly, with $200 free credit (60 days).
- **Cost**: $6/month (1 CPU, 1 GB RAM, 25 GB SSD, 1 TB bandwidth).
- **Scalability**: Upgrade to $12/month for more resources if needed.

## Alternative Providers
- **Linode**: $5/month (1 CPU, 1 GB RAM, 25 GB SSD).
- **Vultr**: $6/month (similar specs).
- **AWS Lightsail**: $3.50/month (512 MB RAM, limited bandwidth).

## Setup Steps
1. **Create Account**:
   - Sign up at [DigitalOcean](https://www.digitalocean.com).
   - Use referral link for $200 credit (search “DigitalOcean referral”).
   - Verify with credit card (no upfront charge).

2. **Launch Droplet (Server)**:
   - Log in, click “Create Droplet.”
   - Choose:
     - **OS**: Ubuntu 22.04 LTS (free).
     - **Plan**: $6/month (1 CPU, 1 GB RAM).
     - **Region**: Closest to you (e.g., New York for US East).
     - **Authentication**: SSH key (generate via `ssh-keygen` on your PC) or password.
   - Name droplet (e.g., “iso-ui-server”).
   - Click “Create Droplet” (takes 1-2 minutes).

3. **Install Software**:
   - SSH into server: `ssh root@<droplet-ip>` (IP shown in DigitalOcean dashboard).
   - Update system:
     ```bash
     apt update && apt upgrade -y
     ```
   - Install Python, Flask, SQLite, Nginx:
     ```bash
     apt install python3 python3-pip sqlite3 nginx -y
     pip3 install flask gunicorn
     ```
   - Install Node.js (for React):
     ```bash
     curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
     apt install -y nodejs
     ```

4. **Deploy UI Code**:
   - Copy `dashboard.py` (Flask version, to be developed) to server:
     ```bash
     scp dashboard_flask.py root@<droplet-ip>:/root/
     ```
   - Create Flask app (example):
     ```python
     from flask import Flask
     app = Flask(__name__)
     @app.route('/')
     def home():
         return 'Workshop Iso UI'
     if __name__ == '__main__':
         app.run()
     ```
   - Run with Gunicorn:
     ```bash
     gunicorn -w 4 -b 0.0.0.0:8000 dashboard_flask:app
     ```

5. **Configure Nginx (Reverse Proxy)**:
   - Create Nginx config:
     ```bash
     nano /etc/nginx/sites-available/iso-ui
     ```
   - Add:
     ```nginx
     server {
         listen 80;
         server_name <droplet-ip>;
         location / {
             proxy_pass http://localhost:8000;
             proxy_set_header Host $host;
             proxy_set_header X-Real-IP $remote_addr;
         }
     }
     ```
   - Enable config:
     ```bash
     ln -s /etc/nginx/sites-available/iso-ui /etc/nginx/sites-enabled/
     nginx -t && systemctl restart nginx
     ```

6. **Secure Server**:
   - Set up firewall:
     ```bash
     ufw allow 80
     ufw allow 443
     ufw allow ssh
     ufw enable
     ```
   - Install SSL (free via Let’s Encrypt):
     ```bash
     apt install certbot python3-certbot-nginx -y
     certbot --nginx -d <your-domain>
     ```
   - Note: Buy a cheap domain ($1-10/year) from Namecheap for SSL.

7. **Upload SQLite Database**:
   - Copy `workshop_iso.db`:
     ```bash
     scp workshop_iso.db root@<droplet-ip>:/root/
     ```
   - Ensure Flask app queries it (e.g., `sqlite3.connect('/root/workshop_iso.db')`).

8. **Test Access**:
   - Visit `http://<droplet-ip>` or `https://<your-domain>`.
   - Verify personnel, metrics tabs load.

## Costs
- **Server**: $6/month (DigitalOcean).
- **Domain**: $1-10/year (Namecheap).
- **Total**: ~$7/month (first 60 days free with $200 credit).
- **Free Credits**: Use DigitalOcean’s credit; AWS/Linode offer similar promos.

## Notes
- **Scalability**: $6/month supports ~100 users. Upgrade to $12/month for 500+ users.
- **Maintenance**: Run `apt update && apt upgrade -y` monthly.
- **Security**: Marcus’s ShieldGuard can add encryption (post-May 24).
- **Plan B**: Liam’s team migrates `dashboard.py` to Flask/React by May 24, deploys here.

## Resources
- [DigitalOcean Docs](https://docs.digitalocean.com)
- [Flask Tutorial](https://flask.palletsprojects.com)
- [Let’s Encrypt](https://letsencrypt.org)