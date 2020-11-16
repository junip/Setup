1. Install Homebrew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
# this is a self explanatory script that will install required packages.
# a package manager for the macos
```
2. Install Git 
```
brew install git
```
3. Setup for Git

[SSH key configurations for git](https://github.com/junipdewan/Setup/blob/master/git.md)

4. Install required softwares
  - VS code
  - Iterm

4. Install VS code extensions 

- Better comments
- Bracket pair colorizer.
- Eslint
- Git file histroy by Rodrigo pmbo
- Tab nine
- path intellisense.
- Quokka.js
- Markdown preview enhanced.
- Material Icon theme.

6. Install ZSH 

```
brew install zsh
```

```
Instal the ohmyzsh framework

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

7. Install powerlevel 10k

Install the theme for zsh
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```


8. Install NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.0/install.sh | bash
```
then install the script add the following codes to your respective profile.


```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" 


[ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
```

9. install rvm for ruby

```
curl -sSL https://get.rvm.io | bash -s stable --ruby
```

10. Install Zsh and its Plugins
 - zsh autosuggestions 
 ```
 #installation
 git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions 

 #Add to your zshrc file
 source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
 ```
 - zsh syntax highlighting
 ```
 # clone it 
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

# add to your zsh file  
plugins =(
    zsh-syntax-highlighting
)
 ```