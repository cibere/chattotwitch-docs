# Change log

This document will contain the changes between ChatToTwitch versions. For a github commit history, you can see the [ChatToTwitch github thread](https://discord.com/channels/986344051110473769/1040403464691392573) on our [discord server](https://discord.gg/pP4mKKbRvk)

## V3

- New Documentation (Can be found [here](https://ctt-docs.cibere.dev))
- Privacy Policy has been updated. It can be found [here](https://www.cibere.dev/chattotwitch/privacy-policy)
- FAQ/Wiki has been updated. (It can be found [here](https://ctt-docs.cibere.dev/wiki/))
- A premium subscription has been added. It's perks can be found [here](https://ctt-docs.cibere.dev/premium/)
- Autoreconnect has been added, though its a [premium](https://ctt-docs.cibere.dev/premium) perk.
- Customizing embeds, though its a [premium](https://ctt-docs.cibere.dev/premium) perk.
- A better login system, making it more seemless to login.
- Directional settings, which lets you choose if messages go both directions, only to twitch, or only to discord
- Whitelisting system. This will let you whitelist twitch/discord users, and independently toggle if the discord/twitch whitelist(s) should be enabled/disabled.
- More extensive blacklisting system. You can now blacklist twitch users
- Guest-only mode. With this enabled, discord users will have to login through ChatToTwitch to be able to use the crosschat. This can be found [here](https://ctt-docs.cibere.dev/#guest-only-mode)
- Viewing profiles (This allows you to see their settings, twitch username, and stats. This can be found [here](https://ctt-docs.cibere.dev/#profiles))
- Auto-Disconnect. You probably think I added this so more people would buy premium, and although that is one perk of this, it's not the reason. This is here so it's more accurate to figure out how many crosschats are currently active, which will help me do restarts during downtime hours, etc.
- Better message parsing (Ex: when sending a message to discord, emojis, commands, roles, member, and channel mentions will all be stripped down to make it more readable.)
- Reply support (Messages will now display the content and author of the message they are replying to)
- Statistics. Using the `/about` command will let you see global statistics, while using `/profile` will let you see user-specific statistics.
- To maintain a minimilistic view, the `ping` command has been switched to a prefix command. The prefix is the bots mention, so it would be invoked as such: `@ChatToTwitch ping`
- `/crosschat start` will now give you warnings if you have settings enabled that could detereriate the preformance of the bot.
- Premium users can have up to 3 crosschats, and with this `/crosschat stop` will let you specify which channel you want to terminate the crosschat from
- `/accounts` has been removed, as you can now only have one linked account
- `/config` and `/notifications` have been combined into `/settings`, which only lets you edit what you have permission to access.
- `/crosschat bans/unban/ban` have been removed, since this has been replaced by blacklisting and can be edited in the `/settings` command
- `/privacy` and `/support` have been removed, since a link to them has been added to `/about`
- `/vote` and `/videos` have been removed due to me feeling like they are unneccessary commands
- `/tutorial` has been depreciated, and just points you to the [tutorial in the docs](https://ctt-docs.cibere.dev/#tutorial)
- `/about` now has links to the docs, homepage, privacy policy, and support server
- the `invite my devs for assistant` has been removed due to people spamming it
- The Connection error with twitch that causes frequent restarts (is hoped to be fixed)
- The multiple responding when errors occur has been fixed
- Better error handling has been added, with proper permissions being properly marked and the error handler telling you what permission(s) the bot is missing.
- Dynamic [variables](https://ctt-docs.cibere.dev/#variables) have been added

  _Most of the changes were on the backend since the V2 code was very horrible_
