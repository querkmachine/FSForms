---
title: Password
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">Example</figcaption>
<iframe class="iframe__frame" src="{{ "/example/password" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When the user must provide their current password.

When the user must create a new password.

When the user is changing their current password.

## Guidance

Be aware that the label "password" comes with the connotation that the user should use a single uninterrupted string. Using multiple words and encouraging the use of a phrase (complete with spaces and proper punctuation) is often more secure and easier for users to remember.

Allow users to paste into password fields. Doing so also allows the use of password management software, increasing user security.

If a data breach has occurred that includes user's account data you should require the user to change their password on their next interaction with the service. In this instance, you should force the new password to differ from the previous version.

The `autocomplete` attribute values `current-password` and `new-password` can autofill existing passwords and help generate new passwords respectively. Many browsers will do this even if `autocomplete` is set to `off`. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">Error state</figcaption>
<iframe class="iframe__frame" src="{{ "/example/password-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

**The only requirement for new passwords should be a minimum length.**

Ideally, maintain a list of common passwords and blacklist users from using them. These passwords can be broken in a brute force attack very quickly. [The 10,000 most common passwords can be viewed and downloaded here.](https://www.passwordrandom.com/most-popular-passwords)

Do not validate the input for an existing password. Password policies may change over time and the user's current—and correct—password may not meet your amended requirements, locking them out of their account.

### Creating a new password

<figure class="iframe">
<figcaption class="iframe__label">Creating a new password</figcaption>
<iframe class="iframe__frame" src="{{ "/example/password-new" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Provide information on the password field's requirements up front, don't leave it to guesswork or validation messages. If this is a large amount of information it may be beneficial to create a new page or `<fieldset>` for password related actions.

It is unnecessary to ask a user to confirm their password by typing it again if you provide a means of unmasking the password input. By unmasking the input the user can confirm that their input is what they wanted and that they haven't made an error.

Unmasking can be achieved in JavaScript by changing the input to the text `type` when a control is interacted with. iOS and Microsoft Edge provide password unmasking features out of the box. 

### Changing an existing password

<figure class="iframe">
<figcaption class="iframe__label">Changing an existing password</figcaption>
<iframe class="iframe__frame" src="{{ "/example/password-change" | relative_url }}" width="100%" height="300"></iframe>
</figure> 

If the user is changing their password, do not require that the new password be different from the old one. This is not strictly erroneous, and the new password should be accepted so long as it meets other requirements. 

### Password requirements

Arbitrary requirements make it harder for users to create memorable passwords, which makes it more likely that they have to reset the password or store their password in a non-secure place (such as a plain text file or a sticky note).

Password strength is not based on arbitrary requirements but is instead a factor of cryptographic entropy—longer passwords, by nature, take longer to break through brute force. A minimum length of 12 characters is recommended.

Allowing the user to use any combination of letters, digits, symbols, spaces, punctuation, emoji and languages permits a huge variation of inputs. This assists with security and memorability. 

Paradoxically, limitations to the content and length of passwords makes it easier to brute force them, as there are significantly fewer valid passwords possible. 
