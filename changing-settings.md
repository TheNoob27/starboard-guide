---
description: Learn how to view and change basic settings.
---

# Changing Settings

After you've set up the bot, you can view a list of all the settings with `star settings`. For further information about a setting, run `star settings` with the name of the setting, e.g. `star settings starboard`.

And when you need to change a setting just run `star changesettings` with the name of the setting and the new value, e.g. `star changesetting required 3`.

{% hint style="info" %}
You can change multiple settings by providing multiple pairs. For example, `star changesetting required 2 filterBots yes`.
{% endhint %}

### Setting the Starboard Channel

You can set the starboard channel with `star changesetting starboard #starboard`, with `#starboard` being the channel where you want starred messages to go.

### Setting the Required Amount

You can set the amount of stars required to reach the starboard with `star changesetting required <[number]>`.

At some point, a post may lose its stars. We should take posts off the starboard once they fall under a certain amount. You can set this amount with `star changesetting requiredToRemove <[number]>`.

### Setting Other Settings

Any setting can be set just like the three mentioned above. View info about them with `star settings <[setting]>`, where you will also find the usage for changing the setting. Most settings are simple yes/no settings, and to change them you simply do `star changesetting <[setting]> <yes/no/true/false>`.

