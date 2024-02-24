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

### Conditional Access Policies Gate Access and Provide Remediation Activities
  - Are Conditional Access policies tailored to control and gate access to resources effectively implemented and actively managed within your organization?
    - Legacy: Conditional Access policies are virtually absent or only rudimentarily implemented, failing to meet the nuanced access control needs. There's a glaring absence of proactive management or review, leaving the system open to unnecessary risk without the benefits of dynamic access control or strategic remediation avenues.
    - Traditional: While basic Conditional Access policies are in place, they're applied broadly, lacking the granularity needed for effective security management. Updates and reviews are sporadic, indicating a reactive rather than a strategically proactive approach to securing access based on current security landscapes and operational demands.
    - Advanced: There's a clear effort to develop Conditional Access policies that consider multiple variables for access decisions, including user roles, device status, and application sensitivity. Regular reviews and updates are in place, yet there's room for improvement, especially in integrating real-time threat intelligence and automating the response to access challenges.
    - Optimal: Conditional Access policies are meticulously tailored and dynamically managed, incorporating real-time risk assessments, user behavior analytics, and automated remediation strategies. These policies are continually refined, leveraging the latest in security threat intelligence and operational feedback, ensuring both robust security measures and minimal disruption to user productivity.
 
  - In cases where access is restricted by Conditional Access policies, is there a structured remediation process for users to follow to regain access, and how is this oversight conducted?
    - Legacy: There is no structured remediation process in place for users who are denied access by Conditional Access policies. Oversight of such incidents is minimal or non-existent, leading to potential disruptions in productivity and lack of clear guidance for users on how to address access issues.
    - Traditional: A basic remediation process exists for users denied access, but it is generic and not well communicated. Oversight is sporadic and often reactive, with limited tracking or analysis of denied access incidents. This approach results in inconsistent user experiences and missed opportunities for improving access management based on real-world challenges.
    - Advanced: The organization has developed a structured remediation process for users impacted by Conditional Access policies, including clear steps for users to regain access. Oversight is more consistent, with some level of tracking and analysis of denied access incidents. However, there could be further improvements in automating remediation processes and enhancing real-time oversight.
    - Optimal: A highly structured and user-friendly remediation process is actively managed, providing immediate guidance and support for users denied access. Oversight is comprehensive, utilizing real-time tracking, analysis, and feedback mechanisms to continuously refine access controls and remediation processes. Automation and user-centric design ensure efficient resolution of access issues, minimizing disruption and bolstering security posture.

  - Is there a comprehensive strategy in place for planning, testing, and customizing Conditional Access policies to ensure they align with security needs while minimizing impact on user experience?
    - Legacy: There is no comprehensive strategy for planning, testing, or customizing Conditional Access policies. Policies are often created reactively, without thorough testing or consideration for user experience, leading to potential security vulnerabilities and significant disruptions in user productivity.
    - Traditional: A basic strategy exists for the planning and implementation of Conditional Access policies, but it lacks depth in testing and customization. While some efforts are made to align policies with security needs, the impact on user experience is not thoroughly evaluated, leading to potential friction or resistance from users.
    - Advanced: The organization has developed a more structured strategy for planning, testing, and customizing Conditional Access policies, considering both security requirements and user experience. Policies undergo regular review and testing phases, with adjustments made to better meet security objectives while striving to reduce user impact. However, there remains room for further integration of user feedback and continuous improvement processes.
    - Optimal: A comprehensive and dynamic strategy is in place for the planning, testing, and customizing of Conditional Access policies, fully integrating security needs with a focus on optimizing user experience. This strategy includes proactive engagement with stakeholders, iterative testing with real-world scenarios, and continuous feedback loops to refine policies. Automation and advanced analytics are leveraged to ensure policies are both effective and minimally intrusive.

