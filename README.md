# Karølín Issues Tracker

A simple, accessible web application for tracking and managing community issues in the Karlín district of Prague.

## 🌟 Features

- **Interactive Map** - View issues pinned to specific locations in Karlín
- **Issue List** - Browse all reported issues with detailed descriptions  
- **Detailed Pages** - Complete information for each issue with markdown content
- **Czech Language** - Complete localization for Czech users
- **Accessible Design** - WCAG 2.1 AA compliant with warm, readable colors
- **Mobile Responsive** - Works seamlessly on all devices
- **No Installation** - Runs directly in any modern browser

## 🚀 Quick Start

### Option 1: Download & Run Locally
1. Download all files: [`index.html`](https://github.com/sigy/Karolin/raw/main/index.html), [`list.html`](https://github.com/sigy/Karolin/raw/main/list.html), [`detail.html`](https://github.com/sigy/Karolin/raw/main/detail.html)
2. Keep all files in the same folder
3. Double-click `index.html` to open in your browser
4. Data loads automatically from Airtable - no setup required!

### Option 2: View Online
Visit the live demo: **[sigy.github.io/Karolin](https://sigy.github.io/Karolin)**

## 📍 Sample Issues

The application includes 8 sample issues across Karlín:
- 🚨 Křižíkova: rozbité osvětlení
- 🚶 Sokolovská: poškozený chodník  
- 🔊 Staveniště: hluk
- 🎨 Budova Invalidovny: graffiti
- 🗑️ Karlínské náměstí: přeplněné odpadky
- 🚴 Rohanské nábřeží: zablokován cyklopruh
- 🕳️ Pernerova ulice: výboje
- 🪑 Karlínský park: rozbitá lavička

## 🛠️ Technology

- **Frontend**: Pure HTML, CSS, JavaScript (ES6+)
- **Data Storage**: Airtable via REST API
- **Mapping**: Leaflet.js with OpenStreetMap
- **Typography**: Kanit font family
- **Architecture**: Multi-page application with shared navigation
- **No Dependencies**: Runs without build tools or server

## 🎨 Design

- **Warm Color Palette**: Accessible blues and creams
- **Modern Typography**: Kanit font with proper hierarchy
- **Clean Interface**: Minimal, focused on content
- **Responsive Layout**: Desktop and mobile optimized

## 📱 Browser Support

- ✅ Chrome/Chromium (recommended)
- ✅ Firefox
- ✅ Safari  
- ✅ Edge
- ✅ Mobile browsers

## 🏗️ Architecture

This is a **multi-page application** with three main pages:
- **index.html** - Interactive map with issue markers
- **list.html** - Complete list of issues with cards
- **detail.html** - Detailed view of individual issues
- **Airtable** - Real-time data storage and management

Features:
- No build process required
- No server dependencies
- Real-time data from Airtable
- Universal browser compatibility

## 📊 Data Management

Powered by **Airtable** for easy content management:
- **Real-time updates** - Changes in Airtable appear immediately
- **Easy editing** - Non-technical users can update issues
- **Rich content** - Support for detailed markdown descriptions
- **GPS coordinates** - Precise location data for mapping
- **Collaborative** - Multiple people can edit and manage content

## 🌍 Localization

The application is fully localized in Czech:
- All interface text in Czech
- Czech date formats (DD.M.YYYY)
- Natural issue naming conventions
- Proper Czech typography

## ♿ Accessibility

- **WCAG 2.1 AA Compliant** - All color combinations tested
- **Keyboard Navigation** - Full keyboard support
- **Screen Reader Support** - Semantic HTML structure
- **High Contrast** - Excellent readability
- **Focus Indicators** - Clear visual focus states

## 📄 Documentation

For detailed technical documentation, see [`CLAUDE.md`](./CLAUDE.md).

## 🤝 Contributing

This project welcomes contributions! Whether you want to:
- Report bugs or suggest features
- Improve accessibility or design
- Add new functionality
- Enhance documentation

Feel free to open an issue or submit a pull request.

## 📝 License

Open source project - feel free to use, modify, and distribute.

---

**Built for the Karlín community** 🏘️ **Made with ❤️ in Prague**