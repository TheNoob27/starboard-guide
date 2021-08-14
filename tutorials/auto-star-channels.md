---
description: Learn how to create an auto star channel.
---

# Auto Star Channels

### Step 1: Grouping Channels

The first thing you'll need to do is to create channel settings. It is necessary if you wish to have auto star enabled.

You can create a channel settings group with `star channelsettings create Name #channel-a #channel-b`

* Substitute `#channel-a #channel-b` with a list of whatever channels you want to have auto star enabled.
* **Name** is the name of the channel settings and can be whatever you want, you can remove this if you don't want a name.

### Step 2: Enabling AutoStar

To enable autostarring for these channel settings, you need to enable the **AutoStar** setting: `star changesetting autostar yes --channel #channel-a`

* `#channel-a` is any of the channels from the channelsettings you've just created, or the name if it has no spaces.

{% hint style="success" %}
Now, every message from these channels will automatically be starred!
{% endhint %}



## Enhancing The AutoStar Experience

These next steps are all optional, they will ensure the auto star channels are of high quality 😁

{% hint style="info" %}
Make sure you either run these commands in any of the channels in the channel settings, or add `--channel #channel-a` to each command.
{% endhint %}

### Step 3: Filters

You can read up on filters [here](../filters/filters-overview.md). A useful filter to create for autostar channels is an [**Attachments**](../filters/creating-filters.md#attachments) ****filter.

* If you want only messages with an attachment or link to be autostarred, create a filter with the options `required yes`
* Or else if you want only images, videos, gifs to be autostarred, create a filter with the options `mediaRequired yes`
* If you want messages to have a minimum or maximum amount of embeds and attachments, create a filter with the options `min <[number]>` and/or `max <[number]>`

An example of a filter would be `star filters add attachments mediaRequired yes min 2` which creates a filter that requires an image/video/gif and a minimum of 2 embeds/attachments.

{% hint style="info" %}
If you want to create a filter that only applies to when the message is being auto starred, add `autoStar yes` to the options. If you want one that only applies to when the message isn't being autostarred, add `autoStar no`

So for example: `star filters add attachments min 1 max 5 autoStar yes`
{% endhint %}

### Step 4: Blacklisting

You can blacklist users or roles so their messages won't be autostarred if `FilterBlacklisted` is still enabled. You can blacklist a user or role by doing `star blacklist add <[user/role]>`

### Step 5: Deleting Invalid Messages

If you **don't** want messages by blacklisted users or messages that don't pass the filters to be deleted, disable the **DeleteInvalid** setting:  `star changesetting deleteInvalid no`

### Step 6: Disabling Commands

Commands will still be processed in auto star channels, but commands or command responses will not be auto starred. If you want, you can enable the **NoCommands** setting so only commands by moderators will be processed: `star changesetting noCommands yes`

{% hint style="success" %}
That's all! Messages will now be auto starred according to what you've configured in the previous steps.
{% endhint %}



