# Task 4: Setup and Use a Firewall using UFW (Linux)

##  Objective
Configure basic firewall rules using UFW on Linux to block or allow specific network traffic.

---

##  Steps Performed

### Step 1: Install UFW and Enable It
bash
sudo apt update
sudo apt install ufw -y
sudo ufw enable

🔹 Screenshot: 1.png (Installed and enabled UFW)
### Step 2: Check Current Firewall Rules

sudo ufw status numbered

🔹 Screenshot: 2.png (Checked current rules)
### Step 3: Block Port 23 (Telnet)

sudo ufw deny 23/tcp

🔹 Screenshot: 3.png (Blocked port 23)
### Step 4: Allow Port 22 (SSH)

sudo ufw allow 22/tcp

🔹 Screenshot: 4.png (Allowed port 22)
### Step 5: Test Port 23 Block Using Telnet

telnet localhost 23

🔹 Screenshot: 5.png (Connection failed as expected)
### Step 6: Delete the Telnet Block Rule

sudo ufw delete deny 23/tcp

🔹 Screenshot: 6.png (Rule deleted successfully)

🧾 Files Included

    1.png – UFW Installation

    2.png – UFW Status

    3.png – Block Telnet

    4.png – Allow SSH

    5.png – Telnet Test

    6.png – Rule Deleted

    README.md – This file explaining all steps

## Summary

This task demonstrated how to:

    * Use UFW for firewall management in Linux
    * Block insecure ports (Telnet)
    * Allow secure ports (SSH)
    * Test and validate the rules
    * Safely remove the test rule

Firewall rules are essential to manage and secure network access. This exercise gave hands-on experience in doing that with UFW.
