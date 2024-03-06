# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Applications and Workloads

### Gain visibility into the activities and data in your applications by connecting them via APIs
#### Adopt SaaS Security Posture Management - SSPM (Microsoft Defender for Cloud)
  - Is Microsoft Defender for Cloud Apps adopted to work with services for optimizing visibility, governance actions, and usage?
    - Legacy: Applications and services operate without the integration of Microsoft Defender for Cloud Apps, leading to a lack of comprehensive visibility into app-related activities, potential governance gaps, and suboptimal usage optimization. Organizations might rely on disparate, non-integrated security solutions or manual monitoring methods, which can result in oversight gaps and increased security risks.
      - Indicators:
        - Absence of centralized monitoring and governance for applications, leading to potential blind spots in app activity and data security.
        - Increased risk of non-compliance and inefficient app usage due to the lack of integrated visibility and control mechanisms.
        - Challenges in detecting and responding to security threats within applications, impacting the overall security posture and data protection efforts.

    - Initial: Initial steps have been taken to adopt Microsoft Defender for Cloud Apps for a subset of applications and services, starting the process of centralizing visibility and enhancing governance and usage optimization. While this phase indicates the beginning of leveraging Microsoft Defender for Cloud Apps, comprehensive integration across all applications and the full utilization of its capabilities may still be under development.
      - Indicators: 
        - Partial adoption of Microsoft Defender for Cloud Apps, with integration efforts focusing on critical applications or services.
        - Initial improvements in visibility into app activities and data, though a holistic view across all applications is not yet achieved.
        - Some enhancement in governance actions and usage optimization for integrated apps, but with room for expansion and deeper utilization of Microsoft Defender for Cloud Apps features.

    - Advanced: A significant number of applications and services are integrated with Microsoft Defender for Cloud Apps, markedly improving visibility, governance, and usage optimization. This advanced tier reflects a mature approach to application security management, with comprehensive monitoring and control mechanisms in place, though some areas may still require attention for full capability utilization.
      - Indicators: 
        - Broad integration of applications and services with Microsoft Defender for Cloud Apps, facilitating enhanced visibility and governance.
        - Advanced utilization of governance actions and usage optimization features, contributing to more effective and efficient application security management.
        - Significant reduction in security risks and governance gaps, supported by detailed insights into application activities and optimized app usage practices.

    - Optimal: Microsoft Defender for Cloud Apps is fully adopted and integrated across all applications and services, achieving the highest level of application security management, visibility, and governance. This optimal scenario ensures comprehensive monitoring and control over application activities, data security, and usage optimization, leveraging the full suite of capabilities offered by Microsoft Defender for Cloud Apps.
      - Indicators: 
        - Universal and strategic adoption of Microsoft Defender for Cloud Apps across the entire application landscape, ensuring no gaps in visibility or governance.
        - Full realization of the benefits provided by Microsoft Defender for Cloud Apps, including operational efficiencies, enhanced security posture, and optimized application usage.
        - Proactive and comprehensive management of application-related security and governance, underpinned by deep insights and advanced control mechanisms, significantly enhancing the organization's security posture and operational effectiveness.

