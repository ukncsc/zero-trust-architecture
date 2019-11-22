# Create a single strong user identity

Your organisation should use a single user directory and create accounts that are linked to individuals.

To enable granular access control, create specific roles for each user. Ensure the directory can be employed by all the services you plan to use, both internal and external. This will also help when accessing other organisation's services and data.

**Desirable features of an identity service include:**

* Create groups
* Define roles
* Support for strong, modern authentication methods such as multi-factor authentication or even passwordless authentication
* Easily, but securely, distribute credentials to users
* Authenticate to external services (e.g. SAML 2.0 or OpenID Connect)
* Manage user identities in external services (e.g. SCIM 2.0)
* Support for your joiners, movers, and leavers processes

If you have an existing directory, migrating to another directory will require careful planning. Some directory services allow you to import, synchronise or federate between directories, this would allow a phased approach to migration from your legacy directory service to one which supports a zero trust architecture.

Service accounts, keys, tokens and so on, should also be created in a central directory, with tightly defined permissions which are the minimum necessary to allow the service to function properly.

You should also consider how you’ll offer access to the resources your organisation controls, to people from outside your organisation. Your services should be able to use external identity providers to allow access to appropriate services and data. For example, a visitor can see the lunch menu, or a contractor can only access documents related to their work.

Identity is a wide-ranging topic and needs careful consideration as it's a foundational service for zero trust architectures. The NCSC has more in-depth [guidance on identity and access management](https://www.ncsc.gov.uk/guidance/introduction-identity-and-access-management).