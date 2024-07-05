# MacOs Installs

## Software

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

brew install --cask \
  google-chrome  \
  brave-browser \
  visual-studio-code \
  docker \
  ngrok \
  obs \
  android-studio \
  mongodb-compass
```

## Tools
```bash
brew install \
  node \
  bun
```

## ZSH FILE
```
export ANDROID_HOME=$HOME/Library/Android/sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/platform-tools
export ZSH="$HOME/.oh-my-zsh"
eval "$(/opt/homebrew/bin/brew shellenv)"


# Which plugins would you like to load?
plugins=(
  git
#  zsh-completions
#  zsh-autosuggestions
#  zsh-syntax-highlighting
)

# Would you like to use another custom folder than $ZSH/custom?
ZSH_CUSTOM=/Users/ishansingla/Desktop

# Set name of the theme to load --- if set to "random", it will https://github.com/ohmyzsh/ohmyzsh/wiki/Themes
ZSH_THEME="jonathan"


# Uncomment one of the following lines to change the auto-update behavior
zstyle ':omz:update' mode auto

source $ZSH/oh-my-zsh.sh

# get machine's ip address
alias ip="ipconfig getifaddr en0"

# edit global zsh configuration
alias zshconfig="vim ~/.zshrc"
# reload zsh configuration
alias zshsource="source ~/.zshrc"
# reload zsh configuration
alias ohmyzsh="cd ~/.oh-my-zsh"

# navigate to global ssh directory
alias sshhome="cd ~/.ssh"
# edit global ssh configuration
alias sshconfig="vim ~/.ssh/config"

# edit global git configuration
alias gitconfig="vim ~/.gitconfig"

# git aliases
alias giti="git init"
alias gits="git status"
alias gitd="git diff"
alias gitl="git lg"
alias gita="git add ."
alias gitc="git commit -m"

alias loc="npx sloc --format cli-table --format-option head --exclude 'build|\.svg$\.xml' ./"
export PATH="/opt/homebrew/opt/libxml2/bin:$PATH"
export PATH="/opt/homebrew/opt/openjdk/bin:$PATH"

POWERLEVEL9K_DISABLE_CONFIGURATION_WIZARD=true
POWERLEVEL9K_DISABLE_CONFIGURATION_WIZARD=true

```

## Git Setup
```bash
git config --global user.name "IshanBFHL"
git config --global user.email "ishan.singla@bajajfinserv.in"
git config --global init.defaultBranch main
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"

