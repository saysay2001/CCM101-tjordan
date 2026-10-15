# Firewall Configuration Documentation

## 1. Allow SSH Access

```bash
sudo ufw allow ssh
```

This command allows incoming SSH connections on port 22 so administrators can remotely manage the server.

## 2. Set the Default Deny Policy

```bash
sudo ufw default deny incoming
sudo ufw default allow outgoing
```

The first command blocks incoming connections unless they are explicitly allowed by a firewall rule, while the second allows outgoing connections from the server.

## 3. Allow Port 8080

```bash
sudo ufw allow 8080/tcp
```

This command allows incoming TCP traffic on port 8080 so users can access the Nginx web application through the configured port.

## 4. Importance of Allowing SSH Before Enabling UFW

If I ran `sudo ufw enable` before `sudo ufw allow ssh`, the firewall could block incoming SSH connections and lock me out of the remote server, preventing me from managing it remotely until access is restored.
