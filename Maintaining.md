🧙‍♀️ Here be wizards

TODO: flesh this all out

- our review/merge process

- our version release process


Tribal / Conventions

GitHub:
Reviews:
- `nit:` if we're reviewing someone's code, but don't want to insist they take our suggestion

Kanban:
- Assign yourself to a card in the "In Progress" col, so people can see what you're up to.


Discord:

#maintainer-updates channel:
Update when you clock in each day, with your TODOs.
As you work, maintain this message, so that when you clock out it actually shows what you did (and things still to do)
This way we can see what everyone's up to

Reactions
- 👀 (looking at it) -- if someone presents an issue (e.g. a pull-request) we don't want everyone looking at it. So whoever is looking at it, react with 👀
- 👍 to request acknowledgement (or react to acknowledge that you've read it)
- ✅ job done (merged, finished, etc)


# Organizing meetings

- create a thread at the relevant place (e.g. ⁠💬・dev-contributors-chat )
- Hilight e.g. @Contributor
- Propose time using https://r.3v.fi/discord-timestamps/ -- invite 👍 👎 responses
- link a livedoc https://pad.bitlair.nl/ so stakeholders can put together an agenda, so meeting starts hot
- during the meeting, can update further the livedoc like Nick did yesterday, marking out TODOs at bottom of doc
- After the meeting, can screenshot whole convo and dump into thread


# Release process
- Create e.g. `0.3.0` thread in #contributors
- Create livedoc https://pad.bitlair.nl/ for CHANGELOG (that we'll all chip into)
- Ask @Contributor "Any more additions for this release?"
- Compile a list of TODOs, get it on the kanban (maybe a single card with checkbox items that link to other cards)
- get all items / fixes in
- MERGE-freeze
- Round of testing 
    - Discord-wide announcement
    - TODO: Need to DIRECT this testing (does everyone test everything? plugins?)
    - TODO: Need some way to get feedback (into a thread)
- If fail rinse & repeat
- Copy the CHANGELOG to the wiki
- Update BULLETIN.md to link to it
- Make the release
