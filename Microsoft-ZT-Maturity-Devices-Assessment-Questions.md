# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Devices and Workstations

### Endpoints are registered with a cloud identity providers

#### Register corporate devices with Microsoft Entra ID
  - Are corporate devices joined to Microsoft Entra ID via Microsoft Entra join or Microsoft Entra Hybrid join?
    - Legacy: Corporate devices are not joined to Microsoft Entra, relying solely on traditional, on-premises domain join methods. This approach neglects the benefits of integrating with cloud services for identity and access management, leaving device authentication and policy enforcement confined to less secure, conventional methods. The absence of Microsoft Entra's advanced security features in device management leaves the network exposed to potential breaches, as it does not leverage cloud identity for verifying device integrity and user access.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Sole reliance on traditional domain join methods, without leveraging Microsoft Entra for device management.
        - Increased security risks due to the absence of cloud identity provider integration for authentication and policy enforcement.
        - Lack of centralized management for devices, leading to inconsistencies in security policies and updates.

    - Initial: Some corporate devices begin to be joined to Microsoft Entra, either through Microsoft Entra Join for direct cloud integration or Microsoft Entra Hybrid Join for mixed environments. However, this integration is not yet comprehensive, covering only a portion of the device fleet. This partial adoption signifies an initial step towards enhancing security but falls short of fully utilizing Microsoft Entra's capabilities to assess and enforce device compliance and security policies. As a result, the system remains vulnerable to unauthorized access due to inconsistent application of cloud-based identity verification and conditional access policies across all devices.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Selective application of Microsoft Entra Join or Microsoft Entra Hybrid Join, indicating the start of cloud integration.'
        - Moderate improvement in device security and management through initial cloud identity integration.
        - Partial alignment with Zero Trust principles, with some devices still not fully managed through Microsoft Entra.

    - Advanced: A significant portion of corporate devices are now joined to Microsoft Entra, utilizing both Microsoft Entra Join and Microsoft Entra Hybrid Join to accommodate different operational needs. This advanced level of integration marks a substantial improvement in security posture, as more devices are managed through cloud-based identity and access controls. However, gaps still exist in ensuring all devices meet the organization's security standards before granting access to resources. While the system has enhanced its defense against unauthorized access by leveraging cloud identity, the absence of universal enforcement of compliance and health checks leaves room for potential security risks.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Broad implementation of Microsoft Entra Join and Microsoft Entra Hybrid Join, achieving a higher level of cloud integration.
        - Significant reduction in security risks through enhanced cloud-based authentication and policy management.
        - Near-universal coverage of devices under Microsoft Entra management, though some exceptions may exist due to legacy constraints.

    - Optimal: All corporate devices are fully integrated with Microsoft Entra, with a strategic application of either Microsoft Entra Join or Microsoft Entra Hybrid Join based on the specific needs of each device and operational scenario. This optimal integration ensures that no device is exempt from strict compliance and security policy enforcement, leveraging Microsoft Entra's full suite of cloud identity and access management capabilities. Every device's health status and compliance are rigorously verified before access to resources is granted, minimizing the risk of unauthorized access and securing the organizational network against potential threats. This comprehensive approach to device management epitomizes the highest standard of security, aligning perfectly with Zero Trust principles by assuming no implicit trust and verifying every access request based on device integrity and user identity.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Universal application of Microsoft Entra Join and Microsoft Entra Hybrid Join across all corporate devices, ensuring no device is left unmanaged.
        - Maximum security and management efficiency, with comprehensive cloud-based control over device access and policies.
        - Complete alignment with Zero Trust security principles, leveraging advanced cloud identity management features to secure and manage corporate devices.

