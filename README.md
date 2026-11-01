# OAuth & Identity Education Notes

*Author: Jayesh Sharma*

A beginner-friendly study library on **OAuth 2.0, OpenID Connect (OIDC), Identity and Access Management (IAM), Auth0, authentication, authorization and architecture patterns**. Each guide has original explanations, Mermaid diagrams, practical security rules and interview questions.

**Documentation basis:** [Auth0 — Identity Fundamentals](https://auth0.com/docs/get-started/identity-fundamentals). The source documentation groups content into Identity Fundamentals, Authentication and Authorization Flows, and Architecture Scenarios. These notes preserve that structure and link to the relevant primary documentation.

> **Scope:** These are independently written study notes; they are not reproductions of Auth0 text. Several OAuth flow topics are summarized using Auth0's official flow overview, rather than every nested implementation-specific article. Supplemental examples, tables and diagrams are clearly educational explanations. Verify security configurations and protocol requirements against current standards and official Auth0 documentation.

## Study Library

### Identity Fundamentals

- [Introduction to Auth0](01_Identity_Fundamentals/Introduction_to_Auth0.md)
- [Introduction to Identity and Access Management](01_Identity_Fundamentals/Introduction_to_IAM.md)
- [Authentication vs Authorization](01_Identity_Fundamentals/Authentication_vs_Authorization.md)

### Authentication and Authorization Flows

- [Which OAuth 2.0 Flow Should I Use?](02_Authentication_and_Authorization_Flows/Choosing_an_OAuth_2_Flow.md)
- [Authorization Code Flow](02_Authentication_and_Authorization_Flows/Authorization_Code_Flow.md)
- [Authorization Code Flow with PKCE](02_Authentication_and_Authorization_Flows/Authorization_Code_with_PKCE.md)
- [Client Credentials Flow](02_Authentication_and_Authorization_Flows/Client_Credentials_Flow.md)
- [Device Authorization Flow](02_Authentication_and_Authorization_Flows/Device_Authorization_Flow.md)
- [Implicit Flow with Form Post (Legacy)](02_Authentication_and_Authorization_Flows/Implicit_and_Form_Post.md)
- [OIDC Hybrid Flow](02_Authentication_and_Authorization_Flows/Hybrid_Flow.md)
- [Resource Owner Password Flow (Legacy)](02_Authentication_and_Authorization_Flows/Resource_Owner_Password_Flow.md)
- [Client-Initiated Backchannel Authentication](02_Authentication_and_Authorization_Flows/CIBA_Flow.md)
- [Custom Token Exchange](02_Authentication_and_Authorization_Flows/Custom_Token_Exchange.md)
- [Private Key JWT Client Authentication](02_Authentication_and_Authorization_Flows/Private_Key_JWT.md)
- [Mutual TLS (mTLS)](02_Authentication_and_Authorization_Flows/Mutual_TLS.md)
- [Client Credentials Exchange Extensibility](02_Authentication_and_Authorization_Flows/Client_Credentials_Exchange_Extensibility.md)

### Architecture Scenarios

- [Business to Employees](03_Architecture_Scenarios/Business_to_Employees.md)
- [Business to Consumer](03_Architecture_Scenarios/Business_to_Consumer.md)
- [Business to Business](03_Architecture_Scenarios/Business_to_Business.md)
- [Multiple Organization Architecture](03_Architecture_Scenarios/Multiple_Organization_Architecture.md)
- [SSO for Regular Web Apps](03_Architecture_Scenarios/SSO_for_Regular_Web_Apps.md)
- [Server Application with API](03_Architecture_Scenarios/Server_Application_with_API.md)
- [SPA with API](03_Architecture_Scenarios/Single_Page_App_with_API.md)
- [Mobile Application with API](03_Architecture_Scenarios/Mobile_Application_with_API.md)
- [Implementation Planning Checklists](03_Architecture_Scenarios/Implementation_Planning_Checklists.md)
- [Implementation Resources](03_Architecture_Scenarios/Implementation_Resources.md)

## Suggested learning path

1. **Identity fundamentals:** Learn authentication, authorization, IAM, IdPs, scopes and token purposes.
2. **OAuth/OIDC flows:** Understand authorization code, PKCE, M2M client credentials, device authorization and advanced client authentication.
3. **Architectures:** Apply the concepts to enterprise SSO, multi-tenant B2B apps, mobile/SPA/API integration and deployment planning.
4. **Practice:** For each guide, draw the message sequence, predict a failure, and validate what the resource API must independently check.

## Important security notes

- **OAuth 2.0 is primarily authorization; OIDC adds standardized authentication.**
- Use **authorization code with PKCE** for modern interactive public clients; avoid resource owner password and implicit-token patterns in new designs.
- Access tokens are intended for APIs. **ID tokens are not API access tokens.**
- An API should check issuer, signature, audience, expiry and applicable scopes or permissions.
- Never commit client secrets, access tokens, private keys, or refresh tokens.
- Auth0's legacy **Rules and Hooks reach end of life November 18, 2026**. Use supported **Actions** extensibility for new integrations; verify current migration guidance.

## References

- [Auth0 Identity Fundamentals](https://auth0.com/docs/get-started/identity-fundamentals)
- [Auth0 Authentication and Authorization Flows](https://auth0.com/docs/get-started/authentication-and-authorization-flow)
- [Auth0 Architecture Scenarios](https://auth0.com/docs/get-started/architecture-scenarios)
- [OAuth 2.0 RFC 6749](https://www.rfc-editor.org/rfc/rfc6749)
- [OpenID Connect Core](https://openid.net/specs/openid-connect-core-1_0.html)