### Discover and control the use of shadow IT
#### Discover SaaS applications (Microsoft Defender for Cloud Apps Cloud Discovery)
  - Is Cloud Discovery within Microsoft Defender for Cloud Apps implemented to identify shadow IT by integrating with Microsoft Defender for Endpoint, deploying the Microsoft Defender for Cloud Apps log collector, or integrating Defender for Cloud Apps with a proxy?
    - Legacy: The organization has not implemented Cloud Discovery within Microsoft Defender for Cloud Apps, nor integrated it with Microsoft Defender for Endpoint, deployed the log collector, or integrated it with a proxy. This absence of implementation results in minimal visibility into shadow IT, posing potential security risks and compliance issues due to unmonitored and uncontrolled cloud application usage.
      - Indicators: 
        - An absence of Cloud Discovery implementation, leading to insufficient insight into unauthorized cloud application usage across the network.
        - Increased exposure to security vulnerabilities and compliance violations due to the lack of monitoring and governance over shadow IT.
        - Operational challenges in managing cloud application security and compliance, impacting the organization's ability to enforce its security policies effectively.

    - Initial: The organization has taken initial steps to implement Cloud Discovery within Microsoft Defender for Cloud Apps by integrating with Microsoft Defender for Endpoint, deploying the log collector, or integrating with a proxy for some segments of the network. This phase marks the beginning of enhanced shadow IT visibility, though comprehensive coverage and full utilization of Cloud Discovery capabilities may still be in development.
      - Indicators: 
        - Partial implementation of Cloud Discovery, with efforts focusing on integrating with Microsoft Defender for Endpoint, deploying the log collector, or proxy integration for critical network segments or user groups.
        - Initial improvements in detecting and assessing the risk of shadow IT, though a complete, network-wide visibility is not yet achieved.
        - Some enhancement in the organization's ability to govern and control unauthorized cloud application usage, but with further work required for comprehensive shadow IT discovery and risk management.

    - Advanced: Cloud Discovery within Microsoft Defender for Cloud Apps is extensively implemented across a significant portion of the network by integrating with Microsoft Defender for Endpoint, deploying the log collector, or integrating with proxies. This advanced tier reflects a mature approach to shadow IT discovery and control, with comprehensive monitoring mechanisms in place.
      - Indicators: 
        - Broad adoption of Cloud Discovery implementation strategies, facilitating extensive visibility into and control over unauthorized cloud application usage.
        - Enhanced capability to identify, assess, and mitigate risks associated with shadow IT, contributing to a stronger security and compliance posture.
        - A noticeable reduction in security and compliance risks associated with unauthorized cloud apps, supported by detailed insights and effective governance actions based on Cloud Discovery data.

    - Optimal: Cloud Discovery within Microsoft Defender for Cloud Apps is fully implemented and operationalized across the entire network, achieving the highest level of shadow IT discovery and control. This optimal scenario ensures comprehensive monitoring of unauthorized cloud services, enabling proactive risk management, compliance enforcement, and strategic decision-making based on extensive shadow IT insights.
      - Indicators: 
        - Universal and strategic implementation of Cloud Discovery, ensuring no gaps in shadow IT visibility across the network.
        - Full realization of the benefits provided by comprehensive Cloud Discovery, including operational efficiencies, enhanced security posture, and informed governance of unauthorized cloud application usage.
        - Proactive and comprehensive management of shadow IT, underpinned by robust analytics, automated response mechanisms, and a unified policy framework, significantly enhancing the organization's ability to detect, assess, and control shadow IT activities effectively.

