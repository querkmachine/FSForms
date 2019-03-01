---
title: Free text (long)
layout: page
status: wip
---

<figure class="iframe">
<figcaption class="iframe__label">
Example
</figcaption>
<iframe class="iframe__frame" src="{{ "/example/textarea" | relative_url }}" width="100%" height="300"></iframe>
</figure>

## When to use

When collecting a large quantity of text input about a single topic.

## When to consider something else

Users can find open-ended questions difficult to answer. If you can break up one complex question into a series of smaller ones, it's often better to do so. 

If the expected input is brief, use a [standard text input]({{ "/components/free-text-short" | relative_url }}) instead.

If you want to provide the user with formatting options, use a [rich text input]({{ "/components/free-text-rich" | relative_url }}).

## Guidance

Like single line text inputs, make the height of the textarea proportional to the amount of text you expect users to enter.

Allow users to copy and paste into the textarea. Users are more likely to prepare long answers in an external program before pasting it into the textarea.

### Validating input

HTML does not support validating a textarea using the `pattern` attribute. Any regex based validations require third-party code to work.

### Character counting

Even if there is a character limit on the input, do not prevent users from typing more than the allowed limit. A user may wish to get their thoughts written before editing them down to the allowed limit, or may paste from an external application which doesn't provide a character count.

Character counting can often behave unpredictably and incongruently with how backend code works. JavaScript, for example treats a line break as a single character, whereas many systems treat it as two. Emoji also complicate this, for example, four person family emojis (like 👩‍👩‍👧‍👦️ and 👨‍👨‍👧‍👦️) appear as one character, are actually seven characters, and are counted by JavaScript as being 12 characters. 

If accurate character counting is a mission-critical part of the application, consider the creation of [a character weighting system](https://developer.twitter.com/en/docs/developer-utilities/twitter-text.html) as used by Twitter. 