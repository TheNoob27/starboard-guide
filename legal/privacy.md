---
description: Here you can read about what information Starboard stores, and your privacy.
---

# Privacy

Starboard does **not** store information about you. Starboard may store data about the messages you send, but only in some cases.

### Recap - What is Starboard?

Starboard is a bot that allows messages to be "starred" or highlighted, and messages get sent to a separate channel once they get a lot of star reactions from members of your server.



### What data does the bot handle?

The bot can access the content of messages, only because it is necessary for the purpose of displaying the message content back to the server members, in the starboard channel you've set it to. Without server members adding reactions, modifying messages or interacting with the bot via commands, nothing is happening in relation to your server, without your consent.

User data, member data, roles, reactions, emojis, and of course messages, are in use by the bot but only for your own experience, for starboard messages, customisation and tracking valid reactions.



### What data does the bot store?

The main data we _have_ to store are IDs of users, channels, roles and messages. This is necessary for the bot to function in your server. No nicknames are stored and no usernames are stored either - the IDs are the only thing used to identify users, roles, messages, etc.

However, by default, when a starred message is deleted, the message is **encrypted** and **saved** to our database for a maximum of **30** days, in case the layout of the starboard message needs to be changed or resent, or a user wants to view the message by ID, or other similar reasons. **This only happens when the deleted message had been starred before deletion, NOT for all messages.** This behaviour is controlled by an in-bot setting called **LinkDeletes** - when enabled, once the original message gets deleted the starboard message will be deleted too. But when the setting is disabled and a message that was starred before is deleted, the starboard message will stay on the starboard, while the deleted message gets saved temporarily.



### Who can view my messages?

By default, only you and your server members can view your messages. But, a server that isn't age-restricted can opt into having their messages appear in a global random starboard message command called **star explore**. This command brings up a random message from a server that has the in-bot **Visible** setting enabled. A 🌍 globe shows you that the message has been found in the **star explore** command, followed by how many times it has been found.

There's also a global servers leaderboard, viewable by running the command **star leaderboard servers** - servers are listed by name. Permission for your server to appear on this leaderboard is determined by the same in-bot setting, **Visible**.

The owner of Starboard will never view your starred messages or information about your server, unless asked for help or given permission to do so.



### How do I opt-in/opt-out?

You can change most of the in-bot settings listed above with the changesetting command. For example, to enable the **Visible** setting and appear in the **star explore** command, run `star changesetting visible true/false`. You can view all in-bot settings with `star settings`.

You can find the link to this page in the bot by running `star links` or the alias `star privacy`.



#### For any further questions or queries, you can join the bot's [support server](https://discord.gg/rZgxfbH), or you can send a direct message to `TheNoob27#6815`.
