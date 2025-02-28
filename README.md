# Born2beRoot

## 🖥️ Project Overview

Born2beRoot is a system administration project focused on creating a secure virtual machine according to specific requirements. This project demonstrates my skills in setting up and hardening a Linux system, implementing security policies, and managing system resources.

Unlike most coding projects, Born2beRoot emphasizes practical system administration skills that are essential for maintaining secure and efficient server environments.

## 🔒 Implementation Details

### Base System
- **OS**: Debian
- **Partitioning**: Custom LVM partitioning scheme with encrypted volumes
- **SSH**: Secure configuration on a non-default port
- **Firewall**: UFW (Uncomplicated Firewall) with minimal necessary rules

### Security Features
- **Password Policy**: Strong password implementation using PAM
  - Password expiration rules
  - Complexity requirements
  - History management
- **User Management**:
  - Configured user groups and permissions
  - Implemented sudo with strict usage rules
  - Log tracking for all sudo commands

### Monitoring
- Custom bash monitoring script that displays:
  - System architecture and kernel information
  - CPU and RAM usage
  - Disk space utilization
  - Network status
  - User sessions
  - LVM status

## 🛠️ Technical Skills Demonstrated

- **Virtual Machine Setup**: Creating and configuring a VM from scratch
- **Disk Management**: Working with LVM for flexible storage allocation
- **System Hardening**: Implementing security best practices
- **Service Configuration**: Setting up and securing essential services
- **User Administration**: Creating and managing users and groups
- **Shell Scripting**: Creating a monitoring script to display system information
- **Cron Jobs**: Scheduling tasks to run automatically
- **System Monitoring**: Tracking system performance and security events

## 📊 Key Configurations

### Partitioning Scheme
```
Encrypted LVM Structure:
├── sda1 (boot)
└── sda2 (encrypted container)
    └── LVM Volume Group
        ├── root
        ├── swap
        ├── home
        ├── var
        ├── srv
        ├── tmp
        └── var-log
```

### UFW Rules
```
Status: active
Logging: on
Default: deny (incoming), allow (outgoing)
New profiles: skip

To                         Action      From
--                         ------      ----
SSH Port                   ALLOW       Anywhere
```

### Password Policy
```
Password Requirements:
- Minimum 10 characters
- Contains uppercase, lowercase, and numbers
- No more than 3 consecutive identical characters
- Cannot include username
- Expires every 30 days
- Minimum 2 days between changes
- Warning 7 days before expiration
- Different from last 7 passwords
```

## 🧠 Learning Outcomes

Through this project, I gained practical knowledge in:

- **Linux System Administration**: Understanding how Linux systems are structured and managed
- **Security Implementation**: Applying security principles to create a hardened system
- **Service Management**: Configuring and maintaining essential system services
- **Performance Monitoring**: Tracking system resources and user activities
- **Disaster Recovery**: Setting up systems to ensure data integrity and recovery options

## 📝 Evaluation Preparation

This repository contains documentation for the project evaluation, including:

- **Defense Questions**: Common questions and answers for project defense
- **Commands Cheatsheet**: Essential commands for demonstrating system configuration
- **Screenshots**: Visual documentation of key setup components

## ⚠️ Note

As this project involves a virtual machine setup rather than code, the main deliverable was the configured VM itself, not source files. This repository primarily serves as documentation of the implementation and knowledge gained.

For detailed project requirements, see the [born2beRoot.md](born2beRoot.md) file.

---

*This project is part of the 42 School Common Core curriculum.*