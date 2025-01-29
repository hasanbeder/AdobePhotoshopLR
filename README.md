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

## 🐛 Troubleshooting

- Verify Photoshop installation path
- Check macOS security settings
- Ensure script has execute permissions

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
