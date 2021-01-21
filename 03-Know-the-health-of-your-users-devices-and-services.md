# 3. Assess your user's behaviour, devices and services health

You should monitor health signals from your users and devices (including IoT) continuously, to evaluate confidence in their trustworthiness. For example, you may want to know where your users are trying to access services from and have confidence in the health of your devices.

## Device health

You need to have confidence that the devices accessing your services and data are healthy.  The health of these devices represents some of the most important signals used to control access to your data and services. Device health consists of compliance with device configuration policies and device state.

First, define policies which configure devices to be secure - the [NCSC's mobile device guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance) can help with this. Using a device management service, apply these policies to devices and enforce them, then continuously check that devices are compliant. Is the device compliant with the policies that you set?

Device health can be determined based on the state of security features on the platform. For example, is secure boot enabled? [Are the latest operating system updates installed](https://www.ncsc.gov.uk/collection/mobile-device-guidance/keeping-devices-and-software-up-to-date)? [Is virtualisation-based security](https://docs.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-vbs) or [system integrity protection enabled](https://support.apple.com/en-us/HT204899)?

Going further, determining the underlying state of a devices' firmware, boot process, endpoint security suite and operating system kernel are strong signals which help to the determination its overall health. Attestation is a way of achieving this, taking a snapshot of the state of a device with claims about different components of the hardware and operating system. The endpoint security suite can inform whether the device is compromised. This information can be used as a signal that can be used to determine access to a service or data.

## Services

Service health should also be considered, not only when end user devices are accessing them, but also when services are talking to other services. Zero trust infrastructure, such as the policy engine and policy enforcement points should also be considered as services, when reading this principle.

Services should be configured to satisfy the principles of zero trust using their native security functions, as per documentation. For instance, by enforcing strong authentication mechanisms and disabling legacy protocols that don\'t support modern authentication.

Services must be kept up to date with the latest software patches and you should be able to determine the version and patch level of the service you are using. [Patches fixing vulnerabilities should be applied at the earliest opportunity.](https://www.ncsc.gov.uk/guidance/vulnerability-management)

The health of your services needs to be monitored. An unexpected change in state may indicate an unauthorised change, or malicious activity. How this is achieved will depend on the type of service, but ideally this would be carried out programmatically, by interrogating an API provided by the service.

## Users

The behaviour of the users accessing services, devices and data should be carefully considered. Service and data access decisions need to be based on signals of the user and devices being used for the access.

Define policies that check the state of users\' connections. For example, a user connecting in from a different geographical region to where they are normally based, or activity in the middle of the night may be unexpected. Further signals can be requested to improve the integrity of the user action, by asking for another factor of authentication.

Passwordless authentication (e.g. FIDO2) is an ideal solution which provides strong security with an excellent user experience. Consider implementing passwordless authentication for a strong, consistent, and simple authentication experience across all of your services.

Multi-factor Authentication (MFA) is a requirement of zero trust architecture, but with modern devices and platforms, this doesn't mean the user experience has to be poor. The key to preserving the user experience is triggering MFA only when required. For example, when confidence of the user and his or her devices degrades, trigger the MFA. Signals of the users and devices are used to evaluate the confidence. 

 
