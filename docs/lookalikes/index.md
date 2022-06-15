---
id: index
slug: /lookalikes
---

# Lookalikes

Lookalikes provide a way to tackle confusable characters without having to include those characters within regex or standard phrases in blocked terms and keywords. Confusable characters are characters such as Â, Ã, Ä, Å, Ā, Ă. These characters look like a capital A with some additional strokes.

This system is not limited to only confusable characters, though. It will take any phrase entry and convert that to whatever you set as the replacement phrase. For example, say you want to replace the phrase "hello" with "goodbye", and then if you had a keyword/blocked term with "goodbye", it could then match. You could even perform emote-to-text replacements. Say someone has a GG emote and you want to convert that emote into text so that it can match your keyword or blocked term.

Lookalikes perform all phrase replacements in one pass. This pass is executed from top to bottom of your lookalike. You should reorder your entries with highest priority being at the bottom.
