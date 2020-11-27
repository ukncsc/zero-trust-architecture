# 8. Choose services designed for zero trust

Prefer services with built-in support for zero trust.

Given that in a zero trust architecture, you can't trust the network, services need to be designed to protect themselves. This includes the Internet, to which components could be directly exposed.

**Legacy services**

Some services, especially legacy services (services no longer in active development), may need additional components to enable zero trust. This may increase management overhead and cause usability issues, so ensure you have the resources to take this on.

**Do not reinvent the wheel**

Creating your own supporting infrastructure should be avoided, due to the cost, complexity and potential for error. In this case, as elsewhere, the general cyber security principle of using products and services that have been designed and built by trained professionals holds true.

**Look for standards**

Whenever possible, use standards-based technologies. This allows interoperability between devices and services. A good example is authentication and authorisation, where common standards such as [OpenID Connect](https://openid.net/connect/), OAuth or [SAML](https://wiki.oasis-open.org/security/FrontPage) allow you to use a single directory service to authenticate to many services.

Unfortunately, there are currently no standards for policies. However, we recommend that you use a single policy engine and apply the full set of features it offers.
