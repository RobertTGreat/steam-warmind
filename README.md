# Steam Raycast Extension

A Raycast extension for Windows that allows you to launch and manage Steam games directly from your Raycast interface.

## Features

### 📚 Steam Library
- **Real Steam Integration**: Reads your actual installed Steam games
- **Library Parsing**: Automatically detects Steam installation and library folders
- **Game Details**: Shows file sizes, installation paths, and last update times
- **Multiple Libraries**: Supports multiple Steam library locations
- **Launch Games**: Direct launch from your installed library

### 🛒 Steam Store
- Browse Steam Store categories
- Access featured games, new releases, top sellers
- Navigate to different game genres
- Open Steam client and Big Picture mode

## Installation

1. Make sure you have Raycast for Windows beta installed
2. Clone this repository
3. Run `npm install` to install dependencies
4. Use `npm run dev` to test the extension in development mode

## Usage

### Launching Games
1. Open Raycast and search for "Steam Library"
2. Browse your installed games
3. Click on any game to launch it


### Popular Steam App IDs
- **Dota 2**: 570
- **Counter-Strike 2**: 730
- **Team Fortress 2**: 440
- **Grand Theft Auto V**: 271590
- **Apex Legends**: 1172470
- **Baldur's Gate 3**: 1244460

### Steam Store Categories
- Featured games and deals
- New releases
- Top sellers
- Free-to-play games
- Early Access games
- VR Games
- Indie Games
- Action Games
- RPG Games
- Strategy Games
- Simulation Games
- Sports Games

## Technical Details

- **Built with React and TypeScript**
- **Uses Raycast API for Windows**
- **Supports Steam protocol URLs** (`steam://`)
- **Real Steam Integration**:
  - Reads Steam installation from Windows Registry
  - Parses `libraryfolders.vdf` for multiple library locations
  - Reads `appmanifest_*.acf` files for installed games
  - Uses local game database for reliable search
- **PowerShell Integration**: Uses PowerShell for file system access
- **Error Handling**: Graceful fallbacks when Steam is not installed
- **Cross-platform**: Works on Windows (with Steam) and macOS

## Development

```bash
# Install dependencies
npm install

# Start development mode
npm run dev

# Build for production
npm run build

# Lint code
npm run lint

# Fix linting issues
npm run fix-lint
```

## Platform Support

- ✅ Windows (Raycast Beta)
- ✅ macOS (Raycast)

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - see LICENSE file for details

## Author

robert_robertson

## Notes

- **Steam Required**: This extension requires Steam to be installed on your system
- **Real Data**: Uses actual Steam library files and Steam Web API
- **Windows Registry**: Reads Steam installation path from Windows Registry
- **File Permissions**: Requires read access to Steam installation directory
- **API Limits**: Steam Web API has rate limits (handled gracefully)
- **Fallback Data**: Uses popular games list when API is unavailable
- **Raycast Windows Beta**: Designed to work with Raycast for Windows beta

## How It Works

### Library Detection
1. Reads Steam installation path from Windows Registry
2. Parses `libraryfolders.vdf` to find all Steam library locations
3. Reads `appmanifest_*.acf` files for each installed game
4. Extracts game details (App ID, name, size, installation path)


### Game Launching
1. Uses Steam protocol URLs (`steam://run/{appId}`)
2. Launches games through Steam client
3. Works with any Steam game or application