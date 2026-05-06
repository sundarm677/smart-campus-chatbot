# Smart Campus Chatbot 🎓

A modern, fully responsive React chatbot UI for campus-related inquiries with light/dark mode support using Bootstrap 5.

## 🚀 Features

### ✨ **Core Features**
- **React Components** - Modular, reusable component architecture
- **Responsive Design** - Works perfectly on Desktop, Tablet, Mobile, and Small Mobile devices
- **Dark Mode** - Toggle between light and dark themes with smooth transitions
- **Bootstrap 5** - Professional styling and layout components
- **Chat Interface** - Beautiful message bubbles with timestamps
- **Keyboard Support** - Enter to send, Shift+Enter for new line
- **Auto-scroll** - Latest messages automatically scroll into view
- **Typing Indicator** - Shows when bot is processing

### 📱 **Responsive Breakpoints**
- **Desktop** (≥1024px) - Sidebar always visible
- **Tablet** (768-1023px) - Sidebar toggles via menu button
- **Mobile** (<768px) - Full-width chat with toggle sidebar
- **Small Mobile** (<480px) - Optimized for tiny screens

## 📦 Tech Stack

- **React 18.2** - UI library
- **Vite 5.0** - Build tool (Fast HMR)
- **Bootstrap 5** - CSS framework
- **JavaScript (ES6+)** - Programming language
- **CSS3** - Custom styling with variables

## 🔧 Installation

### Prerequisites
- Node.js 16+ 
- npm or yarn

### Setup
```bash
# 1. Clone the repository
git clone https://github.com/sundarm677/smart-campus-chatbot.git
cd smart-campus-chatbot

# 2. Install dependencies
npm install

# 3. Start development server
npm run dev

# 4. Open browser
# Navigate to http://localhost:3000
```

## 📂 Project Structure

```
smart-campus-chatbot/
├── src/
│   ├── components/
│   │   ├── Header.jsx           # Navigation header with theme toggle
│   │   ├── Header.css
│   │   ├── Sidebar.jsx          # Conversation history sidebar
│   │   ├── Sidebar.css
│   │   ├── ChatWindow.jsx       # Main chat window
│   │   ├── ChatWindow.css
│   │   ├── Messages.jsx         # Message display component
│   │   ├── Messages.css
│   │   ├── ChatInput.jsx        # Input field component
│   │   └── ChatInput.css
│   ├── App.jsx                  # Main application component
│   ├── App.css
│   ├── main.jsx                 # React entry point
│   └── index.css                # Global styles & theme variables
├── index.html                   # HTML template
├── vite.config.js              # Vite configuration
├── package.json                # Dependencies
├── .eslintrc.json              # Linting rules
├── .gitignore                  # Git ignore rules
└── README.md                   # Documentation

```

## 🎨 Customization

### Change Theme Colors
Edit CSS variables in `src/index.css`:

```css
:root {
  --bg-primary: #ffffff;
  --text-primary: #212529;
  --chat-user-bg: #007bff;
  --chat-bot-bg: #e9ecef;
}

html.dark-mode {
  --bg-primary: #1a1a1a;
  --text-primary: #ffffff;
  --chat-user-bg: #0056b3;
  --chat-bot-bg: #2d2d2d;
}
```

### Connect Backend API
Update the bot response in `src/components/ChatWindow.jsx`:

```javascript
const response = await fetch('YOUR_API_ENDPOINT', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ message: text })
})
const data = await response.json()
```

## 📱 Responsive Features

| Feature | Desktop | Tablet | Mobile | Small Mobile |
|---------|---------|--------|--------|--------------|
| Sidebar | Visible | Toggle | Toggle | Toggle |
| Chat Width | 70% | 100% | 100% | 100% |
| Font Size | Normal | Normal | Small | Smaller |
| Message Max Width | 60% | 75% | 85% | 90% |
| Padding | 2rem | 1.5rem | 1rem | 0.75rem |

## 🎯 Usage

### Basic Message Flow
1. User types a question in the input field
2. Press Enter or click Send button
3. Message appears as blue bubble on the right
4. Bot processes and responds with gray bubble on the left
5. Messages auto-scroll to latest

### Toggle Dark Mode
Click the 🌙 icon in the header to toggle between light and dark themes

### Manage Conversations
- Click ➕ to create a new conversation
- Click ✕ to delete a conversation

## 🚀 Build & Deploy

### Development Build
```bash
npm run dev
```

### Production Build
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

The optimized files will be in the `dist/` folder ready for deployment.

## 📝 Code Quality

### Linting
```bash
npm run lint
```

Uses ESLint configuration optimized for React development.

## 🎓 Learning Resources

- [React Documentation](https://react.dev)
- [Bootstrap 5 Docs](https://getbootstrap.com/docs/5.0)
- [Vite Guide](https://vitejs.dev)
- [CSS Variables (Custom Properties)](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)

## 🐛 Troubleshooting

### Port Already in Use
```bash
# Change port in vite.config.js
server: {
  port: 3001  // Change to available port
}
```

### Dark Mode Not Persisting
To save theme preference, add localStorage:

```javascript
const toggleTheme = () => {
  setDarkMode(!darkMode)
  localStorage.setItem('darkMode', !darkMode)
}
```

### Slow Message Scroll
Update scroll behavior in `ChatWindow.jsx`:

```javascript
scrollToBottom()  // Change behavior if needed
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see LICENSE file for details.

## 👤 Author

**M SUNDAR**
- GitHub: [@sundarm677](https://github.com/sundarm677)
- Repository: [smart-campus-chatbot](https://github.com/sundarm677/smart-campus-chatbot)

## 🙋 Support

For questions or issues, please open an [GitHub Issue](https://github.com/sundarm677/smart-campus-chatbot/issues).

---

**Built with ❤️ using React & Bootstrap** 🚀
