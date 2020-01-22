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

## Don't impersonate users

Do not empower services to take actions on behalf of end-users without their consent. A strong user identity is undone when components of a network can impersonate your users.

In applications and systems with multiple components, it is common for an application to need to make a request on behalf of an end user to another service to fulfill this users request.

An application making a call on behalf of the end-user may have to authenticate itself to a back end service to make the request, but if there is no artifact of an end-user request associated with this request to the back end, then we have empowered this application or any adversary in control of it to impersonate end users within the architecture.

Wherever possible, artifacts of end-user consent should be included with requests to back end services so that we can have greater confidence that this request originated from the end-user. This is best displayed in the RFC standard for "OAuth Token Exchange", where a system must use the end-user's Access Token and authenticate itself to a central authorization server for the right to call a back end service on behalf of an end-user.


Please note it is not desireable to replay artifacts like an end-user's session token to the front-end application within a system as this increases the chance that it may become compromised.
