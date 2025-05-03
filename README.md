# Khushal's iTerm2 Config

This repository contains my personal iTerm2 configuration.

## 🚀 Setup

To use this config on any Mac:

```bash
git clone https://github.com/YOUR_USERNAME/khushal-iterm2-config.git ~/khushal-iterm2-config
```

1. Open iTerm2.
2. Go to **Preferences > General > Preferences**.
3. Check **"Load preferences from a custom folder or URL"**.
4. Set the folder to `~/khushal-iterm2-config`.
5. Restart iTerm2.

## 🔧 Shell Integration & Auto-Complete

Enable powerful features like auto-complete and command history:

```bash
# Step 1: Install iTerm2 shell integration
curl -L https://iterm2.com/shell_integration/install_shell_integration.sh | bash

# Step 2: Activate immediately (for zsh)
source ~/.iterm2_shell_integration.zsh
```

Note: Shell integration enables features like:
- Command auto-completion
- Command history
- Directory history
- Recent directories
- Shell integration status in prompt

## 💾 Auto-Sync

To auto-save config changes:
- Enable **"Save changes to folder when iTerm2 quits"** in Preferences.

---
