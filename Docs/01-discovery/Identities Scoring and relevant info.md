## Cloud Identity Federates with On-premises Identity Systems

### Connect all of your users to Microsoft Entra ID and federate with on-premises identity systems

**Has the organization integrated Microsoft Entra ID with existing on-premises identity systems to ensure seamless user access across environments?**

**Current Maturity Level:**
- **Advanced:** Cloud identity is federated with on-premises Active Directory using Microsoft Entra Connect password hash synchronization. This approach synchronizes user password hashes from the on-premises Active Directory to the cloud, allowing for rapid authentication without direct access to the on-premises AD at the time of sign-in.
    - Indicators:
        - Deployment of password hash synchronization for federating cloud identities with on-premises AD.
        - Users benefit from seamless access to cloud services with their on-premises credentials, enhancing the authentication process's efficiency.
        - Strengthened security through rapid cloud authentication, leveraging synchronized password hashes.

**Recommended Maturity Level:**
- **Optimal:** Cloud identity is fully integrated with on-premises Active Directory through Microsoft Entra Connect, utilizing both password hash synchronization and seamless SSO with Conditional Access policies. This optimal setup leverages the best aspects of both advanced authentication mechanisms and introduces dynamic access controls based on user behavior, location, device health, and other risk factors.
    - Indicators:
        - Comprehensive integration of cloud and on-premises identities, utilizing the full suite of Microsoft Entra Connect capabilities.
        - Deployment of Conditional Access policies that dynamically adapt authentication requirements, significantly enhancing security.
        - Superior user experience through seamless SSO across environments, bolstered by robust and adaptive security measures.

- **Relevance to NIST SP 800-53 Revision 5:**
    - AC-2 Account Management: The federation and integration of cloud and on-premises identities support the principles of account management by ensuring that user accounts are managed consistently across environments.
    - IA-2 Identification and Authentication (Organizational Users): Utilizing Microsoft Entra Connect for seamless identity integration ensures that organizational users are uniquely identified and authenticated, providing secure and efficient access to networked systems.
    - AC-17 Remote Access: The implementation of seamless SSO and Conditional Access policies enhances secure remote access controls, ensuring that remote connections to the organization’s networks enforce security policies and employ encryption for communications.
    - AC-14 Permitted Actions Without Identification or Authentication: While typically requiring strict controls, the optimal integration scenario, with advanced SSO and Conditional Access, ensures that any exceptions to identification or authentication requirements are securely managed and based on dynamic assessments of risk.

- **Products covered:**
    - Microsoft Entra ID

**Is the organization utilizing Microsoft Entra ID to protect against security threats like brute force, DDoS, and password spray attacks through specific authentication options?**

**Current Maturity Level:**
- **Initial:** Initial efforts have been made to implement Microsoft Entra ID's authentication features, such as multi-factor authentication (MFA), to protect against specific threats. While this phase marks the beginning of improving security defenses, comprehensive adoption of all available authentication options to counter various threats may still be under development.
    - Indicators:
      - Partial deployment of Microsoft Entra ID authentication features, focusing on key systems or user groups.
      - Initial improvements in security against attacks like brute force and password spray, though not uniformly applied across the organization.
      - Some enhancement in the organization’s ability to secure access and user identities, with ongoing efforts to leverage full capabilities of Microsoft Entra ID.

**Recommended Maturity Level:**
- **Optimal:** The utilization of Microsoft Entra ID for advanced authentication and threat protection is fully developed, operationalized, and integrated into the organization's identity and access management strategy. This optimal scenario ensures the highest level of security against brute force, DDoS, and password spray attacks, leveraging the full suite of authentication options provided by Microsoft Entra ID.
    - Indicators:
        - Strategic and universal application of Microsoft Entra ID’s authentication features to protect against common and sophisticated attacks.
        - Comprehensive management of identity and access security, enhancing organizational resilience against cyber threats.
        - Full alignment with security best practices and compliance requirements, supported by an effective and adaptive authentication security framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - IA-2 Identification and Authentication (Organizational Users): Leveraging advanced authentication options supports the unique identification and authentication of users, enhancing security controls to protect against unauthorized access.
    - SC-8 Transmission Confidentiality and Integrity: Implementing strong authentication methods contributes to the protection of information during transmission, safeguarding against interception and unauthorized disclosure.
    - AC-7 Unsuccessful Login Attempts: Features that protect against brute force and password spray attacks help to monitor and limit unsuccessful login attempts, deterring unauthorized access attempts.
    - A-4 Identifier Management: Utilizing Microsoft Entra ID aids in managing identifiers by ensuring they are properly issued, maintained, and retired, supporting secure authentication practices.

