# Khushal's iTerm2 Config

This repository contains my personal iTerm2 configuration, including theme, color schemes, and shell integration. It uses iTerm2's Dynamic Profiles feature for better portability and easier management.

## 📁 Repository Structure

- `iterm2-profile-khushal.json` - iTerm2 profile configuration including:
  - **Terminal Settings**: Type, scrollback, mouse reporting, session handling
  - **Window Settings**: Transparency, blur, dimensions, resizing behavior
  - **Text Settings**: Font rendering, anti-aliasing, bold/italic styles
  - **Color Schemes**: Dark and light mode color configurations
  - **Cursor Settings**: Style, color, and behavior
  - **Keyboard**: Key mappings and special key handling
- `.p10k.zsh` - Powerlevel10k theme configuration with custom prompt settings
- `.gitignore` - Git ignore rules for system and temporary files

## 🎨 Color Scheme

The profile includes a carefully crafted color scheme that:
- Supports both dark and light modes
- Uses high-contrast colors for better readability
- Includes special configurations for cursor, selection, and badges
- Optimized for both regular and bold text

## 🚀 Setup Steps

### 1. Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/khushal-iterm2-config.git ~/khushal-iterm2-config
```

### 2. Configure iTerm2 Dynamic Profile
1. Open iTerm2
2. Create the Dynamic Profiles directory:
```bash
mkdir -p ~/Library/Application\ Support/iTerm2/DynamicProfiles
```
3. Link the profile:
```bash
ln -sf ~/khushal-iterm2-config/iterm2-profile-khushal.json ~/Library/Application\ Support/iTerm2/DynamicProfiles/
```
4. Restart iTerm2 or reload preferences (⌘⇧R)
5. Go to **Profiles** and select the imported profile

### 3. Install Required Font
The configuration uses MesloLGS NF font. Install it by:

```bash
# Create Fonts directory if it doesn't exist
mkdir -p ~/Library/Fonts

# Download all font variants
cd ~/Library/Fonts
curl -fLo "MesloLGS NF Regular.ttf" https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
curl -fLo "MesloLGS NF Bold.ttf" https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf
curl -fLo "MesloLGS NF Italic.ttf" https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf
curl -fLo "MesloLGS NF Bold Italic.ttf" https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf
```

Then configure iTerm2 to use the font:
1. Open iTerm2 Preferences (⌘,)
2. Go to **Profiles > Text**
3. Click on Font and select "MesloLGS NF"
4. Do the same for Non-ASCII Font

### 4. Install Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 5. Install Powerlevel10k Theme
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### 6. Configure Powerlevel10k
1. Copy the p10k configuration:
```bash
cp ~/khushal-iterm2-config/.p10k.zsh ~/.p10k.zsh
```

2. Add these lines to your `~/.zshrc`:
```bash
# Enable Powerlevel10k instant prompt
if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

# Set theme to powerlevel10k
ZSH_THEME="powerlevel10k/powerlevel10k"

# Load Powerlevel10k config
[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
```

### 7. Shell Integration & Auto-Complete

Enable powerful features like auto-complete and command history:

```bash
# Install iTerm2 shell integration
curl -L https://iterm2.com/shell_integration/install_shell_integration.sh | bash

# Activate immediately (for zsh)
source ~/.iterm2_shell_integration.zsh
```

Features enabled by shell integration:
- Command auto-completion
- Command history
- Directory history
- Recent directories
- Shell integration status in prompt

### 8. Auto-Sync Settings
To ensure your preferences are automatically saved:
- Enable **"Save changes to folder when iTerm2 quits"** in Preferences

## 🔄 Updating

To update your configuration:
1. Navigate to the config directory: `cd ~/khushal-iterm2-config`
2. Pull the latest changes: `git pull`
3. Restart iTerm2 to apply changes

## ⚙️ Features
- Custom color scheme
- Powerlevel10k theme with optimized settings
- Shell integration for enhanced functionality
- Pre-configured key mappings
- Optimized terminal settings

---
