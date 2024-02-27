# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary



## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. The following 

## Identities

## Cloud Identity Federates with On-premises Identity Systems

### Connect all of your users to Microsoft Entra ID and federate with on-premises identity systems:

  - Are Microsoft Entra ID and your existing on-premises identity systems integrated to ensure seamless access for users across environments?
    - Legacy: Cloud identity is not federated with on-premises Active Directory using Microsoft Entra Connect. Users manage separate identities for cloud and on-premises environments, leading to inefficiencies and increased security risks due to the lack of centralized identity management.
    - Initial: Cloud identity is federated with on-premises Active Directory using Microsoft Entra Connect pass-through authentication or ADFS integration. This setup allows for real-time authentication requests to be passed directly to the on-premises Active Directory, enabling users to use their existing credentials for cloud services.
    - Advanced: Cloud identity is federated with on-premises Active Directory using Microsoft Entra Connect password hash synchronization. This approach synchronizes user password hashes from the on-premises Active Directory to the cloud, allowing for rapid authentication without direct access to the on-premises AD at the time of sign-in.
    - Optimal: Cloud identity is fully integrated with on-premises Active Directory through Microsoft Entra Connect, utilizing both password hash synchronization and seamless SSO with Conditional Access policies. This optimal setup leverages the best aspects of both advanced authentication mechanisms and introduces dynamic access controls based on user behavior, location, device health, and other risk factors. 

  - Is Microsoft Entra ID being utilized to protect against security threats such as brute force, DDoS, and password spray attacks through specific authentication options?
    - Legacy: Microsoft Entra ID is not actively utilized for protecting against common security threats like brute force, DDoS, and password spray attacks. Authentication mechanisms are basic, lacking advanced security features, leaving systems vulnerable to these types of cyber threats.
    - Initial: Microsoft Entra ID is used with basic security settings to protect against attacks. Basic MFA is implemented, providing an additional layer of security beyond simple passwords. However, more sophisticated conditional access policies and threat protection mechanisms are not fully exploited.
    - Advanced: Microsoft Entra ID is leveraged more effectively, utilizing password hash synchronization and advanced MFA options. Conditional access policies are in place, offering protection based on user behavior, device compliance, and sign-in risk. This setup provides solid defense against brute force, DDoS, and password spray attacks.
    - Optimal: Microsoft Entra ID is fully optimized to protect against security threats, utilizing a comprehensive suite of authentication options and security measures. This includes seamless integration of advanced MFA, adaptive risk-based conditional access, and protection mechanisms specifically designed to thwart brute force, DDoS, and password spray attacks. AI and machine learning algorithms are employed to dynamically adjust security policies and authentication requirements in real-time, based on evolving threat landscapes.

  - Are unnecessary on-premises identities, like service accounts or privileged roles, identified and excluded from cloud federation?
    - Legacy: Unnecessary on-premises identities are not systematically identified or excluded from cloud federation. There is no clear strategy or process in place for assessing which on-premises identities should be federated to the cloud, resulting in potential security vulnerabilities and management inefficiencies.
    - Initial: Some effort is made to identify unnecessary on-premises identities for exclusion from cloud federation, but the approach is manual and lacks comprehensive coverage. Basic guidelines exist for determining which identities to federate, but these are not applied consistently or thoroughly.
    - Advanced: A systematic approach is in place to identify and exclude unnecessary on-premises identities from cloud federation. Automated tools and processes are used to regularly audit on-premises identities, with specific criteria for determining which identities are federated to the cloud. Most non-essential service accounts and privileged roles are excluded.
    - Optimal: Comprehensive and dynamic management of on-premises identities ensures that only necessary identities are federated to the cloud. Advanced automation and intelligence tools are employed to continuously evaluate and adjust which on-premises identities are federated, based on real-time analysis of role necessity, security posture, and usage patterns. Unnecessary service accounts and privileged roles are proactively identified and excluded, ensuring optimal security and efficiency.

### Establish your Identity Foundation with Microsoft Entra ID:
  - Are all access requests passing through Microsoft Entra ID to leverage its policy decision points for enforcing access policies?
    - Legacy: Access requests are not consistently managed or enforced through Microsoft Entra ID. There is no centralized control over access requests, leading to fragmented security policies and potential vulnerabilities in access management.
    - Initial: Some access requests are configured to pass through Microsoft Entra ID, but the implementation is partial or inconsistent. Basic access enforcement is in place, utilizing a limited set of policies within Microsoft Entra ID for certain applications or user groups.
    - Advanced: The majority of access requests are configured to go through Microsoft Entra ID, leveraging its policy decision point capabilities for robust access enforcement. Advanced policies are applied more broadly, though some legacy systems or applications may not yet be fully integrated.
    - Optimal: Every access request is meticulously configured to pass through Microsoft Entra ID, fully utilizing its comprehensive policy decision point capabilities for access enforcement across the entire organization. This setup ensures that all access is governed by dynamic, context-aware policies that adapt to evolving security landscapes and organizational needs.