```

## Node
```bash
npm set init-author-name="Ishan Singla"
npm set init-author-email="ishan.singla@bajajfinserv.in"
npm set init-author-url="https://ishansingla.in"
npm install -g nodemon yarn serve
```

## Vs Code

### Json Setting
```python
{
    "workbench.iconTheme": "material-icon-theme",
    "git.confirmSync": false,
    "files.autoSave": "afterDelay",
    "git.enableSmartCommit": true,
    "git.autofetch": true,
    "liveServer.settings.donotShowInfoMsg": true,
    "emmet.includeLanguages": {
        "javascript": "javascriptreact"
    },
    "[css]": {
        "editor.defaultFormatter": "vscode.css-language-features"
    },
    "[html]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[json]": {
        "editor.defaultFormatter": "vscode.json-language-features"
    },
    "editor.unicodeHighlight.allowedLocales": {
        "es": true
    },
    "editor.accessibilitySupport": "off",
    "rapidapi.terminalLink.enabled": true,
    "editor.minimap.renderCharacters": false,
    "[python]": {
        "editor.formatOnType": true
    },
    "editor.guides.bracketPairs": true,
    "githubPullRequests.pullBranch": "never",
    "[jsonc]": {
        "editor.defaultFormatter": "vscode.json-language-features"
    },
    "security.workspace.trust.untrustedFiles": "open",
    "editor.cursorBlinking": "solid",
    "editor.cursorStyle": "block",
    "files.trimTrailingWhitespace": true,
    "explorer.confirmDelete": false,
    "explorer.compactFolders": false,
    "workbench.statusBar.visible": true,
    "workbench.editor.enablePreview": false,
    "workbench.editor.restoreViewState": true,
    "terminal.integrated.fontFamily": "Hack Nerd Font Mono",
    "editor.find.addExtraSpaceOnTop": true,
    "editor.stickyScroll.enabled": false,
    "editor.fontFamily": "Hack Nerd Font Mono",
    "editor.fontSize": 14,
    "editor.insertSpaces": true,
    "editor.detectIndentation": false,
    "editor.scrollBeyondLastLine": true,
    "editor.minimap.enabled": false,
    "editor.find.seedSearchStringFromSelection": "never",
    "editor.renderLineHighlight": "all",
    "workbench.colorCustomizations": {
        "editor.lineHighlightBackground": "#223851"
    },
    "files.associations": {
        ".env*": "makefile"
    },
    "prettier.singleQuote": true,
    "prettier.printWidth": 70,
    "prettier.tabWidth": 4,
    "editor.formatOnSave": true,
    "[markdown]": {
        "editor.formatOnSave": false
    },
    "[javascript]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[javascriptreact]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescript]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescriptreact]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "prettier.documentSelectors": [
        "**/*.astro"
    ],
    "[astro]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.codeActionsOnSave": {
        "source.fixAll": "explicit",
        "source.fixAll.eslint": "explicit",
        "source.fixAll.tslint": "explicit",
        "source.addMissingImports": "explicit"
    },
    "eslint.validate": [
        "javascript",
        "javascriptreact",
        "typescript",
        "typescriptreact"
    ],
    "javascript.validate.enable": false,
    "javascript.updateImportsOnFileMove.enabled": "always",
    "typescript.updateImportsOnFileMove.enabled": "always",
    "explorer.confirmDragAndDrop": false,
    "js/ts.implicitProjectConfig.checkJs": true,
    "editor.formatOnPaste": true,
    "editor.formatOnType": true,
    "editor.inlineSuggest.enabled": true,
    "github.copilot.enable": {
        "*": true,
        "plaintext": false,
        "markdown": true,
        "scminput": false,
        "yaml": true,
        "javascript": true
    },
    "git.openRepositoryInParentFolders": "never",
    "typescript.preferences.autoImportFileExcludePatterns": [
        "@radix-ui"
    ],
    "cSpell.enableFiletypes": [
        "!asciidoc",
        "!c",
        "!cpp",
        "!csharp",
        "!css",
        "!elixir",
        "!erlang",
        "!git-commit",
        "!go",
        "!graphql",
        "!handlebars",
        "!haskell",
        "!html",
        "!jade",
        "!java",
        "!javascript",
        "!javascriptreact",
        "!json",
        "!jsonc",
        "!jupyter",
        "!less",
        "!php",
        "!pug",
        "!python",
        "!restructuredtext",
        "!rust",
        "!scala",
        "!scminput",
        "!scss",
        "!swift",
        "!typescript",
        "!typescriptreact",
        "!vue",
        "!yaml",
        "!yml",
        "mdx"
    ],
    "prisma.showPrismaDataPlatformNotification": false,
    "[dart]": {
        "editor.formatOnSave": true,
        "editor.formatOnType": true,
        "editor.rulers": [
            80
        ],
        "editor.selectionHighlight": false,
        "editor.suggestSelection": "first",
        "editor.tabCompletion": "onlySnippets",
        "editor.wordBasedSuggestions": "off"
    },
    "github.copilot.chat.scopeSelection": true,
    "markdown.updateLinksOnFileMove.enabled": "always",
    "diffEditor.ignoreTrimWhitespace": false
}

```

### Json keybindings
```python
[
  {
    "key": "ctrl+up",
    "command": "cursorMove",
    "args": {
      "to": "up",
      "by": "line",
      "value": 10
    },
    "when": "editorTextFocus"
  },
  {
    "key": "ctrl+down",
    "command": "cursorMove",
    "args": {
      "to": "down",
      "by": "line",
      "value": 10
    },
    "when": "editorTextFocus"
  }
]
```
