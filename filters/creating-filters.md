---
description: >-
  Filters are very customisable, and this page will run you through on the many
  different options for filters.
---

# Creating Filters

The current types of filters are **Content**, **Attachments** and **Age**. 

* A **Content** filter limits what type of content can be starred, such as the length of the message, stuff it should include/exclude, and whether or not the message is a reply.
* An **Attachments** filter limits the attachments and embeds of a message, such as the amount of them or whether or not media \(images, video, gifs etc\) is required.
* An **Age** filter limits how old/young a message has to be in order to be starred.

The options available are:

### Content

* **Required** - whether or not content is required
* **Minimum** \[number\] - the minimum allowed length of content
* **Maximum** \[number\] - the maximum allowed length of content
* **IsReply** - if yes, only allow replies, if no, do not allow replies
* **Match** \[text/regex\] - text or regex the content must include/match
* **NotMatch** \[text/regex\] - text or regex the content must not include/match

### Attachments

* Required
* Minimum \[number\]
* Maximum \[number\]
* MediaRequired

### Age

* NewerThan \[time\]
* OlderThan \[time\]

### All

* AppliesTo \[list of users/roles\]
* DoesNotApplyTo \[list of users/roles\]

To create a filter, do `star filters add <content/attachments/age>` followed by options.



### Examples:

`star filters add content minimum 5 maximum 200`

* This creates a content filter that requires the content of a message to be 5 or greater in length, and 200 or fewer in length.

`star filters add age newerthan 20d olderthan 10m`

* This creates an age filter that requires the message to be older than 10 minutes but younger than 20 days.

`star filters add attachments required true mediarequired true`

* This creates an attachments filter that requires an attachment or embed, and requires media \(an image, a video, etc\).

`star filters add content match /starboard is a \w+ bot/ notmatch "bad"`

* This creates another content filter that requires the content to match the regex `/starboard is a \w+ bot/` and requires the content to not include `bad`.

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

