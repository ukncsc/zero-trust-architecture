## 5. Authenticate and Authorise everywhere

### Assume the network is hostile - authenticate and authorise *all* connections that access data or services

Build your systems to have strong authentication methods and build applications to [accept access decisions from a policy engine](4-Use-policies-to-authorise-requests.md).

Authentication and authorisation decisions should consider multiple signals, such as device health, device location, user identity and status, when [evaluating the risk associated with the access requests](4-Use-policies-to-authorise-requests.md).

**Multi-factor**

[MFA](https://www.ncsc.gov.uk/guidance/multi-factor-authentication-online-services) is a requirement for a zero trust architecture.

This doesn\'t mean that the user experience has to be poor. On modern devices and platforms, strong MFA can be achieved with a good user experience. For example, only triggering MFA when confidence in the user and device degrades. Some authentication apps provide a push notification on a trusted device, so that users are not burdened with typing a code or finding a hardware token.

It\'s worth noting that not all factors of authentication are visible to users, it could be the case one of the factors could be something like a cryptographically backed passwordless login, using a built-in FIDO2 platform authenticator.

**Usability**

It\'s important that strong authentication doesn\'t hinder the usability of a service. For example, only prompt for additional authentication factors when requests have a higher impact, such as requests for sensitive data or privileged actions, including the creation of new users. SSO should be considered, to reduce the friction of MFA.

A risk-based approach should be considered to mitigate the higher impact caused by additional authentication factors. In the example above, if the confidence level in the user is sufficiently high, additional factors may be avoided.

Passwordless authentication (e.g. FIDO2) is an ideal solution, as it provides strong security, and an excellent user experience. Consider implementing passwordless authentication for a strong, consistent, and positive user experience across all of your services.

**Service to service**

Requests between services also need to be authenticated. This is normally achieved using API tokens, frameworks such as OAuth 2.0 or [Public Key Infrastructure](https://www.ncsc.gov.uk/collection/in-house-public-key-infrastructure).

Use mutual authentication, so you have confidence that both services communicating are genuine. This is key when you're building an allow list, to authorise connections between services based on identity.

**Further reading**

Please see our [authentication policy guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance/enterprise-authentication-policy) for an overview of the type of technologies that can be considered when thinking about solution for this principle.
