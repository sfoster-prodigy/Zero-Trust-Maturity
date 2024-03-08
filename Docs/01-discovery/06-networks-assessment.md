# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Networks

### Fully distributed ingress/egress cloud micro-perimeters and deeper micro-segmentation
#### Applications are partitioned to different Azure Virtual Networks (VNets) and connected using a hub-spoke model

**Has the organization established a central Azure Virtual Network (VNet) to configure the security posture for inter-application connectivity and interconnected the application VNets in a hub-and-spoke architecture?**

- **Legacy:** The organization does not utilize a hub-and-spoke network architecture in Azure, leading to potentially less efficient and secure inter-application connectivity. This absence of a centralized network configuration model may result in increased complexity and reduced security posture due to decentralized management of network traffic and security policies.
    - Indicators: 
          - Lack of a central VNet for overseeing security and connectivity policies across applications.
          - Increased network complexity and potential security vulnerabilities due to ad hoc connectivity solutions.
          - Challenges in maintaining a consistent security posture and efficient network traffic management across multiple VNets.

- **Initial:** Initial efforts have been made to establish a central Azure VNet as a hub for managing inter-application connectivity, with some application VNets connected in a hub-and-spoke architecture. This phase marks the beginning of adopting centralized network management practices, though comprehensive implementation and optimization across all application VNets may still be under development.
    - Indicators: 
        - Partial deployment of a hub-and-spoke network architecture, focusing on key applications or VNets.
        - Initial improvements in centralizing network security posture and connectivity management, though not fully realized across the entire Azure environment.
        - Some enhancement in network efficiency and security, with ongoing efforts to expand the hub-and-spoke architecture.

- **Advanced:** A comprehensive hub-and-spoke network architecture is broadly implemented, with a central Azure VNet effectively managing inter-application connectivity and security across multiple application VNets. This advanced tier reflects a mature approach to network management, ensuring efficient and secure network configurations.
    - Indicators: 
        - Broad adoption of the hub-and-spoke architecture, with a central VNet serving as the hub for multiple application VNets.
        - Enhanced network security and efficiency, supported by centralized management of connectivity and security policies.
        - Significant progress toward simplifying network architecture and improving the security posture through consistent policy application.

- **Optimal:** The hub-and-spoke network architecture, centered around a central Azure VNet, is fully developed, operationalized, and integrated into the organization's overall network strategy. This optimal scenario ensures the highest level of efficiency, security, and manageability for inter-application connectivity across the Azure environment.
    - Indicators: 
        - Strategic and universal application of the hub-and-spoke architecture, with all relevant application VNets connected to a central hub VNet.
        - Comprehensive management of network security and connectivity, enhancing organizational agility and security resilience.
        - Full alignment with network management best practices and compliance requirements, underpinned by an effective and well-managed network architecture.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SC-7 Boundary Protection: Utilizing Azure Firewall supports boundary protection controls by monitoring and controlling communications at the external and internal boundaries of the network to prevent unauthorized traffic flow.
    - AC-4 Information Flow Enforcement: Azure Firewall aids in enforcing approved authorizations for controlling the flow of information within the system and between interconnected systems, in accordance with information flow policies.
    - SI-4 Information System Monitoring: The firewall's capabilities to inspect and log traffic contribute to information system monitoring requirements, enabling the detection of unauthorized activities and potential cybersecurity threats.
    - SC-5 Denial of Service Protection: Azure Firewall can provide denial of service protection mechanisms that manage and mitigate risks associated with denial of service attacks.

**Has the organization deployed Azure Firewall in the hub VNet to inspect and control traffic flow between the various Virtual Networks (VNets) in accordance with the hub-spoke model?**

- **Legacy:** The organization does not use Azure Firewall in the hub VNet, resulting in potential gaps in centralized traffic inspection and control. This lack of a centralized firewall may lead to insufficient security measures for traffic flowing between VNets, increasing the risk of cyber threats.
    - Indicators: 
          - Lack of Azure Firewall for managing and securing network traffic within the hub-and-spoke architecture.
          - Increased vulnerability to network-based attacks due to the absence of centralized traffic inspection and control mechanisms.
          - Difficulty in enforcing consistent network security policies across interconnected VNets.

