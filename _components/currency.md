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

We haven't used the number `type` as these introduce additional controls that are unsuitable for entering large values and may confuse the user. Currency inputs use the `text` type instead.

The inputs are sized appropriate to the values expected, indicating to the user that the input should be short. The `maxlength` attribute reinforces this. 

Allow the user to use the thousands separator when entering large values. Allowing the digits to be visually separated allows the user to more easily validate that their input is correct. 

If the user is entering values that will be compared to other values, align values to the right and using tabulated (fixed width) figures can help scannability. 

<figure class="iframe">
<figcaption class="iframe__label">Multiple fields</figcaption>
<iframe class="iframe__frame" src="{{ "/example/currency-alt" | relative_url }}" width="100%" height="300"></iframe>
</figure>

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

### Mobile devices

The addition of `inputmode="numeric"` forces Android to use the numeric keyboard for this field.