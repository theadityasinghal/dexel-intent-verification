### What does your application do? Please be as detailed as possible, and feel free to include links to image or video examples.

Dexel is an AI-powered Discord bot built around conversational AI assistance in a dedicated chat channel, alongside community engagement, server moderation, and utility features.

Capabilities across modules:
1. AI Assistant: A dedicated conversational chat channel for natural multi-turn discussion (/ai config), voice message audio transcription (/transcribe), image generation (/imagine), and text summarization (/summarize).
2. Moderation & Security: Moderation commands (/ban, /kick, /timeout, /warn), audit logging for message edits, deletions, and member updates (AutoLog), anti-spam trap channels (/honeypot), and nickname dehoisting (/dehoist).
3. Community & Games: Cooperative server counting channels (/counting config), community starboards (/starboard), giveaways (/giveaway), activity score tracking with level role tiers (/activity), and virtual economy (/wallet, /shop).
4. Server Management: Welcome and leave greeting cards with automatic starter roles (/greetings), invite source tracking (/invites), support ticket panels with automated triage (/ticket), persistent channel notices (/sticky), and external RSS/social feeds (/feeds).
5. User Tools: User profile cards (/profile), AFK status with missed mention logging (/afk), scheduled reminders (/remind), and language translation (/translate).

Website: https://dexel.tech
Documentation: https://dexel.tech/docs
Support Server: https://discord.gg/q5PnyU7GGD
Video Walkthrough: https://github.com/theadityasinghal/dexel-intent-verification

### Do you have a public Privacy Policy telling your users about their data usage?

Yes

### Where is your Privacy Policy available?

- Website: https://dexel.tech/legal#privacy
- In-Discord: Via `/settings` ("Data & Privacy" button)
- Documentation: https://dexel.tech/docs

### Please share a link to your Privacy Policy.

https://dexel.tech/legal#privacy

### Which intents are you applying for, if any? (Leave blank if you do not need any of these)

- [x] Server Members Intent
- [ ] Presence Intent
- [x] Message Content Intent

### Why do you need the Guild Members intent?

Dexel requires the Server Members intent (GUILD_MEMBERS) to process member events:

1. Onboarding (on_member_join, on_member_remove): Assigns starter roles and posts welcome/leave cards.
2. Nickname Sanitization (/dehoist): Identifies and renames member nicknames starting with hoist characters (!, ?, symbols).
3. Audit Logging (on_member_update): Logs timeouts, nickname changes, and role assignments to a designated staff channel.
4. Invite Attribution: Checks invite use counts on member join to log invite sources.
5. Activity Roles: Assigns server roles when users reach activity score thresholds.

### Please provide links to screenshots and/or videos that demonstrate your use case

https://github.com/theadityasinghal/dexel-intent-verification

### Are you storing any API Data off-platform (outside of Discord)?

Yes

### Are you storing API Data for 30 days or less?

Yes

### How do users contact you to request deletion of their activity data?

1. In-Discord: Run `/settings` -> "Data & Privacy" -> "Delete All My Data" (confirm by typing "DELETE").
2. Web: Visit https://dexel.tech/profile?tab=privacy -> "Delete Account Data".
3. Support: Email support@dexel.tech or ask in our support server (https://discord.gg/q5PnyU7GGD).

### Are you encrypting the data that you store at rest, as is required by our developer policy?

Yes

### Can users opt-out of having their message content data tracked?

No

Moderation logs, honeypot traps, and counting channels are server-wide rules set by administrators. Individual members cannot bypass them. Users can disable personal AI conversational memory in `/settings`.

### Are you storing message content data off-platform (outside of Discord)?

Yes

### Are you storing user message content data for 30 days or less?

Yes

### How do users contact you to request deletion of their activity data?

1. In-Discord: Run `/settings` -> "Data & Privacy" -> "Delete All My Data" (confirm by typing "DELETE").
2. Web: Visit https://dexel.tech/profile?tab=privacy -> "Delete Account Data".
3. Support: Email support@dexel.tech or ask in our support server (https://discord.gg/q5PnyU7GGD).

### Are you encrypting the data that you store at rest, as is required by our developer policy?

Yes

### Will the message content data be used to train machine learning or AI Models?

No

### If yes, please explain how in the text box below, including how such models would be used.

No. Dexel does not train or fine-tune AI/ML models on Discord user data. AI features use commercial APIs (Google Gemini, Groq) in real-time inference mode with zero data training.

### Why do you need the Message Content intent?

Dexel requires the Message Content intent (MESSAGE_CONTENT) for features where slash commands cannot function:

1. Dedicated AI Chat: Reads messages in the server's designated AI chat channel (/ai config) to generate replies in conversation threads without command prefixes or @mentions.
2. Counting Game: Reads message text in dedicated channels (/counting config) to validate sequential numbers (1, 2, 3...) and reset on errors.
3. Honeypot Anti-Spam: Inspects messages in trap channels (/honeypot) to detect self-bot spam, delete the message, and ban/kick the account.
4. AFK Mentions: Saves brief text snippets of messages mentioning an AFK user to display upon return (purged after 14 days).
5. Ticket Triage: Reads the opening message in support tickets to match FAQ answers.
6. Audit Logs (AutoLog): Dispatches deleted message text and edit diffs directly to staff channels in RAM (not stored in database).

### Please provide links to screenshots and/or videos that demonstrate your use case

https://github.com/theadityasinghal/dexel-intent-verification