- **Initial:** The organization has begun deploying Azure Firewall in the hub VNet for key traffic flows or critical VNets. This phase indicates the start of leveraging Azure Firewall for enhanced network security, though comprehensive traffic control across all spokes may still be under development.
    - Indicators: 
        - Partial deployment of Azure Firewall in the hub VNet, providing some level of traffic inspection and control.
        - Initial steps towards improving network security and traffic management, though not yet fully implemented across the hub-and-spoke model.
        - Ongoing efforts to expand Azure Firewall deployment for comprehensive traffic inspection and control.

- **Advanced:** Azure Firewall is broadly implemented within the hub VNet, significantly improving inspection and control of traffic flow between VNets. This advanced tier reflects a mature approach to network security within the hub-and-spoke architecture, ensuring comprehensive traffic management and threat protection.
    - Indicators: 
        - Comprehensive use of Azure Firewall in the hub VNet, facilitating robust traffic inspection and control across the network architecture.
        - Enhanced security measures in place, supported by the centralized management of traffic flows and security policies.
        - Significant strides in mitigating network-based security risks and ensuring compliance with organizational security requirements.

- **Optimal:** Deployment of Azure Firewall in the hub VNet and its integration within the hub-and-spoke network model are fully operational and integrated into the organization's overall network security strategy. This optimal scenario ensures the highest level of security for inter-VNet traffic, leveraging advanced firewall capabilities for thorough traffic inspection and policy enforcement.
    - Indicators: 
        - Strategic application of Azure Firewall within the hub VNet across all aspects of traffic flow and security within the hub-and-spoke architecture.
        - Comprehensive and proactive management of network traffic and security, enhancing organizational resilience against network-based threats.
        - Full alignment with network security best practices and compliance requirements, supported by an effective and well-managed firewall implementation.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SC-7 Boundary Protection: Azure Firewall supports boundary protection controls by monitoring and controlling communications at the network's external and internal boundaries to prevent unauthorized traffic flow.
    - AC-4 Information Flow Enforcement: The firewall aids in enforcing authorized information flows within the system and between interconnected systems, in accordance with organizational information flow policies.
    - SI-4 Information System Monitoring: Azure Firewall's capabilities to inspect and log traffic contribute to the information system monitoring requirements, enabling the detection of unauthorized activities and potential cybersecurity threats.
    - SC-5 Denial of Service Protection: Azure Firewall can provide denial of service protection mechanisms that manage and mitigate risks associated with denial of service attacks.

**Has the organization partitioned applications into different Azure Virtual Networks (VNets), creating dedicated virtual networks for various applications or application components?**
- **Legacy:** The organization has not adopted network segmentation strategies using Azure Virtual Networks (VNets), leading to a flat network topology that could increase the risk of lateral movement in the event of a compromise. This absence of segmentation may result in less effective isolation of application components, potentially exposing sensitive applications to unnecessary risk.
    - Indicators: 
          - Applications and their components reside within a single or a few large networks without adequate segmentation, increasing potential attack surfaces.
          - Increased risk of internal and external threats due to the lack of effective isolation between different applications or application components.
          - Challenges in managing network traffic and access controls efficiently, impacting the overall security posture and compliance.

- **Initial:** Initial steps have been taken to implement Azure VNets for segmenting critical applications or components. While this phase marks the beginning of adopting network segmentation practices, comprehensive and strategic partitioning across all applications may still be under development.
    - Indicators: 
        - Partial deployment of Azure VNets, focusing on high-priority applications or components that require isolation.
        - Initial improvements in network security and application isolation, though not consistently applied across the entire application portfolio.
        - Some enhancement in the organization's ability to control access and reduce potential attack vectors, with ongoing efforts to expand network segmentation.

- **Advanced:** Azure VNets are broadly implemented across the organization's application landscape, significantly improving the isolation and security of various applications or components. This advanced tier reflects a mature approach to network segmentation, ensuring that applications are partitioned into dedicated virtual networks as appropriate.
    - Indicators: 
        - Comprehensive adoption of Azure VNets for creating dedicated networks for different applications or application components, facilitating effective micro-segmentation.
        - Enhanced security measures in place, supported by the ability to tailor network policies and controls to the needs of each segmented application environment.
        - Significant progress toward minimizing risks associated with network-based attacks and ensuring compliance with security policies through robust network segmentation.

