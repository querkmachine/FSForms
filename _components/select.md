---
title: Select
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/select" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When it is *required* that the user choose *only one* option from a pre-defined list of possibilities.

## When to consider something else

Select inputs should be considered an input of last resort. User research has found that they tend to be more confusing and slower to use than many equivalent input types.

For short lists of pre-defined options, consider using [radio buttons]({{ "/components/radio-button-groups" | relative_url }}). 

If the user can select zero or more options, consider using [checkboxes]({{ "/components/checkbox-groups" | relative_url }}). 

## Guidance

Order all of the options alphabetically unless there is a more intuitive ordering means (e.g. by quantity). This makes it easier for users to find the option relevant to them.

If there is an option that most users are likely to choose, consider having that option be selected by default.

Consider using `<optgroup>` to combine related choices into groups.

Keep option labels short. Selects will usually only show a single line of copy and will truncate any excess text. It may not be possible for a user to read all of the label if the text is too long. 

### Validating input

Select inputs are always considered to have a valid value, as all `<option>`s are considered valid. As a result, native browser validation will never mark a select as being invalid. 

### Multiple selects

It is possible for a user to select multiple items if the `multiple` attribute is set, however the user must hold down a system-defined key when doing so (by default <kbd>Ctrl</kbd> on Windows and <kbd>&#8984;</kbd> on Mac). Many users are unaware of this requirement and may become frustrated when the input does not work as they expect it to.

The `multiple` attribute does not work on all devices. 

For these reasons using multiple selects should be avoided.

### Mobile devices

All devices (desktop, tablet and mobile) use a native control for the `<select>` dropdown menu. Some systems incorporate limited CSS styling in the dropdown, including inheriting typeface, font size and colours from the parent `<select>`. It is not possible to style the dropdown independently of the main input. 

Some select attributes, particularly `size` and `multiple` are not supported on mobile devices and may cause the select to render incorrectly.