- **Products covered:**
    - Microsoft Entra ID

**Has the organization identified and excluded unnecessary on-premises identities, such as service accounts or privileged roles, from cloud federation?**

**Current Maturity Level:**
- **Initial:** Some effort is made to identify unnecessary on-premises identities for exclusion from cloud federation, but the approach is manual and lacks comprehensive coverage. Basic guidelines exist for determining which identities to federate, but these are not applied consistently or thoroughly.
    - Indicators:
        - Partial assessment and management of on-premises identities for federation, focusing on easily identifiable unnecessary accounts or roles.
        - Initial steps toward reducing the number of unnecessary federated identities, though a systematic approach may not yet be fully implemented.
        - Some improvement in security and access management for federated environments, with ongoing efforts to refine identity federation practices.

**Recommended Maturity Level:**
- **Optimal:** Comprehensive and dynamic management of on-premises identities ensures that only necessary identities are federated to the cloud. Advanced automation and intelligence tools are employed to continuously evaluate and adjust which on-premises identities are federated, based on real-time analysis of role necessity, security posture, and usage patterns. Unnecessary service accounts and privileged roles are proactively identified and excluded, ensuring optimal security and efficiency.
    - Indicators:
        - Strategic and universal application of best practices for identity federation, ensuring only necessary on-premises identities are included.
        - Comprehensive and proactive management of federated identity risks, enhancing organizational resilience and compliance.
        - Full alignment with identity management best practices and regulatory requirements, supported by an effective and well-managed federation process.

- **Relevance to NIST SP 800-53 Revision 5:**
    - AC-2 Account Management: The review and exclusion of unnecessary on-premises identities from cloud federation supports the principle of least privilege, ensuring accounts are managed according to their necessity for business functions.
    - A-2 Identification and Authentication (Organizational Users): Ensuring that only necessary identities are federated enhances the identification and authentication controls by reducing the potential for unauthorized access.
    - AC-6 Least Privilege: Carefully managing which on-premises identities are federated to cloud services enforces the least privilege principle, minimizing unnecessary access rights and reducing security risks.
    - CM-2 Baseline Configuration: The process of identifying and excluding unnecessary federated identities contributes to maintaining a secure baseline configuration, ensuring that only approved identities have access within the federated environment.

- **Products covered:**
    - Microsoft Entra ID

### Establish your Identity Foundation with Microsoft Entra ID:

**Has the organization ensured that all access requests pass through Microsoft Entra ID to leverage its policy decision points for enforcing access policies?**

**Current Maturity Level:**
- **Advanced:** The majority of access requests are configured to go through Microsoft Entra ID, leveraging its policy decision point capabilities for robust access enforcement. Advanced policies are applied more broadly, though some legacy systems or applications may not yet be fully integrated.
    - Indicators:
        - Comprehensive routing of all access requests through Microsoft Entra ID, facilitating centralized and consistent policy enforcement.
        - Enhanced security measures in place, supported by the systematic application of access controls and policies.
        - Significant progress toward minimizing access management complexities and security risks, bolstered by the centralized management of access requests.

**Recommended Maturity Level:**
- **Optimal:** Every access request is meticulously configured to pass through Microsoft Entra ID, fully utilizing its comprehensive policy decision point capabilities for access enforcement across the entire organization. This setup ensures that all access is governed by dynamic, context-aware policies that adapt to evolving security landscapes and organizational needs.
    - Indicators:
        - Strategic and universal application of Microsoft Entra ID for policy decision-making across all user access scenarios and environments.
        - Comprehensive management of access policies, enhancing organizational agility, security resilience, and compliance with access control best practices.
        - Full alignment with identity and access management best practices and compliance requirements, supported by an effective and well-managed access control framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - AC-2 Account Management: Utilizing Microsoft Entra ID as the central point for access decisions supports the management of user accounts, ensuring that access is granted based on defined policies and principles of least privilege.
    - AC-3 Access Enforcement: The enforcement of access decisions through Microsoft Entra ID aids in controlling access to organizational resources based on approved authorizations, supporting the access enforcement control.
    - AC-25 Access Control Policies and Procedures: Leveraging Microsoft Entra ID for policy decision points aligns with the establishment and maintenance of access control policies and procedures, ensuring that access to resources is managed and enforced in a consistent manner.
    - AC-1 Access Control Policy and Procedures: Centralizing access requests through Microsoft Entra ID supports the organization’s access control policies by ensuring that access to systems and applications is governed by comprehensive procedures.

