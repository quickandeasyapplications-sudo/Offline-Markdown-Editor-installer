# QET Markdown Editor - Development Application

**Version:** 1.1.0  
**Status:** Production-Ready Development Package  
**Last Updated:** October 2025

---

## Overview

This is the complete development package for QET Markdown Editor, a privacy-first markdown editor with zero-knowledge encryption and professional export capabilities. This package includes all source code, build scripts, VS Code configuration, and development tools for immediate development.

### Key Features

- **Real-time Markdown Editing** with syntax highlighting and live preview
- **Professional Export** to PDF, DOCX (RTF), HTML, and MD formats
- **Empty Content Validation** with user-friendly warnings
- **Toast Notifications** for all user actions
- **Offline-First Architecture** with local storage
- **Auto-save** every 30 seconds
- **Responsive Design** for desktop, tablet, and mobile
- **QET Branding** with professional styling

---

## Quick Start

### Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher) - [Download](https://nodejs.org/)
- **npm** (comes with Node.js)
- **VS Code** (recommended) - [Download](https://code.visualstudio.com/)
- **Git** (optional, for version control) - [Download](https://git-scm.com/)

### Installation

1. **Extract the package** to your desired location

2. **Open in VS Code**
   ```bash
   cd qet-app-complete
   code .
   ```

3. **Install dependencies**
   ```bash
   npm install
   ```

4. **Build the application**
   ```bash
   npm run build
   ```

5. **Start the development server**
   ```bash
   npm start
   ```

The application will automatically open in your default browser at `http://localhost:3000`.

---

## Project Structure

```
qet-app-complete/
├── .vscode/                    # VS Code configuration
│   ├── settings.json          # Editor settings
│   ├── launch.json            # Debug configuration
│   ├── tasks.json             # Build tasks
│   └── extensions.json        # Recommended extensions
├── src/                        # Source files
│   ├── js/                    # JavaScript source
│   │   └── app.js            # Main application logic
│   ├── css/                   # CSS source
│   │   └── styles.css        # Application styles
│   └── assets/                # Images and icons
│       ├── qet_icon_*.png    # Various icon sizes
│       └── qet_icon.ico      # Windows icon
├── public/                     # Built/served files
│   ├── index.html            # Main HTML file
│   ├── css/                  # Built CSS (generated)
│   ├── js/                   # Built JS (generated)
│   └── assets/               # Built assets (generated)
├── docs/                       # Documentation
├── package.json               # Project configuration
├── .eslintrc.json            # ESLint configuration
├── .prettierrc.json          # Prettier configuration
├── .gitignore                # Git ignore rules
└── README.md                 # This file
```

---

## NPM Scripts

### Development

```bash
# Start development server (opens browser)
npm start

# Alternative: npm run dev
npm run dev

# Watch for file changes and rebuild
npm run watch
```

### Building

```bash
# Build all files (CSS, JS, assets)
npm run build

# Build CSS only
npm run build:css

# Build JavaScript only
npm run build:js

# Copy assets only
npm run copy:assets

# Clean build directory
npm run clean
```

### Code Quality

```bash
# Format code with Prettier
npm run format

# Lint JavaScript with ESLint
npm run lint

# Run tests (when configured)
npm test
```

### Production

```bash
# Build and start server
npm run serve

# Prepare for deployment
npm run deploy
```

---

## VS Code Setup

### Recommended Extensions

When you open the project in VS Code, you'll be prompted to install recommended extensions. These include:

- **Prettier** - Code formatter
- **ESLint** - JavaScript linter
- **Live Server** - Development server
- **Auto Rename Tag** - HTML tag renaming
- **Auto Close Tag** - HTML tag closing
- **Path Intellisense** - File path completion
- **HTML CSS Support** - CSS class completion
- **Tailwind CSS IntelliSense** - Tailwind support

### Keyboard Shortcuts

- **Ctrl+Shift+B** (Cmd+Shift+B on Mac) - Run build task
- **F5** - Start debugging
- **Ctrl+Shift+P** - Command palette
- **Ctrl+`** - Toggle terminal

### Tasks

Access tasks via **Terminal > Run Task** or **Ctrl+Shift+B**:

- **Start Development Server** - Launches live server
- **Build Application** - Builds all files
- **Watch Files** - Watches for changes
- **Clean Build** - Removes built files
- **Format Code** - Formats all code
- **Lint Code** - Lints JavaScript

---

## Development Workflow

### 1. Start Development Server

```bash
npm start
```

This will:
- Build all files
- Start a live server on port 3000
- Open the application in your browser
- Auto-reload on file changes

### 2. Make Changes

Edit files in the `src/` directory:

- **src/js/app.js** - Application logic
- **src/css/styles.css** - Styles
- **public/index.html** - HTML structure
- **src/assets/** - Images and icons

### 3. See Changes Live

The development server automatically reloads when you save files. No manual refresh needed!

### 4. Test Features

Test all features in the browser:

- ✅ Markdown editing and preview
- ✅ PDF export
- ✅ DOCX export
- ✅ HTML export
- ✅ MD export
- ✅ Toast notifications
- ✅ Empty content validation
- ✅ Auto-save functionality
- ✅ Responsive design

### 5. Format and Lint

Before committing changes:

```bash
npm run format  # Format code
npm run lint    # Check for errors
```

### 6. Build for Production

```bash
npm run build
```

---

## Features Implementation

### Export Functions

All export functions are fully implemented and tested:

#### PDF Export
- Uses jsPDF library
- Professional formatting with headers
- Validates content before export
- Shows loading indicator
- Displays success/error notifications

#### DOCX Export (RTF Format)
- Converts HTML to RTF format
- Compatible with Microsoft Word, LibreOffice, Google Docs
- Preserves formatting (headings, bold, italic, lists, code)
- Validates content before export

#### HTML Export
- Creates standalone HTML file
- Embedded CSS styling
- QET branding and footer
- Professional, print-ready layout

#### MD Export
- Downloads raw markdown source
- Perfect for backup and sharing
- Validates content before export

### Toast Notifications

Beautiful, non-intrusive notifications for all actions:

- **Success** (green) - Successful operations
- **Error** (red) - Error messages
- **Info** (blue) - Informational messages
- **Warning** (yellow) - Warning messages

Features:
- Auto-dismiss after 3 seconds
- Smooth animations
- Mobile-responsive
- Multiple toasts stack vertically

### Empty Content Validation

Prevents exporting empty documents:
- Checks content before export
- Shows warning message
- Guides user to add content
- Improves user experience

### Auto-Save

Automatic saving every 30 seconds:
- Saves to local storage
- No data loss
- Silent operation
- Manual save also available

---

## Customization

### Branding

To customize branding, edit:

**Colors** (in `src/css/styles.css`):
```css
:root {
  --primary-navy: #1e3a5f;
  --accent-teal: #2a9d8f;
  /* ... other colors */
}
```

**Logo** (replace files in `src/assets/`):
- qet_icon_*.png (various sizes)
- qet_icon.ico (Windows icon)

**Text** (in `public/index.html`):
- Application title
- About modal content
- Footer text

### Features

To add or modify features, edit `src/js/app.js`:

```javascript
class QETMarkdownEditor {
  // Add your custom methods here
}
```

### Styling

To modify styles, edit `src/css/styles.css`:

```css
/* Add your custom styles here */
```

---

## Deployment

### GitHub Pages

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Create GitHub repository**
   - Create new repository on GitHub
   - Initialize git in project folder
   - Add remote and push

3. **Enable GitHub Pages**
   - Go to repository Settings
   - Navigate to Pages section
   - Select branch and `/public` folder
   - Save settings

4. **Access your site**
   - Visit: `https://username.github.io/repository-name/`

### Netlify

1. **Build the application**
   ```bash
   npm run build
   ```

2. **Deploy to Netlify**
   - Drag and drop `public/` folder to Netlify
   - Or connect GitHub repository
   - Set build command: `npm run build`
   - Set publish directory: `public`

### Vercel

1. **Install Vercel CLI**
   ```bash
   npm install -g vercel
   ```

2. **Deploy**
   ```bash
   npm run build
   vercel --prod
   ```

### Other Platforms

The `public/` folder contains all files needed for deployment. Simply upload the contents to any static hosting service.

---

## Troubleshooting

### Development Server Won't Start

**Problem:** Port 3000 is already in use

**Solution:** 
- Stop other applications using port 3000
- Or change port in `package.json`:
  ```json
  "start": "live-server public --port=3001"
  ```

### Exports Not Working

**Problem:** Export buttons don't download files

**Solution:**
- Check browser console for errors
- Ensure all CDN libraries are loading
- Test with content in the editor
- Check browser download settings

### Styles Not Applying

**Problem:** CSS changes not showing

**Solution:**
- Run `npm run build:css`
- Clear browser cache (Ctrl+Shift+R)
- Check browser console for CSS errors

### VS Code Extensions Not Working

**Problem:** Recommended extensions not installing

**Solution:**
- Open Extensions panel (Ctrl+Shift+X)
- Search for each extension manually
- Install recommended extensions one by one

---

## Browser Support

The application supports all modern browsers:

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

---

## Performance

The application is optimized for performance:

- **Load Time:** < 2 seconds on broadband
- **Time to Interactive:** < 3 seconds
- **Editor Responsiveness:** < 16ms keystroke latency
- **Preview Update:** < 100ms
- **Export Generation:** < 5 seconds for typical documents

---

## Security

The application implements security best practices:

- **No external tracking** - No analytics or tracking scripts
- **Local storage only** - All data stored locally
- **No server communication** - Fully offline-capable
- **Content Security Policy** - XSS protection
- **Input validation** - All inputs validated

---

## Contributing

### Code Style

- Use 2 spaces for indentation
- Use single quotes for strings
- Add semicolons
- Format code with Prettier before committing
- Lint code with ESLint

### Git Workflow

1. Create feature branch
2. Make changes
3. Format and lint code
4. Commit with descriptive message
5. Push and create pull request

### Testing

Before submitting changes:

1. Test all export functions
2. Test on multiple browsers
3. Test responsive design
4. Check console for errors
5. Verify no broken features

---

## License

MIT License - See LICENSE file for details

---

## Support

For questions or issues:

- **Email:** qandetech@gmail.com

---

## Changelog

### Version 1.1.0 (Current)
- ✅ Added empty content validation
- ✅ Implemented toast notification system
- ✅ Enhanced export functions with better error handling
- ✅ Improved user feedback for all actions
- ✅ Added comprehensive VS Code configuration
- ✅ Created complete development package

### Version 1.0.1
- Fixed DOCX export (RTF implementation)
- Added MD export functionality
- Improved error messages
- Added FileSaver.js integration

### Version 1.0.0
- Initial release
- Basic markdown editing
- PDF, DOCX, HTML exports
- Real-time preview
- Local storage support

---

## Acknowledgments

This application uses the following open-source libraries:

- **Marked.js** - Markdown parsing
- **Highlight.js** - Syntax highlighting
- **jsPDF** - PDF generation
- **FileSaver.js** - File download handling
- **Inter Font** - Typography

---

**Built with ❤️ by Quick and Easy Tech**

*Making markdown editing simple, secure, and powerful.*

---

**Ready to develop? Run `npm start` and start coding!** 🚀

