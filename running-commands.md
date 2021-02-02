# Running Commands

In command usages, there are various symbols to indicate how to run the command.

#### Example: `star rewardroles (add/remove) ([role]) ([stars]) --channel ([channel])`

* `<>` means the argument is required. The command will not run without this argument \(changesetting being the only exception\).
* `()` means the argument is optional. It doesn't matter whether or not you provide this argument, the command will still work fine.
*  `[]` is a placeholder. For example, `[channel]` means provide a channel, being a \#mention, channel name or channel ID. If it is `<[channel]>`, it means you are required to provide a channel, if its `([channel])` it means you can optionally provide a channel.
* `--` is for [flags](running-commands.md#flags). Flags are always optional, and can be used anywhere in the message.
* If there's a `/`, it means you can provide one of those options. For example, `(first/second/third/[number])` means \(optionally\) provide either `first`, `second`, `third` or a number.
* `...` indicates you can provide more than one. `(...[channels])` means you can provide multiple channels.

### Flags

Some commands allow you to use flags. They are all optional and most of the time you won't need to worry about them. Flags can be prefixes with either `--`, `-` or a space. Flags can also have values, which are either optional or required. `--channel ([channel])` means that you can do either `--channel` or `--channel #mention`

Examples:

* `star rewardroles add @Cool People 50 --channel #general`
* * Add a reward role for \#general
* `star rewardroles channel #general`
* * View info about reward roles for \#general.
* `star rewardroles`
* * View info ablut reward roles

{% hint style="info" %}
The above examples utilise the `--channel` flag. Quite a few commands have a channel flag, you can read more about it [here](channel-settings/channel-settings-overview.md).
{% endhint %}



{% hint style="danger" %}
When running commands, do NOT provide `<>`, `[]` or `()`, these are only present in the usages to show you what type of argument needs to be passed. 
{% endhint %}

