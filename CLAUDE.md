# Karølín Issues Tracker

## Project Overview
A simple, universal web application for tracking and managing issues in the Karlín district of Prague. The application provides an interactive map view and detailed list view for district issues using an accessible, warm design system with Czech language throughout.

## Tech Stack
- **Frontend**: Pure HTML, CSS, and JavaScript (ES6+)
- **Styling**: Custom CSS with accessible warm color palette
- **Typography**: Kanit font family with proper weight hierarchy
- **Icons**: Material Icons from Google Fonts
- **Mapping**: Leaflet.js with OpenStreetMap tiles
- **Data Storage**: Static JavaScript objects (no database required)
- **Language**: Czech language throughout the application

## Architecture
- **Single-file application**: All code contained in `index.html`
- **No build process**: Runs directly in any modern browser
- **No server required**: Works from local file system
- **CDN dependencies**: All external libraries loaded via CDN
- **Universal compatibility**: Works on desktop and mobile browsers

## Project Structure
```
karolin/
├── index.html             # Complete standalone application
├── CLAUDE.md              # This specification file
└── .gitignore             # Git ignore file
```

## Data Model
Issues are stored as JavaScript objects with the following structure:
```javascript
{
  id: string,
  name: string,           // Format: "Location: issue name" (not capitalized)
  description: string,
  lat: number,           // GPS latitude
  lng: number            // GPS longitude
}
```

## Features

### 1. Accessible Design System
- **Warm color palette**: WCAG AA compliant with excellent contrast ratios
- **Typography**: Kanit font family with weights 300-700
- **Component styling**: Clean, minimal borders and consistent spacing
- **Responsive design**: Adapts to mobile and desktop screens
- **Accessibility**: WCAG 2.1 AA compliance throughout

### 2. Interactive Map Tab
- **Leaflet.js integration**: Lightweight, accessible mapping library
- **Light theme tiles**: Clean, readable map background
- **District boundaries**: Map bounds restricted to Karlín area with gutter
- **Issue markers**: 7 POI markers for geolocated issues
- **Simple popups**: Clean popups without borders, matching design system
- **Zoom controls**: Limited to levels 14-18 for optimal district viewing

### 3. Comprehensive List Tab
- **Clean cards**: Each issue displayed in elevated card with left accent
- **GPS badges**: Solid badges for geolocated issues only
- **Czech content**: Issue titles, descriptions, and dates in Czech
- **Responsive layout**: Cards adapt to screen width
- **Hover effects**: Subtle animations with accessible focus states

### 4. Sample Issues (8 total - Czech)
1. **Křižíkova: rozbité osvětlení** - Safety concern with GPS location
2. **Sokolovská: poškozený chodník** - Accessibility issue with GPS location
3. **Staveniště: hluk** - Regulatory violation (no GPS)
4. **Budova Invalidovny: graffiti** - Historic preservation with GPS location
5. **Karlínské náměstí: přeplněné odpadky** - Sanitation with GPS location
6. **Rohanské nábřeží: zablokován cyklopruh** - Traffic safety with GPS location
7. **Pernerova ulice: výboje** - Road maintenance with GPS location
8. **Karlínský park: rozbitá lavička** - Park maintenance with GPS location

## Karlín District Boundaries
The map is geographically bounded by these GPS coordinates with added gutter:
- **North**: 50.1032842N, 14.4652511E
- **East**: 50.0990650N, 14.4752922E
- **South**: 50.0882928N, 14.4425064E
- **West**: 50.0913503N, 14.4363522E

**Map bounds coordinates (with gutter):**
- Southwest: [50.0872928, 14.4353522]
- Northeast: [50.1042842, 14.4762922]
- Center point: [50.0957885, 14.4558222]
- Zoom levels: 14 (min) to 18 (max), default 15

## Installation & Usage

### Method 1: Direct File Access (Recommended)
1. Download/save `index.html` to your computer
2. Double-click the file to open in your default browser
3. Or drag and drop the file into any browser window

