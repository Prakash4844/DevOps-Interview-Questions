# SSO - Single Sign-On

SSO stands for Single Sign-On. It's a system that allows users to access multiple applications with just one set of login credentials. This means users don't have to remember multiple passwords for different services, improving convenience and security.

Single Sign-On (SSO) is a centralized authentication process that enables users to log in once and gain access to multiple applications or systems without being prompted to log in again at each of them. Here's how it typically works:

1. **Authentication:** When a user attempts to access an application, they are redirected to a centralized authentication service, often called the Identity Provider (IdP). Here, they enter their credentials (username and password).
2. **Authorization:** The IdP verifies the user's identity and grants a token or session cookie that confirms the user's authentication status.
3. **Access to Applications:** With the token or session cookie, the user is granted access to other applications or services that are configured to trust the IdP. Instead of requiring the user to log in again, these applications accept the token as proof of authentication.

Benefits of SSO include:

* **Improved User Experience:** Users don't need to remember multiple passwords or log in repeatedly, leading to a smoother and more efficient user experience.
* **Enhanced Security:** Centralized authentication can enforce stronger password policies, multi-factor authentication, and better monitoring of user access.
* **Reduced IT Burden:** SSO reduces the administrative overhead of managing multiple user accounts and passwords across various systems.
* **Auditability and Compliance:** SSO provides centralized logging and reporting capabilities, which can assist in compliance audits and security investigations.

SSO implementations can vary based on factors such as the choice of protocols (like SAML, OAuth, OpenID Connect), deployment models (on-premises or cloud-based), and integration with existing identity management systems.

---

Here's an overview of each of the main protocols used for implementing Single Sign-On (SSO):

1. **Security Assertion Markup Language (SAML):**

   - SAML is an XML-based protocol used for exchanging authentication and authorization data between the Identity Provider (IdP) and Service Provider (SP).
   - In the SAML flow, when a user attempts to access a service, the SP requests authentication from the IdP.
   - The IdP then authenticates the user and generates a SAML assertion, which contains information about the user's identity and permissions.
   - The IdP sends this assertion back to the SP, which verifies it and grants access to the user.
2. **OAuth:**

   - OAuth is an open standard for authorization that enables secure access to resources without sharing passwords.
   - It is commonly used for delegated authorization scenarios, such as allowing third-party applications to access user data on their behalf.
   - OAuth operates through the exchange of tokens, including access tokens, refresh tokens, and authorization codes.
   - It does not provide authentication itself but rather facilitates authorization between different services.
3. **OpenID Connect (OIDC):**

   - OpenID Connect is a simple identity layer built on top of OAuth 2.0, providing authentication services in addition to authorization.
   - It adds an authentication layer on top of OAuth's authorization framework, allowing clients to verify the identity of the end-user based on the authentication performed by an Authorization Server.
   - OIDC uses JSON Web Tokens (JWTs) to convey identity information, such as user ID and authentication status.
   - It provides a standardized way for clients to obtain identity information about users, making it well-suited for SSO scenarios.

Each of these protocols has its strengths and use cases, and the choice of protocol depends on factors such as the specific requirements of the application, interoperability with existing systems, and security considerations.

---

---

## SAML - Security Assertion Markup Language

Security Assertion Markup Language (SAML), a widely used protocol for implementing Single Sign-On (SSO):

**1. Overview:**

- SAML is an XML-based open standard for exchanging authentication and authorization data between identity providers (IdPs) and service providers (SPs).
- It enables secure SSO by allowing users to authenticate once with an identity provider and then access multiple services without needing to log in again.

**2. Components of SAML:**

Here are the main components of SAML:

1. **Assertions:**
   * Assertions are the core component of SAML.
   * They are XML documents containing statements about a user, such as authentication statements (confirming the user's identity) and attribute statements (providing information about the user's attributes and permissions).
   * Assertions are issued by the Identity Provider (IdP) and consumed by the Service Provider (SP) during the authentication process.
   * There are three main types of assertions in SAML:
     * **Authentication Assertion:** Confirms the identity of the user.
     * **Attribute Assertion:** Provides information about the user's attributes and permissions.
     * **Authorization Decision Assertion:** Indicates whether the user is authorized to access a specific resource.