### Protect sensitive information and activities automatically by implementing policies
#### Implement data protection policies with SSPM (Microsoft Defender for Cloud Apps policies)
  - Are Microsoft Defender for Cloud Apps policies implemented to automatically protect sensitive information and user activities in the cloud?
    - Legacy: The organization has not implemented Microsoft Defender for Cloud Apps policies, resulting in a lack of automated protection mechanisms for sensitive information and cloud-based user activities. This absence leaves sensitive data exposed to potential threats and unauthorized access, due to manual or non-existent data protection and activity monitoring processes.
      - Indicators: 
        - An absence of policy implementation within Microsoft Defender for Cloud Apps, leading to insufficient protection of sensitive information.
        - Increased risk of data breaches and unauthorized activities due to the lack of automated monitoring and protection mechanisms.
        - Operational inefficiencies in safeguarding sensitive data and monitoring user activities, impacting the organization's overall security strategy and compliance posture.

    - Initial: Initial efforts have been made to implement Microsoft Defender for Cloud Apps policies for protecting sensitive information and monitoring user activities in the cloud, marking the beginning of an automated data protection strategy. While this phase indicates the start of policy implementation, comprehensive coverage of all sensitive data and activities and full utilization of policy capabilities may still be under development.
      - Indicators: 
        - Partial implementation of policies within Microsoft Defender for Cloud Apps, focusing on critical data and high-risk user activities.
        - Initial improvements in the automated protection of sensitive information and monitoring of user activities, though a complete, organization-wide policy enforcement is not yet achieved.
        - Some enhancement in the organization's ability to protect sensitive data and control cloud-based activities, but with further work required for full policy coverage and optimization.

    - Advanced: A significant number of Microsoft Defender for Cloud Apps policies are implemented, significantly improving the automated protection of sensitive information and monitoring of user activities in the cloud. This advanced tier reflects a mature approach to data protection and activity monitoring, with comprehensive policy enforcement mechanisms in place.
      - Indicators: 
        - Broad adoption of policy implementation within Microsoft Defender for Cloud Apps, enabling extensive protection of sensitive information and robust monitoring of user activities.
        - Enhanced capability to automatically detect, alert, and remediate potential threats to sensitive data and unauthorized user activities, contributing to a stronger security and compliance posture.
        - A noticeable reduction in risks associated with data breaches and unauthorized access, supported by detailed insights and effective automated governance actions based on policy enforcement.

    - Optimal: Microsoft Defender for Cloud Apps policies are fully implemented and operationalized across the organization, achieving the highest level of automated protection for sensitive information and user activities in the cloud. This optimal scenario ensures comprehensive coverage, enabling proactive data protection, compliance enforcement, and strategic decision-making based on extensive monitoring and policy insights.
      - Indicators: 
        - Universal and strategic implementation of policies within Microsoft Defender for Cloud Apps, ensuring no gaps in the protection of sensitive data and monitoring of user activities.
        - Full realization of the benefits provided by comprehensive policy enforcement, including operational efficiencies, enhanced security posture, and compliance with data protection regulations.
        - Proactive and comprehensive management of sensitive information and cloud-based user activities, underpinned by robust analytics, automated response mechanisms, and a unified policy framework, significantly enhancing the organization's ability to protect and monitor its cloud environment effectively.

#### Refine data protection policies with SSPM (Microsoft Defender for Cloud Apps policies)
  - Are Anomaly Detection Policies tuned and scoped according to business need in Microsoft Defender for Cloud Apps?
    - Legacy: The organization has not customized or effectively implemented Anomaly Detection Policies within Microsoft Defender for Cloud Apps, leading to a generic approach to threat detection that may not align with specific business needs or risk profiles. This lack of tailored anomaly detection results in missed opportunities for early identification of sophisticated threats and potentially increases the risk of false positives.
      - Indicators: 
        - Absence of tuned Anomaly Detection Policies, resulting in a one-size-fits-all approach that may not effectively address specific organizational risks.
        - Increased potential for overlooking genuine threats or encountering high rates of false positives due to the lack of policy customization.
        - Challenges in responding to and mitigating cyber threats in a timely and effective manner, impacting the organization's overall security resilience.

    - Initial: Initial efforts have been made to tune and scope Anomaly Detection Policies within Microsoft Defender for Cloud Apps according to business needs, marking the beginning of a more targeted threat detection strategy. While this phase indicates the start of policy customization, comprehensive coverage and full optimization of anomaly detection capabilities may still be under development.
      - Indicators: 
        - Partial customization of Anomaly Detection Policies, with efforts focusing on high-priority areas or specific threat vectors identified as significant risks.
        - Initial improvements in the accuracy of threat detection and reduction in false positives, though a complete, organization-wide tuning of policies is not yet achieved.
        - Some enhancement in the organization's ability to detect and respond to anomalies, but further work required for full alignment of detection policies with business needs and risk profile.

    - Advanced: Anomaly Detection Policies within Microsoft Defender for Cloud Apps are extensively tuned and scoped, significantly improving the organization's capability to detect and respond to cyber threats and rogue apps in alignment with business needs. This advanced tier reflects a mature approach to anomaly detection, with policies carefully customized to maximize threat detection accuracy and minimize false positives.
      - Indicators: 
        - Broad customization and application of Anomaly Detection Policies, enabling precise threat detection tailored to the organization's unique risk factors and business requirements.
        - Enhanced capability to quickly identify and mitigate genuine threats with minimal false positives, contributing to a stronger security posture and more efficient incident response.
        - A noticeable reduction in the impact of cyber threats and rogue apps, supported by detailed insights and effective, business-aligned anomaly detection policies.

    - Optimal: Anomaly Detection Policies within Microsoft Defender for Cloud Apps are fully customized, implemented, and operationalized across the organization, achieving the highest level of threat detection and response tailored to specific business needs. This optimal scenario ensures comprehensive and accurate identification of anomalies, leveraging the full capabilities of Microsoft Defender for Cloud Apps for dynamic and effective protection against cyber threats and rogue apps.
      - Indicators: 
        - Universal and strategic customization of Anomaly Detection Policies, ensuring comprehensive protection that is fully aligned with the organization's business needs and risk profile.
        - Full realization of the benefits provided by customized anomaly detection, including operational efficiencies, enhanced security posture, and effective mitigation of cyber threats with a high degree of accuracy.
        - Proactive and comprehensive management of cybersecurity threats, underpinned by robust analytics, automated response mechanisms, and a unified, business-need-focused anomaly detection framework, significantly enhancing the organization's resilience against cyber threats and rogue application activities.

