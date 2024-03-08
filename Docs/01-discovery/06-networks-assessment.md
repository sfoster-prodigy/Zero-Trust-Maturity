# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Networks

### Fully distributed ingress/egress cloud micro-perimeters and deeper micro-segmentation
#### Applications are partitioned to different Azure Virtual Networks (VNets) and connected using a hub-spoke model

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

####



####

####

### Machine learning-based threat protection and filtering with context-based signals
#### Leverage Azure Web Application Firewall (WAF) for Comprehensive Protection

**Has the organization implemented cloud-native filtering and protection for known threats by activating Azure Web Application Firewall (WAF) for endpoints with HTTP/S traffic, using the default or OWASP top 10 protection rulesets, enabling bot protection rules, and adding custom rules to guard against specific business-related threats?**

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


### All traffic is encrypted
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
