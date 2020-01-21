---
title: Optional and required fields
layout: page
status: wip
---

**We prefer to mark what fields are optional rather than which are required.** We mark them by including "(optional)" text in the label or legend for the question, usually in a lighter shade to provide a different—but not overpowering—visual appearance. 

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/gender" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## Why we don't use required

UX research comparing the methods has found that marking which fields are required results in users only filling out those fields, whereas marking what is optional—or not marking fields at all—resulted in users filling out all of the fields. This is consistent with paper forms, which rarely denote which fields are required. 

<aside class="aside aside--correction">
Some studies suggest that "backgrounder" forms (forms where a large amount of information is optional, such as if someone was providing medical background information) perform better when the required fields are highlighted instead; as users don't expect to fill out the majority of the fields. Ultimately, context is king. 
</aside>

## Why we don't use an asterisk

Required fields have traditionally been denoted with a red asterisk (<span style="color:red">\*</span>), but user studies have found that users often don't know what this means; and even if a description of it is provided somewhere on the page, users often fail to read it. This abstraction of necessary information delays the user's ability to complete the task and is effectively meaningless to those who aren't familiar with it. 

The abstraction is also downright hostile to screen readers and other assistive technology, which cannot provide context, nor even necessarily read the asterisk character.

The use of the colour red usually makes the information unnecessarily prominent, and can also cause confusion with errors, which are usually also red. 

## Further reading
* [Required versus optional fields – a new standard?](https://www.formulate.com.au/blog/required-versus-optional-fields-new-standard/)
* [Designing form fields: Optional versus required](https://blog.optimalworkshop.com/designing-form-fields-optional-versus-required)
