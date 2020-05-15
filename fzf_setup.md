## Fzf setup

Download and `install fzf` for commands fuzzy finder
- [Github repo link for fzf](https://github.com/junegunn/fzf)
- you will find the downloads and other things in the github original repo 
- Add it to your bashrc or zshrc file

```
[ -f ~/.fzf.zsh ] && source ~/.fzf.zsh
```

## Forgit Setup
- Forgit only works if you have already installed the **fzf** 
- [forgit](https://github.com/wfxr/forgit)
- directly add the following commands to your bash/zsh file.(make sure you have curl installed)

```sh
# for bash / zsh
source <(curl -s https://raw.githubusercontent.com/wfxr/forgit/master/forgit.plugin.zsh)

```