### Method 2: File URL
1. Navigate to the file location in your browser:
   `file:///path/to/karolin/index.html`

### Method 3: GitHub Pages
- Live demo available at: https://sigy.github.io/Karolin

### No Installation Required
- **No Node.js, npm, or build tools needed**
- **No local server required**
- **No database setup**
- **Works offline** (after initial CDN library download)

## Browser Compatibility
- **Chrome/Chromium**: Full support (recommended)
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile browsers**: Responsive design works on all modern mobile browsers

## Dependencies (CDN)
- **Leaflet.js 1.7.1**: Mapping library
- **Kanit Font**: Typography from Google Fonts
- **Material Icons**: Icon library from Google Fonts
- **OpenStreetMap**: Tile provider (no API key required)

## Design System Specifications

### Colors (Accessible Warm Palette)
- **Primary Dark**: #1B3C53 (Headers, main text)
- **Primary Medium**: #456882 (Accents, descriptions, borders)
- **Secondary**: #6B5B73 (Meta text)
- **Accent Dark**: #2C4A5C (Descriptions in popups)
- **Background**: #F9F3EF (Main background, cards)
- **All combinations meet WCAG AA standards**

### Typography (Kanit Font Family)
- **Main Header**: 28px, weight 600, letter-spacing 0.5px
- **Issue Titles**: 18px, weight 600, letter-spacing 0.3px
- **Tab Labels**: 14px, weight 500, uppercase, letter-spacing 0.8px
- **Body Text**: 14px, weight 400, line-height 1.5
- **GPS Badges**: 11px, weight 500, uppercase
- **Meta Text**: 12px, weight 300-400, letter-spacing 0.3px

### Spacing & Layout
- **Header Padding**: 18px/24px (desktop), 14px/18px (mobile)
- **Card Padding**: 22px (desktop), 18px (mobile)
- **Container Padding**: 24px (desktop), 18px (mobile)
- **Card Gaps**: 18px between cards
- **Border Radius**: 4px for cards and controls
- **Max Content Width**: 1200px

### Interactive States
- **Hover Effects**: Enhanced shadow and translateX(4px)
- **Active Tab**: Solid background with contrasting text
- **Button Hover**: Background color changes
- **Card Hover**: Smooth transforms with accessible focus

## Accessibility Features
- **WCAG 2.1 AA Compliance**: All color combinations tested
- **Semantic HTML**: Proper heading hierarchy and structure
- **Keyboard Navigation**: Full keyboard support for all interactions
- **High Contrast**: Excellent contrast ratios throughout
- **Focus Indicators**: Clear, visible focus states
- **Screen Reader Support**: Descriptive labels and content structure
- **Font Weights**: Increased weights for better readability

## Performance Features
- **Lightweight**: Single HTML file under 20KB
- **Fast Loading**: CDN resources cached by browsers
- **Efficient Rendering**: No framework overhead
- **Mobile Optimized**: Responsive breakpoints and touch-friendly UI
- **Accessible Design**: No performance impact from accessibility features

## Czech Language Implementation
- **Complete localization**: All text in Czech language
- **Proper formatting**: Czech date formats (DD.M.YYYY)
- **Natural naming**: "Location: issue name" format
- **Metadata labels**: "vytvořeno", "poslední aktualizace"
- **UI elements**: "MAPA", "SEZNAM" navigation
- **No capitalization**: Natural Czech text styling

## Development Notes
- **Git repository**: https://github.com/sigy/Karolin
- **Main branch**: `main`
- **Authentication**: SSH configured for sigy@sigy.cz
- **Clean codebase**: Removed all React/Vite artifacts
- **Single file**: Complete application in index.html

## Future Enhancement Possibilities
- **Data Persistence**: Local storage for user-added issues
- **Issue Creation**: Form interface for adding new issues
- **Filtering/Search**: Client-side filtering by category or location
- **Offline Support**: Service worker for full offline functionality
- **Print Styles**: Optimized CSS for printing issue reports
- **GitHub Pages**: Automatic deployment from main branch