#### Register personal Windows devices with Microsoft Entra ID
  - Are personal Windows devices registered with Microsoft Entra ID?
    - Legacy: Personal Windows devices access corporate resources without being registered with Microsoft Entra ID. This lack of registration indicates minimal security controls, exposing the organization to increased risks of unauthorized access and potential data breaches.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Use of personal devices for corporate data access without the security and policy enforcement that comes with Microsoft Entra ID registration.
        - Heightened security vulnerabilities due to the absence of centralized identity management and device policy application.
        - Lack of visibility into the security posture of personal devices accessing corporate resources, leading to potential unauthorized access.

    - Initial: Initial steps are taken to register personal Windows devices with Microsoft Entra ID, establishing a foundational level of security. This registration process begins to integrate identity verification and applies basic security policies to personal devices.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - An increase in personal devices registered with Microsoft Entra ID, providing a rudimentary layer of security and policy enforcement.
        - Despite registration, a comprehensive device management and security strategy is not fully realized, limiting the depth of security controls.
        - Initial improvement in managing access and applying basic security measures to registered personal devices, enhancing the security landscape.

    - Advanced: A significant number of personal Windows devices are registered with Microsoft Entra ID, enhancing security through better identity verification and the application of more detailed security policies. This advanced tier reflects improved control over personal devices accessing corporate resources.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Widespread registration of personal devices with Microsoft Entra ID, significantly improving the security posture for accessing corporate resources.
        - Enhanced control and monitoring of access from registered personal devices, applying more stringent security policies and compliance checks.
        - Improved application of advanced security measures to registered devices, including conditional access policies and enhanced compliance requirements, elevating the security framework.

    - Optimal: All personal Windows devices interacting with corporate resources are registered with Microsoft Entra ID, achieving the highest level of security control available through registration alone. This optimal scenario ensures comprehensive application of security policies and access controls to all personal devices.
      - Indicators: Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Universal registration of personal Windows devices with Microsoft Entra ID, ensuring comprehensive identity verification and policy enforcement.
        - Full implementation of the most stringent security policies and access controls for registered personal devices, mirroring the security standards of fully managed devices.
        - Strategic and comprehensive application of security measures, including rigorous conditional access policies and compliance enforcement, securing corporate data accessed by personal devices to the fullest extent possible through registration.

#### Enable and configure Windows Hello for Business
  - Is Windows hello for Business enabled and configured for windows devices?
    - Legacy: No utilization of Windows Hello for Business, with organizations relying solely on traditional password-based authentication methods. This approach lacks the security benefits of modern authentication mechanisms, leaving devices more vulnerable to common cyber threats.
      - Indicators: 
        - Absence of biometric, PIN, or security key-based authentication methods.
        - Reliance on passwords without any form of multi-factor authentication.
        - No deployment of Windows Hello for Business across any devices.
 
    - Initial: Initial setup of Windows Hello for Business on a select number of devices, testing the waters with modern authentication methods. This stage involves basic configuration without fully leveraging all the capabilities of Windows Hello for Business.
      - Indicators:
        -  Limited deployment of Windows Hello for Business, possibly in a pilot program or specific departments.
        -  Basic configuration settings, such as enabling PIN or biometric authentication without advanced security features.
        -  Initial reduction in reliance on passwords, with some movement towards stronger authentication mechanisms.

    - Advanced: Comprehensive deployment of Windows Hello for Business, with a significant number of devices using biometric, PIN, or security key authentication. Advanced configurations are applied, including TPM requirements and anti-spoofing measures, but not yet at full capacity.
      - Indicators: 
        - Broad enablement of Windows Hello for Business across the organization's devices.
        - Use of advanced configuration options such as TPM integration, PIN complexity requirements, and anti-spoofing technologies.
        - Enhanced security posture with a significant reduction in password dependency and increased use of multi-factor authentication.

    - Optimal: Full utilization of Windows Hello for Business with all available security features enabled and applied across all devices without exceptions. This optimal state ensures the highest level of security and user experience by leveraging the full spectrum of Windows Hello for Business capabilities, including TPM, biometric authentication, PIN complexity, and anti-spoofing measures.
      - Indicators:
        - Universal deployment of Windows Hello for Business with comprehensive use of all its features.
        - Maximum security with zero reliance on passwords, fully embracing multi-factor and biometric authentication.
        - Comprehensive policy enforcement and management, ensuring consistent application of security settings across all devices, supported by real-time monitoring and response mechanisms for authentication attempts.

