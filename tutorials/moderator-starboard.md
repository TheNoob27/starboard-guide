# Moderator Starboard

This will walk you through how to only allow mods to star messages.

### Step 1: Blacklist Everyone

The first thing you'd need to do is blacklist everyone. You'll see why later.

You can do this by running `star blacklist add everyone`

### Step 2: Whitelist Mods

Next, you'll need to whitelist a moderator role. It can be a moderator role, or simply one admin, it doesn't matter.

You can do this by running `star whitelist add @Admins`

Now, everyone except the `@Admins` role is blacklisted and cannot star or be starred.

If you need to whitelist multiple roles/users, you can run this command more than once.

### \[Optional\] Step 3: Allow Blacklisted to be Starred

If you want blacklisted users to be able to get their messages on the starboard, you need to disable the **FilterBlacklisted** setting.

You can do this by running `star changesetting filterblacklisted no`

If you skip this step, mods can only star messages from other mods.

{% hint style="success" %}
Now only moderators can star messages!
{% endhint %}

