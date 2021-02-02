---
description: 'Edit the name, or which channels they apply for.'
---

# Editing Channel Settings

To edit channel settings, you can do `star channelsettings edit #channel-a #channel-a #channel-b --name "Edited Settings"` 

The first argument, `#channel-a`, is like the channel flag but is not a flag, meaning you can provide a channel or a channel settings name. You can optionally remove the first argument and instead use the channel flag, so that example would look like `star channelsettings edit #channel-a #channel-b --name "Edited Settings" --channel #channel-a`

* If you want to only change the name, don't provide a list of channels.
* If you want to only change the list of channels, don't provide the name flag.

In this example, `#channel-a` is tied to channel settings named **Channel Settings**.

This example will edit **Channel Settings** by changing the name to **Edited Settings** and setting the channels which it applies to to `#channel-a` and `#channel-b` \(removing `#channel-c`\)

