# 🛠️ Splunk Enterprise Installation on Ubuntu


!!!!!! YOU FIND THE IMAGES IN /images in this directory !!!!!!!!!!!!!!!!!!!!!!!!!!!!
## 📘 Overview

This guide walks you through installing **Splunk Enterprise** on an Ubuntu machine. The setup is part of the SOC Lab project and is essential for collecting and analyzing security event logs.

---

## ✅ Prerequisites

- A Splunk account (register at [splunk.com](https://www.splunk.com))
- An Ubuntu system with sudo privileges
- Internet access on the machine
- Firewall access to port `8000` (for the web interface)

---

## 🔽 Step 1: Download Splunk Enterprise

1. Go to the [Splunk Downloads Page](https://www.splunk.com/en_us/download/splunk-enterprise.html)
2. Choose:
   - Product: **Splunk Enterprise**
   - Platform: **Linux (Debian package)**
3. Copy the **direct download link** or download it manually.

Use `wget` to download the `.deb` file from your terminal:

```bash
wget -O splunk.deb 'https://download.splunk.com/products/splunk/releases/X.X.X/linux/splunk-X.X.X-XXXXXXX-linux-2.6-amd64.deb'
```

> Replace the URL with the latest version from the Splunk website.

---

## 📦 Step 2: Install Splunk

Use the following command to install the downloaded package:

```bash
sudo dpkg -i splunk.deb
```

---

## 🚀 Step 3: Start Splunk

Navigate to the Splunk installation directory and start the service:

```bash
cd /opt/splunk/bin/
sudo ./splunk start --accept-license
```

- You'll be prompted to create a **username and password**.
- Choose a **strong, secure password** (especially for production/lab environments).

---

## 🌐 Step 4: Access Splunk Web Interface

Once Splunk is running, open your browser and go to:

```
http://<your-server-ip>:8000
```

> Replace `<your-server-ip>` with the IP address of your Ubuntu system.

You should see the Splunk login page — log in with the credentials you just created.

---

## 🔧 Additional Notes & Troubleshooting

### 🧑‍💻 Use a Sudo-Enabled User

Ensure you're logged in with a user that has `sudo` privileges. Non-sudo users may face permission issues during installation and startup.

---

### 🔥 Open Firewall Port 8000

If you're running a firewall (e.g., UFW), allow traffic on Splunk’s default web port:

```bash
sudo ufw allow 8000/tcp
```

You may also need to allow HTTP traffic if you're accessing it remotely.

---

### 🔄 Restarting and Stopping Splunk

To restart or stop Splunk:

```bash
sudo ./splunk restart
sudo ./splunk stop
```

To enable Splunk to start on boot:

```bash
sudo ./splunk enable boot-start
```

---

## ✅ Installation Complete

Splunk is now installed and running on your Ubuntu machine. You can begin indexing logs and building detections for your SOC lab.

> 🧪 Continue by integrating log sources, building dashboards, and setting up alerts.

---

## 📎 Related Resources

- [Splunk Official Docs](https://docs.splunk.com/)
- [Splunk Admin Manual](https://docs.splunk.com/Documentation/Splunk/latest/Admin/Adminmanual)
- [SOC Lab Project README](./README.md)
