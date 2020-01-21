---
title: "\"One thing per page\""
layout: page
status: wip
---

"One thing per page" is essentially what it says: That forms should be broken down into smaller steps to such a degree that each page only concerns itself with a single piece of information. 

<aside class="aside aside--correction">
One thing per page only applies to processes, such as registration, checkout or applications. For more 'static' forms (such as an edit profile page) then you don't need to abide by one thing per page... but still don't just dump everything onto one page because you can.
</aside>

### What should be a page?

Start by making each page contain just one thing. A 'thing' can be:

* A piece of information the user needs to know. 
* A decision the user has to make.
* A question the user has to answer. 

A 'thing' is not necessarily a single input. For example, we may ask a user for their address with multiple individual inputs, but the user is still answering one question: What is your address?

Over time user feedback and UX studies may find places where merging multiple pages together makes for a faster process. A step asking about the user's contact information may include fields for email address, phone number and postal address.

### For example

Consider a checkout process. A typical process may start at the user's cart—where they can add and remove items, change quantities and add a voucher or discount code; then collecting delivery information (if the product is physical); payment information (which can be by card, direct debit, PayPal, etc.); billing address; a review step (with updated totals for shipping fees and payment method); and finally a confirmation, invoice and/or receipt. If there is a guest checkout functionality, you may need to request even more information. 

That is not just a lot of steps, that's a lot of *conditional* steps. There are myriad situations where a user could skip most—if not the all—of the checkout process, only stopping at the steps that need amendment. 

Why build one long form with an overabundance of if statements and conditional JavaScript when you can just make several smaller, simpler forms? 

Under one thing per page, that full checkout process might look like this:

1. Cart.
	* Voucher form.
2. Guest checkout information/log in prompt (if applicable).
3. Delivery options (if applicable).
    1. Select address.
        * Add new address sub-process.
    2. Delivery method. 
4. Payment (if applicable).
    1. Card payment/PayPal.
        * 3D Secure validation.
    2. Direct Debit payment.
        * Direct Debit Guarantee.
5. Select billing address.
    * Add new address sub-process.
6. Review. 
7. Confirmation.

As a worst case scenario the will have to go though 11 tasks (if they have no account, are using a voucher, are purchasing a physical product, have different delivery and billing addresses, and are paying though a combination of card and Direct Debit). Note that a task is not analogous to an individual page, and some tasks (such as adding a new address) could conceivably be included in the parent task, however it is ultimately a deviation from the happy path. 

The vast majority of customers will not need to go through all of these tasks, and returning customers can benefit by having information saved on their account, in the best case turning 11 tasks into three:

1. Cart.
2. Review.
3. Confirmation.

## Benefits 

There are a ton of benefits to the one thing per page methodology, most of which are cribbed from the Smashing Magazine article linked below. 

### Reduced cognitive load

The user only has to focus on a single task at a time. Reducing the amount of stuff on screen and making the user to only work on one question at once reduces friction and keeps people on task. 

### Error handling is simplified

Errors can be caught and presented when the user is still filling out information relevant to the error, not long after when they've moved on to something else. 

It becomes quicker for users to resolve errors because they aren't context switching as much. 

### Pages load faster

Smaller pages mean faster load times. Faster load times leads to increased conversions and a higher perceived service quality. 

### Designing is easier

When building a complex process it becomes easier to understand when broken down into parts. Separated, these parts can be reordered, tweaked and analysed without having to look at the page as a whole.

### Debugging is easier

If everything is one large page, testing, reproducing and debugging problems become significantly harder as the cause could be any combination of expanded/hidden controls, validation rules, AJAX calls, JavaScript incompatibilities, or something else entirely. 

With one thing per page, the responsibility each page has is reduced to a bare minimum and issues can normally be tracked to the server-side, simplifying testing and bugfixing procedures. 

### Tracking behaviour is easier 

Analytics and event tracking can be more granular. It's easier to see where users are struggling and where they're dropping off the process.

### Tracking and resuming progress is easier

We can more easily track where users have gotten up to in a process. If a user drops off, we can save what they've given us so far and prompt the user to return to the process without them having to re-enter information they've already given us. 

### Branching is easier

Often we'll need to expose different inputs or steps depending on what options they've selected; sometimes we might want a user to see the same page multiple times (such as adding information about multiple people). One thing per page makes this simple: submit the form and the server determines what the user needs to see next. 

JavaScript and AJAX can achieve this behaviour too, but it's more complicated to build and to validate inputs, and a significant effort to make accessible. These pages require more stringent UX work to ensure the frequent shifting/appearing/disappearing of panels isn't jarring to the user. If JavaScript fails the process can become impossible to complete, and loading a page with all possible permutations inline adds significantly to the page weight. 

### Second-time experiences are faster

If we already have billing and delivery information for the customer we can skip these steps entirely and take them straight to the review step. 

### A better experience for screen readers

Less page content means less superfluous information for screen readers. 

### Amending information is easier

Going from the review page to a dedicated page is easier than going back to a section within a page. Even if you jump the user to the relevant section, or collapse the other sections accordion style, this is additional logic and page content that is irrelevant to the user's current task. 

### Resuming the process is easier

A form that's split up into multiple steps allows for saving information as it is provided. This can come in handy if the user's internet connection times out, their computer freezes, or they need to exit the process and want to resume it later, as the user will still have some or all of their input.

### Less scrolling 

Scrolling isn't a big deal, but it's much easier for users to review the information they've provided if they can see all of it at once. 

### Giving users control

If a user wants more information, they can click a link to get that information. If the user wants to continue to the next step, they have the choice of continuing. They aren't having everything pushed on them from the moment they load the page, saving attention spans and data allowances.

### Creating a sense of progression

Because the user is constantly moving through the form they get a welcome sense of progression; something it's harder to achieve when dwelling on a single page for several minutes. 

### Complementing mobile-first 

Mobile-first design encourages optimisation to the bare essentials. One thing per page does the same. 

## Possible issues

The main issues with the one thing per page methodology are technical.

One thing per page requires storing the user's inputs across multiple pages without necessarily storing them to a database or CRM system. The user should be able to add, remove and amend that information all the way up until they confirm the order after the review step. It will need to record all of the user's choices, even those that will ultimately be discarded and have no effect on the end result, in case the user wants to amend that information. 

This requires the temporary, server-side storage of a hefty amount of data, in a format that can be read back into the page on-demand. Developers need to consider how long this information should be stored and when it should be purged—particularly as it is likely to contain sensitive personal information. 

## Further reading 

* [Better Form Design: One Thing Per Page (Case Study)](https://www.smashingmagazine.com/2017/05/better-form-design-one-thing-per-page/) on Smashing Magazine
* [Structuring forms](https://www.gov.uk/service-manual/design/form-structure) on the GOV.UK Service Manual