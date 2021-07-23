## 8. Choose services which have been designed for zero trust

### Select services with built-in support for zero trust network architectures

When choosing the components of a zero trust architecture, you should prefer services with built-in support for zero trust.

In a zero trust architecture, you can\'t trust the network, so services need to be designed to protect themselves from all potential sources of attack. This includes the Internet, to which components could be directly exposed.

**Legacy services**

Some services, especially legacy services (services no longer in active development or support), may need additional components to enable zero trust. This could increase management overhead and cause usability issues, so ensure you have the resources to take this on. Please see our [Obsolete products guidance](https://www.ncsc.gov.uk/collection/mobile-device-guidance/managing-the-risks-from-obsolete-products) for more information on how to manage legacy.

**Do not reinvent the wheel**

Creating your own supporting infrastructure should be avoided, due to the cost, complexity and potential for error. In this case, as elsewhere, the general cyber security principle of using products and services that have been designed and built by trained professionals holds true.

**Look for standards**

Whenever possible, use standards-based technologies. This allows interoperability between devices and services. A good example is authentication and authorisation, where common standards such as [OpenID Connect](https://openid.net/connect/), [OAuth 2.0](https://tools.ietf.org/html/rfc6749) or [SAML](https://wiki.oasis-open.org/security/FrontPage) allow interoperability between services and identity providers.

**Managed services in the cloud**

There are a number of cloud hosted services that have been designed for zero trust. It\'s important that you're confident you can trust the vendors running theses services. Our [cloud security principles](https://www.ncsc.gov.uk/collection/cloud-security) can help gain that trust.