- **Optimal:** The strategic use of Azure VNets for partitioning applications into dedicated virtual networks is fully developed, operationalized, and integrated into the organization’s network security strategy. This optimal scenario ensures the highest level of network isolation and security for applications and their components across the Azure environment.
    - Indicators: 
        - Strategic and universal application of network segmentation practices, employing Azure VNets to partition all relevant applications and components effectively.
        - Comprehensive management of network access and traffic flows, enhancing the security and resilience of application environments.
        - Full alignment with network security best practices and compliance requirements, underpinned by an effective and well-managed network segmentation framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SC-7 Boundary Protection: Utilizing Azure VNets supports the enforcement of boundary protections, controlling the flow of information between networks under different levels of trust and enhancing the security of network perimeters.
    - AC-4 Information Flow Enforcement: Network segmentation through Azure VNets aids in enforcing approved authorizations for controlling the flow of information within the system and between interconnected systems, in accordance with information flow policies.
    - SC-32 Network Segmentation: The strategic implementation of network segmentation using Azure VNets directly supports this control, enhancing security by isolating system components into separate security zones, thereby reducing the risk of unauthorized access to sensitive information.
    - SC-2 Application Partitioning: Partitioning applications into different Azure VNets helps in isolating and protecting individual applications or application components, ensuring that security and functionality are not compromised by interactions between components.

### Machine learning-based threat protection and filtering with context-based signals
#### Leverage Azure Web Application Firewall (WAF) for Comprehensive Protection

**Has the organization implemented cloud-native filtering and protection for known threats by activating Azure Web Application Firewall (WAF) for endpoints with HTTP/S traffic, using the default or OWASP top 10 protection rulesets, enabling bot protection rules, and adding custom rules to guard against specific business-related threats?**

- **Legacy:** The organization has not implemented Azure WAF or similar web application protection measures. This absence of a web application firewall results in increased exposure to common web vulnerabilities and threats, potentially compromising the security of HTTP/S endpoints.
    - Indicators: 
          - Lack of protection against web-based threats and vulnerabilities, including those identified in the OWASP top 10.
          - Increased risk of successful cyber attacks targeting web applications due to the absence of bot protection and custom security rules.
          - Challenges in securing web applications and ensuring compliance with security standards and best practices.

- **Initial:** Initial steps have been taken to deploy Azure WAF for critical web applications, using default protection rulesets. While this phase marks the beginning of web application protection efforts, comprehensive coverage, including the activation of bot protection rules and the implementation of custom rules for specific threats, may still be under development.
    - Indicators: 
        - Partial deployment of Azure WAF, primarily relying on default or OWASP top 10 protection rulesets for key endpoints.
        - Initial improvements in web application security, though advanced protections such as bot management and custom rule configuration are not yet fully utilized.
        - Ongoing efforts to enhance web application protection by expanding the use of Azure WAF features and tailoring security measures to address specific organizational threats.

- **Advanced:** Azure WAF is broadly implemented across the organization's web applications, significantly improving security posture with the use of OWASP top 10 protection rulesets, bot protection rules, and custom rules tailored to specific business-related threats.
    - Indicators: 
        - Comprehensive adoption of Azure WAF, including advanced configurations for bot protection and the development of custom security rules.
        - Enhanced protection against a wide range of web-based threats, supported by a robust configuration of WAF policies and rules.
        - Significant progress in securing web applications against known and emerging threats, bolstered by the strategic application of Azure WAF capabilities.

- **Optimal:** The deployment and configuration of Azure WAF for protecting web applications are fully developed, operationalized, and integrated into the organization’s overall web security strategy. This optimal scenario ensures the highest level of security for HTTP/S endpoints, leveraging Azure WAF's full spectrum of protection features.
    - Indicators: 
        - Strategic and universal application of Azure WAF across all web applications, employing a comprehensive set of protection rules, including custom rulesets.
        - Comprehensive management of web application security, enhancing resilience against cyber threats and aligning with industry best practices.
        - Full compliance with relevant security standards, supported by an effective and well-managed Azure WAF implementation.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SC-7 Boundary Protection: Azure WAF acts as a boundary protection mechanism for web applications, inspecting incoming HTTP/S traffic to prevent unauthorized access and data exfiltration.
    - SI-3 Malicious Code Protection: By employing protection rules, including those based on the OWASP top 10, Azure WAF helps protect web applications from malicious code execution.
    - SC-5 Denial of Service Protection: Azure WAF includes features for bot protection and can mitigate denial of service attacks, supporting the availability of web services.
    - SI-4 Information System Monitoring: The capability of Azure WAF to log and monitor web traffic aids in the detection of unauthorized activities, anomalies, and security events, contributing to comprehensive information system monitoring.

