---
description: You can create channel settings using other settings as a base.
---

# Cloning Channel Settings

The channelsettings command also has a `--channel` flag, using this you are able to make a group from another group. To do this, you can do something like`star channelsettings create Cloned Settings #channel-d #channel-e --channel #channel-a`

This will create a new set of channel settings, using **Channel Settings** \(the group which `#channel-a` is a member of\) as a base. All of its settings will be copied over to the new channel settings, **Cloned Settings**.

By default, channel settings are cloned from the server settings.

{% hint style="info" %}
If you want to make channel settings from scratch, you have to input `--channel none`
{% endhint %}

{% hint style="warning" %}
If you clone channel settings, it doesn't mean that the clone will update when you update the original.
{% endhint %}

