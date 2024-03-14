Document Title: Overview of DekkoSecure and Whitelist Request for DekkoSecure Meetings

Date: [Insert Date]

Prepared by: [Your Name]

Introduction
This document provides an overview of DekkoSecure, a secure communication and collaboration platform, and outlines the privacy and security controls in place to protect user data. Additionally, this document presents a request for whitelisting specific URLs and network configurations necessary for the functionality of DekkoSecure Meetings within our organization.

Overview of DekkoSecure
DekkoSecure is a secure communication and collaboration platform designed to provide users with a high level of privacy and security. The platform offers various features, including secure messaging, file sharing, and video conferencing, making it suitable for organizations that require confidential communication.

Privacy and Security Controls
DekkoSecure implements several privacy and security controls to protect user data and ensure the confidentiality of communications:

End-to-End Encryption: All communications and data shared on the platform are encrypted end-to-end using industry-standard encryption protocols, such as AES-256 and TLS 1.2, ensuring that only the intended recipients can access the information.
Data Sovereignty: DekkoSecure adheres to data sovereignty principles, ensuring that data is stored and processed within the legal jurisdiction of the user's choice. This helps organizations comply with local data protection regulations and maintain control over their data.
Compliance: The platform complies with various data protection and privacy regulations, including GDPR, HIPAA, and SOC 2. DekkoSecure undergoes regular audits to maintain these certifications and ensure ongoing compliance.
Access Controls: DekkoSecure provides robust access controls, allowing administrators to manage user access and permissions effectively. This includes features like role-based access control, two-factor authentication, and single sign-on integration.
Regular Security Audits: The platform undergoes regular security audits conducted by independent third-party firms to identify and address potential vulnerabilities. DekkoSecure also has a bug bounty program to encourage responsible disclosure of security issues.
Whitelist Request for DekkoSecure Meetings
To ensure the smooth functioning of DekkoSecure Meetings within our organization, the following network configurations and browser policies are requested to be whitelisted:

Network/Firewall/VPN Configuration:

Whitelist all subdomains of DekkoSecure (*.dekko.io).
Open TCP port 443 (HTTPS) and allow UDP ports 10000-20000 (SRTP) for *.dekko.io.
Browser Policies:

Allow cookies from au.dekko.io.
Allow cookies from au-api-core.dekko.io.
Risks and Considerations:

Whitelisting the specified URLs and opening the required ports may potentially introduce security risks if not properly managed. It is crucial to ensure that the whitelisted domains are legitimate and trusted.
Opening UDP ports 10000-20000 for SRTP traffic should be carefully evaluated to ensure it does not conflict with other applications or services running on the network.
Regularly monitor and review the whitelisted URLs and opened ports to ensure they remain necessary and do not introduce any vulnerabilities.
Statement
As part of the Governance, Risk, and Compliance (GRC) team, this document provides an overview of the privacy and security controls of DekkoSecure and outlines the necessary configurations for DekkoSecure Meetings. It is important to note that this document does not constitute a decision to whitelist the requested URLs and configurations. The final decision will be made by the appropriate decision-making body within our organization, taking into account the security and operational requirements.

Next Steps:

Review and validate the information provided in this document with relevant stakeholders, including IT security, legal, and compliance teams.
Conduct a thorough risk assessment to evaluate the potential impact of whitelisting the specified URLs and opening the required ports.
Obtain necessary approvals from the appropriate decision-making body within the organization.
Implement the approved whitelisting configurations and establish monitoring and auditing mechanisms to detect and respond to any suspicious activities or security incidents.
Provide training and guidance to users on the secure usage of DekkoSecure Meetings and the importance of protecting sensitive information.
Conclusion
In conclusion, DekkoSecure offers a secure platform for communication and collaboration, with robust privacy and security controls in place. The whitelisting of specific URLs and network configurations is necessary for the optimal functionality of DekkoSecure Meetings within our organization. This document serves as an overview and recommendation, highlighting the key considerations and next steps. The final decision will be made in accordance with our organization's security policies and procedures, prioritizing the protection of sensitive data and maintaining a secure environment.

[Your Name]
[Your Position]
[Your Department]
