# RGB Role Flasher Bot

RGB Role Flasher Bot is a customizable Discord bot that allows server administrators to manage roles with RGB color flashing, custom color settings, and delays. It includes a wide variety of commands for managing RGB roles, colors, and server-specific configurations.

## Features
- **RGB Role Flashing**: Automatically cycles through a set of colors for specified roles.
- **Custom Colors**: Add or remove custom colors for RGB role flashing.
- **Role Management**: Add or remove roles for RGB flashing.
- **Delay Configuration**: Set or reset the delay for RGB role color changes.
- **Help Menu**: Provides a list of available commands and descriptions.

## Installation

### Prerequisites
- [Node.js](https://nodejs.org/) (v16.9.0 or later)
- [Discord Developer Portal Application](https://discord.com/developers/applications) with a bot token

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/ThunderDoesDev/RGB-Role-Flasher-Bot.git
   cd RGB-Role-Flasher-Bot
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure the bot:
   - Rename `config.example.json` to `config.json`.
   - Update the configuration with your bot token and server-specific settings:
     ```json
     {
       "bot": {
         "botName": "YOUR_BOT_NAME",
         "botID": "YOUR_BOT_ID",
         "token": "YOUR_BOT_TOKEN"
       },
       "guilds": {
         "YOUR_GUILD_ID": {
           "roles": [],
           "colors": {
             "defaultColors": ["#FF0000", "#FF7F00", "#FFFF00", "#00FF00", "#0000FF", "#4B0082", "#8B00FF"],
             "customColors": []
           },
           "flashing": {
             "delay": 1000
           },
           "status": "stopped"
         }
       }
     }
     ```

4. Start the bot:
   ```bash
   node index.js
   ```

## Commands
| Command         | Description                                        |
|------------------|----------------------------------------------------|
| `/start_rgb`     | Starts the RGB role flashing.                     |
| `/stop_rgb`      | Stops the RGB role flashing.                      |
| `/add_color`     | Adds a custom color to the RGB role.              |
| `/remove_color`  | Removes a custom color from the RGB role.         |
| `/list_colors`   | Lists default and custom colors for the RGB role. |
| `/add_role`      | Adds a role to the RGB role flashing list.        |
| `/remove_role`   | Removes a role from the RGB role flashing list.   |
| `/list_roles`    | Lists roles currently configured for RGB flashing.|
| `/rgb_delay`     | Sets the delay for RGB role flashing (in ms).     |
| `/reset_rgb_delay` | Resets the delay for RGB role flashing to 1000ms.|
| `/help`          | Displays the help menu with all commands.         |

## Usage
1. Invite the bot to your server using the OAuth2 URL from the Discord Developer Portal.
2. Use the `/help` command to see the list of available commands.
3. Configure roles and colors using the commands.

> **Note**: Setting the delay for RGB role flashing to 1000ms or lower may cause excessive API requests, which could result in your IP being temporarily banned by Discord.

## Development

### Logging
The bot uses a logger for tracking events. Ensure the `logger.js` file is present in the project directory.

### Errors Handling
The bot uses a error handling for tracking errors. Ensure the `errors.js` file is present in the project directory.

## Support
For support, issues, or enhancements, please open an issue in this repository or join our discord support server.

[Join Support Server](https://discord.gg/thunderdoesdev)

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [Discord.js](https://discord.js.org/) for providing the library for Discord API integration.
- [CFonts](https://github.com/dominikwilkowski/cfonts) for the beautiful console fonts.
