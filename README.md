# Zero trust architecture design principles

**Ten principles to help you design and deploy a zero trust architecture.**

>
> ALPHA: This guidance is an initial draft that we'd like to share with the community for comment.
>
> [Our blog](https://www.ncsc.gov.uk/blog-post/zero-trust-architecture-design-principles) introduces this guidance and covers our approach.
>
> If you have any feedback or ideas you can [create an issue](https://help.github.com/en/github/managing-your-work-on-github/creating-an-issue) or if you'd like to contribute [create a pull request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request).
>
> You can also e-mail us on zerotrust@ncsc.gov.uk
>

## Introduction
Network architecture is changing. More services are moving to the cloud, there is a surge in the use of Software as a Service (SaaS), and users are embracing flexible working on multiple devices in a variety of locations. The traditional network perimeter is disappearing and with it, the value of traditional defences.

In a zero trust architecture, inherent trust is removed from the network. Just because you're connected to a network doesn't mean you should be able to access everything on that network. This is commonly seen in breaches; an attacker gains a foothold in a network and is able to move laterally because everything on the network is trusted. In zero trust, should be treated as hostile.

However, in order to remove trust from the network, you need to instead gain confidence that you can trust a connection. This is achieved by building trust into the user's identity, their devices, and the services they access. For this model to be effective, each connection to a service should be authenticated, authorised against a policy, and encrypted, regardless of where the connection request come from. 

To enable authorisation decisions, access policies need to be defined, based on who can access which service or data, under which circumstances. How much confidence you need to trust a connection depends on the value of data being accessed or impact of action being performed.

## What does this guidance do?
These principles are intended to help you design and deploy a secure end-to-end, zero trust architecture. This will stretch from your users and their devices, through to the services and data they are accessing. You'll also get a clear understanding of the zero trust model, the benefits it brings and the risks you'll need to consider.

These principles are also not intended as a list of compliance standards. Consider all the principles and develop a plan on how you can implement them on your journey to a zero trust architecture.

## Who is this guidance for?
This guidance is aimed at a technical audience such as Systems Engineers, Solution and Security Architects, and CISOs. The principles are also useful for reviewing architectures when carrying out security assessments or assurance activities.

When implementing your design, these principles can be used as a guide for the features to look for in any specific technologies you plan to use.

Companies or open source projects implementing zero trust related technologies can also use these principles to guide their development and assess which part of the zero trust puzzle they fit into.

Using these principles does not guarantee a secure architecture but should help you to focus your efforts.

## Terminology
When discussing zero trust architectures it’s useful to have a common language. Below are some terms used throughout our principles. We’ve tried to closely align these terms with other publications to help when comparing between different flavours of zero trust architecture. 

* Access Policy – Policies that determine the required context of a request for it to be considered trusted and authorised.
* Configuration Policy – Policies that describe configuration options for devices and services.
* Signal – A piece of information used to gain confidence that you can trust an asset.
* Signal database - A long term store of signals used to make access decision and for analysis.
* Policy Engine – The component that takes signals and compares them with access policies to determine an access decision.
* Policy Enforcement Point – Mediates requests from a device to a service using the Policy Decision Engine to determine if the connection is trusted.

## Stay nimble
IT systems rarely stand still, they change over time, these principles are not intended to be applied once and be forgotten. This is especially important for a zero trust architectures as they are relatively new and still evolving. They should be used throughout the lifecycle of your system.

Your architecture needs to be flexible enough to evolve, meeting changing needs, without impacting users. Consider how you would add new services, move between services, enabling and disabling features. This flexibility will allow your users to take advantage of new features but also permit you to quickly respond to new vulnerabilities and threats.

Your organisation, technologies and good practice will change over time. Re-visit your architecture periodically and implement any changes that improve the usability and security of your system.

## Take your time
An existing system’s architecture can’t usually be completely changed overnight.

Deploying the zero trust model to an existing network, regardless of its age or number of legacy services, will require a phased approach with many iterations. It will take time to get the foundations required in place. For example, establishing a strong identity for users and devices or deploying modern authentication across your organisation can be time consuming.

While transitioning to a new architecture don't start decommissioning traditional security controls before you have implemented and tested your zero trust controls. Due to the nature of a zero trust architecture you may leave your systems exposed and at considerable risk if they aren't properly configured and tested.

Even with the luxury of a greenfield environment, the zero trust model can be challenging. Many of the principles outlined below can’t be fully satisfied with current, commercially available offerings. As always in security architecture, a risk managed approach is required.

## The principles

We then dive into the ten principles. These are the foundation of designing a zero trust architecture.

### 1. Know your architecture
In the zero trust network model it’s more important than ever to know about your assets.

[Read more](1-know-your-architecture.md)

### 2. Create a single strong user identity
Your organisation should use a single user directory and create accounts that are linked to individuals.

[Read more](2-create-a-single-strong-user-identity.md)

### 3. Create a strong device identity
Each device owned by your organisation should be uniquely identifiable in a single device directory.

[Read more](3-create-a-strong-device-identity.md)

### 4. Authenticate everywhere
In a zero trust architecture assume the network is hostile, authenticate all connections.

[Read more](4-authenticate-everywhere.md)

### 5. Know the health of your devices and services
The health of devices and services is one of the most important signals used to gain confidence in them.

[Read more](5-know-the-health-of-your-devices-and-services.md)

### 6. Focus your monitoring on devices and services
Given that devices and services are more exposed to network attack than in traditional architectures it’s important that comprehensive monitoring for attacks is carried out.

[Read more](6-focus-your-monitoring-on-devices-and-services.md)

### 7. Set policies according to the value of services or data
The power of a zero trust architecture comes from the access policies you define.

[Read more](7-set-policies-according-to-the-value-of-the-service-or-data.md)

### 8. Control access to your services and data
Each request to a service should be authorised against a policy.

[Read more](8-control-access-to-your-services-and-data.md)

### 9. Don’t trust the network, including the local network
In order to remove trust from the network you need to build trust into the devices and services.

[Read more](9-dont-trust-the-network.md)

### 10. Choose services designed for zero trust

Prefer services with built-in support for zero trust network architectures.

[Read more](10-choose-services-designed-for-zero-trust.md)
