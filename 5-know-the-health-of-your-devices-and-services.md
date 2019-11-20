# Know the health of your devices and services

The health of devices and services is one of the most important signals used to gain confidence in them.

## Devices
Determining if the device accessing your services is up-to-date, compliant with your device configuration policies and in a healthy state is important as it one of the most important signals used to control access to services and data. 



First, define policies which configure devices to be secure, NCSC’s end-user device guidance can help. Using a device management service, apply these policies to devices and enforce them, then continuously check that devices are compliant.



Device health consists of compliance with device configuration and device state. Is the device compliant with the policies that you set? Is the device in the expected state?



Device state can be determined based on the state of security features on the platform. For example, is secure boot enabled? Are the latest operating system updates installed? Is virtualisation-based security or system integrity protection enabled?



Going further, determining the underlaying state of a devices’ firmware, BIOS, and operating system kernel are strong signals which contributes to determining its overall health. Attestation is a way of achieving this, taking a snapshot of the state of a device with claims about different components of the hardware and operating system are reported to the signal database for analysis.

## Services
The health of services should also be considered, not only when end-user devices are accessing services but also when services are talking to other services. The supporting zero trust infrastructure, such as the policy engine and policy enforcement points should also be considered services when reading this principle.



Services should be configured to use their native security functions as per documentation and to satisfy the principles of zero trust. For instance, enforcing strong authentication mechanisms and disabling legacy protocol that don't support modern authentication.



Services also need to be kept up-to-date with the latest software patches and you need to be able to determine the version and patch level of the service you are using. Patches fixing vulnerabilities should applied at the earliest opportunity.



The health of your services needs to be monitored, an unexpected change in state may indicate an unauthorised change or malicious activity. How this is achieved will depend on the type of service, ideally this would be carried out programmatically by interrogating an API that the service provides.