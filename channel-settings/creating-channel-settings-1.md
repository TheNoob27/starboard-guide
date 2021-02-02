---
description: How do you create channel settings?
---

# Creating Channel Settings

It's better to explain an example, let's explain this:

`star channelsettings create #channel-a #channel-b #channel-c --name "Channel Settings"` 

This command will create new channel settings for the channels `#channel-a`, `#channel-b` and `#channel-c`. So these 3 channels will have channel settings, and the rest of the server's channels will have just the server's settings.

These channel settings will be named **Channel** **Settings**, because of the `--name "Channel Settings"`.

{% hint style="info" %}
If you want a name with spaces, it's necessary to use quotes. You can use quotes with `"`, `'` or `````
{% endhint %}

If you want to edit settings for these channel settings, do `star changesetting <setting> <value> --channel #channel-a` 

`#channel-a` can be any one of those channels set, or the name of the channel settings, only if its a name with no spaces.

{% hint style="info" %}
If you run the changesetting command \(or any command that has a --channel flag\) in a channel with channel settings, it will automatically use the channel settings. If you want to change server settings while in those channels, do `star changesetting <...> --channel none`
{% endhint %}

Most commands that change settings \(changesetting, blacklist, rewardroles, setup, whitelist, etc\) have a `--channel` flag, which changes which settings get changed.

**Here is a list of the changes that will happen for each of those commands:** 

* **Changesetting**: You can change settings for channel settings, which will be different to the server's settings and other channel settings.
* **Blacklist**: You can blacklist users or roles so that they cannot interact with the starboard **in these channels**. If they try to star a message from these channels, their reaction will be removed, even if it was on the starboard message in the starboard channel.
* **Whitelist**: You can whitelist users or roles so that they bypass the blacklist in these channels.
* **Setup**: Setup settings for these channels
* **RewardRoles**: Create reward roles that can only be earned if they earn enough stars in these channels. So if a reward role needs 50 stars, and a user gets 225 stars in `#channel-d`, they won't have that reward role. Unfortunately \(right now\) stars earned for channel specific reward roles cannot be reset, unlike for server reward roles.



