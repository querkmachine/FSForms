---
title: Radio button groups
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/radio-button-groups" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When the user must select a single option from a fixed list of possibilities. 

Radio buttons are intended for mutually exclusive options; where the user will only ever have a single option apply to them.

## When to consider something else

If the user should be able to select more than one option, use a [checkbox group]({{ "/components/checkbox-groups" | relative_url }}).

There are some types of data that at face value seem like they could be a radio button group, but in practice should not be, such as [gender]({{ "/components/gender" | relative_url }}) and [title]({{ "/components/title" | relative_url }}). 

If the list of options is exceptionally long, consider using a [select]({{ "/components/select" | relative_url }}). If possible ask users questions in the preceding steps that allow you to whittle down the list of options rather than using a select.

## Guidance

The user should be able to click on a radio button's text label to select and deselect and select and deselect the radio.

A radio button can only be linked to a single label, which should describe the value of the radio button. Group related radios into a `<fieldset>` and set the fieldset's `<legend>` to the question you want the user to answer instead of using a label or heading. 

A radio button's label should ideally be self-explanatory, however you can provide users with additional hints to help them understand the options available.

Radio buttons should always be displayed as a vertical list. This makes it easier for the user to scan the list of options and select the relevant one, as the labels and controls are consistently located.

Order radio buttons alphabetically unless there is good reason not to do so.

Do not select an option by default. This makes it more likely that users will forget to select an option or submit incorrect information.

If the user should be able to select none of the options in a radio button group, provide an option that indicates this is the case, such as 'none of the above' or 'prefer not to say'. Radio button groups cannot be cleared by the user, rendering it difficult for them to correct if they select an option when they didn't intend to. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">
Error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/radio-button-groups-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Radio button groups operate as a single entity and should be validated collectively.

### Presenting two options 

<figure class="iframe">
<figcaption class="iframe__label">
Alternative layout for two options
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/radio-button-groups-two" | relative_url }}" width="100%" height="300"></iframe>
</figure>

An alternative layout is acceptable for radio button groups with only two short options. 

This layout should only be used if both of the possibilities are short (one or two words) and do not have any associated hint copy; otherwise the standard layout should be used.