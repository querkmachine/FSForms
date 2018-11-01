---
title: Currency
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">Example</figcaption>
<iframe class="iframe__frame" src="{{ "/example/currency" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When the user has to enter a monetary value. 

## When to consider something else

For non-currency numerical values, see the [number]({{ "/components/number" | relative_url }}) page.

## Guidance

We have used the `number` input type to provide the benefits of easy numerical (`min`/`max`) validation, but have hidden the stepper input controls as these provide little user benefit when entering large values and may confuse the user by making it appear that they must use the stepper instead of being able to type their input. 

The inputs are sized appropriate to the values expected, indicating to the user that the input should be relatively short.

Allow the user to use the thousands separator when entering large values. Allowing the digits to be visually separated allows the user to more easily validate that their input is correct. This is called [subitizing](https://en.wikipedia.org/wiki/Subitizing).

If the user is entering values that will be compared to other values, aligning values to the right and using tabulated (fixed width) figures can aid with scannability. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">Error state</figcaption>
<iframe class="iframe__frame" src="{{ "/example/currency-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

To check that currency is valid, make sure that:

* The value is numerical (with the exception of thousands separators, decimal separators and minus value symbol).
* The value has no more than two decimal places.
* The value is equal to or greater than zero, if it's expected to be positive.
* The value is equal to or lower than zero, if it's expected to be negative.
* The value is equal to or higher than the minimum value (if applicable).
* The value is equal to or lower than the maximum value (if applicable).

Don't enforce the number of decimal places as having to be exactly two, the user may wish to enter '20' when you expect '20.00'. Their input is not wrong, so don't punish them for providing information in that format. 

### Mobile devices

Although set to `type="number"`, neither iOS nor Android prevent the user from entering non-numerical values. 

### Internationalisation

Different countries have different methods of writing currency values. These differences will be automatically activated by the browser depending on the user's configured locale. Browsers will usually normalise the value of a `number` input type to remove thousands separators and use a decimal period when submitting to the server.

Some currency formats and prominent countries that use them:

* 1,234,567.89 — Ireland, New Zealand, UK, US
* 1 234 567.89 — Australia, Canada (English)
* 1 234 567,89 — Canada (French), Russia, most European nations
* 1.234.567,89 — Argentina, Netherlands
* 12,34,567.89 — Bangladesh, India
* 1'234'567.89 — Liechtenstein, Switzerland
* 123,4567.89 — China