- **Products covered:**
    - Microsoft Entra ID

### Integrate all your applications with Microsoft Entra ID:

**Has the organization integrated both modern and legacy applications with Microsoft Entra ID for single sign-on and consistent identity and access management?**

**Current Maturity Level:**
- Initial: Modern applications are partially integrated with Microsoft Entra ID for SSO, but legacy applications remain disconnected, leading to a split in the user experience and access management. Efforts to unify identity management are underway, but not all applications are covered.
    - Indicators:
        - Partial deployment of SSO and identity management through Microsoft Entra ID, focusing on a subset of modern applications.
        - Initial improvements in user access management and security for integrated applications, though legacy systems may remain isolated.
        - Some enhancement in the organization's approach to identity and access management, with ongoing efforts to extend Microsoft Entra ID integration.

**Recommended Maturity Level:**
- Optimal: Every application, both modern and legacy, is fully integrated with Microsoft Entra ID for seamless SSO and consistent identity and access management across the entire application portfolio. Advanced solutions, including custom integration for the most challenging legacy applications, ensure a unified and secure user experience.
    - Indicators:
        - Strategic and universal application of Microsoft Entra ID for identity and access management across the entire application landscape.
        - Comprehensive and proactive management of access security, enhancing organizational agility, security resilience, and compliance.
        - Full alignment with identity and access management best practices and compliance requirements, supported by an effective and well-managed unified access control framework.

- **Relevance to NIST SP 800-53 Revision 5:**
        - AC-2 Account Management: Utilizing Microsoft Entra ID supports the management of user accounts, ensuring that access is granted based on the principles of least privilege and need-to-know.
        - AC-14 Permitted Actions Without Identification or Authentication: The comprehensive integration of applications with Microsoft Entra ID for SSO helps minimize instances where actions can be performed without proper identification or authentication, enhancing security.
        - IA-2 Identification and Authentication (Organizational Users): Ensuring consistent identity management across all applications via Microsoft Entra ID supports the unique identification and authentication of users, enhancing security controls.
        - IA-8 Identification and Authentication (Non-Organizational Users): For applications accessed by non-organizational users, integration with Microsoft Entra ID can provide robust mechanisms for identifying and authenticating these users according to established policies.

- **Products covered:**
    - Microsoft Entra ID

**Has the organization integrated all identity and access management functions into Microsoft Entra ID to ensure a seamless and secure user experience across the entire application portfolio, with advanced security measures applied consistently?**

**Current Maturity Level:**
- Initial: Initial efforts to consolidate IAM engines have begun, focusing on integrating some systems with Microsoft Entra ID. While some applications now benefit from unified access management, others remain outside this integrated environment, resulting in a partial enhancement of security and user experience.
    - Indicators:
        - Partial deployment of Microsoft Entra ID for identity and access management, focusing on high-priority applications or systems.
        - Initial improvements in user access management and security for integrated applications, though not uniformly applied across the entire portfolio.
        - Some enhancement in the organization’s identity management strategy, with ongoing efforts to extend Microsoft Entra ID integration across all functions.

**Recommended Maturity Level:**
- Optimal: A fully consolidated IAM environment has been achieved, with all identity and access management functions integrated into Microsoft Entra ID. This ensures a seamless and secure user experience across the entire application portfolio, with advanced security measures applied consistently.
    - Indicators:
        - Strategic and universal application of Microsoft Entra ID for comprehensive identity and access management across the organization.
        - Comprehensive management of user identities and access, enhancing organizational agility, security resilience, and compliance.
        - Full alignment with identity management best practices and regulatory requirements, supported by an effective and well-managed identity management framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - AC-2 Account Management: Centralizing identity and access management with Microsoft Entra ID supports the management of user accounts according to the least privilege principle and the need-to-know basis, enhancing control over user access.
    - IA-2 Identification and Authentication (Organizational Users): Consolidating identification and authentication functions within Microsoft Entra ID ensures that users are uniquely identified and authenticated across all systems, supporting robust security controls.
    - AC-3 Access Enforcement: Integration with Microsoft Entra ID facilitates the enforcement of approved authorizations for accessing systems and applications, aligning with access control policies.
    - IA-8 Identification and Authentication (Non-Organizational Users): For applications accessed by non-organizational users, Microsoft Entra ID can provide comprehensive mechanisms for identification and authentication in line with established policies.

