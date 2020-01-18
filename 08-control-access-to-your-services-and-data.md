# Control access to your services and data

Each request to a service should be authorised against a policy. Use products and protocols that support this continuous authentication and authorisation process, while protecting your data in transit with encryption.

A zero trust architecture includes a component which mediates connections to services. This is a Policy Enforcement Point which actively applies the access policy you have defined based on a response from the Policy Engine.

How this is achieved practically depends on the zero trust supporting infrastructure you use and the flavour of zero trust technologies you deploy.

If using software defined perimeter (SDP), the policy enforcement point is usually the SDP controller that controls connections from a central location which may also be the Policy Engine. Enforcement points will focus on properties of the network connection to control access, for example which network protocols can be used, the origin of the connection, the network segments that can communicate based on the policy.

When using micro-segementation there is often a gateway in the form of a reverse proxy component. This component can enforce policy at many layers, from the network layer through to the application layer. At the application layer the gateway would need to understand the protocols being used by the application and how they are used. This may require complex logic in both the policy engine and the enforcement point.

Often in a cloud environment you may control access using an authentication and authorisation broker which provides single sign-on functionality to variety of applications. Enforcement is usually session based, policies will be assessed as a connection is established and the broker provides a short lived access token which allows users connect to the services they originally requested.

You may use a combination of the options above, or even different ways, to control access to your services and data. Regardless of how you design your zero trust architecture the component should only allow connections if the access policies you define are satisfied. As monitoring is important in a zero trust architecture your enforcement point should support logging connections and their properties.

## Other considerations
When an access decision is denied consider how the user will be informed about the reasons why. Too much information may facilitate an attacker, too little may frustrate a legitimate user.

Should an emergency arise where access to data is critical, you may need to have a process in place which allows a connection to be established even if an access policy can't be satisfied. In such a scenario the risk needs to be managed carefully to prevent this feature being abused. For example, limit the risk of emergency access by allowing an individual user account, a specific device, from a specific location, for a limited time.