### Integrate all your applications with Microsoft Entra ID:
  - Are both modern and legacy applications integrated with Microsoft Entra ID for single sign-on and consistent identity and access management?
    - Legacy: Neither modern nor legacy applications are integrated with Microsoft Entra ID for single sign-on (SSO) or identity and access management. Applications operate in silos, each with its own access management protocols, leading to inconsistent user experiences and heightened security risks.
    - Initial: Modern applications are partially integrated with Microsoft Entra ID for SSO, but legacy applications remain disconnected, leading to a split in the user experience and access management. Efforts to unify identity management are underway, but not all applications are covered.
    - Advanced: Both modern and many legacy applications are integrated with Microsoft Entra ID for SSO and consistent identity and access management. Efforts include using application proxies or wrappers for legacy applications to fit them into the SSO ecosystem, improving overall security and user experience.
    - Optimal: Every application, both modern and legacy, is fully integrated with Microsoft Entra ID for seamless SSO and consistent identity and access management across the entire application portfolio. Advanced solutions, including custom integration for the most challenging legacy applications, ensure a unified and secure user experience.

  - Are all identity and access management functions integrated into Microsoft Entra ID to ensure a seamless and secure user experience across the entire application portfolio with advanced security measures applied consistently?
    - Legacy: Multiple, disparate IAM engines are in use across the environment without any efforts towards consolidation. This leads to fragmented identity and access management practices, creating inefficiencies and potential security vulnerabilities due to inconsistent policy enforcement and user experiences.
    - Initial: Initial efforts to consolidate IAM engines have begun, focusing on integrating some systems with Microsoft Entra ID. While some applications now benefit from unified access management, others remain outside this integrated environment, resulting in a partial enhancement of security and user experience.
    - Advanced: Significant progress has been made in consolidating IAM engines, with the majority now integrated into a unified Microsoft Entra ID environment. This consolidation covers most modern and legacy applications, greatly enhancing security and user experience through consistent access management practices.
    - Optimal: A fully consolidated IAM environment has been achieved, with all identity and access management functions integrated into Microsoft Entra ID. This ensures a seamless and secure user experience across the entire application portfolio, with advanced security measures applied consistently.

### Verify explicitly with strong authentication:
  - Is Microsoft Entra multifactor authentication (MFA) fully deployed and enforced across the entire organization without exception?
    - Legacy: Microsoft Entra MFA has not been deployed, leaving the organization reliant on basic, single-factor authentication methods. This lack of MFA exposes the organization to increased security risks, such as unauthorized access and compromised user sessions.
    - Initial: Microsoft Entra MFA has been partially deployed in the organization. Key systems or sensitive roles may be protected by MFA, but it is not uniformly applied across all users and applications. This partial deployment offers improved security over the Legacy stage but leaves significant gaps in protection.
    - Advanced: Microsoft Entra MFA is widely deployed across the organization, covering most users and applications. Efforts have been made to standardize MFA usage, significantly reducing user session risks. However, some areas or legacy systems might still operate without full MFA protection.
    - Optimal: Microsoft Entra MFA is fully deployed and enforced across the entire organization without exceptions. This comprehensive MFA coverage ensures the highest level of security for all user sessions, applications, and systems, effectively mitigating risks associated with compromised credentials.

  - Is the organization blocking all legacy authentication methods, fully embracing modern authentication protocols without exceptions, and enforcing strict access policies that require secure authentication mechanisms to eliminate the risks associated with legacy methods?
    - Legacy: Legacy authentication methods are fully permitted within the organization. There's no policy or mechanism in place to block these outdated authentication methods, leaving the organization vulnerable to a variety of security threats that exploit weaknesses in these older protocols.
    - Initial: The organization has started to recognize the risks associated with legacy authentication methods and has initiated efforts to block them in certain high-risk scenarios or systems. However, this blockade is not comprehensive, and many systems still rely on legacy authentication due to various constraints.
    - Advanced: Significant progress has been made in blocking legacy authentication methods across the majority of the organization's systems and applications. Efforts include transitioning to modern authentication protocols and applying conditional access policies to enforce these standards. Some legacy systems may still use older methods due to technical limitations.
    - Optimal: The organization has achieved comprehensive blocking of all legacy authentication methods, fully embracing modern authentication protocols without exceptions. This includes enforcing strict access policies that require secure authentication mechanisms, effectively eliminating the risks associated with legacy methods.

