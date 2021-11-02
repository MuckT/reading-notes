# 401 Bearer Authorization

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Client ID | The client_id is a public identifier for apps. |
| Client Secret | The client_secret is a secret known only to the application and the authorization server. It must be sufficiently random to not be guessable. |
| Authentication Endpoint | Endpoint authentication is an authentication mechanism used to verify the identity of a network's external or remote connecting device. This method ensures that only valid or authorized endpoint devices are connected to a network. |
| Access Token Endpoint | Where apps make a request to get an access token for a user. |
| API Endpoint | The place of interaction between applications. |
| Authorization Code | A temporary code that the client will exchange for an access token |
| Access Token | a tiny piece of code that contains a large amount of data. Information about the user, permissions, groups, and timeframes is embedded within one token that passes from a server to a user's device. |

### Write the following steps in the correct order:

1. Register your application to get a client_id and client_secret.
2. Redirect to a third party authentication endpoint.
3. Ask the client if they want to sign in via a third party.
4. Make a request to the access token endpoint.
5. Receive access token.
6. Make a request to a third-party API endpoint.
7. Receive authorization code.

### What can you do with an authorization code?

An authorization code can be stored on a users device to remain logged in without having to request new access tokens and/or send their username and password on every request.


### What can you do with an access token?

An access token is a temporary token used to retrieve a authorization code from a third-party API endpoint, with it you can receive an authorization code.

### What’s a benefit of using OAuth instead of your own basic authentication?

OAuth provides prevents the users credentials from being sent with every request and provide more granularity of access and expiry of the access after a certain date.

## Sources

[Authorization Code Grant](https://www.oauth.com/oauth2-servers/server-side-apps/authorization-code/)

[Access Token: Definition, Architecture, Usage & More](https://www.okta.com/identity-101/access-token/)

[Endpoint – What is an API Endpoint?](https://rapidapi.com/blog/api-glossary/endpoint/)

[The Client ID and Secret](https://www.oauth.com/oauth2-servers/client-registration/client-id-secret/)

[Grant Type Flow](https://developer.okta.com/docs/guides/implement-grant-type/authcode/main/#grant-type-flow)

[Endpoint Authentication](https://www.techopedia.com/definition/23918/endpoint-authentication)

[Access Tokens](https://www.oauth.com/oauth2-servers/access-tokens/)
