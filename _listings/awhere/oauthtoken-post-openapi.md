---
swagger: "2.0"
x-collection-name: aWhere
x-complete: 0
info:
  title: aWhere Get a Token
  description: "This is the first API call you will make any time you use the API
    \n(but you only need to use once per hour). This request will \nrequest a security
    access token and save it to Postman. Later \nAPI calls will use the token from
    Postman's saved variables. \n\n[Authentication Documentation](http://developer.awhere.com/api/authentication)\n\nPrior
    to using this API call you should load the aWhere Environment\nfile into Postman
    and change the settings to your API Key and Secret.\nYou can also see where the
    key and secret should go, or enter\nthem manually, by choosing the \"Authorization\"
    tab below, selecting\n\"Basic Auth,\" and then entering the key and secret as
    the username\nand password."
  version: 1.0.0
host: api.awhere.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /oauth/token:
    post:
      summary: Get a Token
      description: "This is the first API call you will make any time you use the
        API \n(but you only need to use once per hour). This request will \nrequest
        a security access token and save it to Postman. Later \nAPI calls will use
        the token from Postman's saved variables. \n\n[Authentication Documentation](http://developer.awhere.com/api/authentication)\n\nPrior
        to using this API call you should load the aWhere Environment\nfile into Postman
        and change the settings to your API Key and Secret.\nYou can also see where
        the key and secret should go, or enter\nthem manually, by choosing the \"Authorization\"
        tab below, selecting\n\"Basic Auth,\" and then entering the key and secret
        as the username\nand password."
      operationId: OauthTokenPost
      x-api-path-slug: oauthtoken-post
      parameters:
      - in: formData
        name: grant_type
      responses:
        200:
          description: OK
      tags:
      - Agriculture
      - Token
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