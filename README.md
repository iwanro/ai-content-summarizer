# 🤖 AI Content Summarizer

A powerful Chrome extension that summarizes any web page using AI technology (DeepSeek or Google Gemini). Get instant, concise summaries of articles, blog posts, documentation, and any web content with just one click!

![Version](https://img.shields.io/badge/version-0.0.1-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Chrome](https://img.shields.io/badge/chrome-extension-orange)

## ✨ Features

- 🚀 **One-Click Summarization** - Summarize any webpage instantly
- 🤖 **Multiple AI Providers** - Choose between DeepSeek or Google Gemini
- 🎯 **Smart Content Extraction** - Automatically extracts relevant text from any page
- 💎 **Free & Pro Tiers**:
  - **Free**: 5 summarizations per day
  - **Pro**: Unlimited summarizations (simulated toggle in settings)
- 🎨 **Clean, Modern UI** - Beautiful interface built with React and TailwindCSS
- ⚙️ **Customizable** - Configure your preferred AI provider and API key
- 🔄 **Daily Reset** - Free tier credits reset automatically every day

## 📸 Screenshots

### Popup Interface
The main extension popup where you can summarize the current page:
- View your remaining credits (Free plan)
- One-click summarization
- Clean, readable summary display

### Settings Page
Configure your AI provider and manage your plan:
- Switch between DeepSeek and Gemini
- Enter your API key
- Toggle Pro plan for unlimited access

## 🛠️ Tech Stack

- **Framework**: [Plasmo](https://www.plasmo.com/) - The browser extension framework
- **UI**: React + TypeScript
- **Styling**: TailwindCSS
- **Storage**: Chrome Storage API via @plasmohq/storage
- **AI Providers**:
  - [DeepSeek API](https://platform.deepseek.com/)
  - [Google Gemini API](https://ai.google.dev/)

## 📦 Installation

### Prerequisites

- Node.js (v16 or higher)
- pnpm (recommended) or npm
- Chrome browser

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/ai-content-summarizer.git
   cd ai-content-summarizer
   ```

2. **Install dependencies**
   ```bash
   pnpm install
   # or
   npm install
   ```

3. **Get an API Key**
   
   Choose your preferred AI provider and get an API key:
   
   **Option A: DeepSeek (Recommended - Lower cost)**
   - Go to [DeepSeek Platform](https://platform.deepseek.com/)
   - Sign up for an account
   - Generate an API key
   
   **Option B: Google Gemini**
   - Go to [Google AI Studio](https://aistudio.google.com/)
   - Sign in with your Google account
   - Create an API key

4. **Build the extension**
   
   For development (with hot reload):
   ```bash
   pnpm dev
   # or
   npm run dev
   ```
   
   For production:
   ```bash
   pnpm build
   # or
   npm run build
   ```

5. **Load the extension in Chrome**
   
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable **Developer mode** (toggle in top-right corner)
   - Click **Load unpacked**
   - Select the `build/chrome-mv3-prod` folder (or `build/chrome-mv3-dev` for development)

6. **Configure the extension**
   
   - Click on the extension icon in your toolbar
   - Click the gear icon (⚙️) to open settings
   - Select your AI provider (DeepSeek or Gemini)
   - Enter your API key
   - Click **Save Options**

## 🚀 Usage

1. **Navigate to any webpage** you want to summarize
2. **Click the extension icon** in your browser toolbar
3. **Click "Summarize Page"** button
4. **Read the AI-generated summary** in seconds!

### Free Plan
- 5 summarizations per day
- Credits reset automatically at midnight
- Perfect for casual users

### Pro Plan (Simulated)
- Go to Settings (gear icon)
- Check **"Simulate Pro Plan (Unlimited)"**
- Click **Save Options**
- Enjoy unlimited summarizations!

## 🔧 Development

### Project Structure

```
ai-content-summarizer/
├── assets/              # Extension icons and images
├── utils/
│   ├── ai.ts           # AI integration (DeepSeek & Gemini)
│   └── storage.ts      # Storage utilities & user management
├── popup.tsx           # Main popup interface
├── options.tsx         # Settings/options page
├── content.ts          # Content script (text extraction)
├── manifest.json       # Extension manifest
├── style.css           # Global styles
└── tailwind.config.js  # TailwindCSS configuration
```

### Available Scripts

```bash
# Development with hot reload
pnpm dev

# Production build
pnpm build

# Package for distribution
pnpm package

# Format code with Prettier
pnpm format
```

### Making Changes

1. Edit the source files (`.tsx`, `.ts`)
2. The extension will automatically rebuild (in dev mode)
3. Reload the extension in `chrome://extensions/`
4. Test your changes

## 🔐 Privacy & Security

- **API Keys**: Stored locally in Chrome's secure storage
- **No Data Collection**: We don't collect or store any user data
- **Content Processing**: Page content is sent only to your chosen AI provider
- **Open Source**: Full transparency - review the code yourself

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🐛 Known Issues

- TypeScript warning about string/boolean comparison in storage.ts (harmless, handles both string and boolean values)
- TailwindCSS content pattern warning (doesn't affect functionality)

## 🗺️ Roadmap

- [ ] Support for more AI providers (Claude, OpenAI, etc.)
- [ ] Customizable summary length
- [ ] Summary history
- [ ] Export summaries to markdown/PDF
- [ ] Multiple language support
- [ ] Real payment integration for Pro plan

## 💡 Tips

- **Choose DeepSeek** for lower API costs
- **Use Pro mode** during development for unlimited testing
- **Check Console** (F12) for any API errors
- **Daily limits** reset at midnight in your timezone

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Check existing issues for solutions
- Review the code - it's well-commented!

## 🙏 Acknowledgments

- Built with [Plasmo Framework](https://www.plasmo.com/)
- AI powered by [DeepSeek](https://www.deepseek.com/) and [Google Gemini](https://deepmind.google/technologies/gemini/)
- Icons from [Heroicons](https://heroicons.com/)

---

**Made with ❤️ with Antigravity**

⭐ Star this repo if you find it helpful!
