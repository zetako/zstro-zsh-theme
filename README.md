# zstro-zsh-theme
A re-written version of astro-ssh-zsh-theme.

## Astro-ssh-zsh-theme

> Astro theme is based on [`ys`](http://blog.ysmood.org/my-ys-terminal-theme/) theme and `robbyrushell` (default theme) theme.
> 
> Astro-SSH theme is based on Astro theme with a patch to show hostname when using ssh connect 

## Screenshot

![Screenshot of Zstro](screenshot.png)

## Progress

### What's new?

Basically, there is nothing new, expect a proxy display using MY OWN global variable called `$ZETAKO_PROXY`. If you don't have a script interact with it, it will be no different with the old astro-ssh theme.

### TO-DO

- [ ] Give return value when return error.
- [ ] Rewrite scripts, using zsh script's function.
- [ ] Add a one-line installation command or a .sh to help install.

## Installation

### Clone the repository:
```
git clone https://github.com/zetako/zstro-zsh-theme.git
```

### Apply theme 
1. Copy `zstro.zsh-theme` file into the `~/.oh-my-zsh/themes/` directory.
2. Change the theme variable name to `ZSH_THEME="zstro"` in `~/.zshrc`
```shell
cp ~/.zshrc ~/.zshrc.bak
sed -i "s/ZSH_THEME=\"[^\"]*\"/ZSH_THEME=\"zstro\"/" ~/.zshrc
```
3. Reload ZSH with `source ~/.zshrc`

## Others

- What's `setproxy` in your screenshot?

    - It's just a script, like belows. No matter which method you choose to set your proxy, just add the last 2 line to tell zstro your proxy.


```shell
#/bin/sh

### First set proxy
export http_proxy="localhost:8889"
export https_proxy="localhost:8889"
export ftp_proxy="localhost:8889"

### Then set env to tell ZSH
export ZETAKO_PROXY="V2Ray"
source ~/.zshrc
```