### Access is only granted to cloud-managed and compliant endpoints and apps
#### Create a compliance policy with Microsoft Intune (all platforms)
  - Are compliance policies in place for all device platforms with Microsoft Intune?
    - Legacy: No implementation of compliance policies across device platforms using Microsoft Intune, with organizations possibly relying on manual configurations or disparate, non-integrated tools for device management. This approach lacks the centralized control and visibility offered by Intune, making it difficult to ensure devices meet security and compliance standards.
      - Indicators
        - Absence of centralized management and compliance policies across device platforms.
        - Reliance on manual device management processes without cloud-based automation.
        - No use of Microsoft Intune for monitoring device compliance or enforcing security policies.

    - Initial: Initial adoption of Microsoft Intune for creating basic compliance policies across some but not all device platforms. Organizations begin to explore the capabilities of Intune with fundamental policies focusing on simple device health checks and basic security settings.
      - Indicators:
        - Limited deployment of compliance policies in Microsoft Intune, possibly focusing on a single platform or select devices.
        - Basic compliance settings, such as requiring a PIN or password and ensuring devices are not jailbroken or rooted.
        - Initial steps toward centralized device compliance management without extensive use of Intune's advanced features.

    - Advanced: Expanded use of Microsoft Intune to enforce compliance policies across multiple device platforms. Organizations implement more detailed policies, including device health, system security settings, and integration with Microsoft Defender for additional security measures.
      - Indicators:
        - Broader implementation of compliance policies in Microsoft Intune across various device platforms.
        - Use of advanced configuration options in policies, such as device health criteria, minimum or maximum OS versions, and integration with Microsoft Defender Antimalware.
        - Increased security posture with detailed compliance requirements and automated actions for noncompliance.

    - Optimal: Full utilization of Microsoft Intune for comprehensive compliance policy management across all device platforms. This optimal state leverages the entire suite of Intune capabilities, including advanced threat protection, data protection policies, and seamless integration with other Microsoft security tools, to ensure the highest level of device compliance and security.
      - Indicators:
        - Universal deployment of compliance policies in Microsoft Intune, covering all device platforms without exception.
        - Comprehensive use of all Intune features for compliance policy management, including advanced device health checks, system security settings, and data protection policies.
        - Maximum security and compliance posture, supported by real-time monitoring, automated remediation actions for noncompliance, and full integration with the Microsoft security ecosystem.

#### Automate notification email and add additional remediation actions for noncompliant devices in Intune (all platforms)
  - Are automated email notifications and remediation actions configured and enabled for non-compliant devices in Intune?
    - Legacy: No automated processes in place for managing non-compliant devices. Organizations rely solely on manual checks and communications, leading to delayed responses and increased risk of security breaches due to non-compliant devices remaining unaddressed.
      - Indicators
        - Absence of automated email notifications for non-compliance incidents.
        - Manual tracking and remediation of non-compliant devices, leading to inefficiencies and potential oversights.
        - Lack of proactive measures for addressing device compliance, relying on ad-hoc or manual interventions.

    - Initial: Initial setup of automated email notifications for non-compliant devices in Intune. At this stage, automated remediation actions might be limited or not fully utilized, focusing mainly on alerting IT administrators and users about non-compliance without extensive follow-up actions.
      - Indicators:
        - Basic automated email notifications set up to alert on non-compliance, targeting IT administrators or device users.
        - Limited or no automated remediation actions configured, requiring manual follow-up to resolve compliance issues.
        - Initial efforts to improve compliance management, with some reliance on manual processes for remediation.

    - Advanced: Advanced configuration of both automated email notifications and some remediation actions for non-compliant devices in Intune. Organizations at this stage have a more proactive approach, including automated lock or password reset actions for certain types of non-compliance.
      - Indicators:
        - Automated email notifications fully implemented, with detailed information on non-compliance issues and guidance for resolution.
        - Selected automated remediation actions configured, such as device lock or password reset, for specific compliance violations.
        - Improved compliance management efficiency, with a mix of automated and manual remediation strategies based on the severity of the non-compliance.

    - Optimal: Comprehensive utilization of Intune's capabilities for automated email notifications and a full range of remediation actions for non-compliant devices. This tier represents a fully proactive and automated compliance management system, with real-time alerts, detailed guidance for users on self-remediation, and automatic enforcement of compliance policies to secure devices.
      - Indicators:
        - Full deployment of automated email notifications, providing immediate alerts and detailed remediation steps to both IT administrators and end-users.
        - Comprehensive suite of automated remediation actions configured for all types of non-compliance, ensuring immediate response to secure devices.
        - Maximum efficiency in compliance management, with minimal need for manual intervention, supported by detailed reporting and analytics on compliance status and remediation actions.

