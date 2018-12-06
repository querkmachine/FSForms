---
title: Date
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/date" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When asking for dates relative to the current day.

## When to consider something else

Date inputs are **an input of last resort**. This is because of the significant inconsistencies between implementations and lack of support in some of the browsers we still maintain.

For memorable dates or historical dates, such as a date of birth, see the [date of birth]({{ "/components/date-of-birth" | relative_url }}) page.

If asking for a date that needs to match the format on a specific document, such as a credit card, create an input that matches that document's format. For expiry dates, see the [payment card]({{ "/components/payment-card" | relative_url }}) page.

## Guidance

Supporting browsers set the user-facing date format based on the user's locale. For example, the date will be formatted as `DD/MM/YYYY` to a person in the UK, `MM/DD/YYYY` to a person in the US and `YYYY-MM-DD` to a person in Japan. 

Supporting browsers will usually pop open a native calendar control that is customised to the user's locale. The design of these controls varies wildly depending on the capabilities and screen size of the browser and device. 

For selecting from a small pool of dates in the near future, it may be beneficial to provide users with buttons to set the date for them (e.g. "Tomorrow").

The inputs are sized appropriate to the values expected, indicating to the user that the input should be relatively short.

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">
Error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/date-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

To check that dates are valid, make sure that:

* The date is real, for example, not 2018-02-31.
* Past dates are in the past.
* Future dates are in the future. 
* The date is not prior to an allowed range (if applicable).
* The date is not after an allowed range (if applicable).

Validate the date as a whole, not the day, month and year separately. You can often do this by trying to create a date object with the inputs and seeing whether it returns an error or not.

The HTML date input always returns the value in the [ISO 8601](https://www.iso.org/standard/40874.html) format of `YYYY-MM-DD`, regardless of the user's locale settings. The input `value` also expects dates to be in this format. 

### Date ranges

<figure class="iframe">
<figcaption class="iframe__label">
Asking for a date range
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/date-range" | relative_url }}" width="100%" height="300"></iframe>
</figure>

Ensure that the 'end' date occurs after a 'start' date when asking for a range. 

### Custom calendar controls

Custom calendar controls (or 'datepickers') should be used with caution as they deviate from the user's standard means of inputting a date and may override native controls on the operating system. They also introduce significant accessibility hurdles that need to be overcome in order for the control to be usable by assistive technologies. 

Custom calendar controls are not guaranteed to return an input's results in ISO format, potentially requiring backend changes to manually parse and validate values.

Do not make a calendar control the only way for a user to select a date. Provide an input for the user to type into too.

### Browser support

Google Chrome has historically been inconsistent when determining date input format, as it uses it's internal locale setting instead of the operating system's locale setting. Because Chrome does not signpost what the format of an empty date input is, this forced users to guess what format the input was expecting, usually being surprised when the date was incorrect or returned a validation error.  

Internet Explorer and Safari on macOS do not support the date input type, however Safari on iOS does.

Some devices signal support for date inputs but do not reveal the associated controls or validate values correctly. This behaviour can be detected by trying to set the value of the input to something obviously invalid (such as "This is not a date"). If the input allows the value to be set, it does not support the date input correctly.

Note that some operating systems provide a "clear" option on their datepickers. **This does not clear the input.** This returns the input to the `value` it was set to before the user manipulated it, which is not necessarily an empty value.

### Internationalisation

This document assumes the use of dates in the Gregorian calendar. 

Many locales such as China, Israel, Japan, Korea, the Indonesian island of Bali and many countries in the Middle East do not use the Gregorian calendar, although citizens there may be familiar with it. 