#### Implement Azure Firewall for Layer 4 Threat Intelligence-Based Filtering
**Has the organization implemented Azure Firewall for threat intelligence-based filtering at Layer 4, deploying and configuring it within the hub VNet to inspect and control traffic across all endpoints, regardless of HTTP status, and enabled threat intelligence features for traffic analysis?**

- **Legacy:** The organization has not implemented Azure Firewall or its threat intelligence-based filtering capabilities. This lack of advanced network security measures can result in increased exposure to known threats and reduced capability to respond to emerging cybersecurity challenges effectively.
    - Indicators: 
          - Absence of Azure Firewall deployment for network security and threat intelligence analysis.
          - Increased risk of cyber threats due to the lack of advanced filtering and traffic inspection capabilities.
          - Challenges in achieving a proactive security posture and efficiently managing traffic across network endpoints.

- **Initial:** Initial efforts have been made to deploy Azure Firewall with basic configurations, focusing on fundamental traffic control without fully leveraging threat intelligence-based filtering. While this phase marks the start of enhancing network security, the comprehensive integration of threat intelligence features and optimization for all traffic types may still be under development.
    - Indicators: 
        - Partial implementation of Azure Firewall, with limited use of threat intelligence features for traffic analysis.
        - Initial improvements in network security, though not fully exploiting the capabilities of threat intelligence-based filtering.
        - Some enhancement in the organization's ability to monitor and regulate network traffic, with ongoing efforts to fully enable and configure threat intelligence features.

- **Advanced:** Azure Firewall is broadly implemented and configured for threat intelligence-based filtering at Layer 4 within the hub VNet. This advanced tier reflects a mature approach to network security, ensuring that traffic is inspected and controlled across all endpoints, leveraging threat intelligence for comprehensive traffic analysis.
    - Indicators: 
        - Comprehensive adoption of Azure Firewall with threat intelligence-based filtering enabled, facilitating robust security measures across the network.
        - Enhanced capability to identify and mitigate known threats, supported by the proactive analysis of traffic patterns and threat intelligence.
        - Significant progress toward securing network endpoints against a wide range of cybersecurity threats, bolstered by advanced filtering techniques and threat intelligence insights.

- **Optimal:** The deployment and configuration of Azure Firewall for threat intelligence-based filtering are fully developed, operationalized, and integrated into the organization’s network security strategy. This optimal scenario ensures the highest level of network protection, with advanced threat intelligence capabilities actively monitoring and controlling traffic across all endpoints.
    - Indicators: 
        - Strategic and universal application of Azure Firewall's threat intelligence features, covering traffic analysis and filtering across the entire network.
        - Comprehensive management of network security, enhancing the organization's resilience against known and emerging cyber threats.
        - Full alignment with network security best practices and compliance requirements, underpinned by an effective and well-managed threat intelligence-based filtering framework.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SI-4 Information System Monitoring: Leveraging Azure Firewall's threat intelligence capabilities supports the monitoring of information systems for unauthorized access, use, anomalies, and cybersecurity threats, enhancing system monitoring efforts.
    - SC-7 Boundary Protection: Azure Firewall acts as a boundary protection mechanism, monitoring and controlling communications at the network's external and internal boundaries to prevent unauthorized traffic flow based on threat intelligence.
    - SI-3 Malicious Code Protection: The threat intelligence-based filtering features of Azure Firewall contribute to protecting against malware and other forms of malicious code by analyzing traffic for known threat indicators.
    - RA-5 Vulnerability Scanning: Enabled threat intelligence features aid in identifying vulnerabilities and threats by analyzing network traffic patterns, supporting vulnerability management processes.