- **Are automated email notifications and remediation actions configured and enabled for non-compliant devices in Intune?**

  - **Legacy:** Automated processes for managing non-compliant devices are absent. This stage represents a critical vulnerability, as organizations depend entirely on manual efforts for identifying and addressing non-compliance, leading to delayed responses and increased security risks.
    - **Indicators**
      - No automated email notifications for non-compliance, leaving significant gaps in timely communication.
      - Reliance on manual tracking and remediation efforts, introducing inefficiencies and potential for oversight.
      - A complete lack of automated interventions for non-compliant devices, heavily relying on ad-hoc manual processes.

  - **Initial:** Begins with the setup of automated email notifications for non-compliant devices in Intune, marking the first step towards leveraging automation for security compliance. However, comprehensive automated remediation actions are not fully established, emphasizing primarily on notifications.
    - **Indicators:**
      - Implementation of basic automated email alerts for non-compliance, aimed at IT administrators and device users.
      - Minimal or absent automated remediation processes, necessitating manual intervention for compliance resolution.
      - Early efforts in streamlining compliance management, albeit with continued reliance on manual remediation methods.

  - **Advanced:** This stage sees the advanced configuration of automated email notifications alongside the introduction of some automated remediation actions for non-compliant devices in Intune. It indicates a proactive shift towards automation, incorporating actions like automatic device lock or password resets for certain compliance failures.
    - **Indicators:**
      - Comprehensive automated email notifications, delivering detailed non-compliance reports and corrective advice.
      - Implementation of specific automated remediation actions, enhancing the efficiency of compliance management.
      - A balanced approach to managing device compliance, blending automated solutions with manual oversight for complex scenarios.

  - **Optimal:** Represents the fullest integration of Intune's automated email notifications and remediation capabilities for non-compliant devices. At this pinnacle, the system operates with full automation, providing real-time alerts, comprehensive self-remediation guidance for users, and enforcing compliance policies autonomously.
    - **Indicators:**
      - Universal deployment of automated notifications, ensuring immediate and detailed alerts for both IT staff and users.
      - A complete suite of automated remediation actions, allowing for instant response to any form of non-compliance.
      - Peak efficiency in compliance management, virtually eliminating the need for manual intervention, supported by exhaustive reporting and analytics.


### Data loss prevention (DLP) policies are enforced for corporate devices and BYOD

#### Apply recommended security settings
  - Are recommended security settings applied to Windows 10 and later devices to protect corporate data?
    - Legacy: Windows 10 and later devices operate without the application of Microsoft-recommended security settings. This gap indicates a foundational lapse in security practices, leaving the organization vulnerable to threats due to insufficient protection mechanisms.
      - Indicators
        - Deployment of Windows 10 and later devices without the security enhancements provided by recommended settings.
        - Increased exposure to cybersecurity threats due to the lack of essential security configurations and controls.
        - Inadequate oversight over the security configuration of devices, potentially leading to gaps in protection against unauthorized access and data compromise.

    - Initial: Initial efforts are made to configure Windows 10 and later devices with Microsoft-recommended security settings, laying the groundwork for enhanced security. This phase marks the beginning of adopting a structured approach to device security, although not yet fully comprehensive.
      - Indicators:
        - A growing number of devices being configured with recommended security settings, establishing a basic level of protection.
        - Despite these initial steps, a holistic approach to device security and policy enforcement remains underdeveloped, limiting the effectiveness of implemented controls.
        - Some improvement in the security landscape, with registered devices beginning to benefit from enhanced access management and basic security policies.

    - Advanced: A significant portion of Windows 10 and later devices are configured with Microsoft-recommended security settings, advancing the organization's security posture. This tier reflects a more mature approach to security, with an increased focus on comprehensive device policy enforcement and identity verification.
      - Indicators:
        - Widespread application of recommended security settings across Windows devices, markedly improving the organization's defense mechanisms.
        - Enhanced monitoring and control over device access, with the implementation of more sophisticated security policies and compliance requirements.
        - Notable advancements in applying rigorous security measures to devices, including conditional access and more stringent policy applications, strengthening the overall security framework.

    - Optimal: All Windows 10 and later devices in the organization are configured with the full spectrum of Microsoft-recommended security settings, achieving the highest standard of security achievable through configuration alone. This optimal condition ensures that every device adheres to stringent security policies and access controls, mirroring the protection levels of fully managed corporate devices.
      - Indicators:
        - Universal application of recommended security settings across all Windows devices, ensuring robust identity verification and comprehensive policy enforcement.
        - Complete realization of the most advanced security policies and access controls for all devices, aligning with the highest security benchmarks.
        - Strategic enforcement of security measures, incorporating exhaustive conditional access rules and compliance mandates, safeguarding corporate data accessed via Windows devices to the utmost degree permissible through configuration.


