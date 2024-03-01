# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Devices and Workstations

### Endpoints are registered with a cloud identity providers

#### Register corporate devices with Microsoft Entra ID
  - Are corporate devices joined to or registerd with Microsoft Entra ID via Microsoft Entra join or Microsoft Entra Hybrid join?
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
    - **Indicators:**
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
  - Is Windows Updates for Business configured and enabled for automated update management?
    - **Legacy:** Windows devices are managed through on-premises update management solutions, or updates are applied manually, without leveraging the automation and cloud-based features of Windows Updates for Business. This approach reflects traditional update practices, which may not provide the agility and security benefits of modern, automated update management systems. The reliance on legacy methods can lead to inconsistent update deployments, increased administrative overhead, and potential security vulnerabilities due to delayed patching.
      - **Indicators:**
        - Absence of a structured and automated approach to managing Windows updates, leading to potential delays in critical security patching.
        - Increased risk exposure due to the reliance on manual intervention for updates, resulting in potential inconsistencies and overlooked updates.
        - Lack of assurance that all devices are operating on the latest software versions, increasing the organizational risk profile.

    - **Initial:** Initial steps are taken to configure Windows Updates for Business for some devices, introducing a basic level of automated update management. This phase marks the beginning of a shift towards more consistent and reliable update practices, though not yet fully comprehensive across the device fleet.
      - **Indicators:**
        - A portion of the device fleet is enrolled in Windows Updates for Business, starting the transition towards automated update management.
        - Despite these initial configurations, comprehensive coverage and the full utilization of Windows Updates for Business capabilities are not yet achieved.
        - Some improvement in update consistency and security posture, with automated updates beginning to reduce the window of vulnerability.

    - **Advanced:** A significant number of devices are configured with Windows Updates for Business, significantly enhancing the organization's approach to update management. This advanced tier indicates a mature update strategy, with increased automation and consistency in applying updates across the device fleet.
      - **Indicators:**
        - Broad adoption of Windows Updates for Business across the device fleet, leading to more consistent application of updates.
        - Enhanced control over the update process, with the ability to schedule updates and manage bandwidth, improving operational efficiency.
        - Noticeable reduction in the risks associated with outdated software, through improved compliance with security updates and patches.

    - **Optimal:** Windows Updates for Business is fully configured and enabled across all Windows devices within the organization, achieving the highest level of automated update management. This optimal scenario ensures that every device consistently receives updates as soon as they are available, minimizing the risk of security vulnerabilities and maximizing operational efficiency.
      - **Indicators:**
        - Universal configuration and utilization of Windows Updates for Business, ensuring all devices receive timely and consistent updates.
        - Strategic management of the update process, with advanced features like update deferral and bandwidth optimization fully leveraged to suit organizational needs.
        - Comprehensive mitigation of risks associated with outdated software, through a proactive and automated update management strategy that ensures the highest levels of security and compliance.

