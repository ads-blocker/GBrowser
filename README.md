# 🌐 Gorstak's Browser

A feature-rich, privacy-focused web browser built with PyQt6 and QtWebEngine. Gorstak's Browser combines modern browsing capabilities with built-in ad blocking, credential management, and a clean, customizable interface.

![Python Version](https://img.shields.io/badge/python-3.8+-blue.svg)
![PyQt6](https://img.shields.io/badge/PyQt6-6.0+-green.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## ✨ Features

### Core Browsing
- **Multi-Tab Interface** - Modern tabbed browsing with drag-and-drop tab reordering
- **Full Video Support** - Watch videos with automatic codec support and fullscreen capabilities
- **Persistent Sessions** - Automatically saves and restores your browsing session
- **Fast Navigation** - Smooth page loading with hardware acceleration

### Privacy & Security
- **Built-in Ad Blocker** - Blocks ads and trackers from major networks (Google, Facebook, etc.)
- **Secure Credential Manager** - Encrypted password storage with auto-fill functionality
- **Special Discord Support** - React-aware credential injection for Discord login
- **No Tracking** - Hyperlink auditing disabled by default

### User Experience
- **Bookmark Management** - Quick access to your favorite sites with visual indicators
- **Download Manager** - Built-in download handling with progress tracking
- **Custom Styling** - Dark theme interface optimized for extended use
- **Smart URL Bar** - Automatic HTTPS upgrade and search integration

## 📋 Requirements

- Python 3.8 or higher
- PyQt6
- PyQt6-WebEngine
- BeautifulSoup4

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/gorstaks-browser.git
cd gorstaks-browser
```

### 2. Install Dependencies
```bash
pip install PyQt6 PyQt6-WebEngine beautifulsoup4
```

### 3. Run the Browser
```bash
python GBrowser.py
```

## 💻 Usage

### Basic Navigation
- **Back/Forward** - Navigate through your browsing history
- **Reload** - Refresh the current page
- **Home** - Return to your home page (Google by default)
- **Search/URL Bar** - Enter URLs or search terms

### Tab Management
- **New Tab** - Click the "+" button or use Ctrl+T (when implemented)
- **Close Tab** - Click the "×" on any tab
- **Switch Tabs** - Click on tabs or drag to reorder

### Bookmarks
- **Add Bookmark** - Click the bookmark button in the navigation bar
- **Access Bookmarks** - Use the overflow menu to view all bookmarks
- **Manage Bookmarks** - Edit or delete bookmarks from the bookmark manager

### Ad Blocking
The ad blocker is enabled by default and blocks:
- Major ad networks (Google Ads, DoubleClick)
- Social media trackers (Facebook, Twitter, LinkedIn)
- Analytics platforms (Google Analytics, Mixpanel, Segment)
- Popup and overlay annoyances

### Credential Management
- **Auto-Save** - Credentials are automatically captured on login
- **Auto-Fill** - Saved credentials are automatically filled on return visits
- **Secure Storage** - All credentials are stored in `~/.gorstak_browser/credentials.json`

## ⚙️ Configuration

Configuration files are stored in `~/.gorstak_browser/`:
- `CONFIG_FILE` - Browser settings, bookmarks, and window geometry
- `credentials.json` - Encrypted login credentials
- `storage/` - Persistent browser storage and cookies
- `cache/` - Temporary cache files

### Customizing Ad Blocking
Edit the `AD_DOMAINS` set and `AD_URL_PATTERNS` list in the source code to add or remove blocked domains.

## 🗂️ Project Structure

```
gorstaks-browser/
├── GBrowser.py           # Main application file
├── README.md             # This file
└── .gorstak_browser/     # Auto-generated config directory
    ├── CONFIG_FILE       # Browser configuration
    ├── credentials.json  # Saved credentials
    ├── storage/          # Persistent storage
    └── cache/            # Temporary cache
```

## 🔧 Technical Details

### Architecture
- **Framework**: PyQt6 with QtWebEngine (Chromium-based)
- **UI Design**: Custom dark theme with SVG icons
- **Storage**: JSON-based configuration with file system persistence
- **Ad Blocking**: Request-level URL interception

### Key Components
- `Browser` - Main window and application controller
- `BrowserTab` - Individual tab with web view
- `CustomWebPage` - Enhanced web page with custom permissions
- `AdBlocker` - Request interceptor for ad blocking
- `CredentialsManager` - Secure credential storage and retrieval
- `BookmarkManager` - Bookmark CRUD operations

## 🛡️ Privacy

Gorstak's Browser prioritizes your privacy:
- ✅ Local-only credential storage
- ✅ Built-in ad and tracker blocking
- ✅ No telemetry or usage tracking
- ✅ Full control over cookies and cache
- ✅ Persistent storage isolated to user directory

## 🐛 Known Issues

- Cache lock files may persist after crashes (automatically cleaned on startup)
- Some JavaScript-heavy sites may require special handling
- Download progress may not show for all file types

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Setup
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built with [PyQt6](https://www.riverbankcomputing.com/software/pyqt/)
- Web engine powered by [Chromium](https://www.chromium.org/)
- Ad blocking inspired by common blocklist formats

## 📧 Contact

For questions, issues, or suggestions, please open an issue on GitHub.

---

**Note**: This browser is designed for personal use and learning purposes. For production environments, consider using established browsers with professional security audits.
