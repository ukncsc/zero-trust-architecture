# 6. Focus your monitoring on users, devices and services

### Comprehensive monitoring is essential, because devices and services are more exposed to network attack

In a zero trust architecture it is highly likely that your monitoring strategy will change to focus on users, devices and services. Monitoring your devices, services and user behaviour will help you to [establish their cyber health.](3-Assess-user-behaviour-service-and-device-health.md)

Monitoring should be carried out on the device and be periodically exported or streamed over a secure transport (such as mutually authenticated TLS) to a central location. User behaviour, like normal working hours or normal working location, is another important metric to monitor. It\'s also important to have visibility of your services and understand interaction between users and their data. This information [can be used as a signal](4-Use-policies-to-authorise-requests.md), with any abnormal activity observed could be used by a policy engine to make an access decision.

You should know what actions devices, users and services are performing and what data they are accessing. Your monitoring should link back to [the policies you have set](4-Use-policies-to-authorise-requests.md), verifying they are being enforced as you expect.

**Protective monitoring may have to move**

User devices within a traditional walled garden network architecture should use a VPN to send all traffic through a controlled path. This enables monitoring at a central location on this controlled path. In a zero trust architecture, this central location is most likely not part of your architecture any more, so protective monitoring has to be moved onto each device.

[3-Assess-user-behaviour-service-and-device-health.md](3-Assess-user-behaviour-service-and-device-health.md) highlighted the importance confidence in device health, because a compromised - *unhealthy* - device cannot be trusted to provide reliable monitoring, since its logs could have been tampered with.

Endpoint security suites can also provide a good source of monitoring information, as they have features to detect threats, or alert on strange behaviour which may indicate compromise.

**BYOD and Guest devices**

If you are using Bring Your Own Device (BYOD), or have guest devices in your environment, you may not be able to fully achieve all your monitoring goals. In this case, you should decide not to trust these devices to the same degree as ones that you can fully monitor.

There are technical controls that can be implemented across BYOD deployments that can increase confidence in the security of such devices. This includes the use of [Mobile Device Management (MDM)](https://www.ncsc.gov.uk/collection/mobile-device-guidance/choosing-and-using-mobile-device-management-services) and [Mobile Application Management (MAM) solutions](https://en.wikipedia.org/wiki/Mobile_application_management).

Our [BYOD guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance/bring-your-own-device) can help further with deploying these types of devices and ensuring that your BYOD policy and controls complement zero trust.

**Network monitoring**

Although the network is untrusted and assumed hostile, network monitoring is still important to ensure good performance and cyber hygiene.

Monitoring should be carried out on your networks to measure performance, identify all devices attached to your network, detect rogue devices, and malicious activity. This is especially true if you\'re hosting on-premise services.

Coupled with device monitoring, network monitoring can help improve visibility and correlation. For example, you could trace network connections back to the process on a device that generated them.

**Further reading**

Further advice and guidance can be found with in the NCSC [Logging and protective monitoring](https://www.ncsc.gov.uk/collection/mobile-device-guidance/logging-and-protective-monitoring), [cloud security guidance](https://www.ncsc.gov.uk/collection/cloud-security/implementing-the-cloud-security-principles/audit-information-for-users) , [SaaS Guidance](https://www.ncsc.gov.uk/collection/saas-security/understanding-saas-security) and [Introduction to logging for security purposes](https://www.ncsc.gov.uk/guidance/introduction-logging-security-purposes).