#### Register devices with Microsoft Entra ID to restrict access from vulnerable and compromised devices
  - Are devices registered with Microsoft Entra ID to ensure that access from vulnerable and compromised devices is appropriately restricted?
    - Legacy: Devices are not consistently registered with Microsoft Entra ID, leading to a lack of control over access from vulnerable or compromised devices. This absence of device registration and management exposes the organization to increased security risks, with no effective mechanism to restrict access based on the device's security posture.
    - Traditional: Some devices are registered with Microsoft Entra ID, but the process is not comprehensive or uniformly enforced across the organization. While there is an attempt to restrict access from vulnerable devices, the lack of a consistent and thorough device management strategy results in gaps in security coverage and potential access by compromised devices.
    - Advanced: A majority of devices are registered with Microsoft Entra ID, and there are structured processes in place to manage device security and restrict access from those identified as vulnerable or compromised. While comprehensive measures are taken to ensure device compliance, occasional lapses in enforcement or updates may still occur, indicating room for further optimization.
    - Optimal: All devices are comprehensively registered with Microsoft Entra ID, ensuring a robust framework to restrict access from any vulnerable or compromised devices effectively. The organization employs a proactive and dynamic approach to device management, leveraging continuous monitoring, real-time threat intelligence, and automated compliance checks to maintain optimal security posture and minimize risks.

  - Is there a system in place to evaluate the health and compliance of devices before granting access to corporate resources, leveraging Microsoft Entra ID capabilities?
    - Legacy: There is no established system for evaluating the health and compliance of devices. As a result, devices may access corporate resources without any assessment of their security posture, significantly increasing the risk of exposing the organization to vulnerabilities and breaches through compromised or non-compliant devices.
    - Traditional: 
    - Advanced: 
    - Optimal:  

  - How are hybrid join or Microsoft Entra join and mobile device management through Intune utilized to manage access and security policies across all user devices?
    - Legacy: Hybrid join and Microsoft Entra join, alongside mobile device management (MDM) through Intune, are not effectively utilized, if at all. This lack of utilization results in a disjointed approach to managing access and security policies across devices, leading to inconsistent security postures and potential vulnerabilities in device management and access control.
    - Traditional: There is a basic implementation of hybrid join, Microsoft Entra join, and MDM through Intune. However, these tools are underutilized or not fully integrated, leading to a piecemeal approach in managing access and security policies. While some devices may be managed and secured, comprehensive coverage and policy consistency across all user devices are not achieved.
    - Advanced: Hybrid join, Microsoft Entra join, and MDM through Intune are utilized to a significant extent, providing a structured approach to managing access and security policies across user devices. While there is good coverage and integration, occasional challenges in policy consistency or enforcement may arise, indicating areas for further refinement and optimization.
    - Optimal: The organization leverages hybrid join, Microsoft Entra join, and MDM through Intune comprehensively, ensuring a seamless and fully integrated approach to managing access and security policies across all user devices. This optimal use includes advanced policy enforcement, real-time compliance checks, and automated remediation actions, ensuring consistent security posture and compliance across the device ecosystem.

### Analytics Improve Visibility

#### Configure your logging and reporting to improve visibility
  - Is logging and reporting configured to capture detailed information on authentication, authorization, and provisioning events?
    - Legacy: Logging and reporting mechanisms are either not configured or are minimally implemented, resulting in a lack of visibility into authentication, authorization, and provisioning activities. This gap hinders the ability to effectively monitor and respond to security incidents.
    - Traditional: Basic logging and reporting are in place, capturing some information on authentication, authorization, and provisioning. While this provides a level of visibility, it may not be sufficiently detailed or comprehensive to support robust security analysis.
    - Advanced: Detailed logging and reporting are configured for most authentication, authorization, and provisioning events, providing a high level of visibility. This advanced implementation supports effective security monitoring and incident response but may exclude some less critical systems.
    - Optimal: Logging and reporting are fully optimized, capturing detailed and comprehensive information on all authentication, authorization, and provisioning activities across the organization. This optimal configuration ensures maximum visibility, supporting the highest standards of security monitoring and analysis.

