## 2\. Know your User, Service and Device identities

**User, Service and Device identity is a really important factor when making access decisions in a zero trust network**

An identity can represent a user (a human), service (software process) or device. Each should be uniquely identifiable and cryptographically verifiable in a zero trust architecture. This is one of the most important factors in deciding whether someone or something should be given access to data or services.

These unique identities are one of a number of signals that feed into a policy engine, which [uses this information to make access decisions](4-Use-policies-to-authorise-requests.md). For example, a policy engine could evaluate user and device identity signals to determine if both are genuine, before allowing access to a service or data.

[Completing a discovery exercise](1-Know-your-architecture-including-users-devices-services-and-data.md) is an important first step towards allocation of a single source of identity to your users, services and devices.

### User Identity

Your organisation should use a definitive user directory, creating accounts that are linked to individuals. This could come in the form of a virtual directory or directory synchronisation, to give the appearance of a single user directory.

Each identity should be assigned to a role and this should be configured to be 'least privilege\', so a user only has access to what they require to carry out their role. In fact, these privileges are often derived from the user's job function with in an organisation.

When it comes time to administrate user accounts and privilege access, our [secure administration guidance](https://www.ncsc.gov.uk/collection/secure-system-administration) is a good place to start.

The directory will need to be compatible with all services within the architecture, no matter where they are accessed from, so there is a single source of identity and sign-on for users. This will allow for a better user experience, but also permit a single strong identity for all services.

**A user identity service should be able to:**

-   Create groups

-   Define roles that have been configured to be \'least privilege\'

-   Support strong, modern authentication methods such as multi-factor or passwordless authentication, see our [authentication policy](https://www.ncsc.gov.uk/collection/mobile-device-guidance/enterprise-authentication-policy) guidance for more information.

-   Securely provision credentials to users

-   Enable federated authentication to services (e.g. SAML 2.0, OAuth 2.0 or OpenID Connect)

-   Manage user identities in external services, where applicable (e.g. SCIM 2.0)

-   Support your joiners, movers, and leavers processes

-   Support 3^rd^ party federated ID (accepting identities from other trusted 3rd parties\' user directories)

**Migration**

If you have an existing directory, migrating to another directory will require careful planning. Some directory services allow you to import, synchronise or federate between directories, this would enable a phased migration or, effectively, provide a shared directory.

**External access**

You should also consider how you\'ll offer access to people from outside your organisation. Your services could federate with external identity providers in order to allow access to appropriate services and data. For example, a visitor can see the lunch menu, or a contractor can only access documents related to their work.

Identity and authentication is a wide-ranging topic needing careful consideration. The NCSC has more in-depth [guidance on identity and access management](https://www.ncsc.gov.uk/guidance/introduction-identity-and-access-management) and [authentication policy](https://www.ncsc.gov.uk/collection/mobile-device-guidance/enterprise-authentication-policy).

**Service Tokens**

Services *should not* have the ability to take limitless actions on behalf of users. If a service like this is compromised, it will provide highly privileged access to any service or any data in your system.

A better way of giving services appropriate access is to tie each action to a scope and time-restricted access token, linked with the user\'s identity. This way, if the same service were to be compromised, the amount of damage done to your service is limited to the permissions of the original action.

If anomalous behaviour is detected, the level of confidence for the users and devices assessing a service or data would deteriorate. Remedial action should be triggered immediately, as the token is less trusted than when issued due to the change in user or device health. Some examples of remedial action are, terminating the connection or triggering a prompt for MFA.

### Service Identity

A service - or more accurately, the software that provides a service - should have its own unique identity and be granted the minimum privileges necessary to function correctly. This includes restricting the network communication between services to the minimum amount required, by maintaining an allow list of connections, based on the identity of the service.

An example authentication approach could involve a unique certificate for each service. The certificate authentication can then be used to form mutual [TLS (Transport Layer Security)](https://www.ncsc.gov.uk/guidance/tls-external-facing-services) connections between the software processes that make up a service.

User access to an application or container platform should be federated into a single user directory and use a [policy engine to authorise access based on a number of signals](4-Use-policies-to-authorise-requests.md). A policy engine can make an access decision and release a token if the policy is satisfied.

### Device Identity

Each device that your organisation owns should be uniquely identifiable in a single device directory. This enables efficient asset management and provides clear visibility of the devices which access your services and data.

The zero trust policies you define will use compliance and health claims from a device to make decisions about which data it can access and the actions it can perform. A strong identity is required to ensure these claims can be validated.

The confidence level at which a device can prove its identity depends on the device type, hardware and platform:

- Using a secure hardware co-processor, such as a TPM, will give you high confidence in the device\'s identity. Key attestation should be used where possible to prove the identity is protected in a secure hardware co-processor.

- On a well-managed device, using a software-based key store gives a lower confidence in the device\'s identity than a TPM-based approach.

- On an unmanaged device, using a software-based key store provides the least amount of confidence in the device\'s identity, relative to the above.

Identifying devices from another organisation will require a trust relationship to be established between the two organisations. This should happen at both a governance and technical level.

### Bring your own device scenarios

When allowing requests from devices you don\'t own and manage, identification can be challenging. Devices in a BYOD model should still have an identity linked to them for monitoring purposes, but the confidence in that device\'s identity would likely be lower. Our [BYOD guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance/bring-your-own-device) can help further with managing these types of devices.

 
