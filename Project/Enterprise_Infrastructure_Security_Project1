Cybersecurity
Securing Linux Servers Using SSH Honeypot Monitoring and IP Blocking

1. Introduction:

Most of the organizations frequently face unauthorized access attempts from against internal
Linux systems, particularly via the Secure Shell (SSH) service. These attacks often originate
from compromised internal hosts. This project focuses on designing and implementing a hostbased SSH honeypot to detect, log, and analyze malicious access attempts within a segmented
enterprise network.

2. Problem Statement:

Secure Defense, a cybersecurity services firm, is responsible for protecting internal Linux-based
systems deployed within segmented enterprise networks. These systems are frequently targeted
by unauthorized SSH access attempts originating from compromised hosts. Due to compliance
and infrastructure limitations, the organization cannot rely on cloud-based monitoring tools or
publicly exposed servers. The challenge is to:
 Detect unauthorized SSH access attempts
 Collect attacker behavior and metadata
 Reduce brute-force and block attacker IP address
3. Project Objective:

To design and implement a controlled security monitoring solution for Secure Defense against unauthorized SSH access attempts. The solution detects, analyzes, and mitigates SSH brute-force attacks on Linux systems by using honeypot-style monitoring, log analysis, SSH hardening techniques, and IP based access control mechanisms.

4. Scope of the Project

 Linux server  SSH service configuration and monitoring  Local logging and analysis  Host-based intrusion prevention

5. System Architecture:

The honeypot system consists of:  Create a SSH service to act as a honeypot.  Prepare a virtual directory to view the logs.  Expose the SSH port.  Capturing brute force attack attempts.  Logging Attackers IP address.  Blocking malicious IP address. All components operate locally without external dependencies.

6. Implementation Details:

6.1 SSH Honeypot Deployment
  A controlled SSH service was configured to log all authentication attempts. Invalid login
  attempts were intentionally allowed to capture attacker behavior without granting shell access.
6.2 SSH Hardening Measures
  Security configurations included:
   Disabling root login
   Limiting authentication retries
   Restricting allowed users
6.3 Logging and Monitoring
  Authentication attempts were logged to centralized log files stored in a secured /reports directory
  with restricted permissions.
6.4 IP-Based Blocking
  Repeated failed login attempts triggered automatic IP blocking to mitigate brute-force attacks
  while preserving honeypot data for analysis.
7. Testing and Results:
  Testing involved simulated brute-force attacks from internal test machines. Results showed:
   Successful logging of all SSH attempts
   Accurate identification of repeated attack sources
   Effective blocking after defined thresholds
   No disruption to legitimate system services
8. Steps to be followed to achieve the results:
  1. Create a SSH service to act as a honeypot.
  2. Prepare virtual directory to view the logs
  3. Expose the SSH port.
  4. Capture the brute force attack attempts.
  5. Log Attackers IP address.
  6. Block malicious IP address.
