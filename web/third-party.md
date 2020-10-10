# Third Party Assets 

## Overview

In web development context, the attack is commonly applied to applications containing assets hosted externally. Note, that the assets can be added into your app at build time, which means all the npm packages are candidates to this type of exploits. Vulnarabilities in tools used at any stage of the software development can lead to the exploits too.

## Common Danger Zones

- External libraries and tools
- Assets delivered for external origin, or Content Delivery Networks (CDNs)

## Defenses

#### Most common prevention measures are:

- Use most recent LTS release of software, especially for your production applications 
- Be conscious about your application dependencies
- Use trusted software to do regular security scans of your dependencies

#### Subresource Integrity

Subresource Integrity enables you to mitigate some risks of the attack by ensuring that the files your web application fetches have been delivered without a third-party having injected any additional content and without any other changes of any kind at all having been made to those files. Integrity is synonymous to hash or checksum.

---

Go back to the [section page](web/README.md).
