# HTTPS Downgrade

## Overview

One of the most common types of the downgrade attack. Downgrade attacks in general are characterized by forcing a victim to abandon a high quality mode of operation in a favor of lower quality mode. In HTTPS, it is often done by intercepting web traffic, and redirecting it to unencrypted HTTP version of the protocol. Often implemented as man-in-the-middle (MITM) attack.

## Common Danger Zones

- Protocols backwards compatible with older system
- Websites and applications using non-TLS channels to communicate e.g. a website served over HTTP 

## Defenses

#### Most common prevention measures are:

- Use software and hardware that is up-to-date with modern specs

#### HTTP Strict Transport Security (HSTS) Header

The HTTP HSTS allows a website to tell browsers that it should only be accessed using HTTPS, instead of using HTTP. In most implementation, web browser will automatically convert all attempts to access the site using HTTP to HTTPS requests instead.

---

Go back to the [section page](web/README.md).
