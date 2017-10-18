# Jony Kalavera's dotfiles

![Always a WIP.](https://media.giphy.com/media/3o7aD4X6EpKpzjGEDK/giphy.gif)

## Install on a new host
* Install vim-spf13
```bash
$ curl http://j.mp/spf13-vim3 -L -o - | sh
```
* Install Tmux Plugin Manager
```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```
* clone this repo
```
git clone git@github.com:jonykalavera/dotfiles.git
cd dotfiles
```
* compare local dotfiles with the ones stored by dotdrop:
```
$ ./dotdrop.sh list
$ ./dotdrop.sh compare --profile=<other-host-profile>
```
Then adapt any dotfile using the template feature and set a new profile for the current host by simply adding lines in the config files, for example:
```
...
profiles:
  host1:
    dotfiles:
    - f_vimrc
    - f_xinitrc
  host2:
    dotfiles:
    - f_vimrc
...
```
When done, you can install your dotfiles using
```
$ ./dotdrop.sh install
```
