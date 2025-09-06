# F | Configuration files

Hey there, configuration enthusiasts! 🎉 This is my personal project, a cheerful haven for your SSH, Vim, and Oh My Zsh configurations. Say goodbye to the days of scattered files and convoluted setups – here, we're all about simplicity, smiles, and personalized awesomeness!

## ssh config

> PATH: `~/.ssh/config`

Configuration file used to manage different git project sites and credentials.

## .vimrc

> PATH: `~/.vimrc`

VIM configuration file with plugins to optimize usage.

### Pre-requirement: vim-plug

#### Unix

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

You can automate the process by putting the command in your Vim configuration file as suggested in vim-plug Tip: [Automatic installation](https://github.com/junegunn/vim-plug/wiki/tips#automatic-installation).

### Windows (PowerShell)

```powershell
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni $HOME/vimfiles/autoload/plug.vim -Force
```

## VIM Plugins

Using [vim-plug](https://github.com/junegunn/vim-plug) (`Plug 'vim-plugin'`) set the next list of VIM Plugins in `.vimrc`:

* **vim-monokai-tasty:** A Vim colorscheme based on the Monokai theme, with a tasty twist.
* **vim-javascript:** A Vim plugin for improved JavaScript syntax highlighting and indentation.
* **vim-jsx-pretty:** Provides better syntax highlighting and indentation for JSX (JavaScript XML) files.
* **vim-styled-components:** Enhances Vim support for styled-components in JavaScript and TypeScript.
* **vim-json:** Improves JSON highlighting and provides additional features for working with JSON files in Vim.
* **vim-graphql:** Adds support for GraphQL syntax highlighting and other features in Vim.
* **nerdtree:** A file system explorer for Vim that allows you to navigate and manipulate files and directories.
* **lightline.vim:** A lightweight and customizable statusline/tabline plugin for Vim.
* **vim-table-mode:** Simplifies creating and editing tables in plain text files within Vim.
* **vim-easy-align:** Provides easy text alignment in Vim, making it convenient to align code and text.
* **vim-github-dashboard:** A GitHub dashboard for Vim, allowing you to interact with GitHub repositories from within Vim.
* **vim-fireplace:** A Clojure REPL environment for Vim, providing features for interactive Clojure development.
* **YCM-Generator:** A plugin that generates configuration files for YouCompleteMe, a code completion engine for Vim.
* **vim-go:** Enhances Vim for Go (Golang) development, providing features like syntax highlighting, code formatting, and more.
* **gocode:** A plugin for the Go programming language that integrates with the gocode autocompletion daemon.
* **fzf:** Integrates the Fuzzy Finder (fzf) into Vim, providing a fast and powerful fuzzy search feature.
* **my-prototype-plugin:** Appears to be a custom or personal plugin located in the user's local file system (~/my-prototype-plugin).

## Oh My Zsh

### Install Zsh

```bash
sudo apt-get update
sudo apt-get install zsh
```

Check installation with `zsh --version`

### Install Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Oh My Zsh Plugins

Edit Zsh config file `vim ~/.zshrc` with the next list of plugins:

* **git:** Provides Git aliases and enhances the Zsh prompt with Git information.
* **zsh-autosuggestions:** Suggests commands as you type based on your command history, making it easier to repeat or modify previous commands.
* **sudo:** Adds aliases and functions for using sudo more efficiently.
* **web-search:** Enables searching the web directly from the terminal by using aliases like goog for Google search, gh for GitHub, and others.
* **copypath:** Adds a command (copypath) that copies the current working directory path to the clipboard.
* **copyfile:** Adds a command (copyfile) that copies the current file path to the clipboard.
* **copybuffer:** Provides a set of commands to copy the contents of the terminal buffer to the clipboard.
* **dirhistory:** Tracks and allows for quick navigation to recently visited directories.
* **jsontools:** Offers functions to pretty-print, minify, and validate JSON data directly from the terminal.
* **python:** Adds aliases and functions for working with Python, including virtual environments.
* **zsh-syntax-highlighting:** Enables syntax highlighting for Zsh commands, making it easier to spot errors and understand command structures.
* **you-should-use:** Provides a set of friendly reminders or suggestions for better practices. For example, it might remind you to use a specific command or option for better efficiency.

## Git Bash (Windows)

### Install gsudo

Open an elevated command prompt or PowerShell and run the following command:

```bash
choco install gsudo
```

### Config .bashrc

To enable some alias, open your `.bashrc` file and add the following lines:

```conf
[ -f ~/.fzf.bash ] && source ~/.fzf.bash
alias python="winpty python"
alias sudo='gsudo'
```

After saving the `.bashrc` file, run the following command in your Git Bash terminal to apply the new configuration immediately:

```bash
source ~/.bashrc
```
