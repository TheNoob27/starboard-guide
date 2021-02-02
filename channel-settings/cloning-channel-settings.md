---
description: You can create channel settings using other settings as a base.
---

# Cloning Channel Settings

The channelsettings command also has a `--channel` flag, using this you are able to make channel settings from another channel settings. To do this, you can do something like`star channelsettings create #channel-d #channel-e --channel #channel-a --name "Cloned Settings"`

This will create a new set of channel settings, using **Channel Settings** as a base. All of its settings will be copied over to the new channel settings, **Cloned Settings**.

By default, channel settings are cloned from the server settings.

{% hint style="info" %}
If you want to make channel settings from scratch, you have to input `--channel none`
{% endhint %}

{% hint style="warning" %}
If you clone channel settings, it doesn't mean that if the clone will update when you update the original.
{% endhint %}

