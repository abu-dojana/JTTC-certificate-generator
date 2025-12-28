Smart Certificate Generator (JTTC & BEF)

A standalone, client-side web application designed to generate, track, and print professional training certificates for Janata Technical Training Institute (JTTC) and Bangladesh Electrician Federation (BEF).

🚀 Features

Smart Serial Numbers: Automatically increments the Serial Number (SL No: 001, 002, etc.) every time a certificate is printed.

Print Logging System: Tracks every printed certificate in the browser's memory. You can download the full history as a .txt log file.

Dynamic QR Code: Generates a scannable QR code linking to online verification (e.g., a Google Doc or Website).

Auto-Fill Logic: Automatically fills the "Duration" field based on the selected Course Topic to prevent errors.

Print-Perfect Layout: Custom CSS ensures the certificate prints perfectly on A4 Landscape paper, hiding all buttons and control panels automatically.

Single-File Architecture: The entire app runs from a single .html file. No database or server installation required.

🛠️ How to Use

Open the App: Double-click the Smart_Certificate_App.html file to open it in any modern web browser (Google Chrome, Edge, Firefox).

Fill Details: Enter the Student Name, Guardian's Name, NID, and Address.

Select Course: Choose the training topic from the dropdown menu. The duration will fill automatically.

Print: Click the green "🖨️ Print Certificate" button.

Note: The Serial Number will increment automatically before the print dialog opens.

Manage Logs:

Click "📜 Download Log" to save a record of all printed certificates.

Click "⚠️ Reset Log" if you need to clear the history and start the Serial Number back at 001.

⚙️ Configuration & Customization

Since this is a single-file app, all configuration is done by editing the code directly.

1. Changing Logos

To update the logos, convert your images to Base64 strings (using a tool like base64-image.de) and paste them into the <img> tags in the HTML:

<!-- Search for this line in the code -->
<img src="YOUR_BASE64_STRING_HERE" class="logo-static" alt="JTTC Logo">


2. Changing the QR Code Link

To change where the QR code points (e.g., to a new Google Doc or website), edit the qrContent variable in the script section:

// Line ~350 in the code
const qrContent = "[https://docs.google.com/document/d/your-new-link-here](https://docs.google.com/document/d/your-new-link-here)";


3. Adding/Editing Courses

To add new courses or change durations, edit the topicDatabase object:
```
const topicDatabase = {
    "New Course Name Here": { 
        duration: "400 Hours" 
    },
    // ... existing courses
};
```

⚠️ Important Note on Data Storage

This application uses Local Storage (browser memory) to save the Serial Number and Logs.

Data is Local: If you open the file on a different computer, the Serial Number will start from 001 again.

Clearing Cache: If you clear your browser's "Cookies and Site Data", the logs and serial counter will be wiped. Always download your log file regularly.

📄 License

This project is for internal use by JTTC & BEF.
