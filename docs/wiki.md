# Wiki

## Why is it that when I send a message, the bot reacts with a red X?

The bot will do this for one of the following reasons:

- The crosschat has [guest-mode disabled](/#guest-only-mode), and you are a guest
- You are [blacklisted](/#blacklist) from the crosschat
- The streamer has [whitelist-only mode](/#whitelist) enabled, and you are not [whitelisted](/#whitelist).

## Is the bot open sourced?

The actual bot? No. But the documentation can be viewed [on github](https://github.com/cibere/chattotwitch-docs)

## Why are messages being sent to discord, but not to twitch?

Is the bot sending a warning message? If so, they will tell you how to fix it. If not, make the twitch account `chattodiscord` a moderator on your stream. If that worked, then it was because you either had followers only mode, subscribers only mode, emote only mode, or some sort of verification the bot was unable to complete. If this did not work, you can [reach out for help](https://discord.com/channels/986344051110473769/1019750029973540865) in our [discord server](https://discord.gg/pP4mKKbRvk).

## Why is the bot is replacing `discord` with `d*****` in a webhooks username?

This has been moved to the [Webhook Name Replacements section](/#webhook-name-replacements)
