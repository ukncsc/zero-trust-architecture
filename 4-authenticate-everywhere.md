# Authenticate everywhere

In a zero trust architecture, assume the network is hostile authenticate all connections.

Services may be available directly over the internet, so authentication of user requests requires a stronger mechanism than just a username and password.

Multi-factor authentication is a requirement for a zero trust architecture. This doesn’t mean that the user experience has to be poor. On modern devices and platforms, strong multi-factor authentication can be achieved with a good user experience.

Consider adding additional factors depending on the impact of the request, using tokens or one-time passwords, device type and state, physical location and user behaviour analytics.

It’s important that strong authentication doesn’t hinder the usability of a service. So, only prompt for additional authentication factors when requests are of high impact or importance. For example, when accessing sensitive data or requesting privileged actions, such as creating users.

Requests between services also need to be authenticated. This is normally achieved using API tokens, frameworks such as OAuth or Public Key Infrastructure (PKI). Use mutual authentication wherever possible.