# Clickjacking

## Overview

Clickjacking, or "UI redress attack", occures when an attacker tricks a user into clicking on a button or link on another page rather than the user originally intended. Thus, the attacker is "hijacking" clicks and routing them to another page. Some versions of the attack can capture keystroked as well.

## Common Danger Zones

- Almost anywhere user can interact with your application
- Most commonly, forms, text inputs, buttons, file uploads, and etc

## Defenses

#### X-Frame-Options Response Headers

The X-Frame-Options header can be used to indicate whether or not a browser should be allowed to render a page inside frame/iframe element. Sites can use the header to ensure that their content is not going to be embeded.

X-Frame-Options headers can have the following values:

- DENY - prevents any domain from framing the content (recommended setting).
- SAMEORIGIN - whitelists current site to frame a content.
- ALLOW-FROM - whitelists some specific site to frame a content.

#### Content-Security-Policy frame-ancestors directive

Similar to X-Frame-Options headers, the frame-ancestors directive can be used in a Content-Security-Policy header to indicate whether or not a browser should be allowed to render a page inside frame/iframe element.

#### Common values of CSP frame-ancestors:

- 'none' - prevents any domain from framing the content (recommended setting).
- 'self' - whitelists current site to frame a content.
- https://mysite.com - whitelists mysite.com on port 443 (HTTPS).

X-Frame-Options headers Content-Security-Policy frame-ancestors directive have limited browser support, which makes some browsers vulnerable to the attack even with appropriate settings in place.

#### Frame Breaking Scripts

One way to defend against clickjacking is to include a "frame-breaker" script in each page that should not be framed. [Learn more](https://cheatsheetseries.owasp.org/cheatsheets/Clickjacking_Defense_Cheat_Sheet.html#best-for-now-legacy-browser-frame-breaking-script) about "frame-breaker" scripts.

The best form of protection against Clickjacking is combination of Frame Breaking scripts, X-Frame-Options Response Headers, and Content-Security-Policy frame-ancestors directive. It allows to have an adequare coverage for most modern, and legacy browsers.

---

Go back to the [section page](web/README.md).