#### Ensure devices are encrypted
  - Are Windows 10 and later devices encrypted with BitLocker and MacOS devices encrypted with FileVault?
    - Legacy: Devices operate without full-disk encryption, relying on either no encryption or partial, inconsistent encryption practices. This approach leaves sensitive data vulnerable to unauthorized access, especially in the event of device loss or theft. Windows devices are not utilizing BitLocker, and MacOS devices are not taking advantage of FileVault, reflecting a significant gap in data protection measures.
      - Indicators
        - Absence of a standardized approach to device encryption, with many devices left unprotected or inconsistently secured.
        - Increased risk of data breaches and non-compliance with data protection regulations due to the lack of effective encryption on Windows and MacOS devices.
        - Operational challenges in managing data protection, with potential gaps in securing sensitive information across the device fleet.

    - Initial: Initial steps are taken to implement BitLocker encryption on Windows 10 and later devices and FileVault encryption on MacOS devices for a subset of the device fleet. This phase marks the beginning of adopting encryption standards, though not yet fully comprehensive or consistently applied across all devices.
      - Indicators:
        - A portion of the device fleet is encrypted with BitLocker for Windows devices and FileVault for MacOS devices, establishing a basic level of data protection.
        - Despite these initial steps, a comprehensive encryption strategy covering all devices and data is not yet in place, limiting the overall effectiveness of data protection measures.
        - Some improvement in the security posture related to data protection, with initial efforts reducing the risk of unauthorized data access on encrypted devices.

    - Advanced: A significant number of Windows and MacOS devices are encrypted with BitLocker and FileVault, respectively, enhancing the organization's data protection capabilities. This advanced tier reflects a more mature approach to encryption, with the majority of devices secured and policies more consistently applied, though some areas may still require attention for full coverage.
      - Indicators:
        - Broad implementation of BitLocker and FileVault encryption across the device fleet, significantly improving data protection.
        - Enhanced management of encryption keys and recovery information, ensuring that encrypted devices remain accessible to authorized users while securing data from unauthorized access.
        - Noticeable reduction in the potential impact of data breaches, with most sensitive data protected by strong encryption methods.

    - Optimal: BitLocker and FileVault are fully deployed and actively managed across all Windows 10 and later devices and MacOS devices, respectively, achieving the highest level of data protection through encryption. This optimal scenario ensures comprehensive coverage, with all devices encrypted and encryption policies consistently enforced, minimizing the risk of unauthorized data access and supporting compliance with data protection standards.
      - Indicators:
        - Universal deployment of BitLocker and FileVault encryption, ensuring that every device is protected by full-disk encryption without exceptions.
        - Strategic and effective management of encryption policies, keys, and recovery mechanisms, facilitating both security and operational efficiency.
        - Comprehensive mitigation of risks associated with data exposure, through proactive and uniform encryption practices that secure sensitive data across all Windows and MacOS devices.


#### Create application protection policies to protect corporate data at the app-level
  - Are application protection policies leveraged to protect corporate data at the app-level with Intune?
    - Legacy: Corporate data is accessed and handled by applications without specific application protection policies in place. This approach signifies a fundamental gap in data security, leaving sensitive information exposed to potential leaks and unauthorized access due to the lack of app-level controls. Organizations might rely on generic or platform-level security measures that do not fully address the unique risks associated with specific applications.
      - Indicators
        - Absence of targeted application protection policies, resulting in inconsistent security measures across different apps.
        - Increased vulnerability to data leaks and breaches due to the lack of app-specific security controls and encryption.
        - Challenges in enforcing data protection standards across applications, leading to potential non-compliance and security risks.

    - Initial: Initial efforts to implement application protection policies are underway, focusing on essential apps that access corporate data. This stage marks the beginning of a more focused approach to app-level data protection, though comprehensive coverage and advanced policy configurations may still be in development.
      - Indicators:
        - Partial deployment of application protection policies, primarily targeting high-priority apps.
        - Basic configurations of app-level data protection measures, such as data encryption and access controls, are in place, offering a foundational level of security.
        - Some improvement in controlling data access and preventing unauthorized data sharing, though a fully integrated app protection strategy is not yet realized.

    - Advanced: A broad range of applications are covered by comprehensive application protection policies, significantly enhancing data security at the app level. This advanced tier reflects a mature approach to app-level security, with detailed policy configurations tailored to the specific risks and requirements of different applications.
      - Indicators:
        - Widespread implementation of application protection policies, encompassing a diverse set of apps that access or manage corporate data.
        - Enhanced app-level security measures, including advanced encryption, access management, and conditional use policies, are systematically applied.\
        - Notable reduction in the risk of data breaches and unauthorized access, supported by robust app-level controls and monitoring of data handling practices.

    - Optimal: Application protection policies are comprehensively deployed and meticulously managed across all relevant applications, ensuring the highest level of data protection at the app level. This optimal scenario guarantees that corporate data is consistently secured across all applications, with dynamic policies that adapt to evolving security threats and business needs.
      - Indicators:
        - Universal and strategic deployment of application protection policies, ensuring that every app handling corporate data is governed by robust security controls.
        - Strategic management of app-level policies, with adaptive measures that respond to new threats and incorporate best practices for data security.
        - Comprehensive mitigation of app-related data security risks, through proactive and uniform application of protection measures, enhancing the overall security posture and compliance.

  - Products and features covered:
    - Microsoft Intune
      - Windows Autopatch
      - Application Protection Policies (APP)
    - BitLocker
    - FileVault
