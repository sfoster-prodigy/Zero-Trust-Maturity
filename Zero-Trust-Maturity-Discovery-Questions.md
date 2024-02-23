# Zero Trust Maturity: Determine your maturity level.

## Summary

Embarking on the journey of Microsoft Sentinel onboarding necessitates a meticulous understanding of the existing cybersecurity landscape within an organization. The subsequent discovery questions are crafted to unravel crucial insights about your current security posture, data sources, and technological stack. This exploratory phase is pivotal to sculpting a robust and tailored security information and event management (SIEM) strategy with Microsoft Sentinel. By delving into the specifics of your existing security solutions, such as Microsoft Defender products and any third-party tools in use, we aim to seamlessly integrate them, ensuring that your transition is both smooth and strategically aligned with organizational security objectives. Your detailed responses will pave the way for us to craft a bespoke implementation plan, ensuring that Microsoft Sentinel is configured and optimized to safeguard your digital estate effectively.

## Microsoft Zero Trust Maturity Level (also defined as pillars) Questions

Questions in the following sections are designed to help us understand your current security tools and data sources. When a question is not about a specific tool or product, please list your implemented tools or remark there are none (e.g., "None", "N/A", etc.) . If you are unsure of the answer, please indicate that in your response. If you have any questions, please reach out to your Prodigy representative.


## Identities

### Cloud Identity Federates with On-premises Identity Systems

#### Connect all of your users to Microsoft Entra ID and federate with on-premises identity systems:

  - Are Microsoft Entra ID and your existing on-premises identity systems integrated to ensure seamless access for users across environments?
    - Legacy: Cloud identity is not federated with on-premises Active Directory using Microsoft Entra Connect. Users manage separate identities for cloud and on-premises environments, leading to inefficiencies and increased security risks due to the lack of centralized identity management.
    - Traditional: Cloud identity is federated with on-premises Active Directory using Microsoft Entra Connect pass-through authentication. This setup allows for real-time authentication requests to be passed directly to the on-premises Active Directory, enabling users to use their existing credentials for cloud services.
    - Advanced: Cloud identity is federated with on-premises Active Directory using Microsoft Entra Connect password hash synchronization. This approach synchronizes user password hashes from the on-premises Active Directory to the cloud, allowing for rapid authentication without direct access to the on-premises AD at the time of sign-in.
    - Optimal: Cloud identity is fully integrated with on-premises Active Directory through Microsoft Entra Connect, utilizing both password hash synchronization and seamless SSO with Conditional Access policies. This optimal setup leverages the best aspects of both advanced authentication mechanisms and introduces dynamic access controls based on user behavior, location, device health, and other risk factors. 

  - Is Microsoft Entra ID being utilized to protect against security threats such as brute force, DDoS, and password spray attacks through specific authentication options?
    - Legacy: Microsoft Entra ID is not actively utilized for protecting against common security threats like brute force, DDoS, and password spray attacks. Authentication mechanisms are basic, lacking advanced security features, leaving systems vulnerable to these types of cyber threats.
    - Traditional: Microsoft Entra ID is used with basic security settings to protect against attacks. Basic MFA is implemented, providing an additional layer of security beyond simple passwords. However, more sophisticated conditional access policies and threat protection mechanisms are not fully exploited.
    - Advanced: Microsoft Entra ID is leveraged more effectively, utilizing password hash synchronization and advanced MFA options. Conditional access policies are in place, offering protection based on user behavior, device compliance, and sign-in risk. This setup provides solid defense against brute force, DDoS, and password spray attacks.
    - Optimal: Microsoft Entra ID is fully optimized to protect against security threats, utilizing a comprehensive suite of authentication options and security measures. This includes seamless integration of advanced MFA, adaptive risk-based conditional access, and protection mechanisms specifically designed to thwart brute force, DDoS, and password spray attacks. AI and machine learning algorithms are employed to dynamically adjust security policies and authentication requirements in real-time, based on evolving threat landscapes.

  - Are unnecessary on-premises identities, like service accounts or privileged roles, identified and excluded from cloud federation?
    - Legacy: Unnecessary on-premises identities are not systematically identified or excluded from cloud federation. There is no clear strategy or process in place for assessing which on-premises identities should be federated to the cloud, resulting in potential security vulnerabilities and management inefficiencies.
    - Traditional: Some effort is made to identify unnecessary on-premises identities for exclusion from cloud federation, but the approach is manual and lacks comprehensive coverage. Basic guidelines exist for determining which identities to federate, but these are not applied consistently or thoroughly.
    - Advanced: A systematic approach is in place to identify and exclude unnecessary on-premises identities from cloud federation. Automated tools and processes are used to regularly audit on-premises identities, with specific criteria for determining which identities are federated to the cloud. Most non-essential service accounts and privileged roles are excluded.
    - Optimal: Comprehensive and dynamic management of on-premises identities ensures that only necessary identities are federated to the cloud. Advanced automation and intelligence tools are employed to continuously evaluate and adjust which on-premises identities are federated, based on real-time analysis of role necessity, security posture, and usage patterns. Unnecessary service accounts and privileged roles are proactively identified and excluded, ensuring optimal security and efficiency.

