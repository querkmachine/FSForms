---
title: Direct Debit
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/direct-debit" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When asking for information about a UK bank account. 

## When to consider something else

Direct Debit is much less common for online payments and gives the issuer much more control than in a card transaction. Users may not be comfortable with this, so provide an alternative payment means if possible. 

For payment by card, see the [payment card]({{ "/components/payment-card" | relative_url }}) page.

## Guidance

The account number and sort code are usually non-memorable strings of digits. Allow users to paste values into them, as this decreases the likeliness of user input error.

The format of account numbers is up to the issuing bank and is not standardised. Most banks use 8-digit codes, however some (such as Lloyds) use 7 digits and others (such as the Yorkshire Building Society) use 9 digits. However, each of these banks support 8-digit numbers for online transactions. The rules they use to increase or decrease the account number's length differ per bank, and it is up to the user to know how to achieve this. 

Accept the sort code with dashes separating each pair of digits. This is how the sort code is written on the face of most cards, and will be the format users are most familar with.

We use text input `type`s for the account number and sort code as we don't want leading zeroes to be removed.

The inputs are sized appropriate to the values expected, indicating to the user that the input should be short. The `maxlength` attribute reinforces this. 

It is a requirement to display the Direct Debit logo and [Direct Debit Guarantee](https://www.directdebit.co.uk/DirectDebitExplained/Pages/DirectDebitGuarantee.aspx) on the same page as the Direct Debit form. 

### Validating input

<figure class="iframe">
<figcaption class="iframe__label">
Error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/direct-debit-error" | relative_url }}" width="100%" height="300"></iframe>
</figure>

To check that an account number is correct, make sure that:

* The account number is populated.
* The account number is numerical.
* The account number is exactly 8 digits (after removing whitespace).

To check that a sort code is correct, make sure that:

* The sort code is populated.
* The sort code is numerical (after removing dashes and whitespace).
* The sort code is exactly 6 digits long (after removing dashes and whitespace).

For the account holder's name, only check that the field is populated. Validating the account holder's name is correct is the responsibility of the bank. 

If there is an error with the transaction as a whole, such as a server error causing it to fail, or an error of indetermine cause, there is an alternative error style available that highlights the whole form.

<figure class="iframe">
<figcaption class="iframe__label">
Transaction error state
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/direct-debit-error-alt" | relative_url }}" width="100%" height="300"></iframe>
</figure>

### Autofill

`autocomplete="cc-name"` has been added to the account holder name field. Although this autocomplete attribute anticipates being used for a credit or debit card, it is likely that the name associated with a card is the same as the name associated with an account. 

There are no autofill allowances for account number or sort code in the W3C specification.

### Mobile devices

The addition of `inputmode="numeric"` makes Android display a numeric keyboard for these fields. Note that the numeric keyboard does not prevent the user from entering non-numeric characters.

The nonstandard `autocorrect` attribute setting disables spelling and grammar correction on Safari, which is usually undesirable on name fields. 

### Internationalisation

Direct Debits are only available to UK bank accounts. Other countries may have different standards for their account numbers and routing codes. In these situations you would usually require an <abbr title="International Bank Account Number">IBAN</abbr> and <abbr title="Bank Identifier Code">BIC</abbr> number. 