## Conditional Access Policies Gate Access and Provide Remediation Activities
  - Is there is a structured remediation process in place for users who are denied access by Conditional Access policies?
    - Legacy: Conditional Access policies are virtually absent or only rudimentarily implemented, failing to meet the nuanced access control needs. There's a glaring absence of proactive management or review, leaving the system open to unnecessary risk without the benefits of dynamic access control or strategic remediation avenues.
    - Initial: While basic Conditional Access policies are in place, they're applied broadly, lacking the granularity needed for effective security management. Updates and reviews are sporadic, indicating a reactive rather than a strategically proactive approach to securing access based on current security landscapes and operational demands.
    - Advanced: There's a clear effort to develop Conditional Access policies that consider multiple variables for access decisions, including user roles, device status, and application sensitivity. Regular reviews and updates are in place, yet there's room for improvement, especially in integrating real-time threat intelligence and automating the response to access challenges.
    - Optimal: Conditional Access policies are meticulously tailored and dynamically managed, incorporating real-time risk assessments, user behavior analytics, and automated remediation strategies. These policies are continually refined, leveraging the latest in security threat intelligence and operational feedback, ensuring both robust security measures and minimal disruption to user productivity.
 
  - In cases where access is restricted by Conditional Access policies, is there a structured remediation process for users to follow to regain access, and how is this oversight conducted?
    - Legacy: There is no structured remediation process in place for users who are denied access by Conditional Access policies. Oversight of such incidents is minimal or non-existent, leading to potential disruptions in productivity and lack of clear guidance for users on how to address access issues.
    - Initial: A basic remediation process exists for users denied access, but it is generic and not well communicated. Oversight is sporadic and often reactive, with limited tracking or analysis of denied access incidents. This approach results in inconsistent user experiences and missed opportunities for improving access management based on real-world challenges.
    - Advanced: The organization has developed a structured remediation process for users impacted by Conditional Access policies, including clear steps for users to regain access. Oversight is more consistent, with some level of tracking and analysis of denied access incidents. However, there could be further improvements in automating remediation processes and enhancing real-time oversight.
    - Optimal: A highly structured and user-friendly remediation process is actively managed, providing immediate guidance and support for users denied access. Oversight is comprehensive, utilizing real-time tracking, analysis, and feedback mechanisms to continuously refine access controls and remediation processes. Automation and user-centric design ensure efficient resolution of access issues, minimizing disruption and bolstering security posture.

  - Is there a comprehensive strategy in place for planning, testing, and customizing Conditional Access policies to ensure they align with security needs while minimizing impact on user experience?
    - Legacy: There is no comprehensive strategy for planning, testing, or customizing Conditional Access policies. Policies are often created reactively, without thorough testing or consideration for user experience, leading to potential security vulnerabilities and significant disruptions in user productivity.
    - Initial: A basic strategy exists for the planning and implementation of Conditional Access policies, but it lacks depth in testing and customization. While some efforts are made to align policies with security needs, the impact on user experience is not thoroughly evaluated, leading to potential friction or resistance from users.
    - Advanced: The organization has developed a more structured strategy for planning, testing, and customizing Conditional Access policies, considering both security requirements and user experience. Policies undergo regular review and testing phases, with adjustments made to better meet security objectives while striving to reduce user impact. However, there remains room for further integration of user feedback and continuous improvement processes.
    - Optimal: A comprehensive and dynamic strategy is in place for the planning, testing, and customizing of Conditional Access policies, fully integrating security needs with a focus on optimizing user experience. This strategy includes proactive engagement with stakeholders, iterative testing with real-world scenarios, and continuous feedback loops to refine policies. Automation and advanced analytics are leveraged to ensure policies are both effective and minimally intrusive.

### Register devices with Microsoft Entra ID to restrict access from vulnerable and compromised devices
  - Are devices registered with Microsoft Entra ID to ensure that access from vulnerable and compromised devices is appropriately restricted?
    - Legacy: Devices are not consistently registered with Microsoft Entra ID, leading to a lack of control over access from vulnerable or compromised devices. This absence of device registration and management exposes the organization to increased security risks, with no effective mechanism to restrict access based on the device's security posture.
    - Initial: Some devices are registered with Microsoft Entra ID, but the process is not comprehensive or uniformly enforced across the organization. While there is an attempt to restrict access from vulnerable devices, the lack of a consistent and thorough device management strategy results in gaps in security coverage and potential access by compromised devices.
    - Advanced: A majority of devices are registered with Microsoft Entra ID, and there are structured processes in place to manage device security and restrict access from those identified as vulnerable or compromised. While comprehensive measures are taken to ensure device compliance, occasional lapses in enforcement or updates may still occur, indicating room for further optimization.
    - Optimal: All devices are comprehensively registered with Microsoft Entra ID, ensuring a robust framework to restrict access from any vulnerable or compromised devices effectively. The organization employs a proactive and dynamic approach to device management, leveraging continuous monitoring, real-time threat intelligence, and automated compliance checks to maintain optimal security posture and minimize risks.

  - Is there a system in place to evaluate the health and compliance of devices before granting access to corporate resources, leveraging Microsoft Entra ID capabilities?
    - Legacy: There is no established system for evaluating the health and compliance of devices. As a result, devices may access corporate resources without any assessment of their security posture, significantly increasing the risk of exposing the organization to vulnerabilities and breaches through compromised or non-compliant devices.
    - Initial: A basic system exists for evaluating device health and compliance, but it is not comprehensive or fully leveraged. While some devices are assessed for compliance, the process lacks depth and consistency, potentially allowing vulnerable devices to access corporate resources.
    - Advanced: A structured system is in place to evaluate the health and compliance of devices using Microsoft Entra ID capabilities. Most devices are assessed before access is granted, reducing the risk of exposure from vulnerable devices. However, continuous improvements and tighter integration could further enhance security.
    - Optimal: A comprehensive and fully integrated system is established to evaluate the health and compliance of all devices leveraging Microsoft Entra ID capabilities. This system ensures rigorous assessments and real-time compliance checks, effectively restricting access from vulnerable devices and significantly enhancing the organization's security posture.

  - Are devices managed using hybrid join, Microsoft Entra join, and MDM through Intune for seamless access and security policy integration across all user devices?
    - Legacy: Hybrid join and Microsoft Entra join, alongside mobile device management (MDM) through Intune, are not effectively utilized, if at all. This lack of utilization results in a disjointed approach to managing access and security policies across devices, leading to inconsistent security postures and potential vulnerabilities in device management and access control.
    - Initial: There is a basic implementation of hybrid join, Microsoft Entra join, and MDM through Intune. However, these tools are underutilized or not fully integrated, leading to a piecemeal approach in managing access and security policies. While some devices may be managed and secured, comprehensive coverage and policy consistency across all user devices are not achieved.
    - Advanced: Hybrid join, Microsoft Entra join, and MDM through Intune are utilized to a significant extent, providing a structured approach to managing access and security policies across user devices. While there is good coverage and integration, occasional challenges in policy consistency or enforcement may arise, indicating areas for further refinement and optimization.
    - Optimal: The organization leverages hybrid join, Microsoft Entra join, and MDM through Intune comprehensively, ensuring a seamless and fully integrated approach to managing access and security policies across all user devices. This optimal use includes advanced policy enforcement, real-time compliance checks, and automated remediation actions, ensuring consistent security posture and compliance across the device ecosystem.

