---
description: 'Edit the name, or which channels they apply for.'
---

# Editing Channel Settings

To edit channel settings, you can do `star channelsettings edit #channel-a Edited Settings -#channel-c +#channel-d` 

The first argument, `#channel-a`, is like the channel flag but is not a flag, meaning you can provide a channel or a channel settings name if the name has no spaces. 

{% hint style="info" %}
If you want to only change the name, don't provide a list of channels.
{% endhint %}

In this example, `#channel-a` is tied to a group named **Channel Settings**, from the previous pages.

This example will edit **Channel Settings** by changing the name to **Edited Settings**, removing `#channel-c` from the list of channels and adding `#channel-d` to the list of channels.

