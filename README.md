# 🚀 BurpSuite Batch Deployment for Docker


Select Language:

- [English](README.md)
- [中文](README_zh.md)





This project allows you to launch **multiple Burp Suite instances** in a Docker environment, supporting both GUI and headless modes.

Current version: **Burp Suite 2020.11.3**


---

## Use cases:

- Batch scanning

- Traffic forwarding

- Crawling backend

- Large-scale cloud deployments


---

## 📁 Docker Image Configuration

Default configuration file path inside the Docker image:
``/usr/local/docker/burp/space/files/default.json``


You can replace this file to customize Burp Suite settings, including proxies, certificates, plugins, etc.

---

## 🖥 GUI Mode

Use this mode if you need to interact visually with Burp Suite.

**Requirements:**

- X11 Server (e.g., MobaXterm)
- Set the DISPLAY variable (example: `127.0.0.1:0.0`)

**Docker Run：**

```bash
docker run -di --name burp-gui \
  -e JAVA_OPTS='-Xmx2g' \
  -e DISPLAY=127.0.0.1:0.0 \
  carpcap/burpsuite-gui:2020.11.3
```

## 🧰 No GUI Mode 
Suitable for batch deployments on servers, saves CPU and memory resources.


```bash
docker run -di --name burp-nogui \
  -e JAVA_OPTS='-Xmx2g' \
  carpcap/burpsuite:2020.11.3
```

