# JTTC Certificate Generator

A professional, standalone certificate generation and printing application for the **Janata Technical Training Institute (JTTC)** and **Bangladesh Electrician Federation (BEF)**.

## Overview

This is a single-file HTML application that allows institutions to create, manage, and print professional training certificates with built-in verification through QR codes. No backend server or installation required—just open the HTML file in your browser.

## Features

✨ **Core Functionality**
- 📄 Professional A4 landscape certificate template
- 🎓 Dynamic student information capture (name, guardian, NID, address)
- 📚 Multi-row training details tracking (date, topic, outcome, duration)
- 🖨️ Optimized print layout with hidden controls
- ➕ Add/remove training rows on the fly
- 🔢 Auto-incrementing serial numbering system

🔐 **Data Management**
- 💾 Browser-based persistent storage (localStorage)
- 📊 Print history log with timestamp tracking
- 📥 Download log as text file (.txt)
- 🔄 Reset functionality for serial numbers
- 🛡️ No data leaves your device (100% private)

🎯 **Smart Features**
- 🔗 QR code generation for certificate verification
- 🎯 Auto-fill duration based on course selection
- 📋 Datalist suggestions for consistent data entry
- ⌨️ Ctrl+P keyboard shortcut support
- 📱 Responsive design elements
- 🌐 Professional branding with logo support

## Quick Start

### 1. **Open the File**
Simply open `JTTC Certificate Generator_v1.0.html` in any modern web browser:
- Windows: Double-click the file
- Mac/Linux: Right-click → Open with → Browser of choice

### 2. **Fill in Certificate Details**

#### Student Information Section:
- **Student Name**: Full name of trainee
- **Guardian's Name**: Parent/guardian information
- **NID**: National Identification Number
- **Address**: Residential address

#### Training Details Table:
- **Date**: Course completion date (date picker)
- **Topic**: Course name (dropdown with suggestions)
- **Outcome**: Competency level achieved (Level 1 or Level 2)
- **Duration**: Total training hours (e.g., "360 Hours")

### 3. **Print Certificate**
- Click **"🖨️ Print Certificate"** button
- Certificate serial number auto-increments
- Print dialog opens
- Print to paper or PDF

### 4. **Manage Records**
- **📜 Download Log (.txt)**: Export all printed certificates as text file
- **⚠️ Reset Log**: Clear history and reset serial numbers to 001

## Technical Details

### Technology Stack
- **HTML5** - Semantic markup
- **CSS3** - Modern styling and print optimization
- **Vanilla JavaScript** - No dependencies required
- **QRCode.js** - QR code generation library (CDN)
- **localStorage API** - Client-side data persistence

### Browser Compatibility
| Browser | Support |
|---------|---------|
| Chrome/Edge | ✅ Full |
| Firefox | ✅ Full |
| Safari | ✅ Full |
| Opera | ✅ Full |
| IE 11 | ⚠️ Limited |

### File Structure
```
JTTC Certificate Generator_v1.0.html
├── HTML Structure
│   ├── Control Panel (buttons)
│   ├── Certificate Template (A4 landscape)
│   ├── Header (org names, title, registration)
│   ├── Student Form
│   ├── Training Table
│   └── Signatures Section + QR Code
├── CSS Styling
│   ├── Root variables (colors, fonts)
│   ├── Layout and responsive design
│   ├── Print media queries
│   └── Component styles
└── JavaScript Logic
    ├── Data management (localStorage)
    ├── Form handling
    ├── QR code generation
    ├── Serial numbering
    └── Print/export functions
```

### Key JavaScript Functions

| Function | Purpose |
|----------|---------|
| `handlePrint()` | Captures data, increments serial, saves log, triggers print |
| `saveLog(entry, count)` | Stores certificate record in localStorage |
| `downloadLog()` | Exports all records as text file |
| `clearLog()` | Resets storage and serial number |
| `generateQR()` | Creates QR code from verification link |
| `addRow()` | Adds new training detail row |
| `deleteRow()` | Removes training row |
| `autoFillDetails()` | Auto-populates duration based on course |

