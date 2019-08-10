:computer: Jazz Up your terminal with Zsh

## :sparkles: Installation ZSH for macOS
--------------------
My Terminal Preview


![Preview 1](images/terminal_1.png?raw=true "Terminal Preview")


![Preview 2](images/terminal_2.png?raw=true "Terminal 2 Preview")

![Preview 3](images/terminal_3.png?raw=true "Terminal 3 Preview")



```
1. Install Homebrew

ruby -e "$(curl -fsSL https://raw.zshhubusercontent.com/Homebrew/install/master/install)"

```

```
2. install zsh

brew install zsh

```

```
3.To set zsh as your default shell, execute the following.

sudo -s 'echo /usr/local/bin/zsh >> /etc/shells' && chsh -s /usr/local/bin/zsh
```

```
4. Install iTerm2 for macOS

brew cask install iterm2

```
### :ok_hand: Install Oh My Zsh

```
Install OhMyZsh

sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

```
Check version

zsh --version
```
```
Upgradation of OhMyZsh

upgrade_oh_my_zsh
```

### :sparkles: Installation For LINUX

```
sudo apt-get update
sudo apt-get upgrade
sudo apt-get install zsh

```
- Red Hat Linux System

```
sudo yum upgrade
sudo yum install zsh
```

- Suse-based linux systems

```
sudo zypper upgrade
sudo zypper install zsh
```

## Change to ZSH shell

```
# change the bash shell to zsh shell

chsh -s $(which zsh)
```

```
1. Install Powerline

sudo apt install fonts-powerline


```

```
2. Update the zshrc 

sudo vi  ~/.zshrc 

# update the theme to 'agnoster'
```

```
3. Install Nerdfont

 # Mkdir 
 - mkdir -p ~/.local/share/fonts
 # install for linux

 - cd ~/.local/share/fonts && curl -fLo "Droid Sans Mono for Powerline Nerd Font Complete.otf" https://github.com/ryanoasis/nerd-fonts/raw/master/patched-fonts/DroidSansMono/complete/Droid%20Sans%20Mono%20Nerd%20Font%20Complete.otf

 # install for macOS

 cd ~/Library/Fonts && curl -fLo "Droid Sans Mono for Powerline Nerd Font Complete.otf" https://github.com/ryanoasis/nerd-fonts/raw/master/patched-fonts/DroidSansMono/complete/Droid%20Sans%20Mono%20Nerd%20Font%20Complete.otf

 # install using Homebrew

 brew tap homebrew/cask-fonts
 
 brew cask install font-hack-nerd-font

``` 

```
4. install powerline font

$ git clone https://github.com/powerline/fonts.git
$ cd fonts
$ ./install.sh

```

## :arrow_forward: For icons in terminal install the powerlevel9k theme 

```
powerlevel 9k theme styles your prompt with coloured segments for different purposes and can include the Nerd Font programming icons.
```

### Install powelevel9k theme and load when zsh starts

```
git clone https://github.com/bhilburn/powerlevel9k.git ~/powerlevel9k

echo 'source  ~/powerlevel9k/powerlevel9k.zsh-theme' >> ~/.zshrc

```
# for macOS with homebrew

1. brew tap sambadevi/powerlevel9k
2. brew install powerlevel9k

If you want to load powerlevel9k in your zsh simply add the following line to your .zshrc:

  source /usr/local/opt/powerlevel9k/powerlevel9k.zsh-theme

Alternatively you can run this command to append the line to your .zshrc

  echo "source /usr/local/opt/powerlevel9k/powerlevel9k.zsh-theme" >> ~/.zshrc

```
# macOS with homebrew


```

### Install powerlevel10k theme its more faster than powerlevel9k and it renders fast 

```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k

# Then edit your ~/.zshrc and set ZSH_THEME="powerlevel10k/powerlevel10k".

```

### Set the font in `.zshrc` file
```
The font needs to be set before Powerlevel9k is initialised in order to use it. If you open your ~/.zshrc, 
it should have the commands in this order.
```
```
# in .zshrc

POWERLEVEL9K_MODE='nerdfont-complete'
source ~/powerlevel9k/powerlevel9k.zsh-theme
```


--------------------------------------------------------

- Specify left and right terminal icons 

```
POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(
dir
# your custome icons
vcs
)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=()

```

## Plugins in zsh 

### :gift: zsh autosuggestion

```
#installation

git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions 

# Add to your zshrc file
 
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh

```

### :gift: zsh syntax highlighting

```
# clone it 

git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# add to your zsh file  
plugins =(
    zsh-syntax-highlighting
)

```

## :fire: Customization with Nerd Font Icons

```
# VCS config

POWERLEVEL9K_VCS_SHORTEN_LENGTH=14
POWERLEVEL9K_VCS_SHORTEN_MIN_LENGTH=5
POWERLEVEL9K_VCS_SHORTEN_STRATEGY="truncate_from_right"
POWERLEVEL9K_VCS_SHORTEN_DELIMITER=".."

```
```
# Directory Config

