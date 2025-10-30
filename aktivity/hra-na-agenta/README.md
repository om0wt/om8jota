# Hra na agenta - Single HTML Version

This is a simplified, single-file version of the "Hra na agenta" application that can be hosted on GitHub Wiki or any static web hosting.

## What's included

- **index.html** - Complete standalone application with all functionality:
  - Game instructions
  - Station protocol generator with cipher wheels
  - Control station protocol generator
  - Alberti cipher encryption
  - Print functionality
  - All styling and JavaScript inline

## Features

✅ No build process required
✅ No dependencies
✅ Works offline
✅ Can be hosted on GitHub Wiki
✅ Print-optimized protocols
✅ Fully responsive design
✅ Generates station protocols with cipher wheels
✅ Generates inner cipher wheels for cutting and assembly
✅ Alberti cipher encryption with customizable keys
✅ Control station protocol generator with automatic word generation

## How to use

### Option 1: Open locally
Simply double-click `index.html` to open it in your web browser.

### Option 2: Host on GitHub Wiki

1. Go to your GitHub repository's Wiki
2. Create a new page
3. Click "Edit" and switch to the "HTML" editor mode
4. Copy and paste the entire contents of `index.html`
5. Save the page

### Option 3: Host on GitHub Pages

1. Copy `index.html` to your repository
2. Enable GitHub Pages in repository settings
3. Set the source to the branch containing the file
4. Access via `https://yourusername.github.io/repository-name/v2/index.html`

### Option 4: Any web server

Upload `index.html` to any web hosting service. The file is completely self-contained.

## Usage

1. **Inštrukcie** tab - Read the game instructions

2. **Protokol stanice** tab - Generate station protocols for printing
   - **Protokol Stanice** subtab:
     - Set the number of copies
     - Click "Tlačiť protokol" to print
   - **Vnútorné Kotúče** subtab:
     - Set wheel size (affects how many fit per page)
     - Set number of inner wheels to generate
     - Click "Tlačiť kotúče" to print
     - Cut out the wheels and place them in the station protocols

3. **Protokol riadiacej stanice** tab - Generate control station protocol
   - Set number of stations
   - Enter encryption key (2 letters, e.g., "xA")
   - Enter result phrase (words separated by spaces)
   - Optionally enter control words for row 2
   - Click "Generovať protokol" to generate
   - Click "Tlačiť" to print

## Technical details

- Pure HTML5, CSS3, and vanilla JavaScript
- No external dependencies
- File size: ~41KB (1112 lines)
- Compatible with all modern browsers
- Print-optimized with separate portrait/landscape modes
- SVG-based cipher wheel generation
- Dynamic page layout calculation for optimal printing

## Differences from original React version

- Single file instead of modular components
- No build step required
- All core functionality maintained including inner cipher wheels
- Simplified styling (no Tailwind CSS or shadcn/ui, but with similar visual design)
- Vanilla JavaScript instead of React hooks and state management

## Converting back to the original

To use the full React version with hot reload and component-based architecture, use the original source files in the parent directory and run:

```bash
npm install
npm run dev
```
