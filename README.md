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
- Add autosuggestion to oh-my-zsh:
  - `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
  - Add the plugin to the list of plugins for Oh My Zsh to load (inside ~/.zshrc):
    ```
    plugins=( 
        # other plugins...
        zsh-autosuggestions
    )
    ```

### Homebrew (https://brew.sh/)
- Install via curl: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
- Register Homebrew to PATH:
    ```
    echo >> /home/username/.zshrc
    echo 'eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"' >> /home username/.zshrc
    eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
    ```
- Install Homebrew's dependencies: `sudo dnf group install development-tools`

### powerLevel10k Theme for zsh (https://github.com/romkatv/powerlevel10k)
- clone with `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
- Set ZSH_THEME to `powerlevel10k/powerlevel10k` on .zshrc file.
- Restart zsh with `exec zsh`
- Configure powerlevel10k
