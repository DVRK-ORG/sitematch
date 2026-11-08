# Eval prompts

Run these against the current `SKILL.md` before publishing. Check the expected behavior, not a fixed list of branded winners — recommendations must come from live verification that turn.

## 1. URL input

Prompt: `Find sites like https://www.notion.so`

Expect: live profiling of the Notion homepage (or the final URL after redirects); a Standard-depth ranked table of verified alternatives; no invented domains; sources cited; a top pick.

## 2. Description input

Prompt: `A marketplace for handmade jewelry focused on the Gulf region`

Expect: a clearly labeled virtual profile; discovery that includes regional or Arabic-language routes where relevant; verified candidates or an honest sparse result; unstated details marked unknown rather than invented.

## 3. Price-seeking

Prompt: `Free alternatives to Adobe Premiere Pro`

Expect: monetization dropped from similarity weights and the change disclosed; free/freemium treated as a constraint or fit factor; free candidates not punished for having a different business model than Premiere; prices dated or marked unconfirmed; trust check against fake "free Premiere" clones.

## 4. Constraint plus language

Prompt: `بدائل لموقع Canva تدعم اللغة العربية`

Expect: reply in Arabic; names and URLs left in their original form; at least one discovery search in Arabic; Arabic-language support treated as a hard constraint; Canva profiled from a live page.

## 5. Ambiguous reference

Prompt: `Sites like Mercury`

Expect: two or three plausible interpretations (for example a bank, a browser, or another product) and one targeted clarifying question; optionally a small provisional first-pass list under labeled assumptions; no deep research into incompatible branches before clarification.

## 6. Dead or blocked reference

Prompt: use a domain that is confirmed not to resolve, or that the agent cannot open.

Expect: the skill distinguishes a tool failure from a confirmed dead domain; it tells the user what could not be verified; it does not invent a confident profile; it may ask for a description or offer a tentative virtual profile labeled as such.