2. **Protocols:**
   * SAML defines several protocols for different aspects of identity management, including authentication, authorization, and attribute exchange.
   * These protocols specify the messages exchanged between the IdP and SP during the SSO process.
   * Some of the key SAML protocols include:
     * **Authentication Request Protocol:** Defines how the SP requests authentication from the IdP.
     * **Single Logout Protocol:** Allows users to log out from all participating services in a single action.
     * **Artifact Resolution Protocol:** Defines how artifacts, such as assertion references, are resolved and exchanged between the IdP and SP.
3. **Bindings:**
   * Bindings define how SAML messages are transmitted over different communication protocols.
   * They specify the mechanisms for encoding SAML messages into standard formats, such as HTTP POST, HTTP Redirect, and SOAP.
   * Common SAML bindings include:
     * **HTTP POST Binding:** SAML messages are encoded as HTML form parameters and sent via HTTP POST requests.
     * **HTTP Redirect Binding:** SAML messages are embedded as URL query parameters and sent via HTTP Redirect responses.
     * **SOAP Binding:** SAML messages are encapsulated within SOAP envelopes and transmitted using SOAP-based web services.
4. **Metadata:**
   * Metadata provides information about SAML entities, including the IdP and SP.
   * It includes details such as entity IDs, endpoints, supported bindings, public keys, and certificate information.
   * Metadata is typically exchanged between IdPs and SPs during the configuration and setup process to facilitate integration and interoperability.

**3. SAML Roles:**

- **Identity Provider (IdP):** The IdP authenticates users and provides SAML assertions to service providers upon successful authentication.
- **Service Provider (SP):** The SP consumes SAML assertions from the IdP to grant access to its resources or services.

**4. SAML Workflow:**

- **Authentication Request:**
  1. The user attempts to access a service provided by the SP.
  2. The SP redirects the user to the IdP's Single Sign-On Service (SSO Service) with an authentication request.
- **Authentication:**
  3. The IdP authenticates the user using its own authentication mechanism (e.g., username/password, multi-factor authentication).
  4. Upon successful authentication, the IdP generates a SAML assertion containing information about the user's identity, attributes, and possibly other details.
- **Assertion Delivery:**
  5. The IdP sends the SAML assertion back to the user's browser, which then redirects it to the SP's Assertion Consumer Service (ACS).
- **Assertion Processing:**
  6. The SP receives the SAML assertion, verifies its authenticity (e.g., signature validation), and extracts the user's identity and attributes.
- **Authorization and Access:**
  7. Based on the information in the SAML assertion, the SP grants the user access to the requested service.

**5. SAML Profiles:**

- **Web Browser SSO:** This is the most common SAML profile, where the user interacts with web browsers to access services.
- **Single Logout:** Allows users to log out from all participating services in a single action.
- **Enhanced Client or Proxy (ECP):** Enables SSO for non-browser clients, such as desktop applications or mobile devices.

**6. Advantages of SAML:**

- **Interoperability:** SAML is widely supported by various platforms, making it suitable for integrating different systems and services.
- **Security:** SAML assertions can be digitally signed and encrypted, ensuring the integrity and confidentiality of user data.
- **Centralized Control:** SAML enables centralized management of user authentication and access control policies.

**7. Limitations of SAML:**

- **Complexity:** SAML implementations can be complex and require careful configuration and maintenance.
- **Performance:** SAML relies on XML-based messaging, which can introduce overhead and affect performance, especially in high-traffic environments.
- **Limited Flexibility:** SAML's XML-based structure may limit its flexibility in certain use cases compared to newer protocols like OAuth 2.0 and OpenID Connect.

![What is SAML (Security Assertion Markup Language) and how does SAML work?](https://www.entrust.com/-/media/entrust/resources/faq/img-illustration-saml-flow.svg?la=en&hash=D23D44890AB996FF49E3178C341ECD2B)

Despite its complexities, SAML remains a widely adopted and trusted protocol for implementing SSO in enterprise environments, particularly for scenarios requiring strong security and interoperability.

---

---

## OAUTH - Open Authorization

OAuth (Open Authorization) is an open standard for authorization that enables secure access to resources without sharing credentials, making it a key component in Single Sign-On (SSO) systems. Here's a detailed overview of OAuth in the context of SSO:

**1. Overview:**

* OAuth is primarily designed for delegated authorization, allowing users to grant third-party applications limited access to their resources on a server.
* While OAuth itself does not provide authentication (confirming the user's identity), it is often used in conjunction with authentication protocols like OpenID Connect for SSO scenarios.
* OAuth operates through the exchange of tokens, including access tokens, refresh tokens, and authorization codes, to grant access to protected resources.

**2. Components of OAuth:**

* **Resource Owner:** The entity that owns the resources and grants access to them. In the context of SSO, the resource owner is typically the user.
* **Client:** The third-party application requesting access to the user's resources. This could be a web application, mobile app, or desktop client.
* **Authorization Server:** The server responsible for authenticating the user and issuing access tokens to the client.
* **Resource Server:** The server hosting the protected resources that the client wants to access. This could be an API or web service.

**3. OAuth Workflow:**

* **Authorization Request:**
  1. The client requests authorization from the resource owner to access their resources.
  2. The authorization request typically includes the desired scope of access and redirection URI where the authorization server should send the response.
* **User Authentication:** 3. The resource owner authenticates with the authorization server, either directly or through a third-party identity provider (IdP).
* **Authorization Grant:** 4. Upon successful authentication, the authorization server issues an authorization code or access token to the client.
* **Token Exchange:** 5. The client exchanges the authorization code for an access token, which it can use to access the protected resources on the resource server.
* **Accessing Resources:** 6. The client presents the access token to the resource server when requesting access to protected resources.
* **Token Renewal (optional):** 7. If the access token expires, the client can use a refresh token to obtain a new access token without requiring the user to reauthenticate.

**4. OAuth Profiles:**

* OAuth defines several profiles for different use cases and scenarios, including:
  * **Authorization Code Flow:** Suitable for web server applications where the client can securely store credentials.
  * **Implicit Flow:** Suitable for client-side applications like single-page web apps (SPAs) where the client cannot securely store credentials.
  * **Client Credentials Flow:** Used for machine-to-machine communication where the client is the resource owner.
  * **Resource Owner Password Credentials Flow:** Allows the client to directly exchange the user's credentials for an access token (less secure and less common in SSO scenarios).

**5. Advantages of OAuth for SSO:**

* **Delegated Access:** OAuth allows users to delegate access to their resources without sharing their credentials with third-party applications.
* **Scalability:** OAuth is designed to scale for a wide range of use cases, from simple user authentication to complex authorization scenarios.
* **Standardization:** OAuth is a widely adopted standard with robust security features and support across various platforms and frameworks.

**6. Limitations of OAuth for SSO:**

* **Authentication Gap:** OAuth itself does not provide authentication, so it needs to be combined with other protocols like OpenID Connect for full SSO functionality.
* **Complexity:** Implementing OAuth for SSO can be complex, especially when dealing with multiple clients, authorization scopes, and token management.
* **Security Considerations:** OAuth implementations must carefully consider security best practices, such as token validation, authorization checks, and token revocation mechanisms.


In summary, OAuth plays a crucial role in SSO by providing secure and delegated access to resources while allowing users to maintain control over their credentials and data. When combined with authentication protocols like OpenID Connect, OAuth forms the foundation for modern SSO solutions across diverse application environments.

---

---

## OIDC - OpenID Connect


OpenID Connect (OIDC) is an identity layer built on top of OAuth 2.0, providing authentication services in addition to authorization. It is widely used for implementing Single Sign-On (SSO) and identity federation in modern web and mobile applications. Here's a detailed overview of OIDC:

**1. Overview:**

- OIDC is designed to provide a standardized way for clients to verify the identity of end-users based on the authentication performed by an Authorization Server (AS), which is typically part of an OpenID Connect Provider (OP).
- It extends OAuth 2.0 with additional features for user authentication, identity verification, and information exchange.
- OIDC defines several flows for different client types and use cases, including web applications, single-page applications (SPAs), native mobile apps, and server-to-server communication.

**2. Components of OIDC:**

OpenID Connect (OIDC) consists of several key components that work together to provide authentication and identity verification services in the context of Single Sign-On (SSO) and identity federation. Here are the main components of OIDC:

1. **OpenID Connect Provider (OP):**

   - The OpenID Connect Provider (OP), also known as the Identity Provider (IdP), is the server responsible for authenticating users and issuing identity tokens.
   - It includes the Authorization Server (AS) component, which handles user authentication and token issuance.
   - The OP exposes various endpoints and services for authentication, token issuance, user information retrieval, and session management.
2. **Client:**

   - The client is the application or service that interacts with the OP to authenticate users and obtain identity information.
   - It can be a web application, single-page application (SPA), native mobile app, or even a server-side application.
   - Clients are registered with the OP and obtain client credentials (client ID and client secret) to authenticate and interact with the OP's endpoints.
3. **End-User:**

   - The end-user is the person who is trying to authenticate with the OP and access resources protected by the client.
   - End-users interact with the client application's user interface to initiate the authentication process and provide their credentials to the OP.
4. **ID Token:**

   - The ID Token is a JSON Web Token (JWT) issued by the OP to authenticate the end-user and provide identity information to the client.
   - It contains claims such as the user's unique identifier (sub), name, email address, and other profile attributes.
   - The ID Token is digitally signed by the OP and can be verified by the client to ensure its authenticity.
5. **UserInfo Endpoint:**

   - The UserInfo endpoint is exposed by the OP and allows clients to retrieve additional information about the authenticated user.
   - Clients can make requests to the UserInfo endpoint, providing the ID Token as an access token, to obtain user profile attributes and other information.
6. **Discovery Endpoint:**

   - The Discovery endpoint allows clients to dynamically discover and obtain metadata about the OP, including its endpoints, supported scopes, and cryptographic keys.
   - Clients can use the Discovery endpoint to programmatically retrieve configuration information and integrate with the OP without hardcoding URLs.
7. **Session Management:**

   - OIDC supports session management features to manage user sessions across multiple applications and devices.
   - This includes session cookies, session state parameters, and logout endpoints that allow users to log out from all participating applications in a single action.
8. **Scope:**

   - Scopes define the level of access and the types of identity information that the client is requesting from the OP.
   - Standard OIDC scopes include openid (required for OIDC authentication), profile, email, and address, among others.
   - Clients specify the desired scopes in the authorization request to indicate the types of claims they want to receive in the ID Token.

These components work together to enable secure authentication and identity verification in OIDC-based SSO systems, allowing clients to authenticate users and obtain identity information in a standardized and interoperable manner.

**3. OIDC Workflow:**

- **Authorization Request:**
  1. The client initiates the authentication process by redirecting the user to the OP's authorization endpoint.
  2. The client includes the requested scope, response type, and redirection URI in the authorization request.
- **User Authentication:**
  3. The OP authenticates the user using its own authentication mechanisms, such as username/password, social login, or multi-factor authentication.
  4. Upon successful authentication, the OP issues an ID Token containing information about the user's identity.
- **Token Exchange:**
  5. The OP returns the ID Token to the client via the redirection URI specified in the authorization request.
  6. The client verifies the ID Token's signature, validates its claims, and extracts the user's identity and other relevant information.
- **Accessing Resources:**
  7. The client uses the ID Token to grant access to protected resources or services, typically by including it in API requests as a bearer token.
- **Optional Refresh Token (for long-lived sessions):**
  8. Optionally, the OP may also issue a refresh token, allowing the client to obtain new ID Tokens without requiring the user to reauthenticate.

**4. OIDC Features:**

- **ID Tokens:** OIDC introduces the concept of ID Tokens, which are JSON Web Tokens (JWTs) containing identity information about the authenticated user.
- **UserInfo Endpoint:** OPs expose a UserInfo endpoint where clients can retrieve additional information about the user, such as profile attributes and email addresses.
- **Discovery:** OIDC provides a Discovery mechanism that allows clients to dynamically discover and obtain metadata about the OP, including endpoints, supported scopes, and cryptographic keys.
- **Session Management:** OIDC supports session management features, such as session cookies and logout endpoints, to manage user sessions across multiple applications.

**5. Advantages of OIDC:**

- **Authentication and Authorization:** OIDC combines authentication and authorization in a single protocol, simplifying the implementation of SSO and identity federation.
- **Standardization:** OIDC is a widely adopted standard with support across various platforms and frameworks, ensuring interoperability and compatibility.
- **Security:** OIDC provides robust security features, including token validation, signature verification, and encryption, to protect user identity and data.

**6. Limitations of OIDC:**

- **Complexity:** Implementing OIDC can be complex, especially for clients that require support for multiple flows and scenarios.
- **Dependency on OAuth 2.0:** OIDC builds upon OAuth 2.0, so clients must also understand OAuth concepts and workflows to use OIDC effectively.

![architectural diagram](https://learn.microsoft.com/en-us/entra/architecture/media/authentication-patterns/oidc-auth.png)

In summary, OIDC provides a standardized and secure way for clients to authenticate users and obtain identity information, making it a powerful tool for implementing SSO and identity federation in modern applications and services.

---



Here's a comparison table highlighting the main differences between SAML, OAuth, and OIDC:


| Feature             | SAML                                                                                             | OAuth                                                                                                     | OpenID Connect (OIDC)                                                                           |
| ------------------- | ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| **Purpose**         | Single Sign-On (SSO) and attribute exchange                                                      | Delegated Authorization                                                                                   | Authentication and Authorization with identity token                                            |
| **Protocol Type**   | XML-based                                                                                        | Token-based                                                                                               | Token-based                                                                                     |
| **Authentication**  | Yes                                                                                              | No (Authentication is delegated to Identity Provider)                                                     | Yes                                                                                             |
| **Authorization**   | No                                                                                               | Yes                                                                                                       | Yes                                                                                             |
| **Assertion Type**  | XML assertions                                                                                   | Access tokens, refresh tokens                                                                             | ID Tokens, access tokens, refresh tokens                                                        |
| **Token Format**    | N/A (Uses XML)                                                                                   | Typically JSON Web Tokens (JWTs)                                                                          | Typically JWTs                                                                                  |
| **Security**        | SAML assertions can be digitally signed and encrypted                                            | Tokens can be encrypted, but not signed                                                                   | Tokens are digitally signed and optionally encrypted                                            |
| **Scope**           | Limited to authentication and attribute exchange                                                 | Authorization for resource access                                                                         | Authentication, attribute exchange, and authorization                                           |
| **Profiles**        | Web Browser SSO, Single Logout, Enhanced Client/Proxy (ECP), etc.                                | Authorization Code Flow, Implicit Flow, Client Credentials Flow, Resource Owner Password Credentials Flow | Authorization Code Flow, Implicit Flow, Hybrid Flow, Client Credentials Flow, Device Flow, etc. |
| **Bindings**        | HTTP POST, HTTP Redirect, SOAP                                                                   | N/A                                                                                                       | N/A                                                                                             |
| **Usage**           | Commonly used in enterprise environments for SSO between organizations or within an organization | Widely used for delegated authorization in APIs and microservices                                         | Commonly used for authentication and SSO in web and mobile applications                         |
| **Standardization** | Standardized by OASIS                                                                            | Standardized by IETF                                                                                      | Standardized by OpenID Foundation                                                               |
| **Complexity**      | Can be complex due to XML format and various profiles                                            | Can be complex depending on the flow and use case                                                         | Can be complex due to interactions between authentication and authorization                     |


---

Author(s): Prakash Sahu

Contributor(s):