POWERLEVEL9K_SHORTEN_DIR_LENGTH=7
POWERLEVEL9K_SHORTEN_DELIMITER=".."
POWERLEVEL9K_SHORTEN_STRATEGY="truncate_absolute"
POWERLEVEL9K_SHORTEN_DIR_LENGTH=5
POWERLEVEL9K_SHORTEN_DELIMITER=".."
POWERLEVEL9K_SHORTEN_STRATEGY="truncate_from_right"
POWERLEVEL9K_PROMPT_ON_NEWLINE=true
POWERLEVEL9K_COLOR_SCHEME='light'
POWERLEVEL9K_PROMPT_ADD_NEWLINE=true
POWERLEVEL9K_VCS_GIT_GITHUB_ICON=$'\uF126 '
POWERLEVEL9K_VCS_GIT_GITLAB_ICON= $'\uf09b'

```
```
# Ruby Icon config

POWERLEVEL9K_CUSTOM_RUBY_FOREGROUND="red"
POWERLEVEL9K_CUSTOM_RUBY_BACKGROUND="white"
POWERLEVEL9K_CUSTOM_GRIN="echo -n '\uf58c' "
POWERLEVEL9K_CUSTOM_GRIN_FOREGROUND="red"
POWERLEVEL9K_CUSTOM_GRIN_BACKGROUND="white"

```
```
# Rails Icon config

POWERLEVEL9K_CUSTOM_RAILS="echo -n '\ue73b' "
POWERLEVEL9K_CUSTOM_RAILS_FOREGROUND="red"
POWERLEVEL9K_CUSTOM_RAILS_BACKGROUND="white"
```

```
# Git lab Icon config

POWERLEVEL9K_CUSTOM_GIT_LAB="echo -n '\uf296'"
POWERLEVEL9K_CUSTOM_GIT_LAB_FOREGROUND="blue"
POWERLEVEL9K_CUSTOM_GIT_LAB_BACKGROUND="white"

```

```
# Java Icon config

POWERLEVEL9K_CUSTOM_JAVA="echo -n '\ue781'"
POWERLEVEL9K_CUSTOM_JAVA_FOREGROUND="yellow"
POWERLEVEL9K_CUSTOM_JAVA_BACKGROUND="white"
```

```
# general vcs config

POWERLEVEL9K_VCS_GIT_ICON='\uf296'
POWERLEVEL9K_VCS_STAGED_ICON='\u00b1'
POWERLEVEL9K_VCS_BRANCH_ICON=' '
POWERLEVEL9K_VCS_UNTRACKED_ICON='\u25CF'
POWERLEVEL9K_VCS_UNSTAGED_ICON='\u00b1'
POWERLEVEL9K_VCS_INCOMING_CHANGES_ICON='\u2193'
POWERLEVEL9K_VCS_OUTGOING_CHANGES_ICON='\u2191'

```
```
# Custom Sass Icon

POWERLEVEL9K_CUSTOM_SASS="echo -n '\ue74b'"
POWERLEVEL9K_CUSTOM_SASS_FOREGROUND="pink"
POWERLEVEL9K_CUSTOM_SASS_BACKGROUND="white"
```
```
POWERLEVEL9K_CUSTOM_CSS3="echo -n '\ue749'"
POWERLEVEL9K_CUSTOM_CSS3_FOREGROUND="021"
POWERLEVEL9K_CUSTOM_CSS3_BACKGROUND="white"
```
```
POWERLEVEL9K_CUSTOM_HTML="echo -n '\ue736'"
POWERLEVEL9K_CUSTOM_HTML_FOREGROUND="013"
POWERLEVEL9K_CUSTOM_HTML_BACKGROUND="white"
```
```

POWERLEVEL9K_CUSTOM_SMILE="echo -n '\uf06d'"
POWERLEVEL9K_CUSTOM_SMILE_FOREGROUND="009"
POWERLEVEL9K_CUSTOM_SMILE_BACKGROUND="white"
```

```
# os ICON config

POWERLEVEL9K_OS_ICON_BACKGROUND="white"
POWERLEVEL9K_OS_ICON_FOREGROUND="red"
```
```
# Vue js Icon 

POWERLEVEL9K_CUSTOM_VUE="echo -n '\ufd42'"
POWERLEVEL9K_CUSTOM_VUE_FOREGROUND="green"
POWERLEVEL9K_CUSTOM_VUE_BACKGROUND="white"
```

```
# Ubuntu icon config

POWERLEVEL9K_CUSTOM_UBUNTU="echo -n '\uf31c' Junip"
POWERLEVEL9K_CUSTOM_UBUNTU_BACKGROUND="white"
POWERLEVEL9K_CUSTOM_UBUNTU_FOREROUND="red"
```
```
# custom sass icon

POWERLEVEL9K_CUSTOM_SASS="echo -n '\ue74b'"
POWERLEVEL9K_CUSTOM_SASS_FOREGROUND="pink"
POWERLEVEL9K_CUSTOM_SASS_BACKGROUND="white"
```
```
POWERLEVEL9K_CUSTOM_CSS3="echo -n '\ue749'"
POWERLEVEL9K_CUSTOM_CSS3_FOREGROUND="021"
POWERLEVEL9K_CUSTOM_CSS3_BACKGROUND="white"
```
```
POWERLEVEL9K_CUSTOM_HTML="echo -n '\ue736'"
POWERLEVEL9K_CUSTOM_HTML_FOREGROUND="013"
POWERLEVEL9K_CUSTOM_HTML_BACKGROUND="white"

```
:rocket:  Enjoy zsh 