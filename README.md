# GLaDOS AI Assistant

A desktop AI assistant that emulates GLaDOS from the Portal video game series, featuring the distinctive Aperture Science aesthetic and personality.

## Features

- 🤖 **GLaDOS Personality**: Sarcastic, condescending, yet helpful AI assistant
- 🎨 **Aperture Labs UI**: Clean, clinical interface with orange and blue accents
- 💬 **Natural Conversations**: Powered by OpenAI's GPT-4 API
- 🖥️ **Desktop Integration**: System tray, global shortcuts, always-on-top mode
- 📊 **System Diagnostics**: Fake monitoring panels with animated progress bars
- ⌨️ **Keyboard Shortcuts**: `Ctrl/Cmd + Shift + G` to show/hide window

## Installation

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn package manager
- OpenAI API key

### Quick Setup

1. **Clone or download the project**
   ```bash
   cd /path/to/GlaDOS
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` and add your OpenAI API key:
   ```
   OPENAI_API_KEY=your_openai_api_key_here
   ```

4. **Run the application**
   ```bash
   npm start
   ```
   
   Or use the convenient launch script:
   ```bash
   ./start-glados.sh
   ```

### Development Mode

To run with development tools enabled:
```bash
npm run dev
```

## Building for Distribution

### Windows
```bash
npm run build:win
```

### macOS
```bash
npm run build:mac
```

### Linux
```bash
npm run build:linux
```

Built applications will be available in the `dist/` directory.

## Configuration

### OpenAI API Key

1. Get an API key from [OpenAI](https://platform.openai.com/api-keys)
2. Add it to your `.env` file as shown above
3. Restart the application

### Customization

- **System Prompt**: Edit `src/renderer.js` line ~35 to modify GLaDOS personality
- **UI Theme**: Modify `src/styles.css` to change colors and styling
- **Window Settings**: Adjust `src/main.js` for window size and behavior

## Usage

### Basic Operation

1. Launch the application
2. Wait for GLaDOS startup sequence
3. Type your questions or requests in the chat input
4. Enjoy the sarcastic but helpful responses!

### Keyboard Shortcuts

- `Ctrl/Cmd + Shift + G` - Show/hide main window
- `Enter` - Send message
- `Ctrl/Cmd + M` - Minimize to system tray

### System Tray

Right-click the system tray icon for options:
- Show GLaDOS
- Run Diagnostic
- Terminate Testing Session

## Project Structure

```
GlaDOS/
├── src/
│   ├── main.js          # Electron main process
│   ├── renderer.js      # Frontend JavaScript
│   ├── index.html       # Main application UI
│   └── styles.css       # Aperture Labs styling
├── assets/              # Application icons and images
├── package.json         # Project configuration
├── .env.example         # Environment variables template
├── .env                 # Your API keys (not committed)
└── README.md           # This file
```

## Development

### File Overview

- **main.js**: Electron main process handling window management, system tray, and global shortcuts
- **renderer.js**: Frontend logic including OpenAI integration and chat functionality  
- **index.html**: Main application UI with Aperture Labs themed interface
- **styles.css**: Complete CSS styling with animations and responsive design

### Adding Features

1. **New UI Elements**: Add to `index.html` and style in `styles.css`
2. **New Functionality**: Add to `GladosAssistant` class in `renderer.js`
3. **System Integration**: Extend `main.js` with new Electron features

### Debugging

- Use `npm run dev` to enable DevTools
- Check console for JavaScript errors
- Verify `.env` file configuration

## Troubleshooting

### Common Issues

**"OpenAI API key not configured"**
- Ensure `.env` file exists in project root
- Verify `OPENAI_API_KEY=your_key_here` is set correctly
- Restart the application

**"Module not found" errors**
- Run `npm install` to install dependencies
- Check Node.js version (v16+ required)

**Window doesn't appear**
- Try `Ctrl/Cmd + Shift + G` to show window
- Check system tray for application icon
- Restart application

**API call failures**
- Verify OpenAI API key is valid and has credits
- Check internet connection
- Review console errors in development mode

**Sandbox errors on Linux**
- The app runs with `--no-sandbox` flag for compatibility
- This is normal for development environments
- For production, consider proper sandbox configuration

## Contributing

Feel free to submit issues and enhancement requests! When contributing:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

This project is a fan creation and is not affiliated with Valve Corporation or the Portal game series. GLaDOS and Portal are trademarks of Valve Corporation.