### Analytics Improve Visibility

### Configure your logging and reporting to improve visibility
  - Is logging and reporting configured to capture detailed information on authentication, authorization, and provisioning events?
    - Legacy: Logging and reporting mechanisms are either not configured or are minimally implemented, resulting in a lack of visibility into authentication, authorization, and provisioning activities. This gap hinders the ability to effectively monitor and respond to security incidents.
      - Indicators:
        - Sparse or non-existent logging of critical security events.
        - Limited ability to audit or review access decisions and provisioning changes.
        - Increased risk due to lack of insight into potentially malicious activities or configuration errors.
    - Initial: Basic logging and reporting are in place, capturing some information on authentication, authorization, and provisioning. While this provides a level of visibility, it may not be sufficiently detailed or comprehensive to support robust security analysis.
      - Indicators:
        - Partial coverage of event logging, with significant activities recorded but lacking granularity.
        - Some capability for security analysis and incident response, though with limitations.
        - Moderate improvement in visibility, but with room for enhancement in detail and coverage.
    - Advanced: Detailed logging and reporting are configured for most authentication, authorization, and provisioning events, providing a high level of visibility. This advanced implementation supports effective security monitoring and incident response but may exclude some less critical systems.
      - Indicators:
        - Comprehensive logging of most security-relevant events with detailed information.
        - Enhanced capability for in-depth security analysis and proactive incident management.
        - Significantly improved visibility into security operations, with minor gaps remaining.
    - Optimal: Logging and reporting are fully optimized, capturing detailed and comprehensive information on all authentication, authorization, and provisioning activities across the organization. This optimal configuration ensures maximum visibility, supporting the highest standards of security monitoring and analysis.
      - Indicators:
        - Universal and detailed logging of all security events without exceptions.
        - Full capability for granular security analysis, auditing, and proactive incident response.
        - Maximized visibility and control over security operations, eliminating blind spots in monitoring and analysis.

## Identities and access privileges are managed with identity governance

### Secure privileged access with Privileged Identity Management
  - Is Privileged Identity Management utilized to control and monitor access to privileged operations and roles?
    - Legacy: No utilization of Privileged Identity Management (PIM) tools or processes. Privileged accounts are managed manually, leading to significant security risks due to the lack of oversight and control over these critical access points.
      - Indicators:
        - Manual management of privileged accounts without automated controls or oversight.
        - Increased risk of unauthorized access to critical systems and data through privileged accounts.
        - Lack of auditing and real-time monitoring for privileged account activities.
    - Initial: Partial utilization of Privileged Identity Management for certain critical roles or systems. While some privileged accounts are under PIM control, comprehensive coverage across all privileged roles and operations is lacking, leading to inconsistent security enforcement.
      - Indicators:
        - Selective application of PIM controls, leaving gaps in privileged account management.
        - Moderate improvement in securing privileged access but with notable vulnerabilities due to incomplete coverage.
        - Some level of auditing and monitoring for privileged activities, though not universally applied.
    - Advanced: Advanced utilization of Privileged Identity Management, covering a broad spectrum of privileged roles and operations. Most privileged accounts are managed through PIM, significantly enhancing security, though minor exceptions may exist for legacy or specialized systems.
      - Indicators:
        - Broad coverage of privileged accounts under PIM control, with comprehensive policies and procedures.
        - Significant reduction in risks associated with privileged access, with enhanced auditing and real-time monitoring capabilities.
        - Occasional exceptions for certain privileged roles or operations, with plans for future inclusion.
    - Optimal: Full utilization of Privileged Identity Management across all privileged roles and operations without exceptions. This optimal state ensures the highest level of security and control over privileged access, with sophisticated monitoring, auditing, and real-time response mechanisms.
      - Indicators:
        - Universal application of PIM controls across all privileged accounts, systems, and data.
        - Maximum security posture for privileged access, with zero trust enforcement and adaptive controls.
        - Comprehensive auditing, real-time monitoring, and automated response to any suspicious privileged activities.