#### Establish your Identity Foundation with Microsoft Entra ID:
  - In what ways have you ensured that every access request passes through Microsoft Entra ID to leverage its policy decision points for enforcing access policies?
    - Legacy: Access requests are not consistently managed or enforced through Microsoft Entra ID. There is no centralized control over access requests, leading to fragmented security policies and potential vulnerabilities in access management.
    - Traditional: Some access requests are configured to pass through Microsoft Entra ID, but the implementation is partial or inconsistent. Basic access enforcement is in place, utilizing a limited set of policies within Microsoft Entra ID for certain applications or user groups.
    - Advanced: The majority of access requests are configured to go through Microsoft Entra ID, leveraging its policy decision point capabilities for robust access enforcement. Advanced policies are applied more broadly, though some legacy systems or applications may not yet be fully integrated.
    - Optimal: Every access request is meticulously configured to pass through Microsoft Entra ID, fully utilizing its comprehensive policy decision point capabilities for access enforcement across the entire organization. This setup ensures that all access is governed by dynamic, context-aware policies that adapt to evolving security landscapes and organizational needs.

#### Integrate all your applications with Microsoft Entra ID:
  - How have you integrated both modern and legacy applications with Microsoft Entra ID for single sign-on and consistent identity and access management?
    - Legacy: Neither modern nor legacy applications are integrated with Microsoft Entra ID for single sign-on (SSO) or identity and access management. Applications operate in silos, each with its own access management protocols, leading to inconsistent user experiences and heightened security risks.
    - Traditional: Modern applications are partially integrated with Microsoft Entra ID for SSO, but legacy applications remain disconnected, leading to a split in the user experience and access management. Efforts to unify identity management are underway, but not all applications are covered.
    - Advanced: Both modern and many legacy applications are integrated with Microsoft Entra ID for SSO and consistent identity and access management. Efforts include using application proxies or wrappers for legacy applications to fit them into the SSO ecosystem, improving overall security and user experience.
    - Optimal: Every application, both modern and legacy, is fully integrated with Microsoft Entra ID for seamless SSO and consistent identity and access management across the entire application portfolio. Advanced solutions, including custom integration for the most challenging legacy applications, ensure a unified and secure user experience.

  - Have you taken steps to eliminate multiple identity and access management (IAM) engines within your environment? If so, how did you consolidate them?
    - Legacy: Multiple, disparate IAM engines are in use across the environment without any efforts towards consolidation. This leads to fragmented identity and access management practices, creating inefficiencies and potential security vulnerabilities due to inconsistent policy enforcement and user experiences.
    - Traditional: Initial efforts to consolidate IAM engines have begun, focusing on integrating some systems with Microsoft Entra ID. While some applications now benefit from unified access management, others remain outside this integrated environment, resulting in a partial enhancement of security and user experience.
    - Advanced: Significant progress has been made in consolidating IAM engines, with the majority now integrated into a unified Microsoft Entra ID environment. This consolidation covers most modern and legacy applications, greatly enhancing security and user experience through consistent access management practices.
    - Optimal: A fully consolidated IAM environment has been achieved, with all identity and access management functions integrated into Microsoft Entra ID. This ensures a seamless and secure user experience across the entire application portfolio, with advanced security measures applied consistently.

#### Verify explicitly with strong authentication:
  - What strategies have you implemented to roll out Microsoft Entra multifactor authentication (MFA) across your organization?
    - Legacy: Microsoft Entra MFA has not been deployed, leaving the organization reliant on basic, single-factor authentication methods. This lack of MFA exposes the organization to increased security risks, such as unauthorized access and compromised user sessions.
    - Traditional: Microsoft Entra MFA has been partially deployed in the organization. Key systems or sensitive roles may be protected by MFA, but it is not uniformly applied across all users and applications. This partial deployment offers improved security over the Legacy stage but leaves significant gaps in protection.
    - Advanced: Microsoft Entra MFA is widely deployed across the organization, covering most users and applications. Efforts have been made to standardize MFA usage, significantly reducing user session risks. However, some areas or legacy systems might still operate without full MFA protection.
    - Optimal: Microsoft Entra MFA is fully deployed and enforced across the entire organization without exceptions. This comprehensive MFA coverage ensures the highest level of security for all user sessions, applications, and systems, effectively mitigating risks associated with compromised credentials.

  - How are you addressing and blocking legacy authentication methods that cannot support modern security challenges?
    - Legacy: Legacy authentication methods are fully permitted within the organization. There's no policy or mechanism in place to block these outdated authentication methods, leaving the organization vulnerable to a variety of security threats that exploit weaknesses in these older protocols.
    - Traditional: The organization has started to recognize the risks associated with legacy authentication methods and has initiated efforts to block them in certain high-risk scenarios or systems. However, this blockade is not comprehensive, and many systems still rely on legacy authentication due to various constraints.
    - Advanced: Significant progress has been made in blocking legacy authentication methods across the majority of the organization's systems and applications. Efforts include transitioning to modern authentication protocols and applying conditional access policies to enforce these standards. Some legacy systems may still use older methods due to technical limitations.
    - Optimal: The organization has achieved comprehensive blocking of all legacy authentication methods, fully embracing modern authentication protocols without exceptions. This includes enforcing strict access policies that require secure authentication mechanisms, effectively eliminating the risks associated with legacy methods.

## Devices and Workstations

### 

#### 
    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal: 

    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal: 

    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal: 

    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal: 
## Applications and Workloads

## Data

## Infrastructure

## Networks

 - 
