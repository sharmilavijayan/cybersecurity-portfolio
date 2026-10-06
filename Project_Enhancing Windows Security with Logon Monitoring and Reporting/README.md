Cybersecurity_Enterprise-Infrastructure-Security_Project2
Enterprise-Infrastructure-Security_Windows based. Enhancing Windows Security with Logon Monitoring and Reporting

1. Introduction:

Cyber threats targeting Windows-based systems are particularly through unauthorized login
attempts and malicious command executions. This project focuses on enabling detailed audit
logging, analyzing security events using Event Viewer and PowerShell, and generating
automated HTML-based security reports. The goal is to proactively detect suspicious activities,
improve visibility into user behavior, and strengthen the organization’s overall security posture.
2. Problem Statement:

TechSecure, a mid-sized enterprise, faces increasing cyber threats targeting its Windows-based
systems, particularly through unauthorized login attempts and malicious command executions.
The challenge is to:
 Analyze failed logins to identify every intrusion.
 Document every executed command.
 Real time tracking of successful logons.
 Create Reports of failed login attempt.
3. Project Objective:

To enhance Windows security by implementing advanced audit configurations, including failed
login analysis, command logging, and real-time reporting. This project leverages Windows Audit
configuration, Group Policies, Event Viewer, PowerShell automation and HTML based reporting
to monitor, detect and mitigate potential security breaches.
4. Scope of the Project:

 Set up audit policy to do logon failure analysis.
 Configure command and process logging.
 PowerShell Logging Configuration
 Create a web-based reporting tool.
5. Implementation Details:

5.1. Advanced Audit Policy Configuration
  Audit policies are configured using Microsoft Management Console (MMC) and Local
  Group Policy. Both successful and failed events are enabled to ensure complete visibility
  into authentication attempts, system access, and process execution.
  Local Computer Policy → Computer Configuration → Windows Settings → Security
  Settings → Advanced Audit Policy Configuration
  The following audit categories were configured for both Success and Failure events:
   Account Logon
  o Audit Credential Validation
  o Audit Other Account Logon Events
   Logon/Logoff
  o Audit Logon
  o Audit Logoff
  o Audit Special Logon
  o Audit Other Logon/Logoff Events
   Detailed Tracking
  o Audit Process Creation
  o Audit Process Termination
   Object Access
  o Audit File System
  o Audit Registry
   Privilege Use
  o Audit Sensitive Privilege Use
  o Audit Non-Sensitive Privilege Use
   System
  o Audit System Integrity
  o Audit Other System Events
  Global Object Access Auditing was configured for both File System and Registry,
  applying auditing rules to the Everyone group.
5.2 PowerShell Logging Configuration
  To ensure visibility into command execution and script activity, PowerShell logging was
  enabled via Group Policy:
   Turn on Script Execution → Enabled (Allow all scripts)
   Turn on Module Logging → Enabled (* to log all modules)
  This ensures that all PowerShell activity is logged and can be analyzed for malicious
  behavior.
5.3. Event Generation and Validation
  To validate the audit configuration, a new local user account named Bob was created. The
  following actions were performed:
   Execute the following commands as Bob:
   ping www.example.com
   Launching applications (e.g., MSPaint)
   Exit from user Bob.
  These actions generated security events in Event Viewer, including:
   Logon events (Event ID 4624)
   Process creation and termination events (Event ID 4688.4489)
  Event Viewer filters were used to verify the presence of Event IDs such as 4688 and
  4689, confirming that auditing was functioning correctly.
  5.4 Security Event Analysis Using PowerShell
  PowerShell scripts were used to extract and analyze specific security events from the
  Windows Security log.
  Event ID 4624 : Successful logon
  Event ID 4625 Failed logon attempt
  Event ID 4688 Process creation
  Event ID 4689
  Process termination
  A custom PowerShell script was developed to:
   Monitor recent security events
   Identify successful and failed login attempts
   Extract usernames and source IP addresses from failed logins
   Track executed processes and commands
  This automation significantly reduces manual log analysis effort and enables faster detection of
  suspicious activity.
 5.5 Automated HTML Security Report Generation
    1. IIS Web Server Deployment
      Internet Information Services (IIS) was installed to host security reports. The PowerShell script
      periodically collects security events and converts them into a structured HTML report stored in:
      C:\inetpub\wwwroot\security_report.html
    2. Real-Time Monitoring
      The script runs continuously and updates the report every five minutes, providing near real-time
      security visibility. The report includes:
       Successful login activity
       Failed login attempts with source IP addresses
       Process creation and command execution events
      The report is accessible via a web browser using:
       http://localhost/security_report.html
       http://localhost:8080/security_report.html (via port proxy configuration)
      Firewall rules and port forwarding were configured to allow secure access to the report.
5.6. Test Implementation and Results
    The implemented solution provides TechSecure with:
     Improved detection of unauthorized login attempts
     Visibility into suspicious IP addresses
     Comprehensive logging of commands and processes
     Automated, centralized security reporting
     Reduced response time to potential security incidents
    This proactive monitoring approach helps prevent unnoticed intrusions and supports forensic
    investigations when incidents occur.
