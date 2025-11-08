# Overview
1) Install ZSH
2) Add the `.zshrc_motd` into your home directory from this directory
3) Append the following to `~/.zshrc`
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
