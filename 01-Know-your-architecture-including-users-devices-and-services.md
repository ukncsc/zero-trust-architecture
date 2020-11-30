# 1. Know your architecture including users, devices, and services

In the zero trust network model it's more important than ever to know your assets. This will most likely involve undertaking an asset discovery phase to understand what you have. In some environments this can be challenging and it might involve using an automated tool to discover assets on the network. It might not always be a technology problem, it could be the case you can determine your assets by querying procurement records. In a micro service architecture it would be advantageous to know the data flows between services before you start to implement zero trust.

In order to get the benefits from zero trust you need to know about each component of your architecture, from users and their devices (including external users), through to the services and data they are accessing.

Your attention should be focused on the components of the system which use the network. The network itself should be considered untrusted and hostile

**Transitioning to zero trust**

This principle is particularly important if transitioning to a zero trust architecture for an established system, with many pre-existing services. If a zero trust architecture is implemented without considering existing services, they may be at higher risk. These services may not be designed for a hostile, untrusted scenario and therefore will be unable to defend themselves against attack.

**Conduct a risk assessment**

Once you know your architecture it puts you in a better position to carry out an exercise to understand the risks to your new network design and ensure they are being mitigated. It would be sensible to start with a risk assessment. This can be used to help you understand if all risks have been mitigated using the zero trust components under consideration.

If all the risks cannot be mitigated using a zero trust approach, the existing security controls from your current network architecture will need to stay in place until this is resolved.
