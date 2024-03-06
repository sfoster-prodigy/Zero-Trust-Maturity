# Microsoft Zero Trust Maturity: Determine a clients maturity level.

## Summary

## Microsoft Zero Trust Maturity Level Discovery Questions

Questions in the following sections are designed to help us understand a clients current Zero Trust maturity level following the Microsoft Zero Trust Maturity framework. 

## Infrastructure
### Centralized management of all virtual machines and servers on which workloads are running
#### Multicloud and on-premises governance with Azure Arc
#### Apply security baselines through Azure Policy, including application of in-guest policies
#### Endpoint Protection and Vulnerability Management through Defender XDR
### Workloads are monitored and alerted to abnormal behavior
#### Activate Microsoft Defender for Cloud and its comprehensive protection plans 

**Has the organization enabled Microsoft Defender for Cloud along with its specific protection plans for servers, storage, containers, SQL, and other supported resource types to enhance security measures?**
    - Legacy: The organization has not implemented Microsoft Defender for Cloud or its specific protection plans, leading to potential vulnerabilities in cloud infrastructure and resources. This absence of comprehensive security monitoring and threat protection measures may result in increased risk of cyberattacks and security breaches.
        - Indicators:
            - No deployment of Microsoft Defender for Cloud to monitor and protect servers, storage, containers, SQL, and other resource types.
            - Increased vulnerability to cyber threats due to the lack of advanced security monitoring and response capabilities.
            - Challenges in maintaining a robust security posture for cloud resources, affecting overall cloud infrastructure protection.

    - Initial: Initial steps have been taken to enable Microsoft Defender for Cloud and some of its specific protection plans for critical resources. While this phase marks the beginning of adopting cloud security practices, comprehensive coverage and consistent application of protection plans across all supported resource types may still be under development.
        - Indicators:
            - Partial implementation of Microsoft Defender for Cloud, focusing on high-priority resources such as servers or SQL databases.
            - Initial improvements in security monitoring and threat detection for covered resources, though not fully realized across the entire cloud environment.
            - Some enhancement in the organization's cloud security capabilities, with ongoing efforts to expand and optimize the deployment of Microsoft Defender for Cloud protection plans.

    - Advanced: Microsoft Defender for Cloud and its specific protection plans are widely implemented, significantly improving security measures for servers, storage, containers, SQL, and other supported resource types. This advanced tier reflects a mature approach to cloud security, ensuring comprehensive monitoring, threat detection, and response across the cloud environment.
        - Indicators:
            - Broad adoption of Microsoft Defender for Cloud, with specific protection plans activated for a wide range of resource types.
            - Enhanced security monitoring and proactive threat protection measures in place, supported by consistent and comprehensive coverage.
            - Significant progress toward securing the cloud infrastructure and resources, bolstered by advanced security analytics and threat intelligence.

    - Optimal: Microsoft Defender for Cloud and all its specific protection plans for supported resource types are fully developed, operationalized, and integrated into the organization’s overall cloud security strategy. This optimal scenario ensures the highest level of security monitoring, threat detection, and protection for the cloud environment.
        - Indicators:
            - Universal and strategic implementation of Microsoft Defender for Cloud, covering servers, storage, containers, SQL, and all other supported resources.
            - Comprehensive and consistent application of advanced security measures, enhancing protection against cyber threats across the cloud infrastructure.
            - Full compliance with security standards and regulations, underpinned by an effective and well-managed cloud security monitoring and response system.

    - Relevance to NIST SP 800-53 Revision 5:
        - SI-4 Information System Monitoring: Microsoft Defender for Cloud supports continuous security monitoring of cloud infrastructure and resources, aligning with the control for detecting unauthorized access, use, and anomalies.
        - RA-5 Vulnerability Scanning: The protection plans within Microsoft Defender for Cloud aid in conducting regular vulnerability scans of cloud resources, helping to identify and mitigate potential vulnerabilities in accordance with RA-5 requirements.
        - SC-7 Boundary Protection: Microsoft Defender for Cloud enhances boundary protection controls by monitoring and protecting cloud resources from cyber threats, ensuring secure communications with external networks.
        - IR-4 Incident Handling: The solution supports incident handling processes by providing alerts and actionable insights on detected threats, enabling rapid response and remediation of security incidents in the cloud.

