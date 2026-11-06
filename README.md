# Cam Fuller

Revenue operations leader in Lehi, Utah. Six years building GTM infrastructure at Weave, from SDR team lead to Director of Revenue Operations. On the side I build software end to end, with AI doing much of the typing and me owning the design, the review and the verification.

Both repos below are private. Ask and I'll add you.

## Stashmap

A live iOS app. Share a TikTok, Instagram or Facebook post and the places in it land on your map, sorted into collections you can plan from and share. Built and run solo since July 2026.

- **Stack:** Expo and React Native client; Cloudflare Workers, D1 and R2 backend; Claude for place extraction; Google Places; RevenueCat; Resend for email.
- **Off a no-code backend:** moved the app off Blink to my own stack while it was live. The data cutover had a 13 minute write window and lost zero rows. Then I replaced Blink's sign-in with my own email and password auth (bcrypt, rotating refresh tokens, verification and reset email on my own domain).
- **Multi-place import:** reads the caption, the transcript or the slideshow images, resolves each place against Google Places, and asks the user to confirm before anything saves.
- **Measured, not guessed:** every import path logs its outcome, so 20 defects were found from the data before any user reported one.
- 10 App Store releases (1.0 on July 30 through 1.2.0 on October 15), nearly 400 commits.

[App Store](https://apps.apple.com/us/app/stashmap-app/id6786569128) · [stashmap.app](https://www.stashmap.app)

## Day One

A prototype for a property management company's transitions team. It reads the prior manager's rent roll, vendor contracts and checklist, checks them against each other with rules written in plain English, and gives the Director of Transitions one ranked queue of what could go wrong on day one, each item with its evidence and a decide-by date.

- AI drafts the follow-up letters but never sees a value from the records. Code fills every figure and date, a checker rejects anything it can't trace, and a person approves. Nothing sends.
- TypeScript pipeline, React on Cloudflare Pages, a Worker for drafting. 534 tests, and an error log of every AI mistake and what caught it.

[Live site](https://day-one-transitions.pages.dev)

## How I build

I use Claude Code heavily and say so. I set the plan, review every diff, and treat a row in the database, not a green screen, as proof something works.