## Customization

### Change Logo/Images
1. Open the HTML file in a text editor
2. Locate the `<img>` tags with `class="logo-static"`
3. Replace the `src` attribute with your Base64 encoded image or URL

### Modify Course Topics
Find this section in the JavaScript:
```javascript
const topicDatabase = {
  "Electrical Installation and Maintenance": {
    duration: "360 Hours",
  },
  // Add more courses here
};
```

### Adjust Colors
Edit CSS variables at the top of the `<style>` section:
```css
:root {
  --primary-green: #006a4e;  /* Change this */
  --accent-red: #f42a41;     /* And this */
  --cursive-font: "Cinzel", serif;
  --body-font: "Lato", sans-serif;
}
```

### Change QR Link
Update this in the JavaScript:
```javascript
const qrContent = `https://your-verification-url.com`;
```

## Data Storage

### What Gets Saved?
Your local browser's `localStorage` stores:

1. **Counter**: Serial number sequence
2. **Logs**: Certificate print history with:
   - Serial number
   - Print timestamp
   - Student details
   - Training information

### Storage Limits
- Typically **5-10 MB** per domain
- Data persists until manually cleared
- Data is **not synced** across devices

### Export Data
- Click "📜 Download Log (.txt)" to backup all records
- Save the file to your computer
- Can be imported into Excel/Google Sheets

## Privacy & Security

🔒 **Your Data is Safe**
- ✅ No internet connection required for core functionality
- ✅ No data sent to external servers
- ✅ All data stored locally on your device
- ✅ QR code links to external verification URL only on print
- ✅ Clear all data anytime with "Reset Log"

## Troubleshooting

### Certificates not printing in color?
- Check "Background graphics" option in print settings
- Ensure `-webkit-print-color-adjust: exact` is enabled

### Serial numbers resetting?
- Clearing browser cache/history may clear localStorage
- Use "Download Log" to backup before clearing data

### QR code not showing?
- Check internet connection (QR library loaded from CDN)
- Verify QRCode.js CDN is accessible

### Datalist suggestions not appearing?
- Try typing the first few letters
- Ensure JavaScript is enabled
- Use an updated browser version

## Version History

### v1.0 (Current)
- ✅ Basic certificate generation
- ✅ Serial numbering with persistence
- ✅ QR code generation
- ✅ Print logging and download
- ✅ Dynamic row management
- ✅ localStorage data storage
- ✅ Professional styling

## Future Enhancements (Potential)

- 🌍 Multi-language support (Bengali, English, etc.)
- 📱 Mobile app version
- ☁️ Cloud backup/sync
- 📊 Advanced reporting dashboard
- 🎨 Template customization UI
- 📧 Email/SMS integration
- 👥 Multi-user authentication
- 📈 Analytics and statistics

## Requirements

- Modern web browser (Chrome, Firefox, Safari, Edge)
- JavaScript enabled
- ~1 MB disk space for HTML file
- Internet connection (for QR code library only)

## License

This project is created for the Janata Technical Training Institute (JTTC) and Bangladesh Electrician Federation (BEF).

**Government Registration**: B-2202

## Support & Feedback

For issues, feature requests, or improvements:
1. Check the troubleshooting section above
2. Verify browser compatibility
3. Clear cache and try again
4. Contact the development team

## Credits

**Created by:** Abu Dojana Tahmid

**Developed for:**
- Janata Technical Training Institute (JTTC)
- Bangladesh Electrician Federation (BEF)

**Libraries Used:**
- [QRCode.js](https://davidshimjs.github.io/qrcodejs/) - QR Code generation
- [Google Fonts](https://fonts.google.com/) - Cinzel & Lato fonts

---

**Last Updated**: December 2025  
**Status**: Production Ready ✅
