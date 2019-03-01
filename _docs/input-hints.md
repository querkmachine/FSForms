---
title: Input hints
layout: page
status: wip
---

Input hints should need no introduction; they're hints given to the user about how to complete the input. 

They come in range of formats, from how the user should obtain the information to how they should fill it out. "Your security code is the last three digits on the back of your card." all the way to "Include hyphens. For example, 40-00-04."

Input hints should be written in sentence case with full punctuation. They should be fairly short—no more than one sentence or a few short phrases—and avoid the use of technical terminology. 

Hints should be linked to the relevant inputs via the `aria-describedby` attribute. Inputs can be linked to more than one hint. 

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/currency" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## Long hints

If you need to provide an extended amount of information about how to fill out an input, render the hint as normal text above the relevant inputs and wrap the whole lot in a fieldset. You should still put an `aria-describedby` attribute on the relevant inputs. 

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/password-new-alt" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## Placeholders

Input placeholders are pieces of copy that appear within a text input before the user has interacted with it.

We generally discourage the use of placeholder copy, as they suffer from particular usability and accessibility issues, including:

* The amount of visible copy is dependent on the size of the input, and in many situations, the size of the user's screen. It is not possible for the user to view the full copy if part of it is cut off.
* The copy cannot be read once the user has focused or begun typing into the field. 
* The default styles for placeholder copy tend to lack enough contrast to meet accessbility guidelines.
* Many screen readers do not read out placeholder text. 

Placeholders, if used at all, should only be used for giving examples of input and not other information. Placeholders are not a replacement for labels or proper input hints. 