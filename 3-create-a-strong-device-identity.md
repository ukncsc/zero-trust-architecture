# Create a strong device identity

Each device owned by your organisation should be uniquely identifiable in a single device directory. This enables efficient asset management and clear visibility of the devices which access services and your data.

Policies you define later will use compliance and health claims from a device to make decisions about which data it can access and the actions it can perform. A strong identity is required to ensure these claims can be authenticated.

The confidence you can have in a device’s identity depends on the device type, hardware and platform:

* Identity stored on a secure hardware co-processor, like a TPM, will give you high confidence in the device’s identity
* Identity stored on a well-managed device using a software-based key store gives a lower confidence in the device’s identity
* Identity on an unmanaged device in a software-based key store gives a low confidence in the device’s identity

When allowing requests from devices you don’t own and manage, identification can be challenging. Devices in a BYOD model should still have an identity linked to them but the confidence in that device’s identity may be lower.

Identifying devices from another organisation will require a trust relationship to be established between the two organisations. This should happen at both a governance and technical level.