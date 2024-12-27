# Discord Status Bot

A Python-based tool to update the status and custom presence of multiple Discord accounts. This script leverages Discord's WebSocket gateway for real-time status updates.

## Features

- Authenticate Discord accounts via token.
- Update status (e.g., online, idle, do not disturb) and set custom statuses with emojis.
- Support for animated emojis.
- Multi-account management with threading for simultaneous status updates.

---

## Prerequisites

### Dependencies
Ensure you have Python installed. The following libraries are required:
- `requests`
- `websocket-client`

You can install the dependencies using pip:

```bash
pip install requests websocket-client

Configuration

    Set Account Details
    Add your Discord account tokens and desired statuses in the accounts list at the bottom of the script:

accounts = [
    {
        "token": "<YOUR_DISCORD_TOKEN>",
        "status": "online",  # Status options: 'online', 'idle', 'dnd', 'invisible'
        "custom_status": "Available for chat",  # Your custom status
        "emoji_name": "smile",  # Name of emoji
        "emoji_id": "",  # ID of custom emoji (leave blank for standard emojis)
        "animated": True  # Set to True for animated emojis
    }
]

Run the Script
Execute the script:

    python <script_name>.py

    Replace <script_name> with the name of the Python file.

How It Works

    Authentication: Validates the Discord token and retrieves account details.
    WebSocket Connection: Connects to Discord's WebSocket gateway for real-time communication.
    Status Update: Sends authentication and custom status update payloads.
    Heartbeat: Maintains a stable connection with Discord's servers.

Example
Sample Configuration:

accounts = [
    {
        "token": "your-discord-token",
        "status": "dnd",
        "custom_status": "Busy coding",
        "emoji_name": "hammer",
        "emoji_id": "",
        "animated": False
    }
]

Output:

Logged in as JohnDoe#1234 (123456789012345678).

Limitations

    Discord's rate limits apply; avoid using too many accounts simultaneously or sending frequent updates.
    Misuse of this script may result in account bans.

Disclaimer

This project is for educational purposes only. Use responsibly and ensure compliance with Discord's Terms of Service and Developer Policy.
Contributing

Feel free to open issues or submit pull requests for improvements or bug fixes.
License

This project is licensed under the MIT License. See the LICENSE file for details.


This `README.md` explains the functionality, setup, and usage of the script while emphasizing responsible use. Let me know if you need any further refinements!

