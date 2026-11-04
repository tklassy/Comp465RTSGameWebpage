# COMP 465 RTS Workflow

**As of:** November 4, 2026

## Document maintenance

- Whenever `AGENTS.md` is modified, update the `As of` date at the top of this file to the date of the change.
- Whenever a website page or file with an `As of` date is modified, update that file's `As of` date as part of the same change.

## Start every work cycle

- Review the current development website and Assets repository before proposing or changing implementation. Do not rely solely on previous chats.
- Website source: https://github.com/tklassy/Comp465RTSGameWebpage
- Assets repository: https://github.com/tklassy/Assets
- Read applicable repository instructions, current changelog, project overview, roadmap, relevant scripts, and recent commits. Check the website's `Last synced Assets commit` marker against the Assets history.
- Use the user's stated work-cycle date. Interpret commit timestamps in America/Los_Angeles rather than assigning a cycle from the UTC date alone.
- Distinguish repository-confirmed changes, user-reported local work, planned work, and tested behavior. If a source is inaccessible, state the gap without claiming it was reviewed.

## Code corrections

- Prefer complete code-file replacements when practical, especially when providing Unity C# corrections for the user to paste into their project.
- Read the current full file first. Preserve unrelated behavior, class names, serialized fields, Inspector references, and public interfaces unless the requested correction requires changing them.
- Identify the exact destination path and provide complete compilable contents without omitted sections or placeholder comments.
- For unusually large files or small targeted fixes where a full replacement would be impractical, Still provide a full replacement.
- Preserve Unity `.meta` files and GUIDs. Explain any required Inspector assignments, scene setup, or prefab changes separately.
- Verify the affected behavior when possible. Clearly state checks that were run and any Unity testing still required.
- For current Unity versions, use the non-deprecated `FindObjectsByType<T>()` or `FindObjectsByType<T>(FindObjectsInactive)` overloads when searching scene objects. Do not use the deprecated overload that passes `FindObjectsSortMode`.

## Changelog format

- Recheck the current site's format each cycle. Match its established structure and wording style.
- Use one work-cycle date section in newest-first order: `Month D, YYYY`, followed by a short title-style theme description.
- Each individual change uses a concise past-tense action title, normally beginning with Added, Updated, Fixed, Expanded, Renamed, or Started. Use title-style capitalization and no final period in titles.
- Group related implementation details beneath the relevant change instead of giving every small detail its own entry. Explain behavior and implementation in short complete-sentence paragraphs.
- The current website uses expandable entries, not literal unordered-list bullets:
  - `<details class="date-entry">` contains the date `<summary>` and `<span class="date-description">`.
  - `<div class="date-content">` contains individual `<details class="change-entry">` elements.
  - Each change has a `<summary>` title and `<div class="change-documentation">` with `<p>` paragraphs.
- For a chat-only bullet summary, use the same date, theme, and action titles. For website-ready output, retain the exact HTML classes and nesting above.
- Do not invent implementation details, test results, or completed features. Keep provenance notes outside publication-ready entry text.

## Roadmap history

- Keep older completed roadmap milestones even when later work supersedes, replaces, or substantially improves them. Completed milestones document the project's development history and should not be removed merely because a newer implementation now exists.
- When a planned roadmap item becomes complete, move or add the completed milestone as appropriate without rewriting unrelated historical completed entries solely to reflect the newest architecture.

## Website changes and publishing

- Keep the website read-only during a work cycle. Maintain proposed entries and other drafts separately from website files.
- Only update website files at the end of a work cycle, and only with explicit user permission covering those edits.
- At the end of the work cycle the user will push all changes made that cycle to the Assets repository. Use that pushed state to assist in preparing changelog and roadmap updates.
- After the user pushes the Assets repository at the end of a work cycle, re-read the newly pushed commit and compare it against the website's current `Last synced Assets commit` marker before preparing final changelog and roadmap edits.
- Before requesting permission, prepare the concrete proposed content and describe the affected files so the user can review the result in chat for a quick review.
- Editing permission does not automatically authorize a push. Push, merge, deploy, or publish only when the user explicitly authorizes that action at the end of the work cycle. A single explicit instruction may authorize both editing and pushing.
- Do not interpret a request to inspect, draft, reformat, or summarize as permission to modify or publish the website.
- After authorized edits, review the diff, check links and expandable sections, and verify any affected pages. Update applicable As of dates and the Assets sync marker only when supported by the actual reviewed content.
- Never claim publication succeeded without checking the result. Report what was edited, what was pushed, what was verified, and anything still pending.

## Project reference material

- Treat synced ChatGPT project files under `sources/` as read-only reference material. Do not edit, rename, move, or delete them.
- Keep generated drafts separate from synced references and preserve unrelated user changes.
