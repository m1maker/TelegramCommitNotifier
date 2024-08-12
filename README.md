# TelegramCommitNotifier

**TelegramCommitNotifier** is a GitHub Action that tracks commits in your repositories and sends notifications to Telegram.

## Installation

### Step 1: Create a Telegram Bot

1. Open Telegram and find the bot [@BotFather](https://t.me/botfather).
2. Send the command /newbot and follow the instructions to create a new bot.
3. After creating the bot, you will receive a token that will be used to send messages.

### Step 2: Get Channel ID

1. Create a new channel in Telegram.
2. Add your bot to the channel as an administrator.
3. To get the channel ID, send any message in the channel, then use the following URL in your browser:
      https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates
   
   Replace <YOUR_BOT_TOKEN> with your token. Find your channel ID in the response.

### Step 3: Set Up Secrets in GitHub

1. Go to your repository on GitHub.
2. Click on Settings > Secrets and variables > Actions.
3. Click on New repository secret.
4. Create two secrets:
   - TELEGRAM_BOT_TOKEN — your bot token.
   - TELEGRAM_CHANNEL_ID — your channel ID.

### Step 4: Add GitHub Action

Create a directory .github/workflows and insert Telegram Notifications.yml file.


## How It Works

- Every time you push to the main branch, this action will trigger.
- It will send a message with information about the new commit to the specified Telegram channel.

Now you're all set to receive notifications about new commits directly in your Telegram channel!