# Set policies according to the value of services or data

The power of a zero trust architecture comes from the access policies you define. These policies can take into account a number of signals from the connection in real-time and from the signals database to a build context for the connection. This context is then used to gain confidence in the connection request and decided if it trusted to continue. It's the role of the Policy Engine perform this policy decision.

In the previous principles we talked about building trust in a user’s identity, their devices and services. Signals from these sources can be used to make access decisions. For example, has a user authenticated using a second factor? Is the device they are using compliant with our configuration policies?

Define your policies based on the value of the data to be accessed or action taken. For example, a high impact action, such as creating a new administrator user, should require a stringent policy compared to a relatively low impact operation such as checking the lunch menu. In the latter example, the confidence required to trust the connection is relatively low.

Signals can include the user’s role, physical location, device state, value of the service they are accessing and risk of the action they are preforming. The richness of the policies you define is determined by the policy engine you are using and is closely linked to the user and device state signals available. When choosing which technologies to use for your zero trust architecture evaluate the signals that are available and capabilities of your policy engine.

Depending on your policy engine's capabilities you may be able to request additional signals to in order to get more confidence in a connection. For example, if a user usually requests access to a high value service for the first time or outside of normal working hours your policy engine could ask for an additional factor of authentication.