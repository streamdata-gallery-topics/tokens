---
swagger: "2.0"
x-collection-name: Context.IO
x-complete: 0
info:
  title: Context.IO Post Connect Tokens
  description: Obtains a new connect_token.
  version: 1.0.0
host: api.context.io
basePath: /2.0/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /connect_tokens:
    get:
      summary: Get Connect Tokens
      description: Lists connect tokens created with your API key.
      operationId: listConnectTokens_
      x-api-path-slug: connect-tokens-get
      responses:
        200:
          description: OK
      tags:
      - Connect
      - Tokens
    post:
      summary: Post Connect Tokens
      description: Obtains a new connect_token.
      operationId: Create_obtainNewConnectToken_
      x-api-path-slug: connect-tokens-post
      parameters:
      - in: query
        name: callback_url
        description: When the users mailbox is connected to your API key, the browser
          will call this url (GET)
      - in: query
        name: email
        description: The email address of the account to be added
      - in: query
        name: first_name
        description: First name of the account holder
      - in: query
        name: last_name
        description: Last name of the account holder
      - in: query
        name: service_level
        description: Sets the service level of the accounts source to be created
      responses:
        200:
          description: OK
      tags:
      - Connect
      - Tokens
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---