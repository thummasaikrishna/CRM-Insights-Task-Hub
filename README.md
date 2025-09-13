# CRM-Insights-Task-Hub
Interactive Retro Board built with Salesforce Lightning Web Components. Features drag-and-drop, real-time editing, and responsive design. Perfect for team retrospectives with customizable columns and optional data persistence. Medium-level LWC project showcasing component architecture and modern UI patterns.
# 🎯 CRM-Insights-Task-Hub- Lightning Web Components

A modern, interactive retrospective board built with Salesforce Lightning Web Components (LWC). This project allows teams to conduct effective retrospective meetings with a clean, intuitive interface.

![Project Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![Salesforce](https://img.shields.io/badge/Salesforce-LWC-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The Retro Board is an interactive Lightning Web Component that enables teams to conduct retrospective meetings directly within Salesforce. Users can add, edit, and organize feedback items across different categories (What Went Well, What Could Be Improved, Action Items).

**Difficulty Level:** Medium  
**Estimated Time:** 4-6 hours  
**Skills Required:** Basic LWC, HTML, CSS, JavaScript

## ✨ Features

### Core Features
- ✅ Interactive board with multiple columns
- ✅ Add, edit, and delete retrospective items
- ✅ Drag and drop functionality (optional)
- ✅ Real-time updates
- ✅ Responsive design for mobile and desktop
- ✅ Clean, modern UI with hover effects

### Advanced Features (Planned)
- 🔄 Data persistence using Salesforce records
- 👥 Multi-user collaboration
- 📊 Export retrospective data
- 🎨 Customizable themes
- 🔔 Notifications and reminders

## 🛠️ Prerequisites

Before you begin, ensure you have:

- **Salesforce Developer Org** (Free signup at [developer.salesforce.com](https://developer.salesforce.com))
- **Salesforce CLI** installed
- **Visual Studio Code** with Salesforce Extension Pack
- **Node.js** (LTS version recommended)
- Basic knowledge of:
  - Lightning Web Components
  - HTML, CSS, JavaScript
  - Salesforce platform basics

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/thummasaikrishna/retro-board-lwc.git
cd retro-board-lwc
```

### 2. Authorize Your Salesforce Org
```bash
sfdx auth:web:login -d -a DevOrg
```

### 3. Deploy to Salesforce
```bash
sfdx force:source:push
```

### 4. Assign Permission Set (if applicable)
```bash
sfdx force:user:permset:assign -n Retro_Board_User
```

### 5. Open Your Org
```bash
sfdx force:org:open
```

## 📱 Usage

### Adding the Component to a Page

1. **Lightning App Builder:**
   - Go to Setup → Lightning App Builder
   - Create new Lightning Page or edit existing
   - Drag the "Retro Board" component to your page
   - Save and activate

2. **Lightning Record Page:**
   - Navigate to any record
   - Click Setup → Edit Page
   - Add the Retro Board component
   - Configure properties as needed

### Using the Retro Board

1. **Add Items:** Click the "+" button in any column
2. **Edit Items:** Click on any item to edit inline
3. **Move Items:** Drag items between columns
4. **Delete Items:** Click the delete icon on hover
5. **Save Progress:** Changes auto-save (if backend connected)

## 📂 Project Structure

```
force-app/main/default/
├── lwc/
│   ├── retroBoard/
│   │   ├── retroBoard.html          # Main component template
│   │   ├── retroBoard.js            # Component logic
│   │   ├── retroBoard.css           # Styling
│   │   └── retroBoard.js-meta.xml   # Component metadata
│   ├── retroItem/
│   │   ├── retroItem.html           # Individual item component
│   │   ├── retroItem.js
│   │   ├── retroItem.css
│   │   └── retroItem.js-meta.xml
│   └── retroColumn/
│       ├── retroColumn.html         # Column component
│       ├── retroColumn.js
│       ├── retroColumn.css
│       └── retroColumn.js-meta.xml
├── classes/                         # Apex classes (if using backend)
├── objects/                         # Custom objects (if using persistence)
└── permissionsets/                  # Permission sets
```

## 🔧 Development

### Running Tests
```bash
# Run LWC tests
npm run test:unit

# Run Apex tests
sfdx force:apex:test:run
```

### Local Development
```bash
# Start local development server (if using LWC Local Development)
sfdx force:lightning:lwc:start
```

### Code Quality
```bash
# Run ESLint
npm run lint

# Format code
npm run prettier
```

## 🏗️ Technical Implementation

### Component Architecture
- **retroBoard**: Main container component
- **retroColumn**: Individual column (What Went Well, To Improve, etc.)
- **retroItem**: Individual feedback item with edit capabilities

### Data Flow
1. Parent component manages overall state
2. Child components communicate via custom events
3. Optional: Apex backend for data persistence

### Key Technologies
- Lightning Web Components (LWC)
- Lightning Design System (SLDS)
- JavaScript ES6+
- CSS3 with Flexbox/Grid
- Apex (optional, for backend)

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Style Guidelines
- Follow Salesforce LWC best practices
- Use ESLint and Prettier for code formatting
- Write meaningful commit messages
- Add tests for new features

## 📚 Learning Resources

- [Lightning Web Components Developer Guide](https://developer.salesforce.com/docs/component-library/documentation/en/lwc)
- [Trailhead: Lightning Web Components](https://trailhead.salesforce.com/content/learn/trails/build-lightning-web-components)
- [Salesforce DX Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.sfdx_dev.meta/sfdx_dev/)

## 🐛 Troubleshooting

### Common Issues

**Issue:** Component not visible after deployment
- **Solution:** Check component metadata and page assignments

**Issue:** Drag and drop not working
- **Solution:** Verify event handlers and CSS touch-action properties

**Issue:** Data not persisting
- **Solution:** Confirm Apex methods are properly connected

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 About the Developer

**Thumma Sai Krishna**
- GitHub: [@thummasaikrishna](https://github.com/thummasaikrishna)
- LinkedIn: [Sai Krishna Thumma](https://www.linkedin.com/in/sai-krishna-thumma-61a936300)
- Passionate Salesforce Developer focused on Lightning Web Components and modern UI development

## 🙏 Acknowledgments

- Inspired by popular retrospective tools like Retrium and FunRetro
- Built following Salesforce Lightning Design System guidelines
- Thanks to the Salesforce Developer Community for best practices

## 📞 Support

- Create an [Issue](https://github.com/thummasaikrishna/retro-board-lwc/issues) for bug reports
- Start a [Discussion](https://github.com/thummasaikrishna/retro-board-lwc/discussions) for questions
- Follow [@thummasaikrishna](https://twitter.com/thummasaikrishna) for updates

---

**⭐ If this project helped you, please give it a star!**

Made by [Thumma Sai Krishna](https://github.com/thummasaikrishna)
