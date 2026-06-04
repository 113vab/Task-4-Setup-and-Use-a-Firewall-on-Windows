# Task 4 – Setup and Use a Firewall on Windows
---

# Aim

The aim of this task was to understand the functionality of a firewall by creating, testing, and managing firewall rules using Windows Defender Firewall. The task focused on controlling network traffic, understanding ports and protocols, and learning how firewalls contribute to overall system security.

---

# Introduction

A firewall is a network security system that monitors and controls incoming and outgoing network traffic based on predefined security rules. It acts as a protective barrier between a trusted network and untrusted networks such as the Internet.

Firewalls play a critical role in cybersecurity by preventing unauthorized access, blocking malicious traffic, and protecting systems from various cyber threats. They are commonly used in personal computers, enterprise networks, servers, and cloud environments.

Windows Defender Firewall is Microsoft's built-in firewall solution that provides advanced traffic filtering and security management capabilities. It allows users to create custom rules to allow or block specific network connections based on ports, protocols, applications, and IP addresses.

---

# Objectives

The objectives of this task were:

* To understand the role of firewalls in network security.
* To learn the difference between inbound and outbound traffic.
* To understand ports and network protocols.
* To configure firewall rules using Windows Defender Firewall.
* To block network traffic on a specific port.
* To understand why Telnet is considered insecure.
* To gain practical experience with firewall management.

---

# What is a Firewall?

A firewall is a security mechanism that monitors and filters network traffic entering or leaving a device. It uses predefined security rules to determine whether traffic should be allowed or blocked.

Firewalls help in:

* Preventing unauthorized access.
* Blocking malicious network traffic.
* Protecting sensitive information.
* Monitoring communication between systems.
* Enforcing security policies.

Firewalls can be implemented as hardware devices or software applications.

Examples:

* Windows Defender Firewall
* Cisco ASA Firewall
* pfSense
* UFW (Linux Firewall)

---

# Understanding Inbound and Outbound Traffic

## Inbound Traffic

Inbound traffic refers to data entering a computer from an external source.

Examples:

* Remote Desktop connections
* File sharing requests
* Incoming network services

Firewall inbound rules determine which incoming connections are allowed or blocked.

---

## Outbound Traffic

Outbound traffic refers to data leaving a computer and traveling to external systems.

Examples:

* Web browsing
* Downloading files
* Sending emails

Outbound rules control what traffic can leave the system.

---

# Understanding Ports and Protocols

Network communication relies on ports and protocols.

## Ports

Ports are communication endpoints used by network services and applications.

Common ports include:

| Port | Service |
| ---- | ------- |
| 21   | FTP     |
| 22   | SSH     |
| 23   | Telnet  |
| 25   | SMTP    |
| 80   | HTTP    |
| 443  | HTTPS   |

---

## Protocols

Protocols define the rules used for communication between devices.

### TCP (Transmission Control Protocol)

TCP provides:

* Reliable communication
* Error checking
* Ordered delivery of data

### UDP (User Datagram Protocol)

UDP provides:

* Faster communication
* Lower overhead
* No delivery guarantee

---

# Why Telnet is Insecure

Telnet is a remote access protocol that operates on Port 23.

The major drawback of Telnet is that it transmits all information in plain text.

Security risks include:

* Usernames can be intercepted.
* Passwords can be intercepted.
* Session information can be captured.
* Attackers can monitor communication.

Because of these risks, SSH (Secure Shell) has replaced Telnet in most modern environments.

SSH uses encryption to protect communications and credentials.

---

# Procedure

## Step 1: Opening Windows Defender Firewall

The Windows Defender Firewall Management Console was opened using:

wf.msc

This launched Windows Defender Firewall with Advanced Security.

---

## Step 2: Reviewing Existing Rules

The Inbound Rules section was examined to view existing firewall rules.

This provided an understanding of how Windows controls incoming network traffic.

---

## Step 3: Creating a New Firewall Rule

A new inbound rule was created using the following configuration:

| Setting     | Value                   |
| ----------- | ----------------------- |
| Rule Type   | Port                    |
| Protocol    | TCP                     |
| Port Number | 23                      |
| Action      | Block Connection        |
| Profiles    | Domain, Private, Public |
| Rule Name   | Block Telnet Port 23    |

---

## Step 4: Applying the Rule

The rule was enabled and applied to all network profiles.

This ensured that Telnet traffic would be blocked regardless of the network environment.

---

## Step 5: Verifying the Rule

The newly created rule was verified in the Inbound Rules section.

The rule appeared successfully and was enabled.

---

## Step 6: Removing the Rule

After testing and verification, the rule was removed to restore the original firewall configuration.

---

# Observations

During the task, the following observations were made:

* Windows Firewall provides an easy-to-use graphical interface for managing security rules.
* Firewall rules can be created based on ports, applications, protocols, or IP addresses.
* Blocking a specific port immediately restricts associated traffic.
* Changes take effect instantly without requiring a system restart.
* Firewall configuration plays an important role in network security management.

---

# Results

A firewall rule was successfully created to block TCP Port 23 (Telnet).

The rule was verified and later removed as part of the task requirements.

The task demonstrated how firewall rules can be used to control network traffic and improve security.

---

# Security Benefits of Firewalls

Firewalls improve security by:

* Preventing unauthorized access.
* Blocking malicious network traffic.
* Reducing attack surfaces.
* Controlling application communications.
* Enforcing organizational security policies.
* Monitoring network activity.

---

# Learning Outcomes

After completing this task, I gained an understanding of:

* What a firewall is.
* The importance of firewalls in cybersecurity.
* The difference between inbound and outbound traffic.
* Ports and protocols used in networking.
* Why Telnet is considered insecure.
* How Windows Defender Firewall works.
* Basic firewall rule management.
* Network traffic filtering techniques.
* Practical implementation of security controls.

---

# Conclusion

This task provided practical experience in configuring and managing firewall rules using Windows Defender Firewall. By creating a rule to block Telnet traffic on Port 23, I learned how firewalls filter network traffic and help secure systems against unauthorized access. The exercise improved my understanding of network security fundamentals, firewall management, and the importance of secure communication protocols in modern computing environments.
