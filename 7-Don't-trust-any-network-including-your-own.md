## 7. Don\'t trust any network, including your own

### Zero trust sees the network as hostile. You must build trust into users, devices and services

Don\'t trust any network between the device and the service it\'s accessing, this includes the local network. Communications over a network, to access data or services, should use a secure transport such as [TLS](https://www.ncsc.gov.uk/guidance/tls-external-facing-services). The device should be configured to prevent attacks that are present on a local network. This includes DNS spoofing, man-in-the-middle attacks and unsolicited inbound connections.

Attacks targeted at foundational network services, such as DNS, can often only be mitigated by encapsulation in a secure transport. For example, you should ensure that the services your users are accessing are protected with authenticated and encrypted protocols. Otherwise, they may still need to be protected by existing solutions, like your corporate [VPN.](https://www.ncsc.gov.uk/collection/mobile-device-guidance/virtual-private-networks)

However you choose to protect network services, [you should be able to apply appropriate monitoring](6-Focus-your-monitoring-on users-devices-and-services.md).

**Enforcing device usage policy**

In a zero trust architecture, network traffic may not be tunnelled back to a central point, meaning that Internet traffic cannot be inspected and monitored. Therefore, the traditional method of enforcing an Internet browsing policy - the blocking of malicious domains and unauthorised use of network protocols - will need to be enforced on the device. Safe web browsing features such as malicious URL and phishing detection should be considered as device security features.

If you can\'t enforce Internet browsing policy using device security features, you may have to route Internet traffic though a managed cloud service, such as a managed cloud proxy.

When using these services, ensure you take into consideration their availability and security posture. Our [cloud security principles](https://www.ncsc.gov.uk/collection/cloud-security/implementing-the-cloud-security-principles) can help you with this.

**General cyber hygiene**

While the network should be treated as hostile and untrusted, maintaining cyber hygiene on the network is still important. For example, monitoring of the local network for unauthorised hosts and patching of network components. This will ensure that the network is performant and available.
