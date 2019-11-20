# Don’t trust the network, including the local network

In order to remove trust from the network you need to build trust into the devices and services.

Don’t trust any network between the device and the service it’s accessing. This includes the local network, the device should be configured to prevent DNS spoofing, Man in the Middle attacks, unsolicited inbound connections etc.

Attacks targeted at foundation network services, such as DNS, can often only be mitigated at higher layers in the stack, for example ensure that services your users are accessing are protected with authenticated and encrypted protocols, such as TLS.

While the network should be treated as hostile and untrusted, maintaining cyber hygiene and good standards on the network is still important ensuring they are performant and available. This is especially important in architectures where you are hosting on-premise services.