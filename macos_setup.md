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

6. Install ZSH 

7. Install powerlevel 10k

8. Install NVM
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.0/install.sh | bash
```
then install the script add the following codes to your respective profile.


```
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
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