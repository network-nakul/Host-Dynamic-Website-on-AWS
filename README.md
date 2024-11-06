# Host-Dynamic-Website-on-AWS

This project is a simple dynamic To-Do List web application built with **HTML**, **CSS**, **JavaScript**, and **PHP**. The website is hosted on an **AWS EC2 instance** using **Apache** as the web server, allowing for real-time task management in the cloud.

## Features

- **Add tasks** to the list
- **Delete tasks** from the list
- **Persistent storage** using PHP sessions (data is stored as long as the server is running)
- **Dynamic functionality** with HTML, CSS, JavaScript, and PHP

## Project Setup

### Prerequisites

- An AWS EC2 instance (Ubuntu or other Linux-based OS)
- Apache installed on the EC2 instance
- WinSCP (for secure file transfer) or any other SCP client

### Steps for Deployment

1. **Launch an EC2 instance** on AWS and configure the security group to allow HTTP access on port 80.
2. **Connect to the EC2 instance** via SSH.
3. **Install Apache** on the EC2 instance (if not installed already):
    ```bash
    sudo apt update
    sudo apt install apache2 -y
    ```

4. **Upload project files**:
    - Use **WinSCP** (or a similar tool) to securely transfer your project files from your local machine to `/var/www/html` on the EC2 instance.

5. **Set permissions** (if necessary) for the transferred files:
    ```bash
    sudo chmod -R 755 /var/www/html
    ```

6. **Restart Apache** to ensure everything is running:
    ```bash
    sudo systemctl restart apache2
    ```

7. **Access the website** by entering the EC2 instance's public DNS in your browser:
    ```
    http://<your-ec2-public-dns>
    ```

## Folder Structure

****