### Endpoint threat detection is used to monitor device risk

#### Route endpoint logs and transactions to Microsoft Sentinel
  - Are endpoint logs and transactions routed to Microsoft Sentinel?
    - Legacy: Endpoint logs and transactions are not systematically collected or analyzed. In this stage, organizations might rely on disparate or manual log review processes, if any, which significantly limits visibility into security events and potential threats. The lack of integration with centralized security information and event management (SIEM) solutions like Microsoft Sentinel results in missed opportunities for proactive threat detection and response.
      - Indicators
        - Absence of a centralized approach for collecting and analyzing endpoint logs and transactions.
        - Limited ability to detect or respond to security incidents promptly due to the lack of comprehensive log data analysis.
        - Increased risk of undetected security breaches and insufficient insights into endpoint security posture.

    - Initial: Initial efforts to route endpoint logs and transactions to a SIEM solution are underway, with some endpoint data being collected and analyzed. This stage marks the beginning of leveraging tools like Microsoft Sentinel for enhanced security monitoring, though comprehensive log coverage and advanced analytics capabilities may still be in development.
      - Indicators:
        - Partial integration of endpoint logs and transactions with Microsoft Sentinel, covering key systems or areas of concern.
        - Basic log analysis capabilities are utilized, providing foundational insights into security events and potential vulnerabilities.
        - Some improvement in the organization's ability to detect and respond to incidents, though a fully optimized SIEM deployment is not yet achieved.

    - Advanced: A significant portion of endpoint logs and transactions are systematically routed to Microsoft Sentinel, enabling more comprehensive security monitoring and analysis. This advanced tier reflects a mature approach to log management, with enhanced analytics capabilities that support proactive threat detection, incident response, and security posture assessment.
      - Indicators:
        - Broad integration of endpoint logs and transactions with Microsoft Sentinel, facilitating a holistic view of the security landscape.
        - Advanced use of analytics and threat detection capabilities within Microsoft Sentinel, enabling more effective identification of suspicious activities and potential threats.
        - Significant improvements in the timeliness and effectiveness of security incident response, supported by detailed log insights and automated alerting mechanisms.

    - Optimal: Endpoint logs and transactions from across the entire organization are fully integrated with Microsoft Sentinel, achieving the highest level of security monitoring and analytics. This optimal scenario ensures comprehensive visibility into endpoint activities, leveraging the full capabilities of Microsoft Sentinel for advanced threat detection, incident response, and security posture enhancement.
      - Indicators:
        - Universal and strategic routing of all endpoint logs and transactions to Microsoft Sentinel, ensuring no gaps in log coverage.
        - Full exploitation of Microsoft Sentinel's advanced analytics, threat detection, and automated response capabilities, optimizing the organization's security operations.
        - Proactive and efficient management of security threats and incidents, underpinned by comprehensive log data analysis and real-time monitoring, significantly enhancing the organization's overall security posture.

### Access control is gated on endpoint risk for both corporate devices and BYOD

