# zsh-welcome-home
My ZSH initialization script

## Installation

### Overview
0) Install ZSH
1) Add the `.zshrc_motd` into your home directory from this directory
2) Append the following to `~/.zshrc`

```
# =======================
# MOTD - lazy way
# ==================
# Source MOTD banner if exists
[[ -f ~/.zshrc_motd ]] && source ~/.zshrc_motd

# Show banner once per interactive shell
if [[ $- == *i* && -z "$WELCOME_PRINTED" ]]; then
  WELCOME_PRINTED=1
  _print_welcome_banner full
fi
```

## Features

- Beautiful welcome banner with system information
- Shows username, hostname, shell version, OS, and kernel info
- Displays current date, time, uptime, and load average
- Only prints once per interactive shell session
- Customizable display modes (full or minimal)

## Usage

After installation, the welcome banner will automatically display when you open a new interactive shell.

You can also manually trigger the banner:
```bash
_print_welcome_banner full    # Full banner with all information
_print_welcome_banner minimal # Minimal one-line banner
```
