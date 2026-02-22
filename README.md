# Task 4 – Configuring a Firewall (Linux)

## Objective
The objective of this task is to install, configure, and verify a Linux firewall using UFW (Uncomplicated Firewall). This task demonstrates basic firewall configuration techniques such as allowing and denying ports, setting default policies, and controlling incoming and outgoing network traffic.

---

## Tool Used
- UFW (Uncomplicated Firewall)
- Operating System: Linux
- Package Manager: apt

---

## Step 1: Install UFW
UFW is installed using the apt package manager.

Command:
sudo apt update
sudo apt install ufw

---

## Step 2: Verify Installation
To check whether UFW is installed correctly, the following command is used:

Command:
ufw

This displays the available UFW commands, confirming successful installation.

---

## Step 3: Firewall Configuration

### Set Default Policies
The default firewall rules are configured as follows:

Command:
sudo ufw default deny incoming
sudo ufw default allow outgoing

- Incoming traffic is denied by default.
- Outgoing traffic is allowed by default.

---

### Allow Specific Ports and Services

Allow SSH service:
sudo ufw allow ssh

Allow HTTP service:
sudo ufw allow http

Allow HTTPS service:
sudo ufw allow https

Allow a specific TCP port (example: port 22):
sudo ufw allow 22/tcp

---

### Deny Specific Ports
Specific ports can be blocked using:

Command:
sudo ufw deny <port_number>

---

## Step 4: Enable Firewall and Check Status

Enable the firewall:
sudo ufw enable

Check firewall status:
sudo ufw status

---

## Result
The firewall is successfully enabled and configured. Only the allowed ports accept incoming connections, while all other ports remain blocked. Outgoing connections are permitted. This ensures better system security and prevents unauthorized access or port scanning attacks.

---

## Conclusion
UFW provides a simple and effective way to manage firewall rules on Linux systems. By configuring default policies and allowing only required services, the system is protected from unnecessary network threats.

---# Task-4-Setup-and-Use-a-Firewall-on-Windows-Linux
