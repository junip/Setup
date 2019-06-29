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

