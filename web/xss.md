# Cross-Site Scripting (XSS)

## Overview

An attacker injects code in place of a text, and force application to execute it. Prevalant vector of attack against client side applications. Older browsers, like IE, are especially sensitive to this kind of attack. Injection itself commonly occures using Man-in-the-Middle attack, and HTTPS downgrade.

## Types

- Stored XSS - Code injection in a database or other persistent storage.
- Reflected XSS - Affected code is injected in web application client from server, or other outside source.
- DOM Based XSS - Attacking a web application client directly, without any server involvement.
- Blind XSS - Similar to Stored XSS. Attacking some other application used by the main application as runtime dependency.

## Common Danger Zones

- WYSIWYG (User generated rich text)
- Non-text inputs (File uploads)
- Embedded content
- Browser plugins
- Third party UI libraries
- Third file compression libraries
- Anywhere user can insert URL directly
- Anywhere user input is sent back (Reflected XSS)
- Anywhere query parameters are rendered into DOM (DOM Based XSS)
- Anywhere where web application renders elements directly into DOM using JS (especially using `innerHTML` property of an element)
- Anywhere unsanitized user data is processed by script, or template engine
- Depending on browser, pdf viewer can execute third party JS, and thus are vulnareble

## Defenses

Most common prevention measures are:

- Any form of user input should be treated as value, not as code
- Sanitize data before it gets stored into persistent storage
- Sanitize data before it renders to end user
- Restrict supported upload formats
- Compress images before storing
- Don't use unescaped expressions while rendering or templating UI
- Use only reliable third party UI and file compression libraries, providing a list of known vulnerabilities, and customer support

Content Security Policy (CSP)

Browsers JS engine cannot tell the difference between scripts fetched from different origins. Eventually, all the scripts get executed as single context. CSP allows to tell supported browsers which sources they could execute, and which not. CSP is set as HTTP response header.

Useful CSP directives:

- child-src - whitelist frames ans workers
- connect-src - whitelist HTTP(fetch), WS, and EventSource
- form-action - whitelist form post
- img-src, media-src, object-src, style-src - whitelist of media and style
- upgrade-insecure-requests - upgrade HTTP links to HTTPS
- default-src - general fallback, for all resources types

---

Go back to the [section page](web/README.md).
