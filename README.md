# Zero trust architecture design principles 

**Eight principles to help you design and deploy a zero trust architecture.**

> BETA: This guidance is a draft that we'd like to share with the community for comment.
>
> Our ALPHA Guidance can be found [here](https://github.com/ukncsc/zero-trust-architecture/tree/962eee06a4071489ab119751102d3f61c2d3dae4) 
>
> [Our blog](https://www.ncsc.gov.uk/blog-post/zero-trust-principles-beta-release) introduces this guidance and covers our approach.
>
> If you have any feedback or ideas you can [create an issue](https://help.github.com/en/github/managing-your-work-on-github/creating-an-issue) or if you'd like to contribute [create a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).
>
> You can also e-mail us on [zerotrust@ncsc.gov.uk](mailto:zerotrust@ncsc.gov.uk)

## Introduction

Network architecture is changing. More services are moving to the cloud and there is continued growth in the use of Software as a Service (SaaS). Meanwhile, many organisations are embracing flexible working, with staff connecting from multiple devices in a variety of locations.

The traditional network perimeter is disappearing and with it, the value of traditional defences. Zero trust is a network architecture designed to cope with these changing conditions. The 8 principles outlined in this guidance will help you to implement your own zero trust network architecture. 

### The network is hostile

In a zero trust architecture, inherent trust is removed from the network. Just because you\'re connected to a network, doesn\'t mean you should be able to access everything on that network.

It is common in breaches to see an attacker gain a foothold on a network and then move laterally, because everything on the network is trusted. In a zero trust architecture, the network is treated as hostile.

### Removing trust from the network

If you remove trust from the network, you must instead gain confidence in your users, device, and services. This is achieved by building trust into the user\'s identity (through authentication), device health, and the services they access (authorisation).

For zero trust to be effective, each connection to a service should be authenticated and the device, user and connection authorised against rules and policies. Theses polices assess the amount of confidence you have in a user and their device, regardless of where the connection request comes from and grant access to resources accordingly.

To enable authorisation decisions, access policies need to be defined, based on who can access which service or data, and under which circumstances. 

How much confidence you need to trust a connection depends on the value of data being accessed or the impact of an action being performed. Devices should be inventoried and device health should be based on defined policies (such as encryption, patch levels, etc).

If you are unsure whether zero trust is the correct network architecture for your needs, or if you would like to learn a bit more about zero trust, our [network architectures guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance/infrastructure/network-architectures-for-remote-access) is a good place to start.

## Who is this guidance for?

This guidance is aimed at anyone who is involved in planning, design, implementation, deployment and operation of organization's information systems and networks including Systems Engineers, Solution and Security Architects, IT and CISOs. The principles are also useful for reviewing architectures when carrying out security assessments or assurance activities.

When implementing your design, these principles can be used as a guide for the features to look for in any specific technologies you plan to use.

Companies or open source projects implementing zero trust related technologies can also use these principles to guide their development and assess which part of the zero trust puzzle they fit into.

Using these principles does not guarantee a secure architecture but should help you to focus your efforts.

## Zero trust is new and evolving

IT systems rarely stand still - they change over time. With this in mind, these principles are not intended to be applied once and then forgotten. This is especially important because zero trust architectures are relatively new and still evolving.

You may find you cannot fully meet all these principles at once, as the technology you have in place does not support a zero trust architecture, as described here. In fact, this might be a common scenario, until zero trust technology matures. 

Try to be pragmatic in the solutions you choose. It may be the case you still need to support traditional security controls. As your system gradually transitions to zero trust, you should keep these principles on hand

Your architecture should be flexible enough to evolve, meeting changing needs, without impacting users. Consider how you would add new services, move between services, enable and disable features. This flexibility will allow your users to take advantage of new features, but also permit you to quickly respond to new vulnerabilities and threats.

Re-visit your architecture periodically and implement any changes that improve the usability and security of your system.

## Implementing zero trust - take your time

An existing system architecture can't be replaced overnight.

Deploying the zero trust model to an existing network, regardless of its age or number of legacy services, will require a phased approach, with many iterations. It will take time to get the necessary foundations in place. For example, establishing a strong identity for users and devices or deploying modern authentication across your organisation can be time consuming.

While transitioning to a new architecture, don\'t start decommissioning traditional security controls before you have implemented and tested your zero trust controls. Due to the nature of a zero trust architecture, this may leave your systems exposed and at considerable risk if they aren\'t properly configured and tested. For example, don\'t remove your VPN connection until you are satisfied that the new zero trust architecture is mitigating all the threats the VPN was covering. 

Legacy systems may still be hosted using a traditional network architecture, or might not support the features of a zero trust architecture. So, in some environments you may need to manage both a traditional network perimeter *and* a zero trust architecture. This could involve using a [split VPN tunnel](https://www.ncsc.gov.uk/collection/mobile-device-guidance/virtual-private-networks#VPNGuidance-update-Splittunnelling) to your legacy application or an authentication proxy. When a legacy system is being updated, try to design in support for zero trust.  

Even with the luxury of a greenfield environment, the zero trust model can be challenging. Many of the principles outlined below can't be fully satisfied with current, commercially available offerings. As always in security architecture, a risk managed approach is required.

## Terminology

When discussing zero trust architectures, it's useful to have a common vocabulary. Below are some terms used throughout these principles. We've tried to closely align these terms with other sources, to help when discussing zero trust technologies. 

-   Access Policy -- A specification of the requirements for access requests to be considered trusted and authorised.

-   Configuration Policy -- Policies that describe configuration options for devices and services.

-   Signal -- A piece of information like device health or location that can be used to gain confidence that you can trust an asset. You will often use a number of signals to make a decision to grant access to a resource. 

-   Signal database - A long term store of signals used to make access decisions

-   Policy Engine -- The component that takes signals and compares them with access policies to determine an access decision. A policy engine will often be a 3rd party product or service that can be purchased from a vendor. 

-   Policy Enforcement Point -- Mediates requests from a device to a service using the Policy Engine to determine if the connection is trusted.

-   Device health -  Confidence that a device is compliant with configuration polic**i**es, and is in a good state i.e. the latest patches have been installed, or a feature like secure boot is enabled. 

## The principles

These are the foundations of zero trust architecture design.

### 1.  Know your architecture including users, devices, and services

In the zero trust network model it's more important than ever to know your assets.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/01-Know-your-architecture-including-users-devices-and-services.md)

### 2. Know your User, Service and Device identities

In a zero trust architecture, identity becomes the new perimeter, it is important to have a single source of identity for each of the following: user (human), service (machine or software process) and device.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/02-Know-your-User-Service-and-Device-identities.md)

### 3. Know the health of your users, devices and services

The health of devices, user behaviour and services are some of the most important signals used to gain confidence in them.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/03-Know-the-health-of-your-users-devices-and-services.md)

### 4. Use policies to authorise requests

Every request to access a data or a service should be checked by a central policy engine, which compares signals with access policies to determine an access decision

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/04-Use-policies-to-authorise-requests.md)

### 5. Authenticate everywhere

In a zero trust architecture, we assume the network is hostile and authenticate *all* connections that access data or services.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/05-Authenticate-everywhere.md)

### 6. Focus your monitoring on devices and services

Given that devices and services are more exposed to network attack than in traditional architectures it's important that comprehensive monitoring for attacks is carried out.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/06-focus-your-monitoring-on-devices-and-services.md)

### 7. Don't trust any network, including your own

In zero trust the network is considered hostile, therefore build trust into users, devices and services rather than the network. 

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/07-Don't-trust-any-network-including-your-own.md)

### 8. Choose services designed for zero trust

Select services with built-in support for zero trust network architectures.

[Read more](https://github.com/ukncsc/zero-trust-architecture/blob/master/08-Choose-services-designed-for-zero-trust.md)