### Restrict user consent to applications
  - Are user consents to applications being restricted to manage and prevent unnecessary data exposure?
    - Legacy: No mechanisms in place to restrict user consent for applications, allowing users to grant application permissions without oversight. This lack of control leads to potential over-privileging and unauthorized data access.
      - Indicators:
        - Users can consent to any application without administrative oversight.
        - High risk of unauthorized data access due to lack of application vetting.
        - Potential for over-privileging of applications with no checks in place.
    - Initial: Basic restrictions on user consent for applications are introduced, such as allowing consent only for apps from verified publishers and for selected permissions. While this introduces a layer of control, it's applied selectively, leaving gaps that could still allow unauthorized applications to access data without comprehensive oversight.
      - Indicators:
        - Approval is required for certain high-risk permissions, but not uniformly enforced.
        - Some level of administrative oversight, but inconsistencies leave gaps in protection.
        - Applications can still access data without comprehensive scrutiny or consistent policy application.
    - Advanced: Advanced mechanisms for restricting user consent are employed, including the admin consent workflow, which enables users to request administrator approval for application permissions directly. Education on the permissions and consent framework for administrators, along with auditing and monitoring of apps and permissions, enhances security. However, the system might still have exceptions for certain business-critical or legacy applications.
      - Indicators:
        - Detailed education and training for administrators on permissions and consent.
        - Auditing and monitoring of applications and permissions to identify and mitigate risks.
        - Business-critical and legacy applications may have exceptions, requiring careful management.
    - Optimal: A comprehensive and proactive approach to controlling user consent for applications is established, ensuring thorough vetting and approval of all applications before access is granted. This includes proactive administrator consent for high-usage applications, stringent evaluation of applications for tenant-wide admin consent, and limiting user access even when admin consent has been granted. This tier represents the pinnacle of preventing unauthorized data access and ensuring adherence to strict organizational policies and security standards.
      - Indicators:
        - Proactive granting of administrator consent for trusted, high-usage applications.
        - Stringent evaluation and approval process for tenant-wide admin consent to applications.
        - User access to applications is limited, even with admin consent, through mechanisms like requiring user assignment.
        - Use of advanced tools for auditing and monitoring consent-related activities, ensuring continuous oversight and compliance.
  - Are successful application authorizations monitored?
    - Legacy: No mechanisms are in place to monitor successful application consent authorizations, leaving organizations blind to which applications users are granting access. This lack of visibility and control significantly increases the risk of unauthorized data access and potential data breaches, as there is no system to track or review the consents given across the organization.
      - Indicators:
        - Users can grant consent to any application without oversight.
        - No centralized tracking or review of application consents.
        - Increased risk of unauthorized data access and potential breaches.
    - Initial: Basic monitoring of application consent authorizations is introduced, enabling organizations to track and review consents for a subset of applications, typically focusing on those deemed high-risk or high-impact. While this represents a step toward better consent management, it remains limited in scope and depth, often relying on manual review processes and lacking real-time monitoring capabilities.
      - Indicators
        - Tracking and review of consents for high-risk or high-impact applications.
        - Manual review processes for a subset of applications.
        - Limited scope and depth in monitoring, with significant gaps remaining.
    - Advanced: Comprehensive mechanisms for monitoring application consent authorizations are employed, including automated tools and processes for tracking, reviewing, and auditing consents across all applications. This approach enhances visibility and control over application consents, allowing for timely detection and remediation of unauthorized or risky consents. However, there may still be challenges in fully automating the review process for all types of applications, particularly those with complex consent requirements.
      - Indicators:
        - Automated tools and processes for tracking, reviewing, and auditing consents.
        - Enhanced visibility and control over application consents.
        - Timely detection and remediation of unauthorized or risky consents, though some automation challenges persist.
    - Optimal: A proactive and fully integrated approach to monitoring application consent authorizations is established, leveraging advanced analytics, real-time monitoring, and automated remediation processes. This tier ensures that all application consents are continuously reviewed and validated against organizational policies and security standards, with immediate action taken on any unauthorized or suspicious consent activities. This comprehensive strategy represents the highest level of control and security in managing application consent authorizations, minimizing the risk of data exposure and unauthorized access to the fullest extent possible.
      - Indicators:
        - Advanced analytics and real-time monitoring of all application consents.
        - Automated remediation processes for unauthorized or suspicious consent activities.
        - Continuous review and validation of consents against organizational policies and security standards.
        - Minimized risk of data exposure and unauthorized access through comprehensive control and security measures.
### Manage entitlement
  - Is there a comprehensive system in place for managing entitlements that ensures users have appropriate access rights to resources based on their roles and responsibilities?
    - Legacy: No comprehensive system is in place for managing entitlements. Users often have inappropriate access rights, leading to potential security risks and operational inefficiencies.
    - Initial: A basic system exists for managing entitlements, but it lacks the depth to ensure users always have access rights aligned with their roles. While there are attempts to match access with responsibilities, inconsistencies and gaps remain.
    - Advanced: There is a structured system for managing entitlements, ensuring users have access rights that largely match their roles and responsibilities. Regular improvements are made, but opportunities for further refinement exist to achieve optimal alignment and security.
    - Optimal: A comprehensive and fully optimized system for managing entitlements is in place, guaranteeing access rights are perfectly aligned with user roles and responsibilities. The system ensures high operational efficiency and security, with access rights dynamically adjusted as roles change.
  - Is the process for granting, modifying, and revoking access rights streamlined and automated to minimize delays and reduce the risk of manual errors?
    - Legacy: The process for granting, modifying, and revoking access rights is manual and cumbersome, leading to significant delays and a high risk of errors.
    - Initial: Some efforts are made to streamline and automate the access rights management process, but these are partial and not fully effective. Delays and manual errors are reduced but not eliminated.
    - Advanced: The process for managing access rights is significantly streamlined and automated, leading to reduced delays and a lower risk of manual errors. While highly effective, there's still room for further enhancements in automation and process efficiency.
    - Optimal: A fully optimized and automated process for managing access rights is in place, minimizing delays and virtually eliminating the risk of manual errors. The process is highly efficient, ensuring timely and accurate granting, modifying, and revoking of access rights.
  - Are there mechanisms in place for monitoring and reporting on entitlement management to detect and respond to unauthorized access attempts or non-compliance with policies?
    - Legacy: There are no mechanisms in place for monitoring and reporting on entitlement management, leaving unauthorized access attempts and non-compliance issues undetected.
    - Initial: Basic mechanisms for monitoring and reporting on entitlement management exist but lack the depth and automation needed for effective oversight and response to unauthorized access or non-compliance.
    - Advanced: Structured mechanisms are in place for monitoring and reporting on entitlement management, providing a good level of oversight and enabling responses to unauthorized access attempts or non-compliance. While effective, there's potential for further optimization and automation.
    - Optimal: Comprehensive and fully automated mechanisms for monitoring and reporting on entitlement management are established, ensuring exceptional oversight and rapid response to any unauthorized access attempts or policy non-compliance. The system is optimized for efficiency and effectiveness.

