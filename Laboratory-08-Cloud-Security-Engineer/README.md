# Laboratory 08 – Cloud Security Engineer

## Mission Overview

This laboratory focuses on securing a web application running inside a Docker container on an Ubuntu server. I deployed an Nginx web server, tested its accessibility using `curl`, and configured UFW (Uncomplicated Firewall) to control incoming and outgoing network traffic. I also applied the Default Deny policy and created specific firewall rules to allow SSH and web traffic on port 8080.

## Objectives

- Deploy an Nginx web server container named `secure-web-app`.
- Verify the application using the `curl` command.
- Understand the Principle of Least Privilege, attack surface, and Default Deny policy.
- Configure UFW to deny incoming traffic by default and allow outgoing traffic.
- Allow SSH access on port 22 before enabling the firewall.
- Create a firewall rule to allow TCP traffic on port 8080.
- Verify firewall rules and document the security configuration.
- Capture screenshots as evidence of the completed tasks.

## Commands Executed

### 1. Check Docker Version

```bash
docker --version
```

### 2. Deploy the Nginx Container

```bash
docker run -d --name secure-web-app -p 8080:80 nginx
```

### 3. Check Running Containers

```bash
docker ps
```

### 4. Test the Web Application

```bash
curl http://localhost:8080
```

### 5. Create the Screenshots Directory

```bash
mkdir -p screenshots
```

### 6. Allow SSH Access

```bash
sudo ufw allow ssh
```

### 7. Configure Default Firewall Policies

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

### 8. Enable the Firewall

```bash
sudo ufw enable
```

### 9. Check Firewall Status

```bash
sudo ufw status verbose
```

### 10. Allow Web Traffic on Port 8080

```bash
sudo ufw allow 8080/tcp
```

### 11. Verify Numbered Firewall Rules

```bash
sudo ufw status numbered
```

## Skills Learned

- **Docker Deployment:** Learned how to run and manage an Nginx container.
- **Application Testing:** Used `curl` to verify that a web application responds to HTTP requests.
- **Firewall Configuration:** Learned how to configure UFW rules to control network traffic.
- **SSH Security:** Understood why SSH access should be allowed before enabling a firewall on a remotely managed server.
- **Default Deny Policy:** Learned to block incoming connections unless they are explicitly permitted.
- **Port Management:** Configured port 8080 to allow access to the web application.
- **Security Documentation:** Practiced documenting commands, security policies, and configuration procedures.
- **Technical Evidence:** Learned to capture and organize screenshots to demonstrate completed laboratory tasks.

---

**Conclusion:** This laboratory helped me understand the importance of firewall configuration, controlled network access, and proper security documentation. By combining Docker deployment with UFW rules, I learned how to establish a basic security boundary around a web application.
