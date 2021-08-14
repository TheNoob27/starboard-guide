---
description: Learn how to create multiple starboards.
---

# Multiple Starboards

In this bot, you can have multiple starboards where each channel is categorised into one. Meaning that channel A and B can go to Starboard A, channel C and D can go to Starboard B, etc.

{% hint style="info" %}
You can have up to 10 starboards on one server.
{% endhint %}

### \[Optional\] Step 1: Unset Server Starboard

If you want to have a default starboard for the rest of the server's channels, skip this step.

To unset the server's starboard, simply do `star changesetting starboard none`

### Step 2: Grouping Channels

You'll need to start creating channel settings so you can group channels together. You can create a channel settings with `star channelsettings create Name #channel-a #channel-b`

* Substitute `#channel-a #channel-b` with a list of whatever channels you want to go to this starboard.
* **Name** is the name of the channel settings and can be whatever you want, you can remove this if you don't want a name.

### Step 3: Create Starboard Channel

To set a starboard channel for a group of channels, you need to: `star changesetting starboard #starboard --channel #channel-a`

* `#channel-a` is any of the channels from the channelsettings you've just created, or the name if the name has no spaces.

{% hint style="info" %}
If the bot has the `Manage Channels` permission, you can have the bot create a starboard channel for you by doing `star changesetting starboard create name --channel #channel-a` where `name` is whatever name you want, defaulting to "starboard".
{% endhint %}

### Step 4: Repeat

For every group of channels with a starboard you want to make, repeat this tutorial.

{% hint style="info" %}
You can edit the settings for each group of channels by running the changesetting command in any of the channels in the group.
{% endhint %}

{% hint style="success" %}
You should have multiple starboards now, one for a group of channels, one for another group, etc.
{% endhint %}

