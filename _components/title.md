---
title: Title
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">Example</figcaption>
<iframe class="iframe__frame" src="{{ "/example/title" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When obtaining a person's title.

## When to consider something else

In many situations it is unnecessary to take a title. Titles potentially reveal the user's gender and marital status, which they may not wish to do. Consider not asking for a title unless there is a clear user benefit to doing so.

For taking the rest of a person's name, see the [name]({{ "/components/name" | relative_url }}) page.

Do not assume a person's gender from their title. See the [gender]({{ "/components/gender" | relative_url }}) page for information on obtaining a person's gender.

## Guidance

There are a significant number of honorifics in the UK, including common titles, formal titles, academic titles, and titles of nobility, clergy and royalty. The UK allows most of these titles to appear on identification and legal documentats. For this reason, using a free text box is the most efficient means of collecting this information accurately.

Do not restrict users to a pre-defined list of options. Titles are typically only used for written communication, if a person has stated that their title is "Banana" then they probably won't mind if a letter refers to them as such. 

### Validating input

You should not run any specific validation on titles. It is possible for titles to be extremely long or short. Some people prefer not to use a title. 

### Autofill

The W3C `autocomplete` attribute is `honorific-prefix`, which expects a free text area. The `autocomplete` attribute is not guaranteed to work on a dropdown list.

### Internationalisation

Outside of the UK there are thousands more titles. Using a free text area permits these.