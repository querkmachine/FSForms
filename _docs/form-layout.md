---
title: Layout
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/layout" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Each row of a form follows **a defined order of label, input hint, error messages, and lastly, input**. This order is used as it provides information and context to the user in a sensible way. 

1. What question we're asking.
2. (Optionally) Further detail on the question and advice on how to answer it.
3. (Optionally) How their current answer doesn't satisfy our expectations.
4. The chance to provide or amend their answer. 

For information on layout out multi-page processes, see [one thing per page]({{ "/docs/one-thing-per-page" | relative_url }}).

## Fieldsets

## Labels

**All inputs should have an associated label. No exceptions.** Accessibility compliance requires that all inputs have individual labels, even if the input is just one of a group (such as in a [date of birth]({{ "/components/date-of-birth" | relative_url }})).

Labels must be linked to their respective inputs thought the use of a unique `id` attribute on the input, matched to a `for` attribute on the label. An input should only ever have one label, and a label only one input. 

<aside class="aside aside--correction">
You can associate a label and input without the `id` or `for` attributes by placing the input *inside* the label. Our forms rarely do this, however. 
</aside>

The label should succinctly describe the question or information that the input is requesting.

## Input hints

For information on writing useful input hints, see [input hints]({{ "/docs/input-hints" | relative_url }}).

## Error messages

Errors are located immediately above the input. This, along with similar visual styling, closely links the input as requiring user intervention because of what the error message describes. 

Errors should be styled so as to clearly stand out to the user when scanning through the page. 

Errors should be styled so that they do not depend solely on colour to stand out, as this is not beneficial to colourblind people. Provide iconography or other alternative styles as well as colour. 

For information on writing useful error messages, see [error messages]({{ "/docs/error-messages" | relative_url }}).

## Actions

The main control on any form should be the one that progresses the user to the next step of the process or, if on the last or only step of a process, submits the form.

**This submit button should be the first submit button on the form.** It's possible for a user to submit a form at any point by pressing the <kbd>Enter</kbd> key, which will default to using the first submit button.

Controls that return to a previous step in a process should be located at the top of the form and be styled so that they don't draw attention. 