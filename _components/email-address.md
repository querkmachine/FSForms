---
title: Email address
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/email-address" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When collecting an email address.

## When to consider something else

For physical addresses, see the [postal address]({{ "/components/postal-address" | relative_url }}) page.

## Guidance

Email addresses may be considered sensitive information. When asking for an email address, tell the user why you require this information. This may be implicit (such as registering for a service) but may not be obvious to the user in all situations. 

Telling the user why you require their email address may also help them choose which one is most appropriate for your service, for example, if they have different work and personal addresses. 

Use `type="email"` to activate browser validation and enable context appropriate keyboards on supporting devices. 

Allow the user to paste their email address from elsewhere. This helps ensure the address is correct, and allows the use of password management software, increasing user security.

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">
Error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/email-address-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

To check that an email address is valid, make sure that:

* It contains at least one @ symbol.
* There is at least one character before the @ symbol (the 'local' part).
* There is at least one character after the @ symbol (the 'domain' part).
* It is no longer than 256 characters.

The requirements for the format of email addresses is defined in [RFC 822](https://tools.ietf.org/html/rfc822). Allowed email addresses according to RFC 822 include:

* johndoe@example.com
* john.doe@example.com
* john+doe@example.com
* john\@doe@example.com
* John\ Doe@example.com
* John.\\Doe@example.com
* "John Doe"@example.com
* "John@Doe"@example.com
* contact/john=doe@example.com
* $JOHNDOE@example.com
* !contact!john%doe@example.com
* _johndoe@example.com

Note that the domain portion of the address can, as well as a typical domain name, be written in non-ASCII characters (`कंपनी.भारत`), be a keyword (`localhost`), [IPv4 address](https://en.wikipedia.org/wiki/IPv4) (`127.0.0.1`) or [IPv6 address](https://en.wikipedia.org/wiki/IPv6_address) (`2001:0DB8:AC10:FE01::`). There is no guarantee that there will be a period, domain extension or similar.

The specification for email addresses is incredibly wide reaching, and it's difficult to make a regular expression that can accurately reflect all possibilities. It is simpler to ensure that the required parts exist, then use another method—such as sending an email to that address—to ensure the address itself is real.

Do not test for a minimum length. Also there are some [very long email addresses](http://www.abcdefghijklmnopqrstuvwxyzabcdefghijklmnopqrstuvwxyzabcdefghijk.com) out there.

### Autofill

Using `autocomplete="email"` tells the browser to autofill the field with the user's email address. If collecting an email address that doesn't belong to the current user, omit this attribute. 

### Mobile devices

Devices with soft keyboards will normally show a context appropriate keyboard for email addresses. This is specifically triggered by the `type="email"` attribute.

The nonstandard `autocorrect` attribute setting disables spelling and grammar correction on Safari, which is usually undesirable on email addresses. 