#### Corporate Windows devices are enrolled with a cloud enrollment service such as DEP, Android Enterprise, or Windows AutoPilot
  - Are corporate Windows devices enrolled with the Windows Autopilot cloud enrollment service?
    - Legacy: Corporate Windows devices are set up and managed manually, without the use of cloud enrollment services like Windows Autopilot. This traditional approach involves significant manual effort for device setup, configuration, and ongoing management, leading to increased operational costs and potential inconsistencies in device provisioning and security configurations.
      - Indicators:
        - Absence of cloud-based enrollment and management for Windows devices, relying instead on manual processes.
        - Increased resource expenditure on device setup and management, with potential for configuration errors and inconsistencies.
        - Limited scalability and efficiency in deploying and managing corporate devices, impacting the organization's agility and security posture.

    - Initial: Initial steps have been taken to enroll some corporate Windows devices with Windows Autopilot, beginning the transition towards automated cloud-based device management. This stage marks the initial adoption of cloud enrollment services, though comprehensive enrollment of all devices and full utilization of Autopilot's capabilities may still be in progress.
      - Indicators:
        - Partial enrollment of corporate Windows devices in Windows Autopilot, focusing on a select group of devices or pilot deployment.
        - Initial reduction in manual setup and configuration efforts for enrolled devices, though not yet fully realized across the entire device fleet.
        - Some improvements in device deployment efficiency and consistency, but with room for further enhancement and broader adoption of cloud enrollment services.

    - Advanced: A significant number of corporate Windows devices are enrolled in Windows Autopilot, significantly improving the efficiency and consistency of device management. This advanced tier indicates a mature approach to device deployment, with the majority of devices benefiting from automated provisioning, configuration, and management through Windows Autopilot.
      - Indicators:
        - Broad adoption of Windows Autopilot for corporate Windows devices, streamlining the deployment and management process.
        - Enhanced operational efficiency and consistency in device provisioning, with reduced manual intervention and lower risk of configuration errors.
        - Improved scalability and security posture through the standardized deployment and management of devices, leveraging cloud-based services for optimal device readiness and compliance.

    - Optimal: All corporate Windows devices are fully enrolled and managed through Windows Autopilot, achieving the highest level of automation, efficiency, and security in device deployment and management. This optimal scenario ensures comprehensive and consistent application of configurations, policies, and security settings across the entire device fleet, facilitated by the advanced capabilities of cloud enrollment services.
      - Indicators:
        - Universal enrollment of corporate Windows devices in Windows Autopilot, eliminating manual setup and management processes.
        - Full realization of operational efficiencies, scalability, and security enhancements offered by automated cloud-based device management.
        - Strategic and proactive management of the device lifecycle, from deployment to retirement, supported by comprehensive insights and controls provided by Windows Autopilot, ensuring a robust and agile IT infrastructure.

  - **Are corporate iOS and iPadOS devices enrolled with the Apple Device Enrollment Program (DEP) cloud enrollment service?**
    - Legacy: Corporate iOS and iPadOS devices are configured and managed manually, bypassing the automation and security benefits provided by cloud enrollment services like the Apple Device Enrollment Program (DEP). This manual approach to device provisioning leads to increased operational burdens and potential inconsistencies in security and configuration settings across devices.
      - Indicators:
        - Absence of automated cloud-based enrollment and management for iOS and iPadOS devices, with a reliance on time-consuming manual processes.
        - Increased resources and time spent on manual device setup, configuration, and management, leading to inefficiencies and potential for configuration disparities.
        - Limited ability to enforce standardized security policies and configurations across all corporate iOS and iPadOS devices, affecting the organization's overall security posture.

    - **Initial:** Initial steps have been taken to enroll some corporate iOS and iPadOS devices with the Apple Device Enrollment Program (DEP), initiating the shift towards automated and secure device management. This phase indicates the beginning of adopting cloud enrollment services, though not all devices may be enrolled, and the full suite of DEP features may not yet be leveraged.
      - Indicators:
        - Partial enrollment of corporate iOS and iPadOS devices in DEP, targeting a select subset of devices or conducting a pilot program.
        - Initial reduction in the manual effort required for device provisioning and management for those devices enrolled in DEP.
        - Some improvements in deployment efficiency and consistency for enrolled devices, though broader adoption and optimization of DEP capabilities are needed.

    - **Advanced:** A significant portion of corporate iOS and iPadOS devices are enrolled in the Apple Device Enrollment Program (DEP), markedly improving the deployment and management process. This tier reflects an advanced approach to device management, with the majority of devices enjoying the benefits of automated provisioning and security configurations facilitated by DEP.
      - Indicators:
        - Broad adoption of DEP for corporate iOS and iPadOS devices, streamlining the deployment and ongoing management process.
        - Enhanced operational efficiency in device provisioning, with a significant reduction in manual setup requirements and a uniform application of security policies and configurations.
        - Noticeable improvements in the organization's ability to manage and secure its mobile device fleet, leveraging DEP for better control over devices and ensuring compliance with corporate standards.

    - **Optimal:** All corporate iOS and iPadOS devices are fully enrolled and managed through the Apple Device Enrollment Program (DEP), achieving the highest level of automation, efficiency, and security in mobile device deployment and management. This optimal scenario ensures that every device is automatically provisioned with the necessary configurations, policies, and security settings right from the start, minimizing operational burdens and maximizing device and data security.
      - Indicators:
        - Universal and strategic enrollment of corporate iOS and iPadOS devices in DEP, eliminating the need for manual device setup and management.
        - Full realization of the benefits offered by DEP, including operational efficiencies, enhanced security posture, and standardized device configurations across the entire mobile device fleet.
        - Proactive and comprehensive management of the mobile device lifecycle, supported by DEP's advanced features, ensuring devices are always ready for business use while maintaining high security and compliance standards.

  - **Are corporate Android devices enrolled with the Android Enterprise cloud enrollment service?**
    - **Legacy:** Corporate Android devices are set up and managed manually, foregoing the benefits of automated enrollment and management offered by cloud services like Android Enterprise. This traditional method results in increased administrative effort, potential inconsistencies in device configurations, and gaps in security policy enforcement across the fleet.
      - Indicators:
        - A reliance on manual processes for the setup, configuration, and ongoing management of Android devices, leading to operational inefficiencies.
        - Increased risk of configuration errors and security policy discrepancies due to the absence of standardized, automated deployment processes.
        - Challenges in ensuring all corporate Android devices are consistently secured and compliant with organizational policies, impacting the overall security posture.

    - Initial: Initial efforts to enroll corporate Android devices with Android Enterprise are in progress, marking the beginning of the transition to automated cloud-based device management. While this phase indicates adoption of cloud enrollment services, comprehensive coverage of all devices and full utilization of Android Enterprise's management capabilities may still be developing.
      - Indicators:
        - Partial enrollment of corporate Android devices in Android Enterprise, possibly focusing on a subset of the device fleet or conducting a pilot program.
        - Initial reduction in manual device management tasks for enrolled devices, though broader adoption and deeper integration with Android Enterprise features are needed.
        - Some improvement in the consistency and security of device configurations, but with further work required to achieve full device fleet management and policy compliance.

    - Advanced: A significant number of corporate Android devices are enrolled in Android Enterprise, significantly enhancing the efficiency, consistency, and security of device management. This advanced tier reflects a mature approach to device management, with the majority of devices benefitting from automated provisioning and comprehensive policy enforcement.
      - Indicators:
        - Broad adoption of Android Enterprise for corporate Android devices, streamlining the deployment and ongoing management process.
        - Enhanced operational efficiency and security through automated device provisioning, uniform policy application, and advanced management capabilities provided by Android Enterprise.
        - Noticeable improvements in the organization's ability to secure and manage its Android device fleet, with increased control over device configurations and compliance with corporate standards.

    - Optimal: All corporate Android devices are fully enrolled and managed through Android Enterprise, achieving the highest level of automation, efficiency, and security in mobile device deployment and management. This optimal scenario ensures comprehensive and consistent application of configurations, policies, and security settings across the entire Android device fleet, facilitated by the advanced capabilities of cloud enrollment services.
      - Indicators:
        - Universal and strategic enrollment of corporate Android devices in Android Enterprise, eliminating manual setup and management processes.
        - Full realization of operational efficiencies, security enhancements, and compliance benefits offered by automated cloud-based device management.
        - Proactive and comprehensive management of the Android device lifecycle, from deployment to retirement, supported by comprehensive insights and controls provided by Android Enterprise, ensuring a robust and agile IT infrastructure.

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