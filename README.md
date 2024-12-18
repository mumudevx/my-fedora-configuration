# My Fedora (only i3 wm / without gnome) Configuration
My personal configuration steps when install Fedora for first time.

Don't forget to replace 'username' variables with real username of device.

## Shell Installations & Configurations

### Zsh
- Install: `dnf install zsh`
- Check version: `zsh --version`
- Make default shell zsh: `chsh -s $(which zsh)`
- Logout: `sudo pkill -u username`
- Check default shell: `echo $SHELL`

### Oh-my-zsh (https://ohmyz.sh/)
- Install via curl: `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

### Homebrew (https://brew.sh/)
- Install via curl: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
- Register Homebrew to PATH:
    ```
    echo >> /home/username/.zshrc
    echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home username/.zshrc
    eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
    ```
- Install Homebrew's dependencies: `sudo dnf group install development-tools`