- **Products covered:**
    - Microsoft Entra ID

### Verify explicitly with strong authentication:

**Has the organization fully deployed and enforced Microsoft Entra multifactor authentication (MFA) across the entire organization without exception?**

**Current Maturity Level:**
- **Advanced:** Microsoft Entra MFA is broadly implemented across the organization, significantly improving security by requiring multiple forms of verification. This advanced tier reflects a mature approach to authentication, ensuring that MFA is applied consistently across all systems and users.
    - Indicators:
        - Comprehensive adoption of MFA for enhanced security across various access points and applications.
        - Enhanced protection against unauthorized access, supported by the systematic application of MFA.
        - Significant progress toward minimizing potential security breaches, bolstered by the widespread enforcement of MFA.

**Recommended Maturity Level:**
- **Optimal:** The deployment and enforcement of Microsoft Entra MFA across the entire organization are fully developed, operationalized, and integrated into the organization’s overall security strategy. This optimal scenario ensures the highest level of authentication security, with MFA required for access to all systems and data without exception.
    - Indicators:
        - Universal application of MFA, ensuring that no exceptions are made in its enforcement.
        - Comprehensive management of authentication practices, enhancing the organization's resilience against various cyber threats.
        - Full alignment with authentication security best practices and compliance requirements, supported by an effective and well-managed MFA framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - IA-2 Identification and Authentication (Organizational Users): The implementation of MFA supports the requirements for unique identification and authentication of users, enhancing security controls against unauthorized access.
    - IA-5 Authenticator Management: Enforcing MFA involves managing the lifecycle of multiple authenticators, aligning with the control's requirements for effective authenticator management practices.
    - AC-7 Unsuccessful Login Attempts: MFA can deter unauthorized access attempts by increasing the complexity of successful authentication, contributing to the control's objective of limiting unsuccessful login attempts.
    - IA-11 Re-authentication: Requiring MFA at re-authentication events ensures that the security of the authentication session is maintained, aligning with the control's emphasis on re-establishing authentication assurances periodically.

- **Products covered:**
    - Microsoft Entra ID

**Has the organization blocked all legacy authentication methods, fully embraced modern authentication protocols without exceptions, and enforced strict access policies that require secure authentication mechanisms to eliminate the risks associated with legacy methods?**

- **Initial:** Initial steps have been taken to identify and limit the use of legacy authentication methods, with partial adoption of modern authentication protocols for certain applications or user groups. While this phase marks the beginning of transitioning to more secure authentication practices, comprehensive enforcement and elimination of all legacy methods may still be under development.
    - Indicators:
        - Partial restriction of legacy authentication methods and gradual adoption of modern protocols like OAuth 2.0 and OpenID Connect.
        - Initial improvements in authentication security, though legacy methods may still be permitted in certain scenarios.
        - Some enhancement in the organization's ability to protect against authentication-related risks, with ongoing efforts to fully transition to modern authentication.

- **Optimal:** The deployment of modern authentication protocols is fully developed, operationalized, and integrated into the organization’s overall access control strategy, with a complete blockade of all legacy authentication methods. This optimal scenario ensures the highest level of security, eliminating risks associated with outdated authentication technologies.
    - Indicators:
        - Universal application of modern authentication protocols across all organizational resources, with no exceptions for the use of legacy methods.
        - Comprehensive and proactive management of authentication practices, enhancing the organization's resilience against various cyber threats.
        - Full alignment with authentication security best practices and compliance requirements, supported by an effective and well-managed authentication framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - IA-2 Identification and Authentication (Organizational Users): Implementing modern authentication supports the requirements for unique identification and authentication of users, enhancing security controls against unauthorized access.
    - IA-5 Authenticator Management: The transition to modern authentication involves managing the lifecycle of secure authenticators, aligning with the control's requirements for effective authenticator management practices.
    - AC-17 Remote Access: Modern authentication protocols support secure remote access control by providing robust mechanisms for authentication over remote connections.
    - IA-8 Identification and Authentication (Non-Organizational Users): For applications accessed by non-organizational users, the adoption of modern authentication can provide comprehensive mechanisms for identification and authentication in line with established policies.

- **Products covered:**
    - Microsoft Entra ID
    - Microsoft Entra Identity Protection

