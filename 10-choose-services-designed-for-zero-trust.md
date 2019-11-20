# Choose services designed for zero trust

Prefer services with built-in support for zero trust.

Some services, especially legacy services, may need additional components to enable zero trust. This may increase management overhead and cause usability issues, so ensure you have the resource to take this on.

Creating your own supporting infrastructure should be avoided, due to the cost, complexity and potential for error involved. In this case, as elsewhere, the general cyber security principle of “don’t roll your own” holds true.

Given that in a zero trust architecture, you can’t trust the network, services need to be designed to protect themselves from hostile networks. This includes the internet, to which components could be directly exposed.

Whenever possible, use standards-based technologies. This allows interoperability between devices and services. A good example is authentication, where common standards such as OpenID Connect or SAML allow you to use a single directory service to authenticate to many services.

Unfortunately, there are currently no standards for policies. We recommend that you use a single policy engine and apply the full set of features it offers.