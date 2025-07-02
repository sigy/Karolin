# Karølín Issues Tracker

## Project Overview
A simple, universal web application for tracking and managing issues in the Karlín district of Prague. The application provides an interactive map view and detailed list view for district issues using an accessible, warm design system with Czech language throughout.

## Tech Stack
- **Frontend**: Pure HTML, CSS, and JavaScript (ES6+)
- **Styling**: Custom CSS with accessible warm color palette
- **Typography**: Kanit font family with proper weight hierarchy
- **Icons**: Material Icons from Google Fonts
- **Mapping**: Leaflet.js with OpenStreetMap tiles
- **Data Storage**: Airtable via REST API
- **Language**: Czech language throughout the application

## Architecture
- **Multi-page application**: Three separate HTML pages with shared design
- **Airtable integration**: Real-time data from Airtable base
- **No build process**: Runs directly in any modern browser
- **No server required**: Direct API calls to Airtable
- **CDN dependencies**: All external libraries loaded via CDN
- **Universal compatibility**: Works on desktop and mobile browsers

## Project Structure
```
karolin/
├── index.html             # Interactive map page
├── list.html              # Issues list page
├── detail.html            # Issue detail page
├── CLAUDE.md              # This specification file
├── README.md              # GitHub documentation
└── .gitignore             # Git ignore file
```

## Data Model
Issues are stored in Airtable with the following field mapping:

### Airtable Fields → Application Fields
```javascript
{
  id: record.fields.id,                    // Issue ID number
  name: Location + ": " + Issue name,      // Combined location and issue
  description: record.fields.brief,        // Short description
  markup: record.fields.description,       // Detailed markdown content (cleaned)
  lat: record.fields.latitude,            // GPS latitude (null if no GPS)
  lng: record.fields.longitude,           // GPS longitude (null if no GPS)
  created: record.fields.created,         // Date in YYYY-MM-DD format
  updated: record.fields['last-update']   // Date in YYYY-MM-DD format
}
```

## Features

### 1. Accessible Design System
- **Warm color palette**: WCAG AA compliant with excellent contrast ratios
- **Typography**: Kanit font family with weights 300-700
- **Component styling**: Clean, minimal borders and consistent spacing
- **Responsive design**: Adapts to mobile and desktop screens
- **Accessibility**: WCAG 2.1 AA compliance throughout

### 2. Interactive Map Page (index.html)
- **Leaflet.js integration**: Lightweight, accessible mapping library
- **Light theme tiles**: Clean, readable map background
- **District boundaries**: Map bounds restricted to Karlín area with gutter
- **Issue markers**: 7 POI markers for geolocated issues
- **Simple popups**: Clean popups with links to detail pages
- **Zoom controls**: Limited to levels 14-18 for optimal district viewing

### 3. Issues List Page (list.html)
- **Clean cards**: Each issue displayed in elevated card with left accent
- **GPS badges**: Solid badges for geolocated issues only
- **Czech content**: Issue titles, descriptions, and dates in Czech
- **Responsive layout**: Cards adapt to screen width
- **Clickable cards**: Each card links to detailed issue page

### 4. Issue Detail Page (detail.html)
- **URL parameters**: Loads specific issue using ?id=X parameter
- **Complete information**: Shows all issue data plus detailed markup
- **Markdown parsing**: Renders markup field with headers and formatting
- **Minimal navigation**: Back button using browser history
- **Error handling**: Appropriate messages for missing issues

### 5. Sample Issues (8 total - Czech)
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
1. Download/save all files (`index.html`, `list.html`, `detail.html`) to your computer
2. Double-click `index.html` to open in your default browser
3. Navigate between pages using the interface
4. Data loads automatically from Airtable

### Method 2: File URL
1. Navigate to the file location in your browser:
   `file:///path/to/karolin/index.html`

### Method 3: Local Server (if CORS issues)
```bash
python3 -m http.server 8000
# Then visit http://localhost:8000
```

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

## Dependencies
- **Leaflet.js 1.7.1**: Mapping library (CDN)
- **Kanit Font**: Typography from Google Fonts (CDN)
- **Material Icons**: Icon library from Google Fonts (CDN)
- **OpenStreetMap**: Tile provider (no API key required)
- **Airtable API**: Data storage and retrieval

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
- **Lightweight**: Total application under 45KB (HTML only)
- **Fast Loading**: CDN resources cached by browsers
- **Efficient Rendering**: No framework overhead
- **Real-time Data**: Direct Airtable API integration
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
- **Multi-page structure**: Three HTML pages with shared navigation
- **Airtable integration**: Direct API calls for real-time data
- **API credentials**: Embedded in HTML (read-only access)

## Airtable Configuration

### Base Setup
- **Base ID**: `appakA8qOKhNzBh8a`
- **Table Name**: `Issues`
- **API Key**: Read-only access token (embedded in application)

### Required Airtable Fields
- `id` (Number): Unique issue identifier
- `Issue name` (Text): Short issue name
- `brief` (Text): Brief description
- `description` (Long Text): Detailed markdown content
- `latitude` (Number): GPS latitude coordinate
- `longitude` (Number): GPS longitude coordinate
- `created` (Date): Creation date
- `last-update` (Date): Last modification date
- `Location` (Text): Location/area name

### Data Processing
- **Markdown cleanup**: Automatically removes escaped characters (`\*` → `*`)
- **Field mapping**: Combines location and issue name for titles
- **Error handling**: Graceful fallbacks for missing data

## Future Enhancement Possibilities
- **Issue Creation**: Web form interface for adding new issues to Airtable
- **Filtering/Search**: Client-side filtering by category or location
- **Offline Support**: Service worker with cached data
- **Print Styles**: Optimized CSS for printing issue reports
- **Advanced Markdown**: Full markdown rendering for markup field
- **Image Support**: Airtable attachments for issue photos
- **API Proxy**: Serverless function to hide API credentials
- **Real-time Updates**: WebSocket or polling for live data sync