#### Enhance security with Azure DDoS protection
**Has the organization enhanced its security posture by activating Azure DDoS Protection Standard to monitor Azure-hosted application traffic, utilize ML-based frameworks for detecting volumetric traffic floods, and implement automatic mitigations, including configuring alerts for DDoS protection metrics?**
- **Legacy:** The organization lacks Azure DDoS Protection Standard or similar DDoS protection measures, leading to potential vulnerabilities to DDoS attacks. This absence of DDoS protection can result in increased risk of service disruption and compromised application availability.
    - Indicators: 
          - No deployment of Azure DDoS Protection Standard or utilization of ML-based detection frameworks for network traffic.
          - Increased susceptibility to volumetric traffic floods, affecting the availability and performance of Azure-hosted applications.
          - Challenges in effectively responding to DDoS attacks, impacting the overall security and operational resilience.

- **Initial:** Initial steps have been made to activate Azure DDoS Protection Standard for critical applications, focusing on basic monitoring and protection capabilities. While this phase marks the beginning of enhancing DDoS defense, comprehensive coverage, including advanced ML-based detection and automated mitigation strategies, may still be under development.
    - Indicators: 
        - Partial implementation of Azure DDoS Protection Standard, with basic monitoring and alerting for potential DDoS events.
        - Initial improvements in DDoS defense, though advanced detection and mitigation capabilities are not yet fully exploited.
        - Some enhancement in the organization’s ability to protect against DDoS attacks, with ongoing efforts to fully leverage Azure DDoS Protection Standard features.

- **Advanced:** Azure DDoS Protection Standard is broadly implemented across the organization's Azure-hosted applications, significantly improving the security posture with ML-based detection of volumetric traffic floods and automatic mitigation measures.
    - Indicators: 
        - Comprehensive adoption of Azure DDoS Protection Standard, including ML-based frameworks for detecting and mitigating DDoS attacks.
        - Enhanced protection against DDoS attacks, supported by automated mitigation actions and configurable alerts for DDoS protection metrics.
        - Significant progress toward ensuring the availability and resilience of Azure-hosted applications against DDoS threats.

- **Optimal:** The deployment and configuration of Azure DDoS Protection Standard for DDoS defense are fully developed, operationalized, and integrated into the organization's overall network security strategy. This optimal scenario ensures the highest level of protection against DDoS attacks, leveraging advanced ML-based detection, automatic mitigations, and comprehensive monitoring.
    - Indicators: 
        - Strategic and universal application of Azure DDoS Protection Standard features across all Azure-hosted applications.
        - Comprehensive and proactive defense against DDoS attacks, enhancing the organization's security posture and application resilience.
        - Full alignment with network security best practices and compliance requirements, underpinned by an effective and well-managed DDoS protection strategy.

- **Relevance to NIST SP 800-53 Revision 5:**
    - SC-5 Denial of Service Protection: Azure DDoS Protection Standard supports the implementation of denial of service protection mechanisms that manage and mitigate risks associated with DDoS attacks, ensuring the availability of networked services.
    - SI-4 Information System Monitoring: The use of ML-based frameworks for detecting DDoS traffic and configuring alerts contributes to the monitoring of information systems for unauthorized access, use, anomalies, and cybersecurity threats, enhancing system monitoring efforts.
    - SC-7 Boundary Protection: Deploying Azure DDoS Protection Standard acts as a boundary protection mechanism, monitoring and controlling communications at the network's external and internal boundaries to prevent unauthorized traffic flows that could lead to DDoS attacks.
    - RA-5 Vulnerability Scanning: While primarily focused on vulnerabilities, Azure DDoS Protection's monitoring and analysis capabilities can aid in identifying potential DDoS vulnerabilities and traffic patterns that may indicate an impending attack, supporting the organization's vulnerability management processes.

### All traffic is encrypted


### Discontinue legacy network security technology
####
****
- **Legacy:** 
    - Indicators: 
          - 

- **Initial:** 
    - Indicators: 
        - 

- **Advanced:** 
    - Indicators: 
        - 

- **Optimal:** 
    - Indicators: 
        - 

- **Relevance to NIST SP 800-53 Revision 5:**
    - 