### Identities and access privileges are managed with identity governance

#### Secure privileged access with Privileged Identity Management
  - Is Privileged Identity Management utilized to control and monitor access to privileged operations and roles?
    - Legacy: No utilization of Privileged Identity Management (PIM) tools or processes. Privileged accounts are managed manually, leading to significant security risks due to the lack of oversight and control over these critical access points.
    - Traditional: Partial utilization of Privileged Identity Management for certain critical roles or systems. While some privileged accounts are under PIM control, comprehensive coverage across all privileged roles and operations is lacking, leading to inconsistent security enforcement.
    - Advanced: Advanced utilization of Privileged Identity Management, covering a broad spectrum of privileged roles and operations. Most privileged accounts are managed through PIM, significantly enhancing security, though minor exceptions may exist for legacy or specialized systems.
    - Optimal: Full utilization of Privileged Identity Management across all privileged roles and operations without exceptions. This optimal state ensures the highest level of security and control over privileged access, with sophisticated monitoring, auditing, and real-time response mechanisms.

#### Restrict user consent to applications
  - Are mechanisms in place to restrict user consent for applications, thereby preventing unauthorized data access?
    - Legacy: No mechanisms in place to restrict user consent for applications, allowing users to grant application permissions without oversight. This lack of control leads to potential over-privileging and unauthorized data access.
    - Traditional: Basic mechanisms to restrict user consent for applications are implemented, requiring approval for certain high-risk permissions. However, this control is applied inconsistently, and many applications can still access data without sufficient oversight.
    - Advanced: Advanced mechanisms are in place to restrict user consent for applications, with a comprehensive approval process for all application permissions. This significantly reduces the risk of unauthorized data access, though some legacy or third-party applications may not be fully covered.
    - Optimal: Complete and optimal control over user consent for applications, ensuring that no application can access data without thorough vetting and approval. This state represents the highest level of data protection and compliance with organizational policies.

#### Manage entitlement
  - Are access packages used to manage entitlements and streamline the access request and approval process?
    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal: 

#### Use passwordless authentication to reduce the risk of phishing and password attacks

### User, device, location, and behavior is analyzed in real time to determine risk and deliver ongoing protection

  - Is real-time analysis being conducted to evaluate risk and protect against it based on user, device, location, and behavior?
  - Has Microsoft Entra Password Protection been enabled for users in the cloud and on-premises to prevent weak passwords and password spray attacks?
  - Is Identity Protection enabled to provide granular session/user risk signals for investigating risk and confirming or dismissing compromise signals?

#### Deploy Microsoft Entra Password Protection
  - Is there a comprehensive strategy in place for deploying Microsoft Entra Password Protection to prevent weak or compromised password usage, tailored to meet the organization's security policies and user compliance?

#### Enable Identity Protection
  - Has the organization established a systematic approach for utilizing Microsoft Identity Protection to detect and mitigate identity threats, including the customization of risk policies according to the organization's risk management framework?
#### Enable Microsoft Defender for Cloud Apps integration with Identity Protection
  - Is there an integrated strategy for leveraging Microsoft Defender for Cloud Apps with Identity Protection to enhance threat detection capabilities, focusing on the utilization of shared signals and data to bolster the organization's security posture?

#### Enable Conditional Access integration with Microsoft Defender for Cloud Apps
#### Enable restricted session for use in access decisions

### Integrate threat signals from other security solutions to improve detection, protection, and response

#### Integrate Microsoft Defender for Identity with Microsoft Defender for Cloud Apps
#### Enable Microsoft Defender for Endpoint
  - Are threat signals from Microsoft Defender for Cloud Apps integrated with Identity Protection to enrich security insights and response capabilities?














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

    - Legacy: 
    - Traditional: 
    - Advanced: 
    - Optimal:  


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
