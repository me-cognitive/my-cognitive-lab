### Github Repository Location
https://github.com/me-cognitive/mathpix-pdf-converter.git

# Mathpix PDF to DOCX Converter

A Windows desktop application that converts PDF files to DOCX format using the Mathpix API. Features a clean, user-friendly interface with real-time conversion status and usage tracking.

## 🚀 Features

- **Simple PDF Conversion**: Convert any PDF file to DOCX format with just a few clicks
- **Automatic File Naming**: Output files are automatically named based on the input PDF filename
- **Real-time Status Updates**: See conversion progress and completion status
- **Usage Tracking**: Monitor your Mathpix API usage with live statistics
- **Clean Interface**: Professional GUI with maximize/minimize/close controls
- **No Console Window**: Runs as a pure Windows GUI application
- **Single Executable**: No installation required - just run the .exe file

## 📋 System Requirements

- **Operating System**: Windows 10 or Windows 11 (64-bit)
- **Internet Connection**: Required for Mathpix API access
- **Disk Space**: Minimal (executable is ~15MB)
- **Dependencies**: None - all required components are bundled

## 🔧 Installation

**For End Users:**
1. Download the `mathpix-converter.exe` file
2. No installation needed - just double-click to run
3. The application will open with a clean, centered window

**For Developers:**
```bash
# Clone or download the source code
# Ensure Go 1.19+ and MinGW-w64 are installed
# Build the application:
$env:PATH += ";C:\ProgramData\mingw64\mingw64\bin"
$env:CGO_ENABLED = "1"
go build -o mathpix-converter.exe -ldflags "-s -w -H=windowsgui" .
```

## 📖 How to Use

### Basic Usage

1. **Launch the Application**
   - Double-click `mathpix-converter.exe`
   - The application window will open in a maximized state

2. **Check Usage Statistics**
   - The top of the window shows your current API usage
   - Format: "📊 Pages: X/5000 (Y left) | Requests: Z"
   - Updates automatically when the app starts

3. **Convert a PDF**
   - Click the "Choose PDF" button in the center
   - Select your PDF file from the file browser
   - Only `.pdf` files are shown in the file picker

4. **Monitor Progress**
   - Status updates appear at the top of the window:
     - "📤 Uploading PDF..." - File is being uploaded to Mathpix
     - "⏳ Processing..." - Mathpix is analyzing the PDF
     - "⏳ Converting to DOCX..." - Creating the DOCX file
     - "📥 Downloading... X%" - Downloading the converted file
     - "✅ Conversion completed!" - Done successfully

5. **Find Your Output**
   - The DOCX file is saved in the same folder as your original PDF
   - Filename format: `[original-name].docx`
   - Example: `document.pdf` → `document.docx`

### Advanced Features

#### Usage Tracking
- **Monthly Limits**: 5,000 pages per month (Mathpix free tier)
- **Rate Limits**: 50 requests per minute
- **Real-time Updates**: Usage refreshes after each conversion

#### Error Handling
- Network connectivity issues are automatically detected
- API errors are displayed with helpful messages
- File access problems show clear error descriptions

#### Window Controls
- **Minimize**: Minimize to taskbar
- **Maximize/Restore**: Toggle between maximized and windowed mode
- **Close**: Exit the application
- **Resize**: Drag window edges to resize (when not maximized)

## 🔍 Troubleshooting

### Common Issues

**"Request too large" Error**
- Solution: The PDF file is too large. Try a smaller PDF or split large documents.

**"API error: status 401"**
- Solution: API credentials may be invalid. Contact the developer.

**"Unable to load usage"**
- Solution: Check your internet connection. Usage tracking requires API access.

**Window appears too small/large**
- Solution: Use the maximize button or resize the window manually.

**No DOCX file created**
- Solution: Check the same folder as your PDF. Ensure you have write permissions.

### Performance Tips

- **Smaller PDFs convert faster** (typically under 30 seconds)
- **Large PDFs may take several minutes** to process
- **Keep the application window open** during conversion
- **Stable internet connection** improves reliability

## 📊 API Usage Limits

### Free Tier (Current)
- **Pages**: 5,000 per month
- **Requests**: 50 per minute
- **File Size**: Up to 100MB per PDF
- **Processing Time**: Usually 30-120 seconds per file

### Usage Monitoring
The application shows:
- Pages used this month vs. total limit
- Remaining pages available
- Total API requests made
- Updates automatically after each conversion

## 🛠️ Technical Details

### Built With
- **Go 1.25+**: Core application language
- **Fyne v2.6+**: Cross-platform GUI framework
- **Mathpix API v3**: PDF to DOCX conversion service
- **MinGW-w64**: C compiler for Windows CGO support

### Architecture
- **Single Executable**: All dependencies bundled
- **Async Processing**: Non-blocking API calls
- **Multipart Uploads**: Efficient file transfer
- **Status Polling**: Real-time conversion updates

### Security
- API credentials are embedded in the executable
- All communication uses HTTPS
- No user data is stored locally
- Files are processed securely via Mathpix

## 📝 File Format Support

### Input Formats
- **PDF**: All standard PDF files
- **Maximum Size**: 100MB per file
- **Pages**: No specific limit (usage counted)

### Output Format
- **DOCX**: Microsoft Word format
- **Compatibility**: Works with Word 2007+, Google Docs, LibreOffice
- **Formatting**: Preserves text, basic formatting, and structure

## 🤝 Support & Contact

### Getting Help
- Check this README for common solutions
- Ensure you have a stable internet connection
- Verify the PDF file is not corrupted

### Reporting Issues
When reporting problems, please include:
- Windows version (e.g., Windows 11 22H2)
- PDF file size and source application
- Complete error message text
- Steps that led to the issue

### Updates
- Check for new versions of the executable
- New features and bug fixes are released periodically
- No automatic updates - manual download required

---

## 📄 License & Credits

This application uses the Mathpix API for PDF to DOCX conversion. Mathpix API usage is subject to their terms of service and usage limits.

Built with ❤️ for easy PDF conversion.
