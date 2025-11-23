# ⚡ Erzo x Bolt - Il2CppDumper Professional Edition

<div align="center">

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Platform](https://img.shields.io/badge/platform-Windows-lightgrey.svg)
![.NET](https://img.shields.io/badge/.NET-6.0-purple.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Status](https://img.shields.io/badge/status-Active-success.svg)

**Professional Il2Cpp Dumping Tool with Modern GUI**

*Optimized for Free Fire Game Analysis*

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Screenshots](#-screenshots) • [Contact](#-contact)

</div>

---

## 📖 About

**Erzo x Bolt** is a professional-grade Il2Cpp dumping tool with a modern graphical user interface, specifically optimized for **Free Fire** game analysis and reverse engineering. This tool combines powerful Il2Cpp dumping capabilities with an intuitive, user-friendly interface designed for both beginners and experts.

### 🎯 What is Il2CppDumper?

Il2CppDumper is a tool to reverse **Unity's IL2CPP** (Intermediate Language To C++) toolchain, allowing you to:
- Extract C# code structures from compiled Unity games
- Generate dummy DLL assemblies
- Create struct definitions for reverse engineering
- Analyze game mechanics and implementations

### 🎮 Compatible Games

**Works with Unity games using IL2CPP backend:**
- ✅ Free Fire (optimized!)
- ✅ PUBG Mobile
- ✅ Genshin Impact
- ✅ Among Us
- ✅ Call of Duty Mobile
- ✅ And many more Unity games

**Requirements:**
- Game must be built with Unity Engine
- Game must use IL2CPP compilation (not Mono)
- Must have access to `libil2cpp.so` / `GameAssembly.dll` and `global-metadata.dat`

### ⚡ Why Erzo x Bolt?

- **Modern GUI** - No more command-line complexity
- **Free Fire Optimized** - Specifically tuned for Free Fire analysis
- **Professional Design** - Dark theme, intuitive layout
- **Real-time Feedback** - See progress as it happens
- **Comprehensive Settings** - Full control over dump options

---

## ✨ Features

### 🎨 User Interface
- **Modern Dark Theme** - Professional, eye-friendly design
- **Three Main Sections:**
  - 🏠 **Home** - File selection and dumping operations
  - ⚙️ **Settings** - Comprehensive configuration options
  - ℹ️ **About** - Application information and credits
- **Real-time Console Output** - Monitor progress with detailed logging
- **One-Click Operations** - Simple, intuitive workflow

### 🔧 Technical Features
- **Multiple Format Support:**
  - PE (Windows)
  - ELF 32/64-bit (Linux/Android)
  - Mach-O 32/64-bit (iOS/macOS)
  - WebAssembly
  - NSO (Nintendo Switch)
- **Advanced Dump Options:**
  - Methods, Fields, Properties, Attributes
  - Field and Method Offsets
  - TypeDef Index
- **Generation Capabilities:**
  - Dummy DLL assemblies
  - Struct definitions
  - IDA/Ghidra scripts
- **Smart Detection:**
  - Automatic format detection
  - Version detection
  - Architecture detection (32/64-bit)

### 🎯 Free Fire Optimization
- Optimized for Free Fire game structure
- Enhanced error handling for mobile game formats
- Specialized metadata parsing

---

## 🚀 Installation

### Prerequisites
- **Windows 10/11**
- **.NET 6.0 Desktop Runtime** - [Download Here](https://dotnet.microsoft.com/download/dotnet/6.0)

### Quick Install

1. **Download the latest release** from [Releases](https://github.com/erzo19/erzo-bolt-il2cppdumper/releases)
2. **Extract the archive** to your desired location
3. **Run `Il2CppDumper.GUI.exe`** to open the application


```bash
# Clone the repository
git clone https://github.com/erzo19/erzo-bolt-il2cppdumper.git

# Navigate to the directory
cd erzo-bolt-il2cppdumper

# Build the GUI
dotnet build Il2CppDumper.GUI/Il2CppDumper.GUI.csproj -c Release

# Run the application
dotnet run --project Il2CppDumper.GUI/Il2CppDumper.GUI.csproj
```

---

## 📖 Usage

### Basic Workflow

1. **Launch the Application**
   ```
   Double-click RUN_GUI.bat
   ```

2. **Select Files** (Home Tab)
   - Click "Browse" next to "Il2Cpp binary file"
   - Select your game's Il2Cpp binary (e.g., `libil2cpp.so`, `GameAssembly.dll`)
   - Click "Browse" next to "global-metadata.dat"
   - Select the metadata file from your game

3. **Configure Settings** (Optional - Settings Tab)
   - Choose what to dump (methods, fields, properties, etc.)
   - Enable/disable dummy DLL generation
   - Enable/disable struct generation
   - Set advanced options if needed

4. **Start Dumping**
   - Click "🚀 Start Dump" button
   - Monitor progress in the console output
   - Wait for completion

5. **View Results**
   - Click "📂 Open Output" to view dumped files
   - Find `dump.cs`, dummy DLLs, and other generated files

### Advanced Usage

#### Force Il2Cpp Version
If auto-detection fails:
1. Go to Settings tab
2. Enable "Force Il2Cpp Version"
3. Enter the version number (e.g., 24.3)
4. Save settings

#### Manual Mode
If automatic registration search fails, the tool will prompt for manual input of:
- CodeRegistration address
- MetadataRegistration address

---

## 📸 Screenshots

### Home Tab - Main Interface
```
┌─────────────────────────────────────────────────────────────┐
│  ⚡ Erzo x Bolt                    🏠 Home  ⚙️ Settings  ℹ️ About │
│  Il2CppDumper Professional Edition                          │
├─────────────────────────────────────────────────────────────┤
│  📁 File Selection                                          │
│  [Il2Cpp binary file...]              [Browse]              │
│  [global-metadata.dat...]             [Browse]              │
│  [Output directory...]                [Browse]              │
│                                                             │
│  ⚡ Quick Actions                                           │
│  [🚀 Start Dump] [🗑️ Clear] [📂 Output] [💬 Contact Dev]  │
│                                                             │
│  📋 Console Output                                         │
│  ╔══════════════════════════════════════════════════════╗  │
│  ║  ⚡ ERZO X BOLT - IL2CPPDUMPER PROFESSIONAL EDITION  ║  │
│  ╚══════════════════════════════════════════════════════╝  │
└─────────────────────────────────────────────────────────────┘
```

### Settings Tab
- Comprehensive dump options with checkboxes
- Advanced configuration settings
- Save/Load functionality

### About Tab
- Application information
- Developer contact (Telegram)
- Feature list and credits

---

## 🛠️ Configuration

### Default Settings
```json
{
  "DumpMethod": true,
  "DumpField": true,
  "DumpProperty": true,
  "DumpAttribute": true,
  "DumpFieldOffset": true,
  "DumpMethodOffset": true,
  "DumpTypeDefIndex": true,
  "GenerateDummyDll": true,
  "GenerateStruct": true,
  "DummyDllAddToken": true,
  "ForceIl2CppVersion": false,
  "ForceVersion": 24.3,
  "ForceDump": false,
  "NoRedirectedPointer": false
}
```

### Output Files
After dumping, you'll find:
- `dump.cs` - Decompiled C# code structures
- `script.json` - Script data for reverse engineering tools
- `DummyDll/` - Generated dummy DLL assemblies
- `*.py` - Python scripts for IDA Pro, Ghidra, etc.

---

## 🆘 Troubleshooting

### Application Won't Start
- **Solution:** Install [.NET 6.0 Desktop Runtime](https://dotnet.microsoft.com/download/dotnet/6.0)

### Build Failed
- **Solution:** Install [.NET 6.0 SDK](https://dotnet.microsoft.com/download/dotnet/6.0)
- Run `dotnet restore` in the project directory

### Dump Failed
- Check console output for specific error messages
- Try enabling "Force Dump Mode" in Settings
- Verify files are not encrypted or protected
- Contact developer for support

### Files Not Found
- Ensure both Il2Cpp binary and metadata files are selected
- Check file permissions
- Verify files are not corrupted

---

## ❓ FAQ (Frequently Asked Questions)

### Q: What games can I use this tool with?
**A:** Only **Unity games** that use the **IL2CPP** backend. This includes most modern mobile Unity games like Free Fire, PUBG Mobile, Genshin Impact, etc.

### Q: Will this work with Unreal Engine games?
**A:** No, this tool is specifically for Unity IL2CPP games only.

### Q: How do I know if a game uses IL2CPP?
**A:** Look for these files:
- Android: `libil2cpp.so` in the APK
- Windows: `GameAssembly.dll` in game folder
- Both need: `global-metadata.dat` file

### Q: Can I use this for Mono Unity games?
**A:** No, this tool only works with IL2CPP compiled Unity games, not Mono backend.

### Q: Is this legal?
**A:** This tool is for educational and research purposes. Always respect game terms of service and local laws.

### Q: Do I need programming knowledge?
**A:** Basic knowledge helps, but the GUI makes it easy for beginners. Just select files and click dump!

### Q: What platforms are supported?
**A:** The tool runs on Windows, but can dump games from:
- Android (APK files)
- iOS (IPA files)
- Windows games
- Nintendo Switch
- WebAssembly

---

## 🏆 Credits & Acknowledgments

### Original Work
- **Il2CppDumper** - [Perfare](https://github.com/Perfare/Il2CppDumper) (2016-2023)
- Original tool that made this possible

### Free Fire Optimization
- **erzo19** - Free Fire specific optimizations and enhancements

### GUI Development
- **[@erzohack](https://t.me/erzohack)** - GUI design, development, and branding
- Modern interface and user experience design

### Special Thanks
- The reverse engineering community
- Unity IL2CPP developers
- All contributors and testers

---

## 📞 Contact & Support

### Developer
**@erzohack**

### Telegram
[![Telegram](https://img.shields.io/badge/Telegram-@erzohack-blue?style=for-the-badge&logo=telegram)](https://t.me/erzohack)

### Support
- 💬 Contact via Telegram: [@erzohack](https://t.me/erzohack)
- 🐛 Report issues: [GitHub Issues](https://github.com/erzo19/erzo-bolt-il2cppdumper/issues)
- 💡 Feature requests: [GitHub Discussions](https://github.com/erzo19/erzo-bolt-il2cppdumper/discussions)

---

## 📜 License

This project is based on Il2CppDumper by Perfare.

```
MIT License

Copyright (c) 2024 Erzo x Bolt (@erzohack)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## ⭐ Star History

If you find this tool useful, please consider giving it a star! ⭐

---

## 🔗 Related Projects

- [Il2CppDumper](https://github.com/Perfare/Il2CppDumper) - Original Il2CppDumper
- [Il2CppInspector](https://github.com/djkaty/Il2CppInspector) - Alternative Il2Cpp analysis tool

---

## 🌟 Repository

**GitHub:** [github.com/erzo19/erzo-bolt-il2cppdumper](https://github.com/erzo19/erzo-bolt-il2cppdumper)

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/erzo19/erzo-bolt-il2cppdumper?style=social)
![GitHub forks](https://img.shields.io/github/forks/erzo19/erzo-bolt-il2cppdumper?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/erzo19/erzo-bolt-il2cppdumper?style=social)

---

<div align="center">

**⚡ Erzo x Bolt - Professional Il2Cpp Dumping Made Easy ⚡**

*Developed with ❤️ by [@erzohack](https://t.me/erzohack)*

[⬆ Back to Top](#-erzo-x-bolt---il2cppdumper-professional-edition)

</div>