### Use passwordless authentication to reduce the risk of phishing and password attacks
  - Is passwordless authentication implemented to minimize the risk associated with phishing and password attacks?
    - Legacy: Passwordless authentication is not implemented, leaving the organization heavily reliant on traditional password-based authentication methods. This reliance increases the risk of falling victim to phishing and password spray attacks, as there are no advanced authentication technologies in place to mitigate these threats.
    - Initial: Basic passwordless authentication methods are in place, such as limited use of Microsoft Authenticator. However, the implementation is not widespread across the organization, and more advanced technologies like Windows Hello and FIDO2 are not yet utilized. This partial implementation offers some protection against phishing and password attacks but leaves gaps in security coverage.
    - Advanced: Passwordless authentication is implemented using a variety of technologies, including Windows Hello, Microsoft Authenticator, and possibly FIDO2, among others. The implementation covers a significant portion of the organization, substantially reducing the risk associated with phishing and password attacks. However, there may be areas or user groups within the organization that are not fully covered, indicating room for broader implementation and integration.
    - Optimal: The organization has fully implemented passwordless authentication, utilizing a comprehensive range of technologies such as Windows Hello, Microsoft Authenticator, and FIDO2 across all areas. This widespread implementation ensures maximum protection against phishing and password attacks, significantly enhancing the security posture by eliminating reliance on passwords and reducing the risk of such attacks to nearly zero.

## User, device, location, and behavior is analyzed in real time to determine risk and deliver ongoing protection

### Deploy Microsoft Entra Password Protection
  - Has Microsoft Entra Password Protection been enabled for users in the cloud and on-premises to prevent weak passwords and password spray attacks?
    - Legacy: Microsoft Entra Password Protection is not deployed, leaving the organization vulnerable to weak or compromised password usage. Security policies do not adequately address password protection, leading to a higher risk of breach due to inadequate password management practices.
    - Initial: Microsoft Entra Password Protection is deployed in a basic form, but the strategy is not comprehensive or fully aligned with the organization's security policies. Efforts to prevent weak password usage are present but not optimized for maximum protection or user compliance.
    - Advanced: Microsoft Entra Password Protection is deployed in a more advanced form, with efforts to tailor the deployment to the organization's security policies. While significant steps are taken to prevent weak or compromised password usage, continuous refinement and alignment with user compliance are needed.
    - Optimal: The organization employs a comprehensive and fully integrated strategy for deploying Microsoft Entra Password Protection, perfectly tailored to meet stringent security policies and ensure user compliance. Advanced measures are in place to prevent any weak or compromised password usage, significantly enhancing the organization's security posture.

### Enable Identity Protection
  - Is Identity Protection enabled to provide granular session/user risk signals for investigating risk and confirming or dismissing compromise signals?
    - Legacy: There is no systematic approach for utilizing Microsoft Identity Protection. The organization lacks customization of risk policies, leaving identity threats undetected and unmitigated.
    - Initial: Microsoft Identity Protection is used, but the approach is not fully systematic or tailored to the organization's risk management framework. Some identity threats may be detected, but the mitigation process is not optimized.
    - Advanced: The organization has established a more systematic approach to utilizing Microsoft Identity Protection, including some customization of risk policies. While many identity threats are effectively detected and mitigated, there's room for further refinement to fully align with the organization's risk management framework.
    - Optimal: A comprehensive and fully tailored strategy is in place for utilizing Microsoft Identity Protection, with risk policies customized to fit precisely within the organization's risk management framework. This approach ensures the highest level of detection and mitigation of identity threats, significantly bolstering the organization's security posture.

### Enable Microsoft Defender for Cloud Apps integration with Identity Protection
  - Are threat signals from Microsoft Defender for Cloud Apps integrated with Identity Protection to improve detection and response to suspicious user behaviors?
    - Legacy: There is no integration of Microsoft Defender for Cloud Apps with Identity Protection, missing opportunities to enhance threat detection capabilities through shared signals and data.
    - Initial: Basic integration of Microsoft Defender for Cloud Apps with Identity Protection exists, but the strategy is not fully developed or optimized. Shared signals and data are underutilized, providing limited enhancements to threat detection capabilities.
    - Advanced: A structured strategy is in place for integrating Microsoft Defender for Cloud Apps with Identity Protection, leveraging shared signals and data to enhance threat detection. While significant improvements are seen, the strategy could be further refined for maximum security posture enhancement.
    - Optimal: The organization employs a comprehensive and fully optimized strategy for integrating Microsoft Defender for Cloud Apps with Identity Protection. This integration maximizes the utilization of shared signals and data, significantly bolstering the organization's security posture with advanced threat detection capabilities.

