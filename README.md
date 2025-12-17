# 🌙 Noctalia Niri Dotfiles

A comprehensive collection of dotfiles for a beautiful, functional Linux desktop environment featuring the **Niri** window manager and the **Noctalia** color scheme.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Maintained](https://img.shields.io/badge/maintained-yes-green.svg)

## 🎨 Theme

This configuration centers around the **Noctalia** theme - a dark, vibrant color scheme with purple, cyan, and yellow accents that creates a stunning visual experience across all applications.

### Color Palette
- **Primary**: `#fff59b` (Yellow)
- **Secondary**: `#a9aefe` (Blue)
- **Tertiary**: `#9bfece` (Cyan)
- **Error/Accent**: `#fd4663` (Red)
- **Surface**: `#070722` (Deep Dark)
- **Surface Variant**: `#11112d` (Dark)

## ✨ Features

- 🪟 **Niri Window Manager** - Modern scrollable-tiling Wayland compositor
- 🐚 **Fish Shell** - User-friendly shell with comprehensive configuration
- 🚀 **Starship Prompt** - Fast, customizable prompt
- 💻 **Alacritty** - GPU-accelerated terminal emulator
- 📊 **btop** - Beautiful resource monitor
- 🎵 **Cava** - Audio visualizer with custom shaders
- 🔍 **Fuzzel** - Application launcher for Wayland
- 📊 **Waybar** - Highly customizable status bar
- 🎭 **Quickshell (Noctalia Shell)** - Advanced shell interface
- ⚡ **Fastfetch** - System information tool

## 📦 What's Included

### Core Components

```
├── alacritty/          # Terminal emulator configuration
├── fish/               # Fish shell configuration with aliases
├── niri/               # Niri window manager config
├── waybar/             # Status bar configuration
├── starship.toml       # Starship prompt configuration
└── noctalia/           # Theme files and color schemes
```

### Utilities & Extras

```
├── btop/               # System resource monitor
├── cava/               # Audio visualizer with shaders
├── fastfetch/          # System info with custom ASCII art
├── fuzzel/             # Application launcher
├── quickshell/         # Advanced shell (Noctalia Shell)
├── dconf/              # GNOME settings
├── nautilus/           # File manager settings
└── pulse/              # PulseAudio configuration
```

## 🚀 Installation

### Prerequisites

Make sure you have the following installed:
- Niri
- Fish shell
- Alacritty
- Waybar
- Starship
- btop
- cava
- fastfetch
- fuzzel

### Quick Install

1. **Backup your existing configs** (important!):
```bash
mkdir -p ~/dotfiles-backup
cp -r ~/.config ~/dotfiles-backup/
```

2. **Clone this repository**:
```bash
git clone https://github.com/youngcoder45/My-Niri-Dotfiles.git
cd My-Niri-Dotfiles
```

3. **Copy configurations**:
```bash
# Copy to .config directory
cp -r alacritty btop cava fastfetch fish fuzzel niri waybar noctalia quickshell ~/.config/

# Copy standalone configs
cp starship.toml ~/.config/
cp pavucontrol.ini ~/.config/
```

4. **Set Fish as your default shell** (optional):
```bash
chsh -s $(which fish)
```

5. **Restart your session or reload configs**:
```bash
# Reload Fish config
source ~/.config/fish/config.fish

# Restart Niri (logout and login again)
```

## 🎯 Key Features

### Fish Shell Configuration
- **450+ lines** of professional configuration
- ZSH-style setup with comprehensive features
- Extensive aliases for productivity
- Custom functions and abbreviations
- Starship prompt integration

### Niri Window Manager
- Scrollable tiling layout
- Custom keybindings
- Noctalia-themed window decorations
- Optimized for Wayland

### Alacritty Terminal
- GPU-accelerated rendering
- Noctalia color scheme
- Multiple theme variants included
- Optimized font rendering

### Cava Audio Visualizer
- Custom GLSL shaders included:
  - Bar spectrum
  - Eye of Phi
  - Northern Lights
  - Spectrogram
  - Winamp line style
- Multiple color themes

### Quickshell (Noctalia Shell)
A complete shell interface with:
- Custom widgets and panels
- System monitoring
- Media controls
- Network management
- Power management
- Theming system
- Custom services

## ⚙️ Configuration

### Customizing Colors

Edit the Noctalia color scheme:
```bash
# Main color configuration
nano ~/.config/noctalia/colors.json

# Alacritty theme
nano ~/.config/alacritty/themes/noctalia.toml

# Niri theme
nano ~/.config/niri/noctalia.kdl
```

### Modifying Keybindings

Niri keybindings are configured in:
```bash
nano ~/.config/niri/config.kdl
```

### Fish Shell Aliases

The Fish configuration includes extensive aliases. Edit:
```bash
nano ~/.config/fish/config.fish
```

## 📸 Screenshots

> Add screenshots of your setup here!

## 🛠️ Troubleshooting

### Fish shell not loading properly
```bash
# Regenerate completions
fish_update_completions

# Clear and rebuild
rm -rf ~/.local/share/fish/
```

### Waybar not showing
```bash
# Kill existing instances
killall waybar

# Restart
waybar &
```

### Niri issues
```bash
# Check logs
journalctl --user -u niri -f

# Validate config
niri validate
```

## 🤝 Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements!

## 📝 License

This project is open source and available under the MIT License.

## 🙏 Credits

- **Noctalia Theme** - Color scheme design
- **Niri** - Window manager by [YaLTeR](https://github.com/YaLTeR/niri)
- **Quickshell Noctalia Shell** - Advanced shell interface
- Various open-source projects that made this configuration possible

## 📧 Contact

For questions or feedback, feel free to open an issue on GitHub.

---

<div align="center">

**⭐ If you find this useful, consider giving it a star!**

Made with 💜 and lots of ☕

</div>
