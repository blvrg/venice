# Multi-Character Chat

This subdirectory contains a multi-character conversation feature where two AI characters can talk to each other.

## How It Works

1. **Character Selection**: Choose two different characters from your available Venice AI characters
2. **Initial Prompt**: Provide a starting prompt that will be sent to Character 1
3. **Conversation Loop**:
   - Character 1 receives the initial prompt and responds
   - Character 1's response becomes the input for Character 2
   - Character 2's response becomes the input for Character 1
   - This continues back-and-forth for the specified number of exchanges

## Features

- **Visual Character Display**: Each character is shown with their avatar and name
- **Conversation Context**: Each character maintains their own conversation history for better context
- **Configurable Exchanges**: Set how many back-and-forth exchanges should occur (1-50)
- **Stop/Start Controls**: Stop the conversation at any time and restart with a new prompt
- **Message Attribution**: Each message clearly shows which character said it
- **Separate Storage**: Uses separate localStorage keys from the main chat app

## Usage

1. Open `multi/index.html` in your browser
2. Enter your Venice AI API key
3. Select two characters you want to have a conversation
4. Set the number of exchanges (default: 10)
5. Enter an initial prompt (e.g., "Let's discuss the meaning of life")
6. Click "Start" to begin the conversation
7. Click "Stop" at any time to pause the conversation

## Example Prompts

- "Let's debate whether AI can be creative"
- "Tell me about your favorite book"
- "What do you think about the future of humanity?"
- "Let's write a story together"

## Technical Details

- Each character maintains separate conversation context (last 20 messages)
- API calls are made sequentially: Character 1 → Character 2 → Character 1...
- The conversation automatically stops when the exchange limit is reached
- All conversations are stored in the browser's localStorage

## Differences from Main Chat

- Supports two characters instead of one
- Automated conversation flow instead of manual user input
- Different localStorage keys (`veniceMultiApiKey`, etc.)
- No image or voice mode (text only)
- Optimized for character-to-character interaction
