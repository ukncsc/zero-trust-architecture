## 3\. Assess user behaviour, service and device health

**ser behaviour, and service or device health, are important indicators when looking to establish confidence in the security of your systems**

You should monitor health signals from your users and devices continuously, to evaluate confidence in their trustworthiness. Measuring user behaviour and device health helps you gain confidence of their cyber hygiene and that they have not been compromised. This information can be fed into a policy engine to make access decisions, as described in [4. Use policies to authorise requests.](4-Use-policies-to-authorise-requests.md)

For example, you may want to know *where* your users are trying to access services from and have confidence in the health of your devices. These health signals can then flow into a policy engine to [help make an access decision](4-Use-policies-to-authorise-requests.md).

Facilitating these assessments, you should [have single sources of identity for users, devices and services](2-Know-your-User-Service-and-Device-identities.md). These should be preceded by [an asset discovery phase](1-Know-your-architecture-including-users-devices-services-and-data.md).

**Devices**

You need to have confidence that the devices accessing your services and data are healthy. The health of these devices represents some of the most important signals used to control access to your data and services. Device health consists of compliance with device configuration policies and device state.

First, define configuration polices which will enforce a secure baseline for devices. The [NCSC\'s mobile device guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance) can help with this. Using a device management service, apply these policies to devices and enforce them. Then continuously check that devices are compliant.

Device health can be determined from the state of security features on the platform. For example, is secure boot enabled? [Are the latest operating system updates installed (https://www.ncsc.gov.uk/collection/mobile-device-guidance/keeping-devices-and-software-up-to-date)? [Is virtualisation-based security](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-vbs) or[[system integrity protection enabled](https://support.apple.com/en-us/HT204899)?

Going further, determining the underlying health of a devices\' firmware, boot process, endpoint security suite and operating system kernel, are strong signals which help to determine overall device health. Attestation is a way of achieving this, taking a snapshot of the state of a device, with claims about different components of the hardware and operating system. Some endpoint security suites can provide signals that can help determine if a device is trustworthy.

You should ensure that legitimate users are given a defined and clear path to bring their devices to good cyber health if it has accidently fallen below the required standard. A legitimate user could be blocked from accessing a service or data if a device has missed some routine maintenance.

For example, if a device has been offline for a period of time and has not received an operating system patch, the user should be given the ability and the required support to update their device, so it can be considered compliant.

**Services**

Service health should also be considered, not only when end user devices are accessing them, but also when services are talking to other services. Zero trust infrastructure, such as the policy engine and policy enforcement points should also be considered as services, here.

Services should be configured to satisfy our principles of zero trust using their native security functions. For instance, by enforcing strong authentication mechanisms and disabling legacy protocols that don\'t support modern authentication.

Services that you are responsible for must be kept up to date with the latest software patches. You should also be able to determine the version and patch level of the service. [Patches fixing vulnerabilities should be applied at the earliest opportunity.](https://www.ncsc.gov.uk/guidance/vulnerability-management)

The health of your services needs to be monitored. An unexpected change in state may indicate an unauthorised change, or malicious activity. Some example signals could be, making sure the service patch\'s are up to date and configured as per a configuration policy - for example, a container not running as privileged user. The source of the code that makes up the service should be verified as from a trusted source i.e. a code delivery pipeline.

**Users**

The behaviour of the users accessing services and data should be carefully considered. You can [use monitoring to define what is normal user activity](6-Focus-your-monitoring-on-users-devices-and-services.md).

You should define policies that check the health of users\' connections. For example, a user connecting in from a different geographical region to where they are normally based, or activity in the middle of the night, may be unexpected.

Further signals can be requested, to improve the integrity of the user action, by asking for [another factor of authentication.](5-Authenticate-and-Authorise-everywhere.md)

**Infrastructure**

Knowing the health of your infrastructure, which could be hosted in a data centre or in the cloud as IaaS (Infrastructure as a service) would also be advantageous.

This health-related information could come from monitoring network flows or information from infrastructure logging.

This could, for example, help you spot a rogue device on a network, an unauthorised data flow beaconing out to a malicious domain, or an unexpected process starting that might indicate malware in the system.
