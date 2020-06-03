# Cross-Site Request Forgery (CSRF)

## Overview

CSRF attack is based on taking advantage of browser passing cookies and basic authentication credentials along with requests. Attacker insert a resource, or snippet of code (such as HTML form) to another website, containing a link to the target site. Web browser attempting to load the resource, will make a request with the cookie/credentials attacked.

## Common Danger Zones

- Server API endpoints (especially handling sensitive data)
- Applications implementing cookie or basic authentication schemes

## Defenses

#### Most common prevention measures are:

- Stay align with REST conventions while implementing API (distinguish safe and idempotent methods)
- Implement authentication using different schmes (web storage)

#### CSRF Token

The server generates some value, and transmitted it to the client. Client included this value with subsequnet request. The value should be unique, and unpredictable in order for the scheme to be secure.

#### Validate Origin

Modern browsers attach Origin header, which cannot be altered by client side scripts. Origin can be checked on the server. If request is coming through proxy, the origin header might be replaced with Referer.

#### Cross-Origin Resource Sharing (CORS)

A mechanism to tell a browsers to give a web client application running at one origin, access to some resources from a different origin. CORS is set as a HTTP header

---

Go back to the [section page](web/README.md).