### Enable Conditional Access integration with Microsoft Defender for Cloud Apps
  - Is Conditional Access integrated with Microsoft Defender for Cloud Apps?
    - Legacy: Conditional Access is not integrated with Microsoft Defender for Cloud Apps, leaving the organization's cloud applications and data exposed to potential security risks. There's no systematic approach to monitor or control access based on the evolving threat landscape, resulting in a static and vulnerable security posture. Without this integration, the organization misses out on advanced security analytics and real-time threat detection, making it difficult to enforce adaptive access policies that respond to assessed risks.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Absence of Conditional Access policies informed by threat intelligence.
        - No evidence of adaptive security measures based on user behavior and risk assessment.
        - Increased incidents of security breaches due to unmonitored application access.
    - Initial: Initial steps are taken to integrate Conditional Access with Microsoft Defender for Cloud Apps, providing a basic level of security monitoring and response capabilities. At this stage, Conditional Access policies begin to leverage some signals from Defender for Cloud Apps to inform access decisions, but the implementation is limited and does not fully utilize the potential of cloud-based threat intelligence. The organization starts to see benefits in terms of improved visibility into access patterns and potential threats, but the coverage is not comprehensive.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Implementation of Conditional Access policies that begin to leverage threat signals.
        - Partial coverage and utilization of threat intelligence for security monitoring.
        - Some improvements in detecting suspicious activities, with gaps in comprehensive threat response.
    - Advanced: The integration between Conditional Access and Microsoft Defender for Cloud Apps is expanded, enabling more sophisticated security controls based on a wider array of signals from user behavior and threat intelligence. Conditional Access policies are dynamically adjusted based on detailed risk assessments, and the organization employs conditional access to enforce security policies more granely. This tier sees improved security outcomes through better detection of suspicious activities and the ability to respond more effectively to identified risks, although there may still be areas for further optimization.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Use of a wide array of signals from user behavior and threat intelligence for Conditional Access.
        - Evidence of dynamic and granular enforcement of security policies.
        - Decrease in successful security breaches due to enhanced detection and response capabilities.
    - Optimal: A fully integrated Conditional Access and Microsoft Defender for Cloud Apps system is in place, offering comprehensive and adaptive security measures that cover all aspects of access and threat response. This level of integration ensures that Conditional Access policies are informed by real-time, detailed threat intelligence from Defender for Cloud Apps, enabling the organization to implement dynamic and context-aware access controls. The optimal tier represents the highest standard of security, with the ability to detect, analyze, and respond to threats in real-time, significantly reducing the risk of unauthorized access and data breaches while maintaining a seamless user experience.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Comprehensive coverage and use of real-time threat intelligence for adaptive access controls.
        - Seamless user experience with robust protection against unauthorized access and data breaches.
        - Significant reduction in incidents of security breaches, demonstrating effective threat detection and response.

### Enable restricted session for use in access decisions
  - Is restricted session enabled for limited access to SharePoint Online and Exchange Online?
    - There are no restrictions on accessing SharePoint Online and Exchange Online from unmanaged devices, allowing full access without any conditional access policies in place. This unrestricted access enables users to download, print, and sync files freely, significantly increasing the risk of data leakage and unauthorized access to sensitive organizational information.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Full access from any device without restrictions
        - No conditional access policies implemented
        - High risk of data leakage and unauthorized access
    - Initial: Basic limitations are introduced for access from unmanaged devices. In SharePoint Online, access is restricted to browser-only, disabling the ability to download, print, or sync files. Similarly, in Exchange Online, conditional access policies restrict the ability to download email attachments to local machines, although users can still view and edit attachments in the browser. This tier introduces a fundamental level of security but lacks comprehensive controls and granularity in access restrictions.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Browser-only access for SharePoint Online
        - Download restrictions for email attachments in Exchange Online
        - Basic level of security with limited granularity
    - Advanced: More sophisticated conditional access policies are implemented. SharePoint Online administrators can now tailor access based on specific user groups, site classifications, or content types, and use PowerShell for detailed policy application. Exchange Online enhances security by allowing finer adjustments to the OwaMailboxPolicy, such as setting attachments to read-only or entirely blocking downloads on non-compliant devices. This tier offers improved security through enhanced control over access and editing capabilities, although some exceptions for specific user needs or applications may remain.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Granular access control based on user groups, site classifications, or content types
        - Use of PowerShell for detailed policy application in SharePoint Online
        - Enhanced security measures for attachments in Exchange Online
        - Improved control with allowances for exceptions
    - Optimal: A holistic approach to managing access from unmanaged devices is adopted, applying comprehensive conditional access policies across all Microsoft 365 services. This includes enforcing strict access controls based on device compliance, user risk profiles, and session restrictions, ensuring a seamless yet secure experience for users across all devices. SharePoint Online and Exchange Online benefit from integrated policies that not only restrict access and editing based on device status but also enforce these policies consistently across the entire suite of Microsoft 365 applications. This tier represents the highest level of security, minimizing data exposure and unauthorized access while maintaining operational flexibility.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Comprehensive conditional access policies across Microsoft 365
        - Enforced access controls based on device compliance and user risk profiles
        - Integrated policies for consistent enforcement across Microsoft 365 applications
        - Highest level of security with operational flexibility

## Integrate threat signals from other security solutions to improve detection, protection, and response

