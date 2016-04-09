git clone this

makesymlink.sh to make the symbolic links and install oh my zsh

make sure zsh and links all worked

edit .zshrc to point to oh-my-zsh on first line

# add vim plugins
```bash
cd .vim/bundle
git clone https://github.com/scrooloose/nerdtree.git
git clone https://github.com/davidhalter/jedi-vim.git
git clone https://github.com/lokaltog/vim-powerline.git
git clone https://github.com/jistr/vim-nerdtree-tabs.git
git clone https://github.com/ctrlpvim/ctrlp.vim.git
```

# edit hostname
```bash
vim /etc/hostname
vim /etc/hosts
```

# adduser/remove user
```bash
passwd
sudo adduser temp sudo
-logout and login as temp
usermod -l newName oldName
mv /home/oldName /home/newName
usermod -d /home/newName -m newName
-logout and login as user
sudo deluser temp
sudo rm -r /home/temp
```

# notes
some issues with symlink to oh-my-zsh files.  Should be able to git clone oh-my-zsh into the dotfiles folder and create the symlink manually (```ln/ /path/to/realfile /path/to/link/location```)

changing default shell - ```chsh -s $(which zsh)```

sometimes doesn't work, can do 
```
sudo su
chsh dramsay9 -s $(which zsh)
```
