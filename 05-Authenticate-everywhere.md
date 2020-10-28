# 5. Authenticate everywhere

In a zero trust architecture, we assume the network is hostile and authenticate *all* connections that access data or services.

Services may be available directly over the Internet, so authentication of user requests requires a stronger mechanism than a simple username and password combination.

Authentication and authorisation should include multiple signals, such as device health, device location and user identity, to build session risk detection.

**Multi-factor**

[MFA](https://www.ncsc.gov.uk/guidance/multi-factor-authentication-online-services) is a requirement for a zero trust architecture. This doesn't mean that the user experience has to be poor. On modern devices and platforms, strong MFA can be achieved with a good user experience.

For higher-impact requests, consider adding additional factors such as: hardware tokens or one-time passwords, device type, and user behaviour analytics

**Usability**

It's important that strong authentication doesn't hinder the usability of a service. So, only prompt for additional authentication factors when requests have a higher impact. For example, when accessing sensitive data or requesting privileged actions, such as creating users. SSO should be considered, to mitigate the friction of using MFA.

Passwordless authentication (e.g. FIDO2) is an ideal solution, as it provides strong security, and an excellent user experience. Consider implementing passwordless authentication for a strong, consistent, and positive user experience across all of your services.

**Service to service authentication**

Requests between services also need to be authenticated. This is normally achieved using API tokens, frameworks such as OAuth or Public Key Infrastructure (PKI). Use mutual authentication wherever possible.
