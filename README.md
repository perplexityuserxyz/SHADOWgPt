# ShadowGPT Telegram Bot

A private, intelligent Telegram bot with conversation memory, owner-controlled access, and AI chat functionality powered by OpenRouter API.

## Features

### 🔐 Security & Access Control
- **Owner Authorization System**: Only the owner (ID: 7924074157) has full control
- **User Whitelist Management**: Owner can approve/deny user access requests
- **Automatic Access Requests**: New users automatically request access
- **Pending User Queue**: Review all pending access requests

### 💬 AI Chat with Memory
- **Conversation History** - Bot remembers up to 20 previous messages
- **Personalized Responses** - Answers based on your chat history
- **Instant Replies** - Typing indicators for real-time feel
- Powered by OpenRouter API
- Supports multiple AI models (DeepSeek R1, Gemini, GPT-4, etc.)
- Multi-language support (English, Hindi, Indonesian, Spanish, Arabic, Thai, Portuguese)
- Auto language detection
- Custom system prompts loaded from file

### 🎨 User Interface
- Beautiful inline keyboard buttons
- **Quick Reply Buttons** - Menu and Clear History always accessible
- Clean, attractive message formatting with emojis
- Easy navigation between menus
- Non-spammy, organized layout
- **Personalized Greetings** - Shows conversation count on start

### ⚙️ Settings
- Change AI model
- Select preferred language
- View bot status and statistics

### 👑 Owner Admin Panel
- View authorized users
- Approve/deny pending requests
- Add users manually by ID
- Remove users from whitelist
- View bot statistics

## Bot Commands

- `/start` - Start the bot and show main menu
- `/menu` - Return to main menu
- `/admin` - Access admin panel (owner only)
- `/cancel` - Cancel current operation

## Main Menu Options

1. **💬 Start Chat** - Begin chatting with ShadowGPT AI
2. **⚙️ Settings** - Configure language and model
3. **📊 Status** - View bot information
4. **ℹ️ Help** - Show help information

## Admin Panel Features (Owner Only)

- **👥 View Whitelist** - See all authorized users
- **🔔 Pending Requests** - Review and approve/deny access requests
- **➕ Add User** - Manually add user by ID
- **➖ Remove User** - Remove user from whitelist
- **📊 Bot Stats** - View detailed statistics

## How It Works

### For New Users:
1. User sends `/start` to the bot
2. Bot automatically sends access request to owner
3. Owner receives notification with user details
4. Owner can approve or deny from admin panel
5. User gets notified of approval/denial

### For Authorized Users:
1. Send `/start` to see the main menu with conversation count
2. Click "💬 Start Chat" to begin conversation
3. Send any message and get instant AI response with memory
4. Bot remembers your previous conversations automatically
5. Use quick reply buttons (📜 Menu / 🗑️ Clear History) anytime
6. Clear chat history when you want to start fresh

### For Owner:
1. Full access to all features
2. Use `/admin` to access admin panel
3. Manage users with inline buttons
4. Approve/deny requests with one click

## Configuration Files

- `shadowgpt_config.json` - Bot configuration (model, language - API key from env only)
- `system-prompt.txt` - Custom system prompt for AI
- `whitelist.json` - List of authorized user IDs
- `pending_users.json` - Queue of pending access requests
- `chat_history/` - Per-user conversation history (auto-created)

## Setup Requirements

### Required Secrets (Environment Variables)

1. **TELEGRAM_BOT_TOKEN** - Get from @BotFather on Telegram
   - Open Telegram and search for @BotFather
   - Send `/newbot` and follow the instructions
   - Copy the token provided

2. **OPENROUTER_API_KEY** - Get from https://openrouter.ai/keys
   - Sign up at https://openrouter.ai/
   - Create a new API key
   - Copy the key (starts with "sk-or-v1-...")
   - Note: Some models are free, others require credits

Add both secrets to Replit Secrets for the bot to work properly.

## Technical Details

- **Language**: Python 3.11
- **Framework**: python-telegram-bot (async with typing indicators)
- **API**: OpenRouter (supports multiple AI providers)
- **Storage**: JSON files for data persistence
- **Memory**: Per-user chat history with 20 message limit
- **Security**: API keys from environment variables only

## Credits

Made By Aakash @CyberOgPro
