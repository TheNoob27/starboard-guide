---
description: >-
  Filters are very customisable, and this page will run you through on the many
  different options for filters.
---

# Creating Filters

The current types of filters are **Content**, **Attachments** and **Age**. 

* A **Content** filter limits what type of content can be starred, such as the length of the message, stuff it should include/exclude, and whether or not the message is a reply.
* An **Attachments** filter limits the attachments and embeds of a message, such as the amount of them or whether or not media \(images, video, gifs etc\) is required.
* An **Age** filter limits how old/new a message has to be in order to be starred.

The options available are:

### Content

* **Required** - whether or not content is required
* **Minimum** \[number\] - the minimum allowed length of content
* **Maximum** \[number\] - the maximum allowed length of content
* **IsReply** - if yes, only allow replies, if no, do not allow replies, unset to allow both
* **Match** \[text/regex\] - text or regex the content must include/match
* **NotMatch** \[text/regex\] - text or regex the content must not include/match
* **AutoStar** yes/no - if this filter should apply to only messages being auto starred, or only messages not being auto starred, unset to apply to both 

### Attachments

* **Required** yes/no - whether or not an attachment/embed is required
* **Minimum** \[number\] - the minimum allowed amont of attachments + embeds
* **Maximum** \[number\] - the maximum allowed amount of attachments + embeds
* **MediaRequired** yes/no - whether or not an image/video/gif is required
* **AutoStar** yes/no - if this filter should apply to only messages being auto starred, or only messages not being auto starred, unset to apply to both 

### Age

* **NewerThan** \[time\] - the maximum age a message can be, e.g. 1w
* **SentAfter** \[date\] - a date which the message has to be sent after, e.g. 14/9/2020
* **OlderThan** \[time\] - the minimum age a message can be, e.g. 5m
* **SentBefore** \[date\] - a date which the message has to be sent before, e.g. 2022

### All

* **AppliesTo** \[list of users/roles\] - list of users/roles this filter should apply to
* **DoesNotApplyTo** \[list of users/roles\] - list of users/roles this filter should not apply to

To create a filter, do `star filters add <content/attachments/age>` followed by options.

{% hint style="warning" %}
You cannot create an age filter with both relative time \(OlderThan/NewerThan\) and static time \(SentBefore/SentAfter\). Instead, you can create two separate age filters.
{% endhint %}



### Examples:

`star filters add content minimum 5 maximum 200`

* This creates a content filter that requires the content of a message to be 5 or greater in length, and 200 or fewer in length.

`star filters add age newerthan 20d olderthan 10m`

* This creates a \(relative\) age filter that requires the message to be older than 10 minutes but younger than 20 days.

`star filters add attachments required true mediarequired true`

* This creates an attachments filter that requires an attachment or embed, and requires media \(an image, a video, etc\).

`star filters add content match /starboard is a \w+ bot/ notmatch "bad"`

* This creates another content filter that requires the content to match the regex `/starboard is a \w+ bot/` and requires the content to not include `bad`.

`star filters add age sentbefore 14/09/21 sentafter 14/09/20`

* This creates a \(static\) age filter that requires the message to be sent before 14/09/2021 and sent after 14/09/2020.

{% hint style="info" %}
For the Match \(and NotMatch\) option, you can either provide a /regex/ or text in "quote" marks. If you provide regex, the content must match the regex, if you pass text then the content must include the text. You can test regex on sites like [regexr](https://regexr.com).
{% endhint %}



### AppliesTo/DoesNotApplyTo

To make filters apply to only a set of roles or users, input appliesTo followed by a list of users or roles. The same goes for doesNotApplyTo

#### Examples:

`star filters add content min 10 appliesTo @Members @Verified`

* This filter only applies to users with the `@Members` or `@Verified` roles.

`star filters add age min 10m appliesto @TheNoob27#6815 @Owners @User#0000 doesnotapplyto @me`

* This filter only applies to `@TheNoob27`, `@User`and users with the `@Owners` role.

{% hint style="info" %}
If you want to select a user or role without mentioning them, just input a part of their name prefixed with `@`, such as `@Noob` or `@members`. If you want to add the everyone role, input `everyone`. Filters apply to everyone by default, though.
{% endhint %}

{% hint style="success" %}
If you wish to test a filter, do ~~`star filters test <[messageURL]>`~~

The bot will respond with ✅ if the message passes the filters and can be starred. It'll respond with ❔ if the bot can't find the message. This could mean the bot can't read message history.
{% endhint %}