**Has the organization implemented Microsoft Defender for Identity and Advanced Threat Analytics to enable signal collection for the identification, detection, and investigation of advanced threats, compromised identities, and malicious insider actions targeting the organization?**
    - Legacy: The organization has not implemented Microsoft Defender for Identity or Advanced Threat Analytics, leading to potential gaps in the identification and mitigation of advanced threats and compromised identities. This lack of advanced threat detection capabilities increases the risk of undetected security breaches and insider threats.
        - Indicators:
            - Absence of advanced threat detection and identity protection solutions, resulting in limited visibility into security threats.
            - Increased vulnerability to advanced threats, compromised identities, and malicious insider actions due to inadequate monitoring and detection capabilities.
            - Challenges in proactively securing the organization against targeted cyber attacks and insider threats, impacting overall security posture.

    - Initial: Initial efforts have been made to deploy Microsoft Defender for Identity and Advanced Threat Analytics for monitoring specific segments of the IT environment. While this phase marks the beginning of adopting advanced threat detection practices, comprehensive coverage and consistent application of these solutions across the organization may still be under development.
        - Indicators:
            - Partial implementation of Microsoft Defender for Identity and Advanced Threat Analytics, focusing on high-priority areas or specific user groups.
            - Initial improvements in detecting advanced threats and compromised identities, though organization-wide detection capabilities are not yet achieved.
            - Some enhancement in the organization's ability to respond to security incidents, with ongoing efforts to expand and optimize threat detection and identity protection strategies.

    - Advanced: Microsoft Defender for Identity and Advanced Threat Analytics are broadly implemented, significantly improving the organization's capability to detect, investigate, and respond to advanced threats, compromised identities, and insider actions. This advanced tier reflects a mature approach to security monitoring, ensuring comprehensive protection against sophisticated cyber threats.
        - Indicators:
            - Broad adoption of Microsoft Defender for Identity and Advanced Threat Analytics, facilitating comprehensive signal collection and threat detection.
            - Enhanced security measures in place, supported by consistent and effective monitoring of user and entity behaviors.
            - Significant progress toward mitigating potential security breaches and insider threats, bolstered by robust detection and response capabilities.

    - Optimal: Microsoft Defender for Identity and Advanced Threat Analytics solutions are fully developed, operationalized, and integrated into the organization’s overall security and risk management strategies. This optimal scenario ensures the highest level of protection against advanced threats, compromised identities, and malicious insider actions.
        - Indicators:
            - Universal and strategic implementation of advanced threat detection and identity protection solutions across all IT environments.
            - Comprehensive and proactive management of security threats, enhancing organizational resilience against cyber attacks and insider threats.
            - Full compliance with security standards and regulations, underpinned by an effective and well-managed threat detection and response system.

    - Relevance to NIST SP 800-53 Revision 5:
        - SI-4 Information System Monitoring: These solutions support the continuous monitoring of information systems for unauthorized access, use, and anomalies, enhancing the detection of advanced threats and compromised identities.
        - AU-6 Audit Review, Analysis, and Reporting: The signal collection and analysis capabilities of Microsoft Defender for Identity and Advanced Threat Analytics aid in the review and analysis of audit records, contributing to the identification of potential security incidents.
        - AC-2 Account Management: Implementing identity protection measures supports effective account management practices by identifying and responding to compromised credentials and insider threats, ensuring accounts are managed securely.
        - IR-4 Incident Handling: The solutions enhance incident handling processes by providing timely detection of and response to advanced threats, facilitating rapid containment, eradication, and recovery from incidents.

#### Leverage Microsoft Sentinel for integrated SIEM and SOAR capabilities across the enterprise

**Has the organization integrated signals from Defender for Cloud, Defender for Identity, Advanced Threat Analytics, and other monitoring systems with Microsoft Sentinel to provide the Security Operations Center (SOC) with a comprehensive, single-pane-of-glass view for monitoring security events across the enterprise?**
    - Legacy: The organization has not integrated its security monitoring systems, including Defender for Cloud, Defender for Identity, Advanced Threat Analytics, with Microsoft Sentinel. This lack of integration results in siloed security monitoring efforts, potentially leading to missed threats and inefficient incident response due to fragmented visibility across the security landscape.
        - Indicators: 
            - Absence of centralized security event monitoring, leading to disjointed and less effective security operations.
            - Increased risk of delayed threat detection and response due to the lack of a unified monitoring view.
            - Challenges in managing and correlating security events across various platforms and systems, impacting the overall effectiveness of the SOC.

    - Initial: Initial steps have been made to integrate some security monitoring systems with Microsoft Sentinel, providing the SOC with improved visibility into security events within selected environments. While this phase marks the beginning of consolidating security event monitoring, full integration and comprehensive visibility across all enterprise systems may still be under development.
        - Indicators: 
            - Partial integration of security monitoring systems with Microsoft Sentinel, focusing on high-priority areas or specific security solutions.
            - Initial improvements in centralized monitoring and incident response capabilities, though comprehensive enterprise-wide visibility is not yet achieved.
            - Some enhancement in the SOC’s ability to detect and respond to security threats, with ongoing efforts to expand the scope of integration with Microsoft Sentinel.

    - Advanced: A broad range of security monitoring systems, including Defender for Cloud, Defender for Identity, and Advanced Threat Analytics, are integrated with Microsoft Sentinel, significantly improving the SOC's visibility and response capabilities across the enterprise. This advanced tier reflects a mature approach to security event monitoring, ensuring effective threat detection and incident management through a unified platform.
        - Indicators: 
            - Broad integration of security monitoring systems with Microsoft Sentinel, facilitating comprehensive visibility into security events across the enterprise.
            - Enhanced SOC efficiency and effectiveness in threat detection, analysis, and response, supported by a single-pane-of-glass monitoring view.
            - Significant progress toward optimizing security operations and incident management, bolstered by integrated analytics and automated response capabilities.

    - Optimal: The organization has fully integrated Microsoft Defender for Cloud, Defender for Identity, Advanced Threat Analytics, and other monitoring systems with Microsoft Sentinel, achieving a comprehensive and unified view for monitoring security events across the entire enterprise. This optimal scenario ensures the highest level of operational efficiency and effectiveness in the SOC, leveraging advanced analytics and automation for proactive security management.
        - Indicators: 
            - Universal and strategic integration of all relevant security monitoring systems with Microsoft Sentinel, covering all aspects of the enterprise security landscape.
            - Comprehensive and consistent operational visibility, enabling proactive and efficient security threat detection, investigation, and response.
            - Full realization of SOC capabilities in managing enterprise security, underpinned by an effective, centralized security event monitoring and management system.

    - Relevance to NIST SP 800-53 Revision 5:
        - SI-4 Information System Monitoring: Integrating diverse security signals into Microsoft Sentinel supports the continuous monitoring of information systems for unauthorized access, use, anomalies, and other cybersecurity-related events, aligning with SI-4 requirements.
        - IR-4 Incident Handling: The consolidation of security event monitoring with Microsoft Sentinel enhances the organization's incident handling capabilities by providing a centralized platform for incident detection, analysis, response, and reporting.
        - AU-6 Audit Review, Analysis, and Reporting: The centralized view offered by Microsoft Sentinel facilitates the review, analysis, and reporting of audit records, contributing to effective audit management and analysis aligned with AU-6.
        - CA-7 Continuous Monitoring: The integration supports the establishment of a continuous monitoring strategy that assesses security controls and risks, leveraging Microsoft Sentinel's analytics and automation capabilities for real-time security insights.

### Every workload is assigned an app identity—and configured and deployed consistently
#### Every server and supported PaaS resource type (e.g. Azure SQL, KeyVault, etc.)  is assigned a managed identity

**Has the organization assigned a managed identity to every server and supported PaaS resource type?**
    - Legacy: 
        - Indicators: 
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

#### Implement and enforce policy-driven workloads and resources

**Has the organization implemented and enforced policies that govern the creation of resources and workloads, including requirements for tagging, resource group assignments, and technical specifications such as allowed regions, VM types, disks, and network policies?**
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

### Human access to resources requires Just-In-Time
#### Implement a protect the administrator program

**Has the organization implemented a protect the administrator program, including measures such as granting just-in-time (JIT) access, auditing elevated permissions, creating High-Value Asset zones, and providing secure admin workstations, to enhance oversight and security of administrative permissions?**
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

##### References
https://www.microsoft.com/insidetrack/blog/improving-security-by-protecting-elevated-privilege-accounts-at-microsoft/?OCID=InsideTrack_Search


### Unauthorized deployments are blocked, and alert is triggered
#### Leverage Azure Blueprints to control deployments and ensure compliance

**Has the organization adopted Azure Blueprints to govern resource deployments, ensuring compliance with approved templates and policies, and to activate necessary alerts or actions in case of policy violations?**
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

### Granular visibility and access control are available across workloads
#### Metrics, logs, and scaling efficiency

**Has the organization adopted metric and log collection capabilities, to support security operations, computing efficiency, and organizational objectives, particularly through the use of Virtual Machine Scale Sets for resource scaling?**
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

#### Role-Based Access Control (RBAC) for efficient permissions management across Workloads

**Has the organization implemented Role-Based Access Control (RBAC) to manage access permissions uniformly across individual and group levels for diverse workloads, using both built-in and custom roles?**
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

    - Relevance to NIST SP 800-53 Revision 5:
        - 

### User and resource access segmented for each workload
#### Utilize VNets, NSGs, ASGs, and Azure Firewalls for enhanced workload access management

**Has the organization leveraged Microsoft Azure's network segmentation capabilities, including Virtual Networks (VNets), VNet peering, Network Security Groups (NSGs), Application Security Groups (ASGs), and Azure Firewalls, to effectively isolate and manage access to workloads?**
    - **Legacy:**
        - Indicators:
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