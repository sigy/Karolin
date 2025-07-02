# Karlín Issues Tracker

## Project Overview
A simple, universal web application for tracking and managing issues in the Karlín district of Prague. The application provides an interactive map view and detailed list view for district issues using a clean, Material 3-inspired design system.

## Tech Stack
- **Frontend**: Pure HTML, CSS, and JavaScript (ES6+)
- **Styling**: Custom CSS with Material 3 design principles
- **Typography**: Google Fonts (Roboto family)
- **Icons**: Material Icons from Google Fonts
- **Mapping**: Leaflet.js with OpenStreetMap tiles
- **Data Storage**: Static JavaScript objects (no database required)

## Localization
- Use Czech language as main language for the whole site, map and all labels

## Architecture
- **Single-file application**: All code contained in `simple.html`
- **No build process**: Runs directly in any modern browser
- **No server required**: Works from local file system
- **CDN dependencies**: All external libraries loaded via CDN
- **Universal compatibility**: Works on desktop and mobile browsers

## Project Structure
```
karolin/
├── simple.html            # Complete standalone application
├── CLAUDE.md              # This specification file
└── [other files]          # Development artifacts (optional)
```

## Data Model
Issues are stored as JavaScript objects with the following structure:
```javascript
{
  id: string,
  name: string,
  description: string,
  lat: number,        // GPS latitude
  lng: number         // GPS longitude
}
```

## Features

### 1. Consistent UI Design
- **Material 3 color palette**: Primary color #6750a4 (purple)
- **Typography**: Roboto font family with proper weights
- **Component styling**: Rounded corners (12px), consistent shadows
- **Responsive design**: Adapts to mobile and desktop screens
- **Accessibility**: Proper contrast ratios and keyboard navigation

### 2. Interactive Map Tab
- **Leaflet.js integration**: Lightweight, accessible mapping library
- **OpenStreetMap tiles**: Standard street view theme
- **District boundaries**: Map bounds restricted to Karlín area
- **Issue markers**: 7 POI markers for geolocated issues
- **Interactive popups**: Click markers to view issue details
- **Zoom controls**: Standard Leaflet zoom and pan controls

### 3. Comprehensive List Tab
- **Material cards**: Each issue displayed in elevated card
- **Location badges**: Visual indicators for geolocated issues
- **Rich content**: Issue titles, descriptions, and metadata
- **Responsive layout**: Cards adapt to screen width
- **Hover effects**: Subtle animations for better UX

### 4. Sample Issues (8 total)
1. **Broken streetlight on Křižíkova** - Safety concern with GPS location
2. **Damaged sidewalk on Sokolovská** - Accessibility issue with GPS location
3. **Noise from construction site** - Regulatory violation (no GPS)
4. **Graffiti on Invalidovna building** - Historic preservation with GPS location
5. **Overflowing trash bins near Karlín Square** - Sanitation with GPS location
6. **Blocked bike lane on Rohanské nábřeží** - Traffic safety with GPS location
7. **Potholes on Pernerova street** - Road maintenance with GPS location
8. **Broken bench in Karlín Park** - Park maintenance with GPS location

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
- Zoom levels: 13 (min) to 18 (max), default 15

## Installation & Usage

### Method 1: Direct File Access (Recommended)
1. Download/save `simple.html` to your computer
2. Double-click the file to open in your default browser
3. Or drag and drop the file into any browser window

### Method 2: File URL
1. Navigate to the file location in your browser:
   `file:///path/to/karolin/simple.html`

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
- **Google Fonts**: Roboto typography and Material Icons
- **OpenStreetMap**: Tile provider (no API key required)

## Design System Specifications

### Colors
- **Primary**: #6750a4 (Material 3 purple)
- **Background**: #fffbfe (Material 3 surface)
- **Text Primary**: #1c1b1f
- **Text Secondary**: #49454f
- **Text Tertiary**: #79747e
- **Border**: #e7e0ec

### Typography Scale
- **Header**: 20px, weight 500
- **Issue Title**: 20px (desktop), 18px (mobile), weight 500
- **Tab Labels**: 14px (desktop), 13px (mobile), weight 500
- **Body Text**: 16px, weight 400, line-height 1.6
- **Metadata**: 12px, weight 400

### Spacing & Layout
- **Card Padding**: 24px (desktop), 16px (mobile)
- **Container Padding**: 24px (desktop), 16px (mobile)
- **Card Gaps**: 16px between cards
- **Border Radius**: 12px for cards and buttons
- **Max Content Width**: 1200px

### Interactive States
- **Hover Effects**: Translate Y(-2px) with enhanced shadow
- **Active Tab**: Purple color with bottom border
- **Button Hover**: Subtle background color overlay
- **Card Hover**: Enhanced elevation and transform

## Performance Features
- **Lightweight**: Single HTML file under 15KB
- **Fast Loading**: CDN resources cached by browsers
- **Efficient Rendering**: No framework overhead
- **Mobile Optimized**: Responsive breakpoints and touch-friendly UI

## Accessibility Features
- **Semantic HTML**: Proper heading hierarchy and ARIA labels
- **Keyboard Navigation**: Full keyboard support for all interactions
- **Color Contrast**: WCAG AA compliant contrast ratios
- **Focus Indicators**: Visible focus states for keyboard users
- **Screen Reader Support**: Descriptive alt text and labels

## Future Enhancement Possibilities
- **Data Persistence**: Local storage for user-added issues
- **Issue Creation**: Form interface for adding new issues
- **Filtering/Search**: Client-side filtering by category or location
- **Offline Support**: Service worker for full offline functionality
- **Print Styles**: Optimized CSS for printing issue reports