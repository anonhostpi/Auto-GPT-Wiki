🧙‍♀️ Here be wizards

TODO: flesh this all out

- our review/merge process
- what else?

# Tribal / Conventions

GitHub:
Reviews:
- `nit:` if we're reviewing someone's code, but don't want to insist they take our suggestion

Kanban:
- Assign yourself to a card in the "In Progress" col, so people can see what you're up to.


# Discord:

One day:  
#maintainer-updates channel:  
Update when you clock in each day, with your TODOs.  
As you work, maintain this message, so that when you clock out it actually shows what you did (and things still to do)
This way we can see what everyone's up to

### Reactions  
Let's be creative:
- 👀 (looking at it) -- if someone presents an issue (e.g. a pull-request) we don't want everyone looking at it.
    So whoever is looking at it, react with 👀
- Ask for a 👍 to request acknowledgement (or react 👍 to acknowledge that you've read it)
- ✅ job done (merged, finished, etc)
- etc.

# Organizing meetings

- create a thread at the relevant place (e.g. ⁠💬・dev-contributors-chat )
- In it Hilight e.g. @Contributor @Catalyst @Maintainer, @Catalyst @Matintainer, or just @Maintainer
    - Propose time using https://r.3v.fi/discord-timestamps/ -- invite 👍 👎 responses
    - link a livedoc https://pad.bitlair.nl/ so stakeholders can put together an agenda, so meeting starts hot
        - seed the agenda
- during the meeting, can update further the livedoc like Nick did yesterday, marking out TODOs at bottom of doc
- After the meeting, summarize actionables in thread


# Release process
- Create e.g. `0.3.0` thread in #contributors
- Create livedoc https://pad.bitlair.nl/ for **Release Notes** (that we'll all chip into)
- Ask @Contributor "Any more additions for this release?"
- Compile a list of TODOs, get it on the kanban (maybe a single card with checkbox items that link to other cards)
- get all items / fixes in
- MERGE-freeze
- Round of testing 
    - Discord-wide announcement
    - TODO: Need to DIRECT this testing (does everyone test everything? plugins?)
    - TODO: Need some way to get feedback (into a thread)
- If fail rinse & repeat
- Copy the **Release Notes** to the wiki
- Update BULLETIN.md to link to it
- Make the release, dropping in the release-notes, and tag master (e.g. v0.3.0)
- Announce it using the main Discord #Announcements channel (which relays to 50k+ other discord users as well as our guild)
- Tweet from official AutoGPT Twitter (Toran)