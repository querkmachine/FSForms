---
title: Date of birth
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">Example</figcaption>
<iframe class="iframe__frame" src="{{ "/example/date-of-birth" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When users need to enter a memorable date, such as their date of birth.

## When to consider something else

For dates relative to the current day, see the [date]({{ "/components/date" | relative_url }}) page.

If asking for a date that needs to match the format on a specific document, such as a credit card, create an input that matches that document's format. For expiry dates, see the [payment card]({{ "/components/payment-card" | relative_url }}) page.

## Accessibility

Each input is individually labeled, giving assistive technology users information on what each field wants. All of the fields are wrapped in a dedicated fieldset, giving context to the input labels. 

Each input is additionally linked to the hint text with `aria-describedby`, so that assistive technology users can hear the example input format.

Do not automatically move the user's cursor to the next input upon completion of the previous one. This is unexpected behaviour (nothing else on the form does this) and prevents users from easily rectifying errors they have just made. Doing so may also clash with certain assistive technologies. 

## Guidance

We're using text inputs as users are usually able to type memorable dates quicker than they can select them from a dropdown list or value stepper. We haven't used the number `type` as these introduce additional controls that may confuse the user, and prevent setting a `maxlength` attribute. 

The inputs are sized appropriate to the values expected, indicating to the user that the input should be short. The `maxlength` attribute reinforces this. 

Each input is individually labeled with what kind of value is desired.

The fieldset includes a hint line giving an example of the expected format. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">Error state</figcaption>
<iframe class="iframe__frame" src="{{ "/example/date-of-birth-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

To check that dates are valid, make sure that:

* The date is real, for example, not 31 2 2018.
* The date is in the past.
* The date is further in the past than any age requirement (if applicable). 

Validate the date as a whole, not the day, month and year separately. You can often do this by trying to create a date object with the inputs and seeing whether it returns an error or not. 

Avoid assuming what is wrong with a date. For example, if the user enters 31 2 2016, the day may be right and the month may be wrong. Give vague error messages (such as "Enter a valid date" or "Enter a date in the past") rather than marking specific fields as being incorrect.

Do not enforce any format other than numerical. Users may use or omit leading zeroes.

### Autofill

An `autocomplete` attribute has been added to each field to indicate to browsers and password managers that these fields relate to the user's date of birth, and that they can safely autofill these values. 

### Mobile devices

The addition of `inputmode="numeric"` makes Android display a numeric keyboard for these fields. Note that the numeric keyboard does not prevent the user from entering non-numeric characters.

The addition of `pattern="[0-9]*"` forces iOS into the 'telephone' keyboard mode, allowing the user to only enter the digits 0 to 9, at the exclusion of any other character. The addition of the `pattern` attribute also ensures that the input is numeric, if client-side validation is available.

### Internationalisation

The separation of the date into individual day, month and year inputs makes it clear to how they are expected to provide the date without enforcing one particular format. The separation also removes ambiguity introduced through browser's differing implementations of the `date` input type, which can require input in an unexpected format if the user's device is misconfigured. 