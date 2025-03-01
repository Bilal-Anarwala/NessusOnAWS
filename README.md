# Vulnerable EC2 Instance Project

This project involves setting up a vulnerable EC2 instance on AWS, identifying security vulnerabilities using Nessus, and remediating them to achieve a clean scan. The goal is to understand common security misconfigurations, learn how to identify vulnerabilities, and apply best practices to secure a system.

## Project Overview

1. **Launched an EC2 Instance**: Created a Windows-based EC2 instance on AWS.
2. **Introduced Vulnerabilities**:
   - Installed outdated versions of software (e.g., Google Chrome, Zoom).
   - Disabled the Windows Firewall.
3. **Performed a Vulnerability Scan**: Used Nessus to scan the instance and identify security issues.
4. **Remediated Vulnerabilities**: Applied fixes to address the identified vulnerabilities.
5. **Re-scanned the Instance**: Ran Nessus again to confirm that the vulnerabilities were resolved.

## Features

- **Vulnerability Identification**: Used Nessus to detect security weaknesses in the EC2 instance.
- **Remediation**: Applied patches, updated software, and re-enabled security features to fix vulnerabilities.
- **Validation**: Re-ran the Nessus scan to ensure the system was secure.

## Steps to Reproduce

### 1. Launch an EC2 Instance
- Log in to the AWS Management Console.
- Navigate to EC2 and launch a Windows-based instance.
- Ensure the instance is publicly accessible for testing purposes.

### 2. Introduce Vulnerabilities
- Connect to the instance via RDP.
- Download and install outdated versions of software (e.g., Google Chrome, Zoom).
- Disable the Windows Firewall:
  - Open `Control Panel` > `System and Security` > `Windows Defender Firewall`.
  - Turn off the firewall for both private and public networks.

### 3. Perform a Nessus Scan
- Install Nessus on a separate machine or use a cloud-based Nessus solution.
- Configure Nessus to scan the EC2 instance's public IP address.
- Run the scan and review the results to identify vulnerabilities.

### 4. Remediate Vulnerabilities
- Update all outdated software to the latest versions.
- Re-enable the Windows Firewall:
  - Open `Control Panel` > `System and Security` > `Windows Defender Firewall`.
  - Turn on the firewall for both private and public networks.
- Apply any additional security patches or configurations as recommended by the Nessus scan.

### 5. Re-run the Nessus Scan
- Perform another scan using Nessus to verify that the vulnerabilities have been resolved.
- Ensure the scan results show no critical or high-severity issues.

## Learning Outcomes

This project demonstrates my ability to:
- Set up and configure an EC2 instance on AWS.
- Intentionally introduce vulnerabilities to simulate real-world scenarios.
- Use Nessus to identify and assess security vulnerabilities.
- Apply remediation techniques to secure a system.
- Validate the effectiveness of remediation efforts through re-scanning.

## Tools Used

- **AWS EC2**: For hosting the vulnerable instance.
- **Nessus**: For vulnerability scanning and assessment.
- **Windows Firewall**: For testing security configurations.
- **Outdated Software**: To simulate common security risks.

## Example Commands

### Disable Windows Firewall (PowerShell or via SSM)
```powershell
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled False
```

### Enable Windows Firewall (PowerShell or via SSM)

```powershell
Set-NetFirewallProfile -Profile Domain,Public,Private -Enabled True
```
## Update Software
- Manually download and install the latest versions of software like Google Chrome and Zoom from their official websites.

### Conclusion

This project highlights the importance of maintaining up-to-date software and enabling security features like firewalls to protect systems from vulnerabilities. By intentionally creating a vulnerable environment and then securing it, I gained hands-on experience in vulnerability management and remediation.


