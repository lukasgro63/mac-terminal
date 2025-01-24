# MAC Terminal Setup with ohmyszh and Powerlevel10k

This guide outlines the steps to enhance the terminal experience by installing and configuring **[Oh My Zsh](https://ohmyz.sh/)** and **[Powerlevel10k](https://github.com/romkatv/powerlevel10k)**.

> **Note:** This setup was performed on macOS using **[iTerm2](https://iterm2.com/)**.
> 
> If you are using macOS, make sure **[Homebrew](https://brew.sh/)** is installed before proceeding.

---

## Install Oh My Zsh

[Oh My Zsh](https://ohmyz.sh/) simplifies managing Zsh configurations.

### Installation

Run the following command to install Oh My Zsh:

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## Install Powerlevel10k Theme

Run the following command to install Powerlevel10k:

```sh
git clone https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

### Install Essential Plugins

#### Syntax Highlighting

zsh-syntax-highlighting adds color to command-line syntax.

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting
```

#### Auto-Suggestions

zsh-autosuggestions provides command auto-completion based on history.

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions.git ~/.oh-my-zsh/custom/plugins/zsh-autosuggestions
```

### Enable Plugins

Modify `~/.zshrc` to enable plugins:

```sh
vi ~/.zshrc
```

Add the following inside the file (also delete git plugin):

```sh
ZSH_THEME="powerlevel10k/powerlevel10k"

plugins=(
git
zsh-syntax-highlighting
zsh-autosuggestions
)
```

## Configure Powerlevel10k

Navigate trow the setup, after opening the terminal again

## Fix VS Code Font

1. Open **VS Code**.
2. Click on **"Code"** (macOS) or **"File"** (Windows/Linux).
3. Click on **"Preferences" → "Settings"**.
4. Type the following in the **search bar** at the top:
    ```sh
    terminal.integrated.fontFamily
    ```

5. **Click on the input field** and set the value to:
    ```sh
    MesloLGS NF
    ```
