# Adobe Photoshop LR (Low Resolution Mode) 🖥️

[![GitHub release](https://img.shields.io/github/release/hasanbeder/AdobePhotoshopLR.svg)](https://github.com/hasanbeder/AdobePhotoshopLR/releases)
[![macOS](https://img.shields.io/badge/macOS-10.15%2B-blue.svg)](https://www.apple.com/macos)
[![Photoshop](https://img.shields.io/badge/Adobe%20Photoshop-Supported-brightgreen.svg)](https://www.adobe.com/products/photoshop.html)

## 🎯 Project Purpose

In recent versions of macOS, the native low-resolution mode checkbox was removed. This utility provides a seamless solution to run Adobe Photoshop in low-resolution mode, particularly beneficial for:
- Older Mac systems
- Low-performance configurations
- Enhanced visual clarity on Retina displays

## ✨ Features

- 🚀 Automatic Photoshop detection
- 🔍 Low-resolution mode launch
- 🔄 Compatible with multiple Photoshop versions
- 💻 Minimal system resource usage
- 🛡️ Easy-to-use and secure

## 🛠 System Requirements

- **Operating System**: macOS 10.15+
- **Processor**: 64-bit Intel or Apple Silicon
- **RAM**: Minimum 4GB
- **Adobe Photoshop**: Any version

## 📦 Installation

### Option 1: Direct Download
1. Visit [Releases](https://github.com/hasanbeder/AdobePhotoshopLR/releases)
2. Download the latest `.zip` file
3. Extract `Adobe Photoshop LR.app`
4. Move to Applications folder

### Option 2: Clone Repository
```bash
git clone https://github.com/hasanbeder/AdobePhotoshopLR.git
```

## 🚀 Usage

⚠️ **IMPORTANT WARNING** ⚠️
**DO NOT RENAME THIS APPLICATION FILE!**
*Renaming the "Adobe Photoshop LR.app" will break the automatic Photoshop launch functionality.*

1. Ensure Adobe Photoshop is installed
2. Launch `Adobe Photoshop LR.app`
3. Photoshop will open in low-resolution mode automatically

## 🛠 Creating Your Own Automator Workflow

### Step-by-Step Guide

1. **Open Automator**
   - Launch from Applications
   - Click "File" > "New"
   - Select "Application"

2. **Add Run Shell Script**
   - Search "Run Shell Script"
   - Drag to workflow area
   - Set shell to `/bin/zsh`

3. **Configure Script**
   ```zsh
   photoshop_path=$(find /Applications -name "Adobe Photoshop*.app" ! -name "Adobe Photoshop LR.app" | head -n 1)
   open "$photoshop_path" --args -AppleMagnifiedMode YES
   ```

4. **Save Workflow**
   - Choose location
   - Name your application

## 🔍 Workflow Customization

- Modify search paths for custom Photoshop installations
- Add error handling
- Customize application icon

## 📋 Customizing Application Icon

### Method 1: Using Finder (Detailed Steps)
1. Locate your new icon file (must be in `.icns` format)
2. Right-click the `Adobe Photoshop LR.app` in Finder
3. Select "Show Package Contents"
4. Navigate to `Contents/Resources/` folder
5. Find the existing `ApplicationStub.icns` file
6. Drag and drop your new icon, replacing the existing one
   - macOS will prompt you to confirm replacement
   - Click "Replace" to update the icon

### Method 2: Using Terminal
```bash
# Rename your icon to match the app's icon
mv "YourNewIcon.icns" "ApplicationStub.icns"

# Replace the app's icon
cp "ApplicationStub.icns" "Adobe Photoshop LR.app/Contents/Resources/"
```

📝 How to Use:
1. Create or download your `.icns` icon file
2. Rename the icon file to match the app's icon name
3. Place the commands in the same folder as the app
4. Run the commands in Terminal
5. The app's icon will change instantly

### Icon Requirements
- Must be in `.icns` format
- Recommended sizes: 16x16, 32x32, 128x128, 256x256, 512x512 pixels
- Use tools like [Image2icon](https://img2icnsapp.com/) for conversion

### Troubleshooting Icon Changes
- If icon doesn't update immediately:
  - Restart Finder: `killall Finder`
  - Clear icon cache: `sudo find /private/var/folders/ -name com.apple.dock.iconcache -exec rm {} \;`
  - Restart Dock: `killall Dock`

## 🐛 Troubleshooting

- Verify Photoshop installation path
- Check macOS security settings
- Ensure script has execute permissions

## 📋 Troubleshooting Permissions
- If the app won't open, try these commands:
  ```bash
  # For the app in Applications folder
  xattr -cr "/Applications/Adobe Photoshop LR.app"
  
  # For the app in a custom location
  xattr -cr "/path/to/Adobe Photoshop LR.app"
  ```
- This removes macOS security attributes that might block the app

## 📋 Known Limitations

- Requires manual updates
- May need reconfiguration after major macOS updates
- Limited to single Photoshop installation

## 🤝 Contributing

Contributions are welcome! 

1. Fork the repository
2. Create your feature branch
3. Commit changes
4. Push to the branch
5. Create a Pull Request

## 📄 License

MIT License. See [LICENSE](LICENSE) for details.

## 📞 Contact & Support

- **GitHub**: [hasanbeder](https://github.com/hasanbeder)
- **X (Twitter)**: [@hasanbeder](https://x.com/hasanbeder)
- **Issues**: [GitHub Issues](https://github.com/hasanbeder/AdobePhotoshopLR/issues)

---

**Made with ❤️ to improve Photoshop experience on Mac**

*Disclaimer: Not affiliated with Adobe. Use at your own discretion.*
