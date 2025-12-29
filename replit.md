# Knight Bot - WhatsApp Bot

## Overview
Knight Bot is a WhatsApp bot built using the Baileys library for group management. It provides features like tagging all members, muting/unmuting, games, stickers, and many more administrative tools for WhatsApp groups.

## Project Architecture

### Main Files
- `index.js` - Main entry point, handles WhatsApp connection and event listeners
- `main.js` - Message and event handlers
- `settings.js` - Bot configuration (owner number, bot name, etc.)
- `config.js` - Additional configuration

### Directories
- `commands/` - Individual command files (ai, sticker, tts, games, etc.)
- `lib/` - Utility functions and helpers
- `data/` - JSON data files for bot state (warnings, bans, settings)
- `assets/` - Static assets (images, stickers)
- `session/` - WhatsApp session credentials (creds.json goes here)

## Setup Requirements

### Session Authentication
To use this bot, you need WhatsApp session credentials:
1. Get a pairing code from the bot's pairing service
2. Upload the generated `creds.json` file to the `session/` folder

### Configuration
Edit `settings.js` to configure:
- `ownerNumber` - Your WhatsApp number (country code + number, no +)
- `packname` - Sticker pack name
- `commandMode` - "public" or "private"

## Running the Bot
The bot runs as a Node.js console application:
```bash
node index.js
```

## Key Features
- Group management (kick, mute, promote, demote)
- Sticker creation
- Text-to-speech
- Games (tic-tac-toe, trivia, hangman)
- Anti-link and anti-spam protection
- Media downloading (YouTube, TikTok, Instagram)

## Dependencies
- Node.js 18+
- FFmpeg (for media processing)
- Baileys library for WhatsApp Web API
