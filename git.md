###  :beer: Configure Git

- git config  --global color.ui true
- git config  --global user.name "name"
- git config  --global user.email "email"


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

------------------


### :wrench:	Multiple Account Setup

<br/>
<br/>

**You can setup multiple vcs account in your system.(Gitub, Bitbucket..)**

**Generate ssh keys with your email**
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

**Give a separate name to your rsa keys**
```
id_rsa_github.pub - id_rsa_github
```
**Configure your ssh config.**

```
~/.ssh
cat config # you will see the previous id_rsa setup.
```
**Modify the config** 
```
My Config 

# Work GitHub account
 Host github.com
 HostName github.com
 User git
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa  # your first setup

# Personal GitHub Account
 Host github.com-junip # give a different name to distinguish your host.
 HostName github.com
 User git
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_per_rsa # change to your private rsa file

# Bitbucket
 Host bitbucket.org-junip
 HostName bitbucket.org
 User git
 AddKeysToAgent yes
 IdentityFile ~/.ssh/id_rsa_bitbucket
 
```

### When you take pull from your personal account then you should add the following

**You need to add the respective git host as below on each clone**

```
# example
git clone git@github.com-junip:junipdewan/jirax.git
```

**If you forgot to add this before clone it will create problem during code push**. <br/>
**You can manually add/remove the remote url**

> First remove the remote url 

```
git remote remove origin
```

> Add the remote origin
```
git remote add origin git@github.com-junip:junipdewan/jirax.git
```

> check git remote -v . You will get the updated url


----------

You need to add the **RSA** key to eval. for this i have written one small alias 

```
 alias add_rsa="cd; ~/.ssh; ssh-add id_per_rsa; ssh-add id_rsa; ssh-add id_rsa_bitbucket; ssh-add -l; cd;"
```
```
run add_rsa. 
```

<br/>

Happy Coding ... :boom::boom:



