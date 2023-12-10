# Transforming Device Management and Security with Microsoft Intune

I've been wanting to look at Microsoft Intune for a while now and wanted to document myself learning it through this blog. I'm impressed by how simple - yet complex it is. It's incredibly easy to navigate as everything is laid out so well and with so many different configuration options that make me understand how so many organizations are utilizing this right now. Let's carry on in the world of Microsoft Intune!

Microsoft Intune is at the forefront of modern device management, providing a powerful solution for overseeing mobile devices, desktops, servers, and applications across diverse environments. This cloud-based platform seamlessly integrates with Microsoft Entra ID, Azure Information Protection, and advanced threat protection products to ensure comprehensive security against digital threats.

![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/89bb3fd1-51e6-446e-ad96-95b99af6ba1b)


**Key Features:**
- Cloud-based Mobile Device Management (MDM)
- Cloud-based Mobile Application Management (MAM)
- Cloud-based PC Management

**Benefits:**
- Efficiently manages Android, iOS, iPadOS, macOS, and Windows devices
- Enhances productivity while safeguarding against advanced digital threats

## Integration:

Intune seamlessly integrates with Microsoft Endpoint Configuration Manager, Endpoint analytics, and Windows Autopilot. This synergy establishes a powerful management infrastructure, enabling organizations to provide IT services, apps, protection, and configurations, maximizing end-user productivity.

By implementing Microsoft Intune, organizations can create a secure and productive digital environment, offering a range of services and protections for end users. This journey into Microsoft Intune unfolds the potential for streamlined device management, enhanced productivity, and robust data security.

## Protecting Endpoint Environments with Microsoft Intune

The Microsoft Intune Admin Center is where you can configure settings for devices, apps, and users to better protect them. It allows for the creation of Configuration Profiles for specific platforms and devices to streamline management.

### Examples of Device Configuration Policies:

- **Restricting Hardware Features:** Control the use of device features like the camera or Bluetooth.
- **Passcode Resets:** Reset passcodes for users facing device lockouts.
- **Compliance Requirements:** Enforce protection standards, such as PIN usage, for device compliance.
- **App Configuration:** Manage compliant and noncompliant apps with alerts and potential installation blocks.
- **App and Data Protection:** Safeguard apps and the data they handle.
- **Identity-based Protection:** Add an extra layer of protection to devices based on user identity.
- **Windows Hello for Business:** Control settings for this alternative sign-in method on Windows 10 and later.
- **Device Retirement:** Securely retire devices and remove associated data.
- **Email Configuration:** Allow seamless access to company email on personal devices without additional setup.


## Protecting and Managing Applications

Intune MAM supports two different configurations: Mobile Device Management (MDM) & Mobile App Management (MAM).

### Mobile App Management (MAM)

IT Admins can manage apps using MAM on devices currently enrolled with Intune MDM. MAM without device enrollment, also known as MAM-WE, allows IT Admins to manage apps using MAM and app protection on devices not enrolled with Intune MDM.

Intune allows for a wide range of app control that can easily be pushed across all devices and users. Examples of some app policies are as follows:

- **Add and Assign Apps:** Seamlessly add and assign apps to devices and users for a tailored experience.
- **Assign Apps to Non-Enrolled Devices:** Extend app assignment even to devices not enrolled with Intune, ensuring flexibility.
- **App-Configuration Policies:** Fine-tune app behavior with configuration policies, gaining control over startup actions.
- **Data Protection:** Safeguard sensitive data by preventing backup from protected apps.
- **Copy and Paste Restrictions:** Enhance security by restricting copy and paste actions between apps.
- **PIN Access Requirement:** Strengthen app security by requiring a PIN for access.
  
## Endpoint Environments

### Cloud Endpoint Management:

Manage devices, apps, and data with Microsoft Intune, also allowing seamless integration with Microsoft 365 and Entra ID, ensuring access control and protection on all fronts!

### On-Premises Endpoint Management:

Optimize Windows 10/11 device management, allowing enhanced security and restriction to remote access. Integrates well with Configuration Manager and Microsoft 365.

### Cloud + On-Premises Endpoint Management:

Enable data flow to Microsoft Endpoint Management via ConfigMgr Connector. Achieve cloud integration without co-management.

### Co-Managed Endpoint Management:

Concurrently oversee Windows 10/11 devices with Configuration Manager and Intune, balancing on-premises and cloud tasks.

![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/3aa6b2aa-dcb8-4851-b791-d2f2382ae55b)

## Provisioning

### Windows Devices:

Windows Autopilot can be used for device provisioning, offering four deployment modes, including Self-Deploying Mode for shared devices and User-Driven Mode for traditional users. Autopilot ensures easy deployment for the latest Windows versions. White Glove facilitates pre-provisioning by partners or IT staff.

### Alternative Windows Provisioning:

Configuration Manager provides diverse methods for deploying Windows OS, from Software Center to PXE. Intune also supports bulk enrollment for Microsoft Entra tenants.

### Apple Devices:

Use Apple Business Manager or Apple School Manager for iOS and macOS provisioning. Set up Intune to enroll Apple devices through Automated Device Enrollment, allowing you to easily accomplish large-scale enrollment.

### Android Devices:

Use the Android Enterprise zero-touch program to provision corporate-owned devices. Zero-touch allows mass provisioning and enrollment without physical contact.

## App Management with Intune

Intune can help manage the apps that a company's workforce uses on devices using Mobile Application Management (MAM).

![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/97ff6f03-3fd5-4e5a-bd32-5a9205b1e4d4)

# App Management Lifecycle

There is a lifecycle to app management, consisting of five key stages: Add, Deploy, Configure, Protect, and Retire.

## Add
This phase enables the addition of applications from various sources, including:
- App store
- Line-of-business AKA In-house developments
- Built-in apps
- Web-based apps
![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/82491633-eb5f-4d89-ab92-8856fb74d0ec)
![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/ce50b469-a283-4f35-9d2b-08ee4187ce85)
![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/d528c710-46df-4439-a45c-e0caaa213f7a)

You have the ability to upload an entire file, such as if you're looking to add an app from the Widnows MSI line-of-business like Microsoft .NET Compact Framework. Line-of-business means an app written in house.

![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/9f3a94a6-3e15-4413-869c-715fad42187e)


## Deploy
In this phase, you assign the app to users and devices, which can be monitored within the Azure portal. The Intune administration console also provides the ability to track license usage for apps that require licenses in bulk.

## Configure

Intune and Configuration Manager provide methods to configure app installation and updates.

- Managed browser policies allow you to configure settings and restrict websites that your users can visit.
- Specific settings for Microsoft Outlook can be configured upon installation.
- Configuring user and system contexts in apps helps detect whether the app is installed or needs to be updated. 

You can even specify the sope of the app configurations as well as group together users/devices and all them to either be Required, Available for enrolled devices or just Uninstall. 

### Eliminating App Setup Problems!

- With the addition of App configuration policies, policies are assigned to end users before running a specific app. Because the settings are unique to each app, end users don't need to take action, and the settings will be applied automatically.

- Configuration policies can be used for iOS/iPadOS or Android apps.

- Any of the following details can be specified for configuration settings:
  - Custom port numbers, language, security settings, branding such as logos.

This protects against the incorrect configuration of settings for apps and allows for smooth running for end users and everyone else!

## Protect

This phase involves implementing policies to safeguard apps, including data leak prevention for apps specific to certain operating systems and app-specific protection policies.

- **Conditional Access**: This feature controls access to email and services based on conditions you specify, such as device types or compliance with deployed policies.

- **App Protection Policies**: These policies work with individual apps to enhance the protection of company data. They restrict data copying between unmanaged and managed apps, and also provide the capability to prevent the operation of jailbroken or rooted devices.

![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/c4d06c78-3b8f-4e9a-b656-30d010957459)
![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/fac74e92-deb1-46eb-bf87-d581debd00d2)
![image](https://github.com/CertainRisk/Microsoft-Intune/assets/141761181/1dd45ed3-10a2-4c43-8191-82377af577db)

# Microsoft Entra Identity

- Microsoft Entra identity isolates organization data from personal data, providing additional security to organizational data.
- It restricts user actions with organizational data, such as copy, paste, save, and view.
- Creation and deployment on devices enrolled with Intune, another MDM service, or not enrolled in any MDM service.

## Protected Apps

Intune supports protected Microsoft Apps and Partner apps that incorporate MAM capabilities. They come with a variety of mobile application protection policies.

- Restrict copy-and-paste and save functions.
- Configure web links to only open in a secure Microsoft browser.
- Support multi-identity use and app-level Conditional Access.
- Application of DLP policies.
- App protection without enrollment.
- App protection on devices managed with 3rd-party EMM tools.

# Intune APP Data Protection Framework Levels

The Intune APP Data Protection Framework is structured into three configuration levels, each tailored to specific security requirements.

## Enterprise Basic Data Protection (Level 1)

This foundational configuration ensures minimal data protection by safeguarding apps with a PIN and encryption. Key features include:

- **PIN Protection and Encryption:** Ensures apps are protected with a PIN and encrypted.
- **Replacement of Basic Exchange Online Policies:** Replaces the need for basic Exchange Online device access policies by introducing a PIN requirement for accessing work or school data.
- **Comprehensive Data Protection:** App Protection Policy extends beyond Exchange Online policies, providing protection beyond mobile messaging scenarios.

## Enterprise Enhanced Data Protection (Level 2)

Recommended as a standard for devices accessing sensitive information, this level builds upon Level 1 by:

- **Minimum OS Version Requirement:** Requires a minimum OS version for enhanced security.
- **Data Transfer Restrictions:** Restricts data transfers to enhance protection.

## Enterprise High Data Protection (Level 3)

Recommended for organizations with sophisticated security needs or those targeted by adversaries, Level 3 introduces:

- **Further Data Transfer Restrictions:** Adds additional restrictions on data transfer scenarios.
- **Increased PIN Configuration Complexity:** Enhances the complexity of PIN configurations.
- **Mobile Threat Detection:** Includes the addition of mobile threat detection for advanced security.

For detailed policy settings for each framework level, refer to the official documentation [here](https://learn.microsoft.com/en-us/mem/intune/apps/app-protection-framework#level-1-enterprise-basic-data-protection).


## Retire
Apps that are outdated and need to be removed can be uninstalled by assigining an **uninstall intent** to a group of users or devices. 

To delete an app in Configuration Manager:
- You delete an app by first retiring the app. 
- Delete all deploymenets of the app and references to the app by other deployments.
- Finally, delete all app's revisions.


# Conditional Access and Endpoint Security in Intune

Conditional Access is a Microsoft Entra capability (for ID P1 and P2 licenses), Intune adds to this capability by adding mobile device compliance and MAM to the mix. 

In Intune, groups are used in applying policies, such as Conditional Access and endpoint security.

**Conditional Access Policies:** Govern access to resources like email, files, and data. They ensure that only trusted users on trusted devices using trusted apps can access these resources.

**Endpoint Security Policies:** Offer vital security measures for your organization's devices.

Conditional Access provides granular access control to gate access to your data based on location, devices, user state and application sensitivity. 

Intune provides different types of Conditional Access:

**Device Based Conditional Access**
 - Conditional Access for Exchange on-premises, Windows PCs (Corporate Owned and BYOD)
 - Conditional Access based on network access control.
 - Conditional Access based on device risk. 

**App-based Conditional Access**

## Conditional Access with Co-Management

I) Intune evaluates every device in your network to determine its level of trustworthiness.
- It ensures devices are securely configured; this evaluation is pre-security breach and configuration-based.
- Configuration Manager also conducts an evaluation on required updates or app compliance.

II) Intune can detect active security incidents on devices using Microsoft Defender for Endpoint and other mobile threat-defense providers.
- They run ongoing behavioral analysis on devices, identifying active incidents.
- This evaluation is post-security breach and incident-based.
- 
## Device Based Conditional Access

Intune and Microsoft Entra ID collaborate to allow access to email, Office 365 services, Software as a Service (SaaS) apps, and on-premises apps only for managed and compliant devices. You can configure a policy in Microsoft Entra ID to restrict access to Office 365 services exclusively for domain-joined computers or mobile devices enrolled in Intune.

Intune offers device compliance policy capabilities to assess the compliance status of devices. The compliance status is reported to Microsoft Entra ID, which utilizes it to enforce the Conditional Access policy established in Microsoft Entra ID when a user attempts to access company resources.

TL;DR Intune and Entra ID work in tandem to ensure that only compliant devices can access email, 365 services, SaaS apps, etc. Compliance status, as reported by Intune, is used by Entra ID to enforce Conditional Access policies.

## Network Access Control Conditional Access

Intune teams up with partners like Cisco ISE, Aruba Clear Pass, and Citrix NetScaler for smart access controls. This means users get access or denial to corporate Wi-Fi or VPN based on whether their device is both managed and compliant with Intune's policies.

## Device Risk Conditional Access

Intune teams up with Mobile Threat Defense partners for strong security against malware, Trojans, and other threats on mobile devices.

**How it works:**
- When the Mobile Threat Defense agent is on a mobile device, it sends messages to Intune about its compliance status, especially when a threat is detected.

## Windows PC-based Conditional Access

**Corporate-Owned**
  - *Microsoft Entra Hybrid Joined*: Companies comfortable with managing PCs through AD policies or Configuration Manager choose this option.
  - *Microsoft Entra Domain Joined*: Cloud-first or Cloud-only organizations allowing access to both cloud and on-premises apps and resources.

