---
title: Authorization
---

# Authorization

REST APIs use authorization to ensure that a client has secure access only to the resources permitted by their roles. If you are building or integrating with a 3rd party API, you can choose between Basic Auth, Bearer Tokens, and OAuth2.0.

Auth details can be added to a header, body, or as parameters to a request. However, if you enter your auth details in the Authorization Tab, Hoppscotch will automatically modify the relevant parts of the request based on your chosen `Auth` type. Storing Auth Credentials or Bearer Tokens as environment variables, lets you re-use these more safely and efficiently.

## Basic Auth

If the API supports basic Auth, you will have to add a verified username and password to your request. In the authorization tab, select basic auth and add your credentials.

## Bearer Tokens

Bearer tokens allow for request authentication using an access key, such as an opaque string or JWT. In the Authorization Tab, select Basic Auth and add your token, or for added security store it in a variable and reference it by name.

Hoppscotch will append the API key value to the text 'Bearer' and add it to the request authorization header.

```
Bearer <Your API key>
```

## OAuth 2.0

In this Authentication Model, you first retrieve an access token for the API and then use that token to authenticate future requests.

An example OAuth 2.0 flow could run as follows:

![OAuth2.0](/images/features/oauth.png)

### Steps

1. In the "**Authorization Tab**" for a request, select OAuth 2.0 from the Authorization Type drop-down.

    ::image
    ---
    src: features/oauth-section
    extension: png
    alt: Hoppscotch OAuth 2.0 Authorization
    ---
    ::

2. Fill out the fields in the section below and click on "**Generate Token**" to generate a new access token.
3. You can save the token to be re-used later.