### Integrate Microsoft Defender for Identity with Microsoft Defender for Cloud Apps
  - Are signals from Microsoft Defender for Identity integrated to enhance the detection and response to risky behaviors in on-premises and cloud environments?
    - Legacy: No integration of signals from Microsoft Defender for Identity exists, leaving a significant gap in the detection and response to risky behaviors across on-premises and cloud environments. Organizations rely solely on traditional, perimeter-based security measures, which fail to address the nuanced threats present in a modern, decentralized IT landscape. This lack of integration results in a reactive posture towards security incidents, with limited visibility and control over identity-related risks.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Absence of centralized identity threat detection mechanisms.
        - Reliance on perimeter-based security controls with no identity signal sharing.
        - Lack of visibility into user activities and security events across environments.
        - No automated response capabilities to identity-related threats.
    - Initial: Basic integration of signals from Microsoft Defender for Identity is established, providing initial insights into risky behaviors within on-premises systems. While this represents a step forward in enhancing security posture, the approach remains fragmented. Integration with cloud security solutions is minimal, leading to inconsistent detection and response capabilities across the IT environment. This stage introduces the concept of identity-based security signals but does not fully leverage their potential in a cohesive security strategy.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Initial efforts to integrate on-premises identity signals with some cloud security solutions.
        - Selective, rather than comprehensive, use of identity signals for threat detection.
        - Inconsistent policy enforcement across on-premises and cloud environments.
        - Some manual processes in monitoring and responding to security alerts.
    - Advanced: Advanced integration techniques are deployed, including comprehensive signal sharing between Microsoft Defender for Identity and cloud security solutions. This integration extends visibility into user activities and risky behaviors across both on-premises and cloud environments, facilitating a more unified and effective response to threats. However, while the framework for leveraging identity signals is in place, occasional lapses in coverage or delays in response may occur due to the complex nature of these integrations and the evolving threat landscape.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Robust integration of identity signals from both on-premises and cloud environments.
        - Automated detection and response to identity-based threats across the digital estate.
        - Use of advanced analytics to understand user behavior and detect anomalies.
        - Presence of policy and governance mechanisms that leverage identity signals for security decisions.
    - Optimal: A fully mature integration of Microsoft Defender for Identity with cloud security solutions is achieved, embodying a proactive and all-encompassing approach to monitoring, detecting, and responding to risky behaviors. This tier ensures seamless real-time signal integration, enabling immediate and informed security responses across the entire digital estate. Optimal use of identity signals empowers organizations to preemptively address potential threats, minimizing risk exposure and reinforcing a robust Zero Trust security posture. This level represents the pinnacle of identity-driven security, ensuring maximum protection and resilience against identity-related threats in both on-premises and cloud environments.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Seamless, real-time integration of identity signals for immediate threat detection and response.
        - Full coverage and visibility into user activities and security events across all environments.
        - Advanced automated response capabilities, minimizing manual intervention in threat mitigation.
        - Continuous assessment and adaptation of security policies based on evolving threats and identity signals.

### Enable Microsoft Defender for Endpoint
  - Is Conditional Access configured in Microsoft Defender for Endpoint to utilize health signals from Windows machines for access decisions?
    - Legacy: There is no Conditional Access configured within Microsoft Defender for Endpoint to utilize health signals from Windows machines, leaving access decisions solely on basic authentication methods. This absence of advanced security measures leaves the system vulnerable to unauthorized access, as it does not consider the health status of devices attempting to access resources.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - The absence of Conditional Access policies in Microsoft Defender for Endpoint.
        - No integration or consideration of device health signals when making access decisions.
        - Sole reliance on traditional authentication methods without additional security checks.
    - Initial: Initial steps towards implementing Conditional Access in Microsoft Defender for Endpoint are taken, with basic policies that utilize some health signals from Windows machines for access decisions. While this introduces a fundamental level of security, it's applied in a limited scope, potentially overlooking nuanced threats and sophisticated attack vectors.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Initial implementation of Conditional Access policies that may include simple rules based on location or user group but lack comprehensive device health considerations.
        - Some use of health signals from Windows machines in access decisions, but applied selectively and not as part of a broader security strategy.
        - Minimal integration with other security solutions, providing a basic level of threat detection and response.
    - Advanced: Conditional Access policies within Microsoft Defender for Endpoint are further refined, incorporating a wider range of health signals from Windows machines to inform access decisions. This includes integration with other security solutions to enhance detection and response capabilities. However, some scenarios may still rely on default or less stringent policies for certain applications or user groups, leaving marginal vulnerabilities.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Advanced Conditional Access policies that utilize a broader range of health signals from Windows machines, including integration with other security solutions for enhanced detection and response.
        - Increased administrative control over Conditional Access policies, including the ability to customize policies based on specific security needs and risk assessments.
        - Use of real-time threat detection and integration with Microsoft Defender for Endpoint for dynamic access decisions based on device health.
    - Optimal: A comprehensive Conditional Access strategy is fully integrated within Microsoft Defender for Endpoint, leveraging all available health signals from Windows machines to make informed and dynamic access decisions. This approach includes real-time threat detection, adaptive access policies, and stringent compliance checks, ensuring that only devices in optimal health status can access organizational resources. This tier exemplifies the highest standard of security and operational efficiency, minimizing the risk of data breaches and unauthorized access through meticulous device health assessment and policy enforcement.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Full integration of Conditional Access within Microsoft Defender for Endpoint, leveraging all available health signals from Windows machines for making informed access decisions.
        - Dynamic and real-time assessment of device health status, with adaptive access policies that respond to the latest threat intelligence and security analyses.
        - Strict adherence to security policies and compliance standards, with thorough vetting of device health and security posture before granting access.

## Applications and Workloads

## Data

## Infrastructure

## Networks