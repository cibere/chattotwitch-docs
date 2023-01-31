<style>
.alert {
  padding: 20px;
  background-color: #2196F3;
  color: white;
}
</style>

# Welcome

<div class="alert"> 
  <strong>Note!</strong> This documentation is for ChatToTwitch V3. <strong>The public version of ChatToTwitch is running V2, and NOT V3</strong>
</div><br>
Here we will go over the different parts of ChatToTwitch.

## Important Links

- [Homepage](https://www.cibere.dev/chattotwitch)
- [Privacy Policy](https://www.cibere.dev/chattotwitch/privacy-policy)
- [Terms Of Service](https://www.cibere.dev/chattotwitch/terms-of-service)
- [Support Server](https://discord.gg/pP4mKKbRvk)

## Tutorial

Now, lets go over a tutorial. You might notice the `/login` command, but that will only redirect you to [an oauth2 link](https://discord.com/oauth2/authorize?client_id=1005605461699088516&redirect_uri=https%3A%2F%2Fwww.cibere.dev%2Fchattotwitch%2Flink&response_type=code&scope=identify%20connections), so we can just go straight there.
Once you authorize the bot, it should say successfully linked. And thats essentially it, you've linked your account. Now you can run `/crosschat start` and your crosschat should start. To stop it, run `/crosschat stop`. This uses the default settings, and I will go more in-depth with settings [in the settings section.](#crosschat-settings)

## Crosschat Settings

When you run the `/settings` command, you get the ability to configure (whatever you can really) but the most is either your crosschat settings or server notifications. I will talk about the crosschat settings here. You can see [the notification section for info about that](#notifications)

- **Switching between embeds/webhooks:**
  When you send a message on twitch, the bot checks your configuration to see if it should send the message to discord through a webhook, or a normal message with an embed. This setting lets you change which the bot does. It's a simple toggle

- **Allow Guests To Chat:**
  This setting is kind of self explanitory. It is also a toggle. When you let them talk, anyone can talk. When you do not, anyone who has not linked their twitch and discord accounts _through chattotwitch_ will be unable to talk through the crosschat.

- **Toggle Autoreconnect:**
  _This is a premium only feature._ When the bot restarts, normally you have to manually run `/crosschat start` again. But with this, the bot will automatically reconnect. This is once again another simple toggle.

- **Edit Embed Format:**
  _This is a premium only feature._ When the bot sends an embed to discord, this setting lets you change how the embed is displayed. It gives you an interactive embed creater which lets you form it, then visualize it with test data. [This setting supports variables](#variables)

- **Edit Webhook Format:**
  _This is a premium only feature._ Currently, this only lets you change the way the bot generates the webhook's username. [This setting supports variables](#variables)

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

## Notifications

When you run the `/settings` command, you get the ability to configure (whatever you can really) but the most is either your crosschat settings or server notifications. I will talk about the server notifications here. You can see [the crosschat settings section for info about that](#crosschat-settings)

- **Restart Notifications:**
  When a restart gets scheduled, the bot will notify you. It will also notify you once it's done starting, and when it just normally comes online.

- **Update Notifications:**
  When the bot recieves an update, it will send a message which contains the main highlights, along with a link that contains the full changelog.

When you change the channel, it will delete the old record so you can only have 1 per server.

## View Settings

Want to view someone else's settings? Well you can run `/settings`, while passing a user to the `user` argument.
