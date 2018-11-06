---
title: Checkbox groups
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/checkbox-groups" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When the user must select one or more options from a fixed list of possibilities. 

Checkbox groups should be used for non-exclusive options; where the user will likely have to select many possibilities.

## When to consider something else

If the user should only be able to select a single option, use a [radio button group]({{ "/components/radio-button-groups" | relative_url }}).

See the [single checkbox]({{ "/components/single-checkbox" | relative_url }}) page for situations that require only one checkbox, such as toggling settings or providing legal consent.

## Guidance

The user should be able to click on the checkbox's text label to check and uncheck the checkbox. 

A checkbox can only be linked to a single label, which should describe the value of the checkbox. Group related checkboxes into a `<fieldset>` and set the fieldset's `<legend>` to the question you want the user to answer instead of using a label or heading. 

A checkbox label should ideally be self-explanatory, however you can provide users with additional hints to help them understand the options available.

Checkboxes should always be displayed as a vertical list. This makes it easier for the user to scan the list of options and select the relevant one, as the labels and controls are consistently located.

Order checkboxes alphabetically unless there is good reason not to do so.

If there are lots of related checkboxes on a page it may be beneficial to provide options to check and uncheck all of the options at once. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">
Error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/checkbox-groups-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Checkboxes groups operate as a single entity and should be validated collectively.