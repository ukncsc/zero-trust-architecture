# 6. Focus your monitoring on devices and services

Given that devices and services are more exposed to network attacks than in traditional architectures, it's important that comprehensive monitoring is carried out.

You should know what actions that devices, users and services are performing and what data they are accessing. Your monitoring should link back to the policies that you set, verifying they are being enforced as you expect.

**No choke points**

User devices within a traditional walled garden network architecture should use a VPN to send all traffic through a controlled path. This enables traffic to be inspected. In a zero trust architecture, this choke point isn't available and protective monitoring has to be moved onto each device.

It's important that you are confident in the device health as a compromised, 'unhealthy' device cannot be trusted to provide reliable monitoring, as logs could have been tampered with.

**Network monitoring**

Although the network is untrusted and assumed hostile, network monitoring is still important to ensure good performance and cyber hygiene. Monitoring should be carried out on your local networks to measure performance, identify rogue devices, and malicious activity, especially if you're hosting on-premise services.

Coupled with device monitoring, network monitoring can help improve visibility and correlation. For example, you could trace network connections to the process on the device that generated them.

Further advice and guidance can be found with in the NCSC [Logging and protective monitoring](https://www.ncsc.gov.uk/collection/mobile-device-guidance/logging-and-protective-monitoring) page.
