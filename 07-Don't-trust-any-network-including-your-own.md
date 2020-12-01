# 7. Don't trust any network, including your own

In zero trust the network is considered hostile, therefore you need to build trust into users, devices and services rather than the network.

Don't trust any network between the device and the service it's accessing, this includes the local network. The device should be configured to prevent attacks that are present on a local network. This would include DNS spoofing, man in the middle attacks and unsolicited inbound connections.

Attacks targeted at foundational network services, such as DNS, can often only be mitigated at higher layers in the stack. For example, you should ensure that the services your users are accessing are protected with authenticated and encrypted protocols, such as TLS.

Whatever solution you choose to protect foundation network protocols, we recommend that organisations maintain control of their services. For example, your DNS servers should remain in your control so that you can conduct monitoring and filtering.

**Enforcing device usage policy**

In a zero trust architecture, some network traffic is no longer tunnelled back to a central point, so Internet traffic cannot be inspected and monitored. Therefore, the traditional method of enforcing an Internet browsing policy; the blocking of malicious domains and unauthorised use of network protocols, will need to be enforced on the device. 

It could be possible another hop in the network might be required e.g a hosted cloud proxy to provide this functionality. If you do need to hop though a remote service, this could affect the performance and user experience.

Protective monitoring of network connections should also be moved onto the device. Safe messaging and browsing features such as malicious URL and phishing detection should be considered as device security features. 

**General cyber hygiene**

While the network should be treated as hostile and untrusted, maintaining cyber hygiene on the network is still important. For example, monitoring of the local network for unauthorised hosts and patching of network components. This will ensure that the network is performant and available. It's especially important in architectures where you are hosting on-premise services.
