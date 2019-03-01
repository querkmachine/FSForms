---
title: Feedback messaging
layout: page
status: wip
---

Feedback messaging is what the user sees as a consequence of performing an action. This could be something innocuous, such as logging out, to error messages upon trying to fill out a form. 

## Appearance

Overarching feedback messages should be visually prominent and placed somewhere where the user will immediately be able to see them—either at the top of a page or via an overlay or notification of some sort. They may be temporal for success messages, but should not dismiss themselves if relating to a warning or error state—as these typically require the user to perform follow-up actions related to them. 

Feedback messages regarding a specific thing (i.e. an invalid form field) should be located proximate to that field. In the case of form validation errors, they should be immediately before the relevant input. 

## Writing error messages

Error messaging is important to get right because it often serves as a barrier to the user's goal, whilst simultaneously being the only help they will get to overcome that barrier. 

Error messages should be friendly, helpful and unintimidating—acting as a guiding voice, not a punishing one. A good error message tells the user what is wrong. A great error message tells the user how to fix it. 

### Writing tips

**Use sentences.** Like [input hints]({{ "/docs/input-hints" | relative_url }}), write errors and feedback messages as though they were standard copy, using sentence case and full, correct punctuation. It's easier for users to read and parse.

**Avoid the passive voice.** The [passive voice](https://en.wikipedia.org/wiki/English_passive_voice) sounds impersonal and robotic.

**Don't use technical words.** Using overly technical terminology can hinder more than it helps. If a user didn't understand what they had to input before, explaining it in more complex terms won't help. 

**Don't use redundant words.** Avoid using words that don’t add value to the message. Avoid overusing ‘please’—be direct and to the point.

**Tell the user what they need to do.** Don't just tell the user the cause of the error—tell them what they can do to rectify it. This might be something as simple as providing a formatting hint or as dire as directing them towards contacting support staff.

**When something goes wrong, take responsibility.** Users don’t like being blamed for things. Even if they’re at fault, take responsibility and consider changing the structure or copy on the form to make those errors easier to prevent.

**When something goes right, give credit.** Conversely, telling a user they did a good job filling out that form is usually appreciated. 

**Talk like a human.** Be personable. Use contractions. Read what you've written out loud. Does it sound normal? Does it make sense when removed from context?

**Be sincere.** Try to be personable, but don't be too jokey or light-hearted. The user is in a situation they ideally don't want to be in, and they may not appreciate a patronising tone. 