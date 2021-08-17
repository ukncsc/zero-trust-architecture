## Introduction to Zero Trust

A zero trust architecture is an approach to system design where inherent trust in the network is removed. Instead, the network is assumed hostile and each access request is verified, based on an access policy.

Confidence in the trustworthiness of a request is achieved by building context, which in turn relies upon strong authentication, authorisation, device health, and value of the data being accessed.

If you are unsure whether zero trust is the correct network architecture for your needs, or if you are new to zero trust, our [network architectures guidance](https://www.ncsc.gov.uk/collection/device-security-guidance/infrastructure/network-architectures#section_2) is a good place to start.

## **Key concepts**

When reading and applying our zero trust principles there are some key concepts to keep in mind.

### The network is hostile

The network should be treated as compromised and therefore hostile, This means you need to remove trust from the network.

In a zero trust architecture, inherent trust is removed from the network. Just because you\'re connected to a network, doesn\'t mean you should be able to access everything on that network. Each request to access data or a service should be authenticated and authorised against an access policy. If a connection does not satisfy the access policy, the connection is dropped. 

It is common in breaches to see an attacker gain a foothold on a network and then move laterally. This is possible because everything and everyone already on the network is trusted with access to the rest of the network. In a zero trust architecture, the network is treated as hostile, so every request for data or service access is continually verified against an access policy. This will also improve monitoring and detection of attempts at lateral movement by an attacker, compared to a traditional wall garden, but zero trust won\'t completely remove the threat.  

### Gain confidence dynamically

If you remove trust from the network, you must instead gain confidence in your users, devices, and services. Rather than taking a snapshot as the user, device or service connects to your network and allowing the resulting permission to persist, you should look to continuously evaluate the trustworthiness of those connections.

For users accessing services, you must build trust in user identity and behaviour and device health before they can access the service. For services interacting with each other, such as data exchange using an API, this is achieved by ensuring the right services are communicating with each other and gaining trust in the health of the services your hosting.

How much confidence you need in order to trust a connection depends on the value of data being accessed, or the impact of the action being requested. 

For example, accessing sensitive personal data could require an access policy which specifies a list of authorised users with strong authentication, on a device which belongs to the organisation and is in a healthy state, based on defined configuration policies such as encryption, patch levels and secure boot being enabled.

On the other hand, accessing low value data, such the lunch menu, may be done by anyone in the organisation, regardless of their strength of authentication or device health.

## **Terminology**

When discussing zero trust architectures, it\'s useful to have a common vocabulary. Below are some terms used throughout the zero trust principles. We\'ve tried to closely align these terms with other sources, to help when discussing zero trust technologies. 

-   **Access Policy** - The requirements for an access request to be trusted and authorised.

-   **Configuration Policy** - Policies that describe configuration options for devices and services.

-   **Signal** - A piece of information like *device health* or *location* that can be used to gain confidence in the trustworthiness of an asset. You will often use a number of signals to make a decision whether to grant access to a resource. 

-   **Policy Engine** - The component that takes signals and compares them with access policies to determine an access decision. 

-   **Policy Enforcement Point** - Mediates requests from a user or a device to a service or data using the Policy Engine to determine if the requests can be authorised.

-   **Device health** - Confidence that a device is compliant with configuration policies, and is in a good state. For example, the latest patches have been installed, or a feature like secure boot is enabled. 
