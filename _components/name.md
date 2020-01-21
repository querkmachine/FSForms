---
title: Name
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/name" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When taking a person's name.

## When to consider something else

For getting a person's title, see the [title]({{ "/components/title" | relative_url }}) page.

For the name of a company or other non-human entity, see the [free text (short)]({{ "/components/free-text-short" | relative_url }}) page.

## Guidance

**Using a single field rather than breaking the name down into its components is preferred because it avoids dealing with the wide diversity of human names and how they're structured.**

Only ask for separate parts of a person's name if it is necessary for a specific purpose. Ideally only the given name should be required in these circumstances. 

You should not restrict the user's ability to change their name. If for some reason you require they go through a manual process or audit to do so, consider allowing them to set an always editable preferred name. 

### Validating input

You should not run any specific validation on names. It is possible for names to be extremely long, short, contain numerals or special symbols and have parts missing. 

### Preferred names

Many individuals use names that differ from their legal name; including those with nicknames, those who choose alternative names for their country of residence (a common practice with east Asian migrants), and transgender people who are in the process of social transition. Some cultures regularly give children contextual given names—one as a legal name, and others used for everyday life. 

In instances where you require the collection of a legal name, it is good form to additionally allow the user to give a preferred name. 

<figure class="iframe">
<figcaption class="iframe__label">
Asking for a preferred name
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/name-preferred" | relative_url }}" width="100%" height="300"></iframe>
</figure>

The preferred name should be used in all situations where the legal name is not required, such as website messaging, public posts, and customer support communications. 

### Using multiple fields

Sometimes it is necessary to collect a name split into multiple parts. 

<figure class="iframe">
<figcaption class="iframe__label">
Multiple name fields
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/name-split" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Only the given name is required. There is no legal requirement for a person to have a family name in many parts of the world, including the United Kingdom. 

The labelling of each part is purposeful. Do not use first/middle/last designators, as the components of a person's name may appear in different orders in different countries. 

Exercise caution if reassembling a name that has been collected in individual parts. You won't know what order they're meant to be in. 

### Autofill 

There are numerous `autocomplete` attribute values for names, including `name` (full name), `given-name`, `additional-name` (middle names), `family-name` and `nickname`.

### Mobile devices

The nonstandard `autocorrect` attribute setting disables spelling and grammar correction on Safari, which is usually undesirable on name fields. 

### Internationalisation

Single input name fields are used on official documentation in some countries, such as passports and birth certificates. Do not assume that a name will be split into distinct first/middle/last name fields. 

In some cultures it is common for individuals to only have a single name (mononyms) or to use matronyms or patronyms instead of family names. Mononyms are also possible in Western cultures, as many name change processes don't require a person to have two or more distinct names. Notable examples of people whose legal name is a mononym include [Elizabeth](https://en.wikipedia.org/wiki/Elizabeth_II), [Teller](https://en.wikipedia.org/wiki/Teller_(magician)) and [Cher](https://en.wikipedia.org/wiki/Cher). 

In some cultures it is common for the family name to be placed before the given name (e.g. Johnson Ralph). Others may not use family names at all, instead using last names derived from the father's name (patronym), mother's name (matronym), both, multiples of both, or neither. 

Some cultures may commonly insert extraneous words between components of the name. These words are often contextually important, providing context for other parts of the name, whilst not being part of the name itself. For example in Arabic naming conventions a man may be called Ahmad bin Tanvir (translated, "Ahmad, son of Tanvir", Tanvir being a patronym), Ahmad al-Tammar ("Ahmad, the seller of dates"), Ahmad Al Saud ("Ahmad, of the family Saud"), or any combination therein—Ahmad al-Tammar bin Tanvir Al Saud. 

Arabic naming convention has some other quirks. For example, the name Muhammad is so commonly used that it is commonplace to use the person's second name in everyday life, with Muhammad either shortened or omitted. Conversely the name Abdul (meaning "servant of") should *always* be qualified with a second name and not given just as Abdul. 

Below are some examples of naming customs and countries where they are common. Multiple different systems may be common within the same country. 

|Format|Example countries|
|:-|:-|
|Given name|Bhutan, Indonesia, Myanmar|
|Given name + family name|Bangladesh, Canada, India, Iran, Israel, Kazakhstan, Pakistan, UK, US, most of Western Europe|
|Family name + given name|Cambodia, China, Hungary, Japan, North Korea, South Korea, Vietnam|
|Given name + patronym|Malaysia|
|Given name + gendered patronym|Iceland|
|Given name + clan name|Mongolia|
|Clan name + given name|Sri Lanka|
|Given name + patronym + family name|Bulgaria, Greece|
|Given name + gendered patronym + family name|Belarus, Kazakhstan, Russia, Tajikistan, Turkmenistan, Ukraine, Uzbekistan|
|Given name + father's surname + mother's surname (+ optional grandparent's names, ad infinitum)|Mexico, Spain, most of South America|
|Given name + mother's surname + father's surname|Angola, Brazil, Portugal|
|Given name + father's name + grandfather's name (+ optional family name)|Algeria, Iraq, Egypt, Libya, Morocco, Oman, Saudi Arabia, Yemen|

In some of these countries, incorrectly parsing a person's name into a given name and surname is considered bad practice. In others, referring to a person by their patronym or matronym is considered rude.