### Deploy adaptive access and session controls for all apps
#### Enable real-time monitoring and control over access to any web app
  - Has Microsoft Defender for Cloud Apps Conditional Access App Control been integrate with Microsoft Entra ID Conditional Access for dynamic access and session control?
    - Legacy: The organization does not utilize Conditional Access App Control for its web applications, resulting in a lack of adaptive access and granular session controls. This absence of Conditional Access App Control leaves web apps more vulnerable to unauthorized access and data breaches, as traditional, static access controls may not adequately address the dynamic nature of security threats and user behavior.
      - Indicators: 
        - Absence of Conditional Access App Control implementation, leading to insufficient adaptive security measures for web apps.
        - Increased risk of unauthorized access and potential data compromise due to the lack of dynamic and context-based access controls.
        - Challenges in enforcing compliance and data protection policies across web applications, impacting the organization's overall security and compliance posture.

    - Initial: Initial steps have been made to protect some web applications with Conditional Access App Control, marking the beginning of enhanced security measures. While this phase indicates the start of adopting Conditional Access App Control, comprehensive coverage of all web apps and full utilization of its capabilities may still be under development.
      - Indicators: 
        - Partial deployment of Conditional Access App Control for critical web applications, focusing on high-risk or high-value apps.
        - Initial improvements in adaptive access control and monitoring of user sessions, though a complete, organization-wide enforcement is not yet achieved.
        - Some enhancement in the organization's ability to dynamically control access and protect sensitive data within web apps, but with further work required for full policy coverage and optimization.

    - Advanced: A significant number of web applications are protected with Conditional Access App Control, significantly improving the organization's security posture by enforcing adaptive access and detailed session controls. This advanced tier reflects a mature approach to web application security, with comprehensive Conditional Access policies in place.
      - Indicators: 
        - Broad adoption of Conditional Access App Control, enabling extensive enforcement of adaptive access and session controls across web applications.
        - Enhanced capability to dynamically manage access based on user context, risk assessment, and compliance requirements, contributing to a stronger security and compliance posture.
        - A noticeable reduction in unauthorized access and data breaches, supported by detailed monitoring, real-time decision-making, and effective session management based on Conditional Access policies.

    - Optimal: Conditional Access App Control is fully implemented and operationalized across all web applications, achieving the highest level of security and compliance enforcement. This optimal scenario ensures comprehensive and consistent application of adaptive access and session controls, leveraging the full capabilities of Conditional Access App Control for dynamic and effective web application protection.
      - Indicators: 
        - Universal and strategic implementation of Conditional Access App Control across all web applications, ensuring no gaps in security enforcement.
        - Full realization of the benefits provided by comprehensive Conditional Access policies, including operational efficiencies, enhanced security posture, and compliance with data protection regulations.
        - Proactive and comprehensive management of web app access

