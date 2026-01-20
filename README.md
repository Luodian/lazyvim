# LazyVim Configuration

My personal LazyVim configuration.

## Prerequisites

### Install Neovim (>= 0.9.0)

**macOS**:
```bash
brew install neovim
```

**Ubuntu/Debian**:
```bash
# Add Neovim PPA for latest version
sudo add-apt-repository ppa:neovim-ppa/unstable
sudo apt update
sudo apt install neovim
```

**Arch Linux**:
```bash
sudo pacman -S neovim
```

**From source** (any platform):
```bash
git clone https://github.com/neovim/neovim.git
cd neovim
make CMAKE_BUILD_TYPE=Release
sudo make install
```

### Install Dependencies

```bash
# Required
brew install git ripgrep fd lazygit

# Optional but recommended
brew install node npm python3
pip3 install pynvim
npm install -g neovim
```

**Ubuntu/Debian**:
```bash
sudo apt install git ripgrep fd-find
# lazygit - install from GitHub releases
```

## Installation

### Fresh Install

```bash
# Backup existing config (if any)
mv ~/.config/nvim ~/.config/nvim.bak
mv ~/.local/share/nvim ~/.local/share/nvim.bak
mv ~/.local/state/nvim ~/.local/state/nvim.bak
mv ~/.cache/nvim ~/.cache/nvim.bak

# Clone this config
git clone https://github.com/Luodian/lazyvim.git ~/.config/nvim

# Start Neovim - plugins will auto-install
nvim
```

### Update Config

```bash
cd ~/.config/nvim
git pull
```

## Structure

```
~/.config/nvim/
├── init.lua              # Entry point
├── lazy-lock.json        # Plugin versions lock
├── lazyvim.json          # LazyVim extras config
├── lua/
│   ├── config/
│   │   ├── autocmds.lua  # Auto commands
│   │   ├── keymaps.lua   # Key mappings
│   │   ├── lazy.lua      # Lazy.nvim bootstrap
│   │   └── options.lua   # Neovim options
│   └── plugins/
│       ├── explorer.lua  # File explorer config
│       ├── markdown.lua  # Markdown support
│       └── python.lua    # Python development
└── stylua.toml           # Lua formatter config
```

## Key Features

- Based on [LazyVim](https://github.com/LazyVim/LazyVim)
- Python development support
- Markdown preview and editing
- Custom file explorer settings

## References

- [LazyVim Documentation](https://lazyvim.github.io/)
- [Neovim Documentation](https://neovim.io/doc/)
