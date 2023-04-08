# Welcome

Here we will go over the different parts of ChatToTwitch.

## Important Links

- [Homepage](https://www.cibere.dev/chattotwitch)
- [Privacy Policy](https://www.cibere.dev/chattotwitch/privacy-policy)
- [Terms of Service](https://www.cibere.dev/chattotwitch/terms-of-service)
- [Support Server](https://discord.gg/pP4mKKbRvk)

## Tutorial

Now, lets go over a tutorial. You might notice the `/login` command, but that will only redirect you to [an oauth2 link](https://discord.com/oauth2/authorize?client_id=1005605461699088516&redirect_uri=https%3A%2F%2Fwww.cibere.dev%2Fchattotwitch%2Flink&response_type=code&scope=identify%20connections), so we can just go straight there.
Once you authorize the bot, it should say successfully linked. And thats essentially it, you've linked your account. Now you can run `/crosschat start` and your crosschat should start. To stop it, run `/crosschat stop`. This uses the default settings, and I will go more in-depth with settings [in the settings section.](#crosschat-settings)

## Crosschat Settings

When you run the `/settings` command, you get the ability to configure (whatever you can really) but the most is either your crosschat settings or server notifications. I will talk about the crosschat settings here. You can see [the notification section for info about that](#notifications)

- **Edit Display Settings:**
  When sending a message to discord, your display setting will determine how its done. Read more about this [here](#display-settings)

- **Allow Guests To Chat:**
  Allowing them to talk disables [Guest-Only mode](#guest-only-mode), while not letting them talk enables [Guest-Only mode](#guest-only-mode).

- **Edit Blacklist Settings:**
  This lets you blacklist a discord/twitch user, or unblacklist them. You can read more about blacklisting [here](#blacklist)

- **Edit Whitelist Settings:**
  This lets you Whitelist a discord/twitch user, or Whitelist them. Also lets you toggle if it's enabled or not. You can read more about whitelisting [here](#whitelist)

- **Edit Directional Settings:**
  Directional Settings will let you choose which way messages are sent. By defualt it is set to both directions for crosschat, but you can change that.

## Premium Settings

_These features require you to be a [premium member](/premium/)_

- **Toggle Autoreconnect:**
  When the bot restarts, normally you have to manually run `/crosschat start` again. But with this, the bot will automatically reconnect. This is once again another simple toggle.

- **Edit Embed Format:**
  When the bot sends an embed to discord, this setting lets you change how the embed is displayed. It gives you an interactive embed creater which lets you form it, then visualize it with test data. [This setting supports variables](#variables)

- **Edit Webhook Format:**
  Currently, this only lets you change the way the bot generates the webhook's username. [This setting supports variables](#variables)

## Profiles

Want to view someone else's profile? Well you can run `/profile` to do so. This will show you their twitch account, crosschat settings, blacklisted and whitelisted users, and their statistics.

## Notifications

When you run the `/settings` command, you get the ability to configure (whatever you can really) but the most is either your crosschat settings or server notifications. I will talk about the server notifications here. You can see [the crosschat settings section for info about that](#crosschat-settings)

- **Restart Notifications:**
  When a restart gets scheduled, the bot will notify you. It will also notify you once it's done starting, and when it just normally comes online.

- **Update Notifications:**
  When the bot recieves an update, it will send a message which contains the main highlights, along with a link that contains the full changelog.

When you change the channel, it will delete the old record so you can only have 1 per server.

## Variables

Some settings support variables, and to sum up what that means is like this: lets say `{test}` is a variable. The bot would replace `{test}` with what the variable will be. Once example is `{username}`, which will be replaced with the users username. All of the bots variables are like so: `{variable_name}`

**Fields that support variables:**

- All fields in `embed format`
- Webhook title

**Variable Index:**

- `username` - the chatters username
- `display_name` - the chatters display_name
- `content` - the message's content
- `profile_picture` - the url of the chatter's profile picture
- `user_id` - the chatters id

## Auto-Disconnect

After an hour of no messages being sent through your crosschat, it will be automatically disconnected. Want this disabled? [premium users](/premium/) get this disabled, along with access to an autoreconnect feature.

## Blacklist

Blacklisting is a feature which allows you to block messages being sent through your crosschat. When you block a discord user, any messages sent from them will not be sent from twitch.
When you block a twitch user, no messages from that user will be sent to discord.

## Whitelist

Whitelisting is a feature which allows you to choose who's messages get sent through your crosschat. You can choose to whitelist discord or twitch users, and toggle if discord whitelist (or twitch) is enabled/disabled independently.

## Guest-only mode

With this enabled, the only way for someone to talk in your crosschat is if they link their discord and twitch accounts through ChatToTwitch. We go over linking them in the [tutorial](#tutorial)

## Webhook Name Replacements

Due to discord restrictions, the name of webhooks can not contain or be certain texts.

Texts that get converted from your username:

| Normal  | After Conversion |
| ------- | ---------------- |
| discord | d\*\*\*\*\*      |
| @       | (a)              |
| #       | %                |
| :       | ;                |
| \`\`\`  | '''              |

Full username changes:

| Username | After Conversion |
| -------- | ---------------- |
| here     | h\*\*\*          |
| everyone | e\*\*\*\*\*\*\*  |

## Display Settings

When sending a message to discord, your display setting will determine how its done. Here are the display settings:

- **Webhooks:**
  ChatToTwitch will send the message to discord via a webhook. Though due to discord restrictions, webhook names will be censored. Read more about that [here](#webhook-name-replacements). You can also customize the webhooks name, though that setting is a [premium feature](/premium)

- **Embeds:**
  ChatToTwitch will send the message to discord via a normal message, with an embed attached. This embed is customizeable, but it is a [premium feature](/premium). By default it shows the chatter's avatar, name, and message's content.

- **Raw:**
  ChatToTwitch will send the message to discord via a normal message. Ex: `chatter_name: message_content`
