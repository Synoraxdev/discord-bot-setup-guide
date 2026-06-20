# 🤖 Discord Bot Application — Complete Guide

> Guide by **Synora 乂 Development** — Support Server: [dsc.gg/synoraxdev](https://dsc.gg/synoraxdev)

Complete step-by-step guide to create a Discord Bot Application from scratch — covering the full Developer Portal, bot profile setup, banner, description, intents, token, OAuth2, and everything in between.

---

## 📋 Table of Contents

| # | Section | Description |
|---|---------|-------------|
| 1 | [What is the Developer Portal?](#-what-is-the-developer-portal) | Overview of Discord's dev dashboard |
| 2 | [Create Application](#-step-1--create-a-new-application) | Register your bot app |
| 3 | [Update Profile & Avatar](#-step-2--update-bot-profile--avatar) | Set name, icon, banner |
| 4 | [Update Description & Tags](#-step-3--update-description--tags) | About section & discovery tags |
| 5 | [Add a Bot User](#-step-4--add-a-bot-user) | Convert app into a bot |
| 6 | [Bot Settings](#-step-5--bot-settings) | Username, avatar, public/private |
| 7 | [Get Bot Token](#-step-6--get-your-bot-token) | Copy & secure your token |
| 8 | [Enable Intents](#-step-7--enable-privileged-gateway-intents) | Message, member, presence intents |
| 9 | [OAuth2 & Invite Link](#-step-8--oauth2--bot-invite-link) | Generate bot invite URL |
| 10 | [Bot Permissions](#-step-9--bot-permissions) | Set what your bot can do |
| 11 | [Installation Settings](#-step-10--installation-settings) | Install link & scopes |
| 12 | [Rich Presence](#-step-11--rich-presence) | Custom activity assets |
| 13 | [Team & Ownership](#-step-12--team--ownership) | Multi-developer access |
| 14 | [Common Errors](#-common-errors--fixes) | Troubleshooting guide |
| 15 | [Quick Reference](#-quick-reference-cheat-sheet) | Everything at a glance |

---

## 🌐 What is the Developer Portal?

The **Discord Developer Portal** is Discord's official dashboard where you:

- Create and manage bot applications
- Configure bot settings, intents, and permissions
- Generate invite links
- Manage OAuth2 scopes
- View analytics and webhooks

**Portal URL:**
```
https://discord.com/developers/applications
```

You must be logged into your Discord account to access it.

---

## 🚀 Step 1 — Create a New Application

### 1.1 — Open the Developer Portal

Go to:

```
https://discord.com/developers/applications
```

### 1.2 — Create New Application

- Click the **"New Application"** button (top right)
- A modal will appear asking for a name

### 1.3 — Name Your Application

Enter your application name:

```
Synora Bot
```

> ⚠️ **Note:** This is the **Application Name** — not the bot username. You can change the bot username separately later in the Bot tab.

### 1.4 — Accept Terms

- Check the box to agree to Discord's Developer Terms of Service
- Click **"Create"**

### 1.5 — You're In

You will land on the **General Information** page of your new application. This is the main hub for all settings.

---

## 🖼️ Step 2 — Update Bot Profile & Avatar

### 2.1 — Go to General Information

You should already be on this page after creating the app. If not, click **"General Information"** in the left sidebar.

### 2.2 — Update Application Name

- Click on the **"Name"** field
- Change it to your desired bot name
- Example:

```
Synora
```

### 2.3 — Upload Application Icon (Avatar)

- Click the **avatar box** (shows a default icon)
- Click **"Upload Image"**
- Requirements:

```
Format      PNG, JPG, GIF (animated for Nitro bots only)
Size        Minimum 128x128 pixels
Recommended 512x512 pixels or 1024x1024 pixels
Max Size    10MB
Shape       Will be cropped to a circle automatically
```

- Select your image file
- Click **"Save Changes"**

### 2.4 — Upload Application Cover Image (Banner)

The **cover image** appears on your bot's profile when users click on it.

- Scroll down to find **"Cover Image"**
- Click **"Upload Image"**
- Requirements:

```
Format      PNG, JPG
Size        Minimum 640x360 pixels (16:9 ratio recommended)
Recommended 1280x720 pixels
Max Size    10MB
```

- Upload your banner image
- Click **"Save Changes"**

> 💡 The cover image shows behind your bot's profile card when someone views your bot's profile in a server.

---

## 📝 Step 3 — Update Description & Tags

### 3.1 — Short Description

This appears on your bot's profile card and in bot lists.

- Find the **"Description"** field on the General Information page
- Write a short, clear description:

```
The all-in-one bot for Synora 乂 Development — moderation, utilities, and more.
```

```
Limits:
Minimum   →  0 characters
Maximum   →  400 characters
```

### 3.2 — Long Description (App Directory)

The long description appears in Discord's App Directory (public bot listing).

- Scroll down to find **"Long Description"**
- Supports **Markdown formatting**:

```markdown
## 🤖 About Synora Bot

Synora is a powerful Discord bot built by **Synora 乂 Development**.

### Features
- 🛡️ Full moderation suite
- 📊 Server statistics
- 🎵 Music playback
- ⚙️ Custom configurations

### Support
Join our support server: https://dsc.gg/synoraxdev
```

### 3.3 — Tags

Tags help users find your bot in the App Directory.

- Find the **"Tags"** section
- Add up to **5 tags** that describe your bot:

```
Moderation
Utility
Music
Fun
Management
```

> Tags must be single words or short phrases. They improve discoverability in Discord's App Directory.

### 3.4 — Save Everything

After filling in all fields, scroll down and click:

```
Save Changes
```

---

## 🤖 Step 4 — Add a Bot User

By default, you only have an **Application** — not an actual bot that can join servers. You need to add a Bot User.

### 4.1 — Go to the Bot Tab

In the left sidebar, click **"Bot"**.

### 4.2 — Add Bot

- Click the **"Add Bot"** button
- A confirmation modal appears:

```
"Are you sure you want to add a bot to this app?"
```

- Click **"Yes, do it!"**

### 4.3 — Bot Created

Your application now has a Bot User attached to it. You will see the bot settings appear on the page.

> ⚠️ **This action is irreversible.** Once you add a bot to an application, you cannot remove it. You would have to delete the entire application and start over.

---

## ⚙️ Step 5 — Bot Settings

### 5.1 — Bot Username

- Find the **"Username"** field under the Bot tab
- This is the actual name that appears in Discord servers
- Change it to:

```
Synora
```

> ⚠️ Bot usernames have limits:
> ```
> Minimum    2 characters
> Maximum    32 characters
> Not Allowed  "discord", "clyde", "everyone", "here" (reserved words)
> ```

### 5.2 — Bot Avatar

- Click the avatar circle under the Bot tab
- Upload a separate avatar specifically for the bot
- This can be different from the Application Icon

> 💡 If you don't upload a bot avatar, it will use the Application Icon from Step 2.

### 5.3 — Public Bot

This controls whether other people can invite your bot using the OAuth2 link.

```
ON   →  Anyone can invite your bot using the invite link
OFF  →  Only you (the app owner) can invite the bot
```

- For development: turn **OFF**
- For production/public use: turn **ON**

### 5.4 — Requires OAuth2 Code Grant

Leave this **OFF** unless you are building a web app with Discord login. For standard bots, this should always be disabled.

---

## 🔑 Step 6 — Get Your Bot Token

The **Bot Token** is a secret key that lets your code log in as your bot. It is the most sensitive piece of information for your bot.

### 6.1 — Reset Token

- Under the Bot tab, find the **"Token"** section
- Click **"Reset Token"**
- Confirm the action

### 6.2 — Copy the Token

- Your token will appear **only once**
- Click **"Copy"** immediately

A token looks like this:

```
MTExxxxxxxxxxxxxxxxxxx.Xxxxxx.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

### 6.3 — Store the Token Safely

Paste it into your `.env` file immediately:

```env
TOKEN=MTExxxxxxxxxxxxxxxxxxx.Xxxxxx.xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
```

> 🚨 **CRITICAL SECURITY RULES:**
> - **NEVER** share your token with anyone
> - **NEVER** commit your token to GitHub
> - **NEVER** paste it in Discord, screenshots, or public places
> - **ALWAYS** store it in `.env` and add `.env` to `.gitignore`
> - If your token is ever exposed — **reset it immediately** from the portal

### 6.4 — What Happens if Token is Leaked?

If someone gets your token, they have **full control** of your bot — they can send messages, ban members, delete channels, and more. Reset the token instantly if this happens.

---

## 🔌 Step 7 — Enable Privileged Gateway Intents

**Intents** tell Discord which events your bot wants to receive. Some intents are **Privileged** — they require manual enabling because they access sensitive data.

### 7.1 — Go to Bot Tab

Click **"Bot"** in the left sidebar.

### 7.2 — Scroll to Privileged Gateway Intents

You will see three toggles:

### Presence Intent

```
PRESENCE INTENT
Allows your bot to receive presence updates (online/offline/dnd status of members)

When to enable:
✅ Your bot shows member online status
✅ Your bot tracks user activity
❌ Not needed for most utility/moderation bots
```

### Server Members Intent

```
SERVER MEMBERS INTENT
Allows your bot to receive member join/leave events and full member lists

When to enable:
✅ Your bot has welcome/goodbye messages
✅ Your bot uses member.fetch() or guild.members.fetch()
✅ Your bot has autorole on join
✅ Your bot tracks member count
❌ Not needed if you don't work with member lists
```

### Message Content Intent

```
MESSAGE CONTENT INTENT
Allows your bot to read the content of messages (required for prefix commands)

When to enable:
✅ Your bot uses prefix commands (e.g. !help, s!ban)
✅ Your bot reads message content for auto-mod
✅ Your bot responds to keywords in messages
❌ Not needed if you only use slash commands (/)
```

### 7.3 — Enable the Ones You Need

- Toggle **ON** the intents your bot requires
- Click **"Save Changes"**

### 7.4 — Add Intents in Code

After enabling in the portal, you must also declare them in your code:

```ts
import { Client, GatewayIntentBits } from "discord.js";

const client = new Client({
  intents: [
    GatewayIntentBits.Guilds,
    GatewayIntentBits.GuildMembers,       // Server Members Intent
    GatewayIntentBits.GuildPresences,     // Presence Intent
    GatewayIntentBits.GuildMessages,
    GatewayIntentBits.MessageContent,     // Message Content Intent
  ]
});
```

> ⚠️ If you enable an intent in code but not in the portal (or vice versa), your bot will either crash or not receive those events.

---

## 🔗 Step 8 — OAuth2 & Bot Invite Link

**OAuth2** is the system Discord uses to let bots join servers. You generate an invite link here.

### 8.1 — Go to OAuth2

In the left sidebar, click:

```
OAuth2 → URL Generator
```

### 8.2 — Select Scopes

Scopes define what the invite link authorizes. For a standard bot:

```
✅ bot              →  Adds the bot to the server
✅ applications.commands  →  Enables slash commands
```

Check both of these.

### 8.3 — Select Bot Permissions

After selecting scopes, a **Bot Permissions** panel appears. Select what your bot needs:

**General Permissions:**
```
✅ View Channels
✅ Manage Channels       (if your bot creates/edits channels)
✅ Manage Roles          (if your bot assigns roles)
✅ Manage Guild          (if your bot edits server settings)
✅ Kick Members          (if moderation bot)
✅ Ban Members           (if moderation bot)
✅ Manage Nicknames
```

**Text Permissions:**
```
✅ Send Messages
✅ Send Messages in Threads
✅ Embed Links
✅ Attach Files
✅ Read Message History
✅ Use External Emojis
✅ Add Reactions
✅ Manage Messages       (if your bot deletes messages)
```

**Voice Permissions (if music bot):**
```
✅ Connect
✅ Speak
✅ Use Voice Activity
```

### 8.4 — Copy the Generated URL

At the bottom, you will see a generated URL like:

```
https://discord.com/api/oauth2/authorize?client_id=123456789&permissions=8&scope=bot%20applications.commands
```

Copy this URL — this is your **bot invite link**.

### 8.5 — Invite Your Bot

- Open the copied URL in your browser
- Select the server you want to add the bot to
- Click **"Authorize"**
- Complete the CAPTCHA
- Your bot will appear in the server (shown as offline until you run your code)

---

## 🛡️ Step 9 — Bot Permissions

### Understanding Permission Integer

When you select permissions in OAuth2, Discord calculates a **permission integer**. This number represents all selected permissions combined.

```
Administrator      →  8
Send Messages      →  2048
Embed Links        →  16384
Common bot setup   →  414539926576  (example)
```

### Using Administrator Permission

```
✅ Pros:  Bot has all permissions, easiest setup
❌ Cons:  Security risk — if bot is compromised, it has full server access
```

> 💡 **Best Practice:** Never use Administrator unless absolutely necessary. Grant only the specific permissions your bot actually needs.

### Checking Permissions in Code

```ts
// Check if bot has a specific permission in a channel
const botMember = interaction.guild.members.me;

if (!botMember.permissions.has("BanMembers")) {
  return interaction.reply("❌ I don't have permission to ban members.");
}
```

---

## 📲 Step 10 — Installation Settings

### 10.1 — Go to Installation

In the left sidebar, click **"Installation"**.

### 10.2 — Install Link

This is the link users will use to install your bot. Options:

```
Discord Provided Link   →  Uses Discord's default install flow
Custom URL             →  Your own landing page or website
None                   →  Disables public installation
```

For most bots, select **"Discord Provided Link"**.

### 10.3 — Default Install Settings

Set the default scopes and permissions for when someone installs your bot:

**Guild Install (adding to a server):**
```
Scopes:       bot, applications.commands
Permissions:  Your standard bot permissions from Step 9
```

**User Install (adding to a user account):**
```
Scopes:       applications.commands
(Only if your bot supports user-installed apps)
```

### 10.4 — Save Changes

Click **"Save Changes"** after configuring.

---

## 🎮 Step 11 — Rich Presence

**Rich Presence** lets you display custom assets (images, text) in game activity status for your bot or application.

### 11.1 — Go to Rich Presence

In the left sidebar, click **"Rich Presence"**.

### 11.2 — Add Assets

- Click **"Add Image(s)"**
- Upload images you want to use as activity assets
- Give each image a unique **Asset Key** (no spaces):

```
Asset Key       Image
-----------     --------------------------------
synora_logo     Your bot logo
synora_banner   A banner/background image
playing_icon    An activity icon
```

### 11.3 — Use Assets in Code

```ts
client.user.setActivity({
  name: "Synora 乂 Development",
  type: ActivityType.Watching,
  // Rich presence assets (requires RPC application)
});
```

> 💡 Rich Presence assets are mainly used for game SDK integrations. For standard Discord bots, setting activity via `client.user.setActivity()` is sufficient.

---

## 👥 Step 12 — Team & Ownership

### 12.1 — What is a Team?

A **Team** lets multiple Discord accounts share ownership of an application. Useful for dev teams working on the same bot.

### 12.2 — Create a Team

- Go to: `https://discord.com/developers/teams`
- Click **"New Team"**
- Enter a team name:

```
Synora Development
```

- Click **"Create"**

### 12.3 — Invite Team Members

- Open your team
- Click **"Invite Member"**
- Enter the Discord username of your developer
- Set their role:

```
Owner   →  Full control (delete app, manage team)
Admin   →  Can manage app settings, add members
Member  →  Read-only access to app credentials
```

### 12.4 — Transfer Application to Team

- Go to your application's **General Information**
- Scroll down to **"App Owner"**
- Click **"Transfer App to Team"**
- Select your team

> ⚠️ Once transferred to a team, only team owners can transfer it back. Be careful with this action.

### 12.5 — Transfer Ownership to Another User

To transfer a solo application to another Discord account:

- Go to **General Information**
- Scroll to the bottom
- Click **"Transfer Ownership"**
- Enter the new owner's Discord username
- Confirm the transfer

---

## ❌ Common Errors & Fixes

| Error | Cause | Fix |
|-------|-------|-----|
| `Invalid Token` | Token is wrong or reset | Go to Bot tab → Reset Token → update `.env` |
| `Disallowed intents` | Intent enabled in code but not in portal | Enable the intent in Developer Portal → Bot tab |
| `Missing Permissions` | Bot doesn't have required permissions in server | Re-invite bot with correct permissions, or grant manually |
| `Unknown Application` | Wrong Client ID in OAuth2 URL | Copy Client ID from General Information tab |
| `Bot is offline after invite` | Code not running | Start your bot with `node boot.js` |
| `Cannot send messages` | Missing Send Messages permission | Grant permission in server or re-invite with it |
| `Interaction failed` | Slash commands not registered | Run your command registration script |
| `401 Unauthorized` | Token exposed and auto-reset by Discord | Generate a new token from Bot tab |
| `50013 Missing Permissions` | Bot role is below the target role | Move bot's role higher in server role hierarchy |
| `Application not found` | Deleted or wrong application | Check your applications list in Developer Portal |

---

## 📊 Quick Reference Cheat Sheet

```
What you need                   Where to find it
-----------------------------   -----------------------------------------------
Developer Portal                https://discord.com/developers/applications
Create New App                  Applications → New Application
Application ID (Client ID)      General Information → Application ID
Bot Token                       Bot → Reset Token → Copy
Change Bot Username             Bot → Username field
Change Bot Avatar               Bot → Click avatar circle → Upload
Add Bot Description             General Information → Description
Add Bot Tags                    General Information → Tags
Enable Intents                  Bot → Privileged Gateway Intents
Generate Invite Link            OAuth2 → URL Generator → Copy URL
Set Bot Permissions             OAuth2 → URL Generator → Bot Permissions
Public/Private Bot              Bot → Public Bot toggle
Transfer Ownership              General Information → Transfer Ownership
Create Dev Team                 https://discord.com/developers/teams
Rich Presence Assets            Rich Presence → Art Assets → Add Image
```

---

## 🗂️ Developer Portal — Full Sidebar Overview

```
General Information   →  App name, icon, description, cover image, tags
Bot                   →  Token, intents, username, avatar, public toggle
OAuth2                →  URL Generator, invite link, scopes
Rich Presence         →  Custom activity assets
App Testers           →  Add testers for unreleased apps
Webhooks              →  Incoming webhook management
Installation          →  Install link, default scopes and permissions
```

---

**Synora 乂 Development** — [Join Support Server](https://dsc.gg/synoraxdev)

*If this guide helped you, consider starring ⭐ the repository!*
