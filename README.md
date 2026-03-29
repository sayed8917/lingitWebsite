# lingit Company Website

A modern, professional company website for "lingit" (DevOps & Cloud Services), built for speed, SEO, and maintainability. It features a premium SaaS UI, dark/light mode toggle, and scroll animations using highly optimized Vanilla HTML, CSS, and JS.

## Features
- **Frontend Framework-less:** Blazing fast performance with raw HTML/CSS/JS.
- **Premium Design:** Glassmorphism, tailored color palettes, modern fonts (Inter).
- **Responsive:** Mobile, tablet, and desktop adaptive layouts.
- **Dark Mode:** User preference and toggleable dark theme using `localStorage`.
- **DevOps Ready:** Containerized with Docker and served via Nginx.

## Folder Structure
```text
.
├── assets/
│   └── images/
│       └── hero-bg.png
├── css/
│   └── style.css       # Theming and styles
├── js/
│   └── main.js         # Interactivity (Dark mode, scroll observer)
├── index.html          # Main HTML structure
├── Dockerfile          # Builds the web server container
├── docker-compose.yml  # Orchestrates deployment
├── nginx.conf          # Nginx static file optimization rules
└── README.md           # This documentation
```

---

## 🚀 How to Run Locally (For Beginners)

If you don't want to use Docker, you can preview the website easily on your computer:

1. Download or clone this repository.
2. If you use **VS Code**, install an extension like [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).
3. Open `index.html` in VS Code, right-click anywhere in the code, and select **"Open with Live Server"**.
4. Alternatively, you can simply double-click the `index.html` file to open it directly in your web browser (e.g., Chrome or Firefox).

---

## 🐳 How to Run with Docker (Local & Server)

This project is built to run effortlessly using Docker and Docker Compose, mirroring a production deployment setup.

### Prerequisites:
- [Docker](https://docs.docker.com/get-docker/) must be installed.
- [Docker Compose](https://docs.docker.com/compose/install/) must be installed.

### Step 1: Build and Start the Container

Open your terminal or command prompt, navigate to the folder containing this code, and run:

```bash
docker-compose up -d
```

- `up`: Builds and starts the container.
- `-d`: Runs the container in "detached" mode (in the background).

### Step 2: View the Website
Open your browser and navigate to:
[http://localhost](http://localhost) (or [http://127.0.0.1](http://127.0.0.1))

### Step 3: Stop the Container
To stop the website from running:

```bash
docker-compose down
```

---

## ☁️ How to Deploy on a Server (VPS)

If you want to host this on a real server (like DigitalOcean, AWS EC2, or Linode) so anyone on the internet can see it:

1. **Provision a Linux Server:** Create an Ubuntu/Debian server and log into it.
2. **Install Docker:** Run `sudo apt install docker.io docker-compose -y`.
3. **Transfer Code:** Upload these files to your server (using Git, FTP, or SCP).
4. **Run Compose:** Navigate to the folder on your server and run:
   ```bash
   sudo docker-compose up -d --build
   ```
5. **(Optional) Add a Domain & HTTPS:** 
   - Point your domain's DNS A Record to the Server's IP address.
   - Use a reverse proxy like [Nginx Proxy Manager](https://nginxproxymanager.com/) or [Traefik](https://traefik.io/) to easily handle free SSL certificates (Let's Encrypt).
