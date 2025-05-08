<p align="center">
  <img src="https://www.docker.com/wp-content/uploads/2022/03/vertical-logo-monochromatic.png" alt="Docker Logo" width="250">
</p>

**[ [🇮🇩 INDONESIAN LANGUAGE VERSION](https://translate.google.com/translate?hl=&sl=en&tl=id&u=https://github.com/albertdveada/Tutorial-Docker-PHP-MySQL) ]**

# Running Docker for PHP & MySQL (Version 8.3)

This repository provides a simple template to run a PHP and MySQL application using Docker. Ideal for beginners or developers who need a fast, isolated, and consistent development environment.

---

## ✨ Key Features

- **Isolation**: Avoid PHP/MySQL version conflicts on your host system.
- **Portability**: Works across multiple operating systems without reconfiguration.
- **Quick Deployment**: Set up your development environment with a single command.
- **Scalability**: Easily extendable for production use.

---

## 🚀 Usage Steps

### 1. Instalasi Docker

- **Download Docker Desktop**:  
  👉 [Download Docker](https://www.docker.com/products/docker-desktop)  
- **User Guide**:  
  👉 [Docker Documentation](https://docs.docker.com/get-started)  
- **Windows Users**:  
  Make sure [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install) is enabled.

---

### 2. Clone Repository & Run the Project

**This repository contains basic configuration for running a PHP and MySQL application using Docker.**

1. **Clone the repository**:
   ```bash
   git clone https://github.com/albertdveada/Tutorial-Docker-PHP-MySQL.git
   
2. **Enter the project directory**:
   ```bash
   cd Tutorial-Docker-PHP-MySQL
   
3. **Start Docker Compose**:
    Run Docker Compose to start the containers in the background.
   ```bash
   docker-compose up -d
   
3. **Access the Application in Your Browser**:

   Once the containers are up, you can access the services at:
   - 🔗 [ Open PHP App (localhost:8080) ](http://localhost:8080)  
   - 🔗 [ Open phpMyAdmin (localhost:8181) ](http://localhost:8181)
   
   
      > 💡 **phpMyAdmin Default Login:**
      > - **Server**: `database`
      > - **Username**: `root`
      > - **Password**: `root_password`

---

### 3. Manage Containers

Use the following commands to manage your Docker container lifecycle:

- **Stop containers**:
  ```bash
  docker-compose stop
- **Restart containers**:
  ```bash
  docker-compose start
- **Remove containers, networks, volumes (for reset)**:
  ```bash
  docker-compose down -v

---

## ⚠️ MySQL Version Notes

- **MySQL 8.1+**: Uses `caching_sha2_password`, **by default.** no additional config needed.
- **MySQL 8.0 or earlier**: Use `mysql_native_password`. Uncomment the following line in `docker-compose.yml`:
  
  ```bash
  command: --default-authentication-plugin=mysql_native_password

## 📁 File Structure:
    📦 Tutorial-Docker-PHP-MySQL/
    ├── docker-compose.yml
    ├── index.php
    └── README.md
    
🔎 **Quick Overview:**
  - `docker-compose.yml`: Defines all services (PHP, MySQL, phpMyAdmin).
  - `index.php`: Example PHP app you can test in the browser.
  - `README.md`: Full setup and usage guide for this project.

💡 You can add folders like `src/`, `config/`, or `public/` as your project grows.

---
Make sure your configuration matches the MySQL version you’re using. For more help, refer to the official Docker or MySQL documentation.
Hope this tutorial helps! 😊
