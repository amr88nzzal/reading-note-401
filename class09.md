# Authorization/Authentication

****

**What header(s) are used in authentication and authorization**

-The WWW-Authenticate and Proxy-Authenticate response headers define the authentication method that should be used to gain access to a resource. They must specify which authentication scheme is used, so that the client that wishes to authorize knows how to provide the credentials

**What is safe to put into a JWT**

- JWS payload : contains verifiable security statements, like the identity of the user.
- JWS signature: used to validate that the token is trustworthy and original.

**How are JWTs validated**

- Check signature. which is used to verify that the token was signed by the sender and not altered in any way.

****

## Document the following Vocabulary Terms

- **RBAC**: Role-based access control (RBAC) is a popular mechanism to enforce authorization in applications. When using RBAC, an application developer defines roles rather than authorizing individual users or groups.

- **User Roles**: It is the permissions that manage resources and what users can do with those resources.

- **JWT Token**: It is the authentication signature which is issued by JWT by passing the pay load and a secret to add more security and keep the user logged in while routes are refreshing.