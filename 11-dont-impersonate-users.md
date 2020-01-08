# Don't impersonate users

Do not empower services to take actions on behalf of end-users without their consent.

In applications and systems with multiple components, it is common for an application to need to make a request on behalf of an end user to another service to fulfill this users request.

An application making a call on behalf of the end-user may have to authenticate itself to a back end service to make the request, but if there is no artifact of an end-user request associated with this request to the back end, then we have empowered this application or any adversary in control of it to impersonate end users within the architecture.

Wherever possible, artifacts of end-user consent should be included with requests to back end services so that we can have greater confidence that this request originated from the end-user. This is best displayed in the RFC standard for "OAuth Token Exchange", where a system must use the end-user's Access Token and authenticate itself to a central authorization server for the right to call a back end service on behalf of an end-user.


Please note it is not desireable to replay artifacts like an end-user's session token to the front-end application within a system as this increases the chance that it may become compromised.


