# Task 4 – Setup and Use a Firewall on Windows

## Objective

The objective of this task is to understand the role of a firewall in protecting computer systems and networks by configuring and managing firewall rules in Windows.

---

## What is a Firewall?

A firewall is a security mechanism that monitors and controls incoming and outgoing network traffic based on predefined security rules. It acts as a barrier between a trusted internal network and untrusted external networks such as the Internet.

Firewalls help:

* Prevent unauthorized access.
* Block malicious traffic.
* Protect sensitive information.
* Monitor network communications.

---

## Tools Used

* Windows Defender Firewall with Advanced Security
* Windows Operating System

---

## Procedure

### Step 1: Open Windows Firewall

1. Press **Windows + R**.
2. Type `wf.msc`.
3. Press Enter.

### Step 2: Review Existing Rules

1. Navigate to **Inbound Rules**.
2. Observe the existing firewall rules.

### Step 3: Create a New Rule

1. Click **New Rule**.
2. Select **Port**.
3. Choose **TCP**.
4. Enter port number **23**.
5. Select **Block the Connection**.
6. Apply the rule to all profiles.
7. Name the rule **Block Telnet Port 23**.

### Step 4: Verify the Rule

1. Locate the newly created rule in the Inbound Rules section.
2. Confirm that the rule is active.

### Step 5: Remove the Rule

1. Select the created rule.
2. Delete it to restore the default configuration.

---

## Understanding Key Concepts

### Inbound Traffic

Inbound traffic refers to network connections entering a device from external sources.

Example:

* A remote user attempting to connect to your computer.

### Outbound Traffic

Outbound traffic refers to network connections initiated from your device to external destinations.

Example:

* Accessing a website using a web browser.

### Ports and Protocols

#### Port

A port is a logical communication endpoint used by applications and services.

Examples:

* Port 80 – HTTP
* Port 443 – HTTPS
* Port 23 – Telnet
* Port 22 – SSH

#### Protocol

A protocol is a set of rules that governs communication between devices.

Examples:

* TCP (Transmission Control Protocol)
* UDP (User Datagram Protocol)

---

## Why Telnet is Insecure

Telnet uses Port 23 and transmits data in plain text.

Security issues:

* Usernames are transmitted without encryption.
* Passwords are transmitted without encryption.
* Attackers can intercept sensitive information.

Modern systems use SSH (Secure Shell) instead of Telnet because SSH encrypts communications.

---

## How Windows Firewall Works

Windows Defender Firewall filters network traffic according to configured rules.

The firewall can:

* Allow specific traffic.
* Block specific traffic.
* Restrict applications.
* Control access based on ports and protocols.

Rules can be configured separately for:

* Inbound traffic
* Outbound traffic

---

## Key Learnings

Through this task, I learned:

* What a firewall is and why it is important.
* The difference between inbound and outbound traffic.
* The role of ports and protocols in network communication.
* Why Telnet is considered insecure.
* How Windows Defender Firewall operates.
* How firewall rules help enforce network security controls.

---

## Outcome

Successfully configured a firewall rule to block Telnet traffic on Port 23, verified the rule, and removed it after testing. This activity demonstrated the practical use of firewall-based access control and basic network security management.
