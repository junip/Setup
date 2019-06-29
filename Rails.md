###  :smile: Ruby On Rails Setup

### Installing HomeBrew -

```  
  ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```  

### Installing Ruby -

```
  brew install rbenv ruby-build
```  

- Add rbenv to bash so that it loads every time you open a terminal

``` 
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

```

###  :beer: Configure Git

- git config  --global color.ui true
- git config  --global user.name "name"
- git config  --global user.email "junip.dewan@gmail.com"


### :pizza: Generate  SSH KEYS 
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

- Copy the public key and [Paste Here](https://github.com/settings/keys)

```
cat ~/.ssh/id_rsa.pub
```

- Check your github connection 

```
ssh -T git@github.com
```
### :wine_glass: Install RAILS -

- Install rails 

```
gem install rails -v 5.2.3
```
- Rails is now installed, but in order for us to use the rails executable, we need to tell rbenv to see it:

```
rbenv rehash
```

- Verify Rails is installed

```
rails -v
# Rails 5.2.3
```