#### Ensure updates are deployed automatically to endpoints
  - 
    - Legacy: 
      - Indicators
        - 

    - Initial: 
      - Indicators:
        - 

    - Advanced: 
      - Indicators:
        - 

    - Optimal: 
      - Indicators:
        - 


#### Ensure devices are encrypted
  - 
    - Legacy: 
      - Indicators
        - 

    - Initial: 
      - Indicators:
        - 

    - Advanced: 
      - Indicators:
        - 

    - Optimal: 
      - Indicators:
        - 


#### Create application protection policies to protect corporate data at the app-level
  - 
    - Legacy: 
      - Indicators
        - 

    - Initial: 
      - Indicators:
        - 

    - Advanced: 
      - Indicators:
        - 

    - Optimal: 
      - Indicators:
        - 


### Endpoint threat detection is used to monitor device risk

#### Route endpoint logs and transactions to Microsoft Sentinel
  - 
    - Legacy: 
      - Indicators
        - 

    - Initial: 
      - Indicators:
        - 

    - Advanced: 
      - Indicators:
        - 

    - Optimal: 
      - Indicators:
        - 


### Access control is gated on endpoint risk for both corporate devices and BYOD

#### Corporate devices are enrolled with a cloud enrollment service such as DEP, Android Enterprise, or Windows AutoPilot
  - 
    - Legacy: 
      - Indicators
        - 

    - Initial: 
      - Indicators:
        - 

    - Advanced: 
      - Indicators:
        - 

    - Optimal: 
      - Indicators:
        - 

### Example
  - Is Conditional Access configured in Microsoft Defender for Endpoint to utilize health signals from Windows machines for access decisions?
    - Legacy: There is no Conditional Access configured within Microsoft Defender for Endpoint to utilize health signals from Windows machines, leaving access decisions solely on basic authentication methods. This absence of advanced security measures leaves the system vulnerable to unauthorized access, as it does not consider the health status of devices attempting to access resources.
      - Indicators Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - The absence of Conditional Access policies in Microsoft Defender for Endpoint.
        - No integration or consideration of device health signals when making access decisions.
        - Sole reliance on traditional authentication methods without additional security checks.
    - Initial: Initial steps towards implementing Conditional Access in Microsoft Defender for Endpoint are taken, with basic policies that utilize some health signals from Windows machines for access decisions. While this introduces a fundamental level of security, it's applied in a limited scope, potentially overlooking nuanced threats and sophisticated attack vectors.
      - Indicators Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Initial implementation of Conditional Access policies that may include simple rules based on location or user group but lack comprehensive device health considerations.
        - Some use of health signals from Windows machines in access decisions, but applied selectively and not as part of a broader security strategy.
        - Minimal integration with other security solutions, providing a basic level of threat detection and response.
    - Advanced: Conditional Access policies within Microsoft Defender for Endpoint are further refined, incorporating a wider range of health signals from Windows machines to inform access decisions. This includes integration with other security solutions to enhance detection and response capabilities. However, some scenarios may still rely on default or less stringent policies for certain applications or user groups, leaving marginal vulnerabilities.
      - Indicators Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Advanced Conditional Access policies that utilize a broader range of health signals from Windows machines, including integration with other security solutions for enhanced detection and response.
        - Increased administrative control over Conditional Access policies, including the ability to customize policies based on specific security needs and risk assessments.
        - Use of real-time threat detection and integration with Microsoft Defender for Endpoint for dynamic access decisions based on device health.
    - Optimal: A comprehensive Conditional Access strategy is fully integrated within Microsoft Defender for Endpoint, leveraging all available health signals from Windows machines to make informed and dynamic access decisions. This approach includes real-time threat detection, adaptive access policies, and stringent compliance checks, ensuring that only devices in optimal health status can access organizational resources. This tier exemplifies the highest standard of security and operational efficiency, minimizing the risk of data breaches and unauthorized access through meticulous device health assessment and policy enforcement.
      - Indicators Assessors should evaluate the client environment against these indicators to determine the current tier of implementation and identify areas for improvement towards achieving an optimal security posture.
        - Full integration of Conditional Access within Microsoft Defender for Endpoint, leveraging all available health signals from Windows machines for making informed access decisions.
        - Dynamic and real-time assessment of device health status, with adaptive access policies that respond to the latest threat intelligence and security analyses.
        - Strict adherence to security policies and compliance standards, with thorough vetting of device health and security posture before granting access.


## Applications and Workloads

## Data

## Infrastructure

## Networks