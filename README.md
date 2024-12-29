# Translation Bot

A simple Telegram bot built using the [Telethon](https://docs.telethon.dev) library and the [Google Translate](https://pypi.org/project/googletrans/) module to translate messages into various languages.

## Features
- Responds to the `/start` command with a welcome message and usage instructions.
- Translates messages into any specified language using the `/trn` command.

## Installation

1. Clone the repository or download the script.
2. Ensure you have Python installed on your system.
3. Install the required modules using pip:
   ```bash
   pip install telethon googletrans==4.0.0-rc1
   ```

## Configuration

1. Get your Telegram API credentials:
   - Obtain an API ID and API Hash from [my.telegram.org](https://my.telegram.org/).
   - Generate a bot token using the [BotFather](https://core.telegram.org/bots#botfather).

2. Replace the following placeholders in the script:
   ```python
   api_id = 'YOUR_API_ID'
   api_hash = 'YOUR_API_HASH'
   bot_token = 'YOUR_BOT_TOKEN'
   ```

## Usage

1. Run the script:
   ```bash
   python main.py
   ```

2. Interact with the bot on Telegram:

   - Send `/start` to receive a welcome message and usage instructions.
   - Use the `/trn` command to translate a message. The format is:
     ```
     /trn <language_code> <message>
     ```
     Example:
     ```
     /trn hi Hello
     ```
     This will translate "Hello" into hindi.

## Example Responses

1. `/start`
   ```
   👋 Hello there!

   Welcome to **My Translate Bot** 🤖.

   ✨ Here are some things I can do:
   - Translate your messages into any language
   Type `/trn <language that you need to translate to> <your msg that you want to be translated>` to start using the bot.
   ex: /trn hi Hello
   ```

2. `/trn ar Hello`
   ```
   translated from en to hi
   नमस्ते
   ```

## Notes
- Make sure the bot token, API ID, and API hash are valid.
- The script uses Google Translate via the `googletrans` module. Ensure you are using version `4.0.0-rc1` for compatibility.

## License
This project is open source and available under the [MIT License](LICENSE).