**BYOD**
- *Workplace Join and Intune Management*: Users bring their own device and access corporate resources with it. Workplace join is used to enroll devices into the Intune MDM and receive device-level policies.


# Group-Based Policy Management

**Assigned Groups** - Manually add users and devices to a static group.

**Dynamic Groups** - Automatically add users and devices to user or device groups based on an expression.
  - Dynamic Groups require Entra ID P1 or P2.

Device categories can be created to automatically add devices to groups based on predetermined rules.
- Different groups can be available for users to choose from during enrollment.
- iPhone/iPad and Android device users have to select a group during setup, while for Windows, this can be done through the Company Portal.
- Once devices are in groups, rules and apps can be assigned to them.

# Implementing Security Rules with Intune's Endpoint Security Node

End point security policies help you focus on security and mitigate risks to devices, allowing you to remediate devices or restore them to a compliant and secure state.

Intune's Endpoint Security centralizes tools for device security:

- **Device Monitoring:** Easily check the compliance status of managed devices and address policy issues.
- **Security Baselines:** Quickly apply best practice security configurations to Windows devices and key applications.
- **Focused Security Policies:** Tailor security settings for antivirus, disk encryption, firewalls, and more through specific endpoint-security policies.
- **Compliance Policies:** Set rules for device and user compliance, including OS versions, passwords, and threat levels.
- **Conditional Access Integration:** Gate access to resources based on compliance, managing both enrolled and unenrolled devices.
- **Microsoft Defender Integration:** Seamlessly integrate with Microsoft Defender for Endpoint for enhanced security tasks and detailed remediation steps.
- **Configuration Manager Integration:** In a co-managed scenario, link Configuration Manager with Microsoft Defender for Endpoint for advanced threat detection, investigation, and response.

# Analyzing and Resolving Compliance Issues with Microsoft Intune

## Intune Tenant Status Page

A tenant is an instance of Microsoft Entra ID that an organization receives when it signs up for Microsoft Intune. This page provides a summary of your tenant's information, including location, name, MDM authority, and a tenant service release number linking to a page with new updates.

Under the **Service Health and Message Center** tab, you can view active incidents and advisories that may impact your tenant, as well as news about planned changes.

## Troubleshooting + Support Page

This page allows help desk operators and admins to view information for addressing user help requests. Organizations with a help desk role can assign the Help desk operator role to a group of users.

The **Troubleshoot** pane displays user-enrollment issues, providing details about the issues and steps for remediation. To assist help desk operators, they only need to enter the user's name, and Intune provides useful data to resolve tier-1 issues, including:
- User Status
- Assignments
- Compliance issues
- Unresponsive device
- Devices not receiving VPN or Wi-Fi settings
- App installation failure

## Intune Reports

Microsoft Intune reports offer the flexibility to proactively monitor activity and the health of endpoints across the organization. Report types are organized into three categories:

- **Operational**: Provides timely and specific data for quick actions.

- **Organizational**: Offers a broader summary of the overall situation, such as the state of device management.

- **Historical**: Shows patterns and trends over time, allowing for the planning of long-term developments.

- **Specialist**: Enables admins to create custom reports using raw data, providing flexibility and granular customization capabilities.

The reporting framework ensures a consistent and comprehensive reporting experience, including the following functionalities:

- **Search and Sort**: Easily search and sort across any column, regardless of the dataset size.

- **Data Paging**: Efficiently scan data based on paging, jumping pages or page-by-page.

- **Performance**: Quickly generate and view reports created from large tenants.

- **Export**: Export reporting data generated from large tenants.


## Enhancing User Experience with Power of Endpoint Analytics

End users often face disruptions, including lengthy boot times, attributed to legacy hardware, suboptimal software configurations, and changes. IT's limited visibility into these issues relies on slow, costly support channels. This not only burdens IT but impacts information workers' productivity, affecting the organization's bottom line.

**Endpoint analytics** aims to boost user productivity and cut IT-support costs by providing insights into the user experience. It enables proactive support, optimizing end-user experiences, and detecting regressions from configuration changes.

Key Focus Areas:
1. **Recommended Software**: Suggestions for an enhanced user experience.
2. **Proactive Remediation Scripting**: Address common support issues before users notice.
3. **Start-up Performance**: Streamline the power-on to productivity process, minimizing boot and sign-in delays.

## Connector Status

Connectors are connections that are configured to external services such as Apple Volume Purchase program or Windows Autopilot. Connectors can also be certificates or credentials that are required to connect to external unmanaged services. Connector Status is based on the last successfull synchronization. 

Unhealthy Connectors show at the top of the list, next are those with warnings and then the healthy connectors and lastly those that have not yet been enabled. 

