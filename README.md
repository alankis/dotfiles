# dotfiles

#### Installation instruction

It will be scripted soon, to make my life easier :)

1. Install 'gnome-terminal'
  ```bash
  $ sudo apt install gnome-terminal
  ```
  
2. Install 'zsh' shell 
  ```bash
  $ sudo apt install zsh
  ```
  
3. Make 'zsh' default shell
  ```bash 
  chsh -s $(which zsh)
  ```
  Log-out && Log-in
  
  Check if default shell is actually zsh
  ```bash
  $ echo $SHELL // /usr/bin/zhs
  ```
  
4. Install 'oh-my-zsh'
  ```bash
  sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
  ```
5. Install 'tmux' if you haven't allready
  ```bash
  $ sudo apt install tmux
  ```
6. Migrate your previous rbenv or RVM configurations from .bashrc
This is *optional*.
```bash
$ tail -n 3 .bahrc >> .zshrc
```
7. Install 'powerline' fonts
```bash
$ cd
$ wget https://github.com/powerline/powerline/raw/develop/font/PowerlineSymbols.otf
$ wget https://github.com/powerline/powerline/raw/develop/font/10-powerline-symbols.conf
$ mkdir ~/.fonts
$ mv PowerlineSymbols.otf ~/.fonts/
$ mkdir -p .config/fontconfig/conf.d #if directory doesn't exists
```
Clear font cache
```bash
$ fc-cache -vf ~/.fonts/
```
Move config file
```bash
$ mv 10-powerline-symbols.conf ~/.config/fontconfig/conf.d/
```
8. Configure .zshrc
