# 🚀 Chatwork Helper Extension

A Chrome Extension that enhances your Chatwork experience with powerful utilities and beautiful modern UI design.

## ✨ Key Features

### 📝 **Formatting Tools**
- **[code]** - Quickly insert code blocks
- **[title]** - Create highlighted titles  
- **[info]** - Insert info notifications
- **[hr]** - Add horizontal dividers

### 😊 **Emoji Picker**
- Rich emoji collection with 80+ emoticons
- Beautiful picker interface with smooth animations
- Quick search and insert functionality
- Support for ESC key and click-outside to close

### ⏰ **Auto Check-in** 
- Automatically send check-in messages in specific rooms
- Only displays in configured rooms
- Auto-send messages without manual Send button click

## 🎨 User Interface

- **Glassmorphism Design**: Modern frosted glass effects
- **Smooth Animations**: Fluid transitions and interactions
- **Hover Effects**: Visual feedback on user interactions
- **Responsive**: Smart positioning that adapts to screen space

## 📦 Installation

### 1. Download Extension
```bash
git clone https://github.com/viethai-dev/chatwork-plus
```

### 2. Install in Chrome
1. Open Chrome and navigate to `chrome://extensions/`
2. Enable **Developer mode** in the top right corner
3. Click **Load unpacked**
4. Select the extension folder
5. Extension will appear in your extensions list

### 3. Usage
1. Navigate to [Chatwork](https://www.chatwork.com)
2. Utility buttons will automatically appear in the chat input area
3. Click buttons to use features

## 🗂️ Project Structure

```
chatwork-helper-extension/
├── manifest.json          # Extension configuration
├── content.js            # Main script
├── assets/
│   └── constant.js       # Emoji list and constants
├── icons/
│   ├── icon16.png       # 16x16 icon
│   ├── icon48.png       # 48x48 icon
│   └── icon128.png      # 128x128 icon
└── README.md            # This documentation
```

## ⚙️ Configuration

### Customize Check-in Room
To change the check-in room, modify the URL in `content.js`:
```javascript
if (window.location.href.includes('#!rid12345678')) {
    // Replace '12345678' with your room ID
}
```

### Customize Check-in Message
```javascript
const checkInMessage = `[To:ID]Bot\nCheckin`;
// Modify message content here
```

### Add/Remove Emojis
Edit the `assets/constant.js` file:
```javascript
export const emojiList = [
    '😀', '😃', '😄', // Add new emojis here
    // ...
];
```

## 🎯 Advanced Features

### Smart Positioning
- Emoji picker automatically adjusts position to avoid screen overflow
- Prioritizes bottom placement, automatically switches to top when needed

### Keyboard Shortcuts
- **ESC**: Close emoji picker
- **Enter**: Send message (standard Chatwork behavior)

### Error Handling
- Fallback emoji list when constants file fails to load
- Graceful degradation when permissions are missing

## 🛠️ Development

### Prerequisites
- Chrome Browser
- Basic knowledge of JavaScript ES6+
- Understanding of Chrome Extension APIs

### Local Development
1. Clone repository
2. Make changes to `content.js` or `assets/constant.js`
3. Reload extension in `chrome://extensions/`
4. Test on Chatwork

### Build & Release
```bash
# Minify and obfuscate code (optional)
# Use tools like terser or webpack

# Create .zip file for Chrome Web Store submission
zip -r chatwork-helper-extension.zip . -x "*.git*" "node_modules/*" "*.md"
```

## 🐛 Troubleshooting

### Extension Not Working
1. Check Console errors in DevTools
2. Ensure `manifest.json` has correct format
3. Reload extension in Chrome Extensions

### Emojis Not Loading
1. Verify `assets/constant.js` has proper exports
2. Check `web_accessible_resources` in manifest
3. Inspect Network tab in DevTools

### Check-in Not Auto-sending
1. Verify room ID in URL
2. Check selector `[data-testid="timeline_send-message-button"]`
3. Verify permissions

## 📝 Changelog

### v1.0 (Current)
- ✅ Formatting tools (code, title, info, hr)
- ✅ Emoji picker with 80+ emojis
- ✅ Auto check-in for specific rooms
- ✅ Glassmorphism UI design
- ✅ Smart positioning system

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Credits

- **Icons**: [Flaticon](https://www.flaticon.com)
- **Emoji**: Unicode Standard
- **Design Inspiration**: Modern Glassmorphism trends

## 📧 Support

If you encounter issues or have suggestions:
- 📧 Email: viethai.dev@gmail.com
- 🐛 Issues: [GitHub Issues](https://github.com/viethai-dev/chatwork-plus/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/viethai-dev/chatwork-plus/discussions)

---

⭐ **Star this repo if you find it helpful!** ⭐
