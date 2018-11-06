---
title: Gender
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/gender" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When asking for information about a user's gender. 

## When to consider something else

If the client lives in denial that this is the 21st Century or is ignorant that gender is a social construct that not all cultures view the same way, you may have to use a [radio button group]({{ "/components/radio-button-groups" | relative_url }}).

Often you don't need to collect information about gender. Consider whether the field is necessary. 

## Guidance

Some people may not be comfortable providing their gender. Unless required for a specific purpose, the user should be able to opt out of providing their gender.

You should not ask for biological sex unless absolutely necessary to do so, such as in a medical application. If you require biological sex, label it as such. 

### Validating input

You should not run any specific validation on gender.

### Autofill 

Use `autocomplete="sex"` to autofill. Note that, despite the name, this value contains the *gender identity* of the user and not their biological sex. 

Also note that the W3C specification states that gender is a free text field. The `autocomplete` attribute is not guaranteed to work with radio buttons.

### Internationalisation

Some countries legally recognise a third gender/sex marker on legal documentation. This is normally shown as an X, in contrast to F (female) and M (male). 

In addition to more contemporary conceptions of gender as a spectrum of possible options, some cultures have long histories of transgender and non-binary gender identities. This includes the Bugis people of Indonesia, [who have five genders](https://en.wikipedia.org/wiki/Gender_in_Bugis_society), Native American [two-spirits](https://en.wikipedia.org/wiki/Two-spirit) and Thai [kathoey](https://en.wikipedia.org/wiki/Kathoey). 

When asking for biological sex, be aware that a small but significant percentage of people are [intersex](https://en.wikipedia.org/wiki/Intersex), wherein they are born with a mixture of male and female sexual characteristics—making them neither male or female biologically. 