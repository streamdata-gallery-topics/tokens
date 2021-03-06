swagger: "2.0"
x-collection-name: Authentiq Connect
x-complete: 1
info:
  title: Authentiq Connect
  description: authentiq-connect-oauth-2-0-and-openid-connect-api-reference-learn-about-authentiq-idhttpswww-authentiq-com-or-check-out-the-authentiq-connecthttpsdevelopers-authentiq-com-developer-documentation-
  termsOfService: https://www.authentiq.com/tos/
  contact:
    name: Team Authentiq
    url: https://www.authentiq.com/
    email: hello@authentiq.com
  version: "1.0"
host: connect.authentiq.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /token:
    post:
      summary: Obtain an ID Token
      description: |-
        Exchange en authorization code for an ID Token or Access Token.

        This endpoint supports both `client_secret_post` and `client_secret_basic` authenticatino methods, as specified by the client's `token_endpoint_auth_method`.

        See also:
          - [OIDC Token Endpoint](http://openid.net/specs/openid-connect-core-1_0.html#TokenRequest)
          - [OIDC Successful Token response](http://openid.net/specs/openid-connect-core-1_0.html#TokenResponse)
          - [OIDC Token Error response](http://openid.net/specs/openid-connect-core-1_0.html#TokenError)
      operationId: token
      x-api-path-slug: token-post
      parameters:
      - in: header
        name: Authorization
        description: HTTP Basic authorization header
      - in: formData
        name: client_id
        description: The registered client ID
      - in: formData
        name: client_secret
        description: The registered client ID secret
      - in: formData
        name: code
        description: The authorization code previously obtained from the Authentication
          endpoint
      - in: formData
        name: grant_type
        description: The authorization grant type, must be `authorization_code`
      - in: formData
        name: redirect_uri
        description: The redirect URL that was used previously with the Authentication
          endpoint
      responses:
        200:
          description: OK
      tags:
      - Token