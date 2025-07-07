
# Kafisent Bot

Telegram bot that scrapes the latest colors from Bulldrop wheel game
and predicts the next color using a simple Markov chain.

## Files
- **bot.py** – main bot logic
- **requirements.txt** – Python dependencies
- **Procfile** – process declaration for Railway/Heroku style deployment

## Quick Deployment on Railway

1. Create new project -> Add service -> Python.
2. Upload bot.py, requirements.txt, Procfile.
3. Add environment variables:
   - BOT_TOKEN: your BotFather token
   - OWNER_ID: your Telegram numeric ID
4. Under Settings, set Start Command to:
   ```
   apt-get update &&
   apt-get install -y chromium chromium-driver &&
   python bot.py
   ```
5. Deploy!

Bot will respond to **/start** and **/predict** commands.
Live predictions are sent every 10 s to OWNER_ID chat.
