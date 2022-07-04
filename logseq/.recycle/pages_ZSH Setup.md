- #zsh #linux #manjaro #macOS
- `nerd-fonts-hack` #font
- ## autojump-rs
- ## fnm
	- background-color:: #978626
	  #+BEGIN_QUOTE
	  Fast and simple Node.js version manager, built in Rust
	  #+END_QUOTE
	- ### Installation
		- `sudo pacman -S fnm-bin` #manjaro
	- ### Setup
		- `eval "$(fnm env --use-on-cd)"` #[[zsh]]
		  id:: 62b440c3-e1ea-4c9c-83a1-3b77547ea45c
- ## Oh-My-Tmux
  collapsed:: true
	- ### Installation
	  collapsed:: true
		- ```zsh
		  git clone https://github.com/gpakosz/.tmux.git ~/.oh-my-tmux
		  ln -s -f ~/.oh-my-tmux/.tmux.conf ~/.tmux.conf
		  cp ~/.oh-my-tmux/.tmux.conf.local ~/.tmux.conf.local
		  ```
	- ### Setup
	  collapsed:: true
		- ```zsh
		  tmux_conf_theme_left_separator_main='\uE0B0'
		  tmux_conf_theme_left_separator_sub='\uE0B1'
		  # tmux_conf_theme_right_separator_main='\uE0B2'
		  # tmux_conf_theme_right_separator_sub='\uE0B3'
		  ```
- ## SSH
  collapsed:: true
	- ### Config
	  collapsed:: true
		- ```config
		  # ~/.ssh/config
		  Host lilina
		  Hostname lilina.csie.ncnu.edu.tw
		  Port 22
		  User 's109321021'
		  ```
- ## Neovim
	- ### Installation
	  collapsed:: true
		- `sudo pacman -S neovim` #manjaro
	- ### Config
	  collapsed:: true
		- ```init.vim
		  set tabstop=4                        
		  set shiftwidth=4          
		  set expandtab
		  imap jk <Esc>
		  ```
-