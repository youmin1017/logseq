-
- `nerd-fonts-hack`
- ## autojump-rs
- ## fnm
	- background-color:: #978626
	  #+BEGIN_QUOTE
	  Fast and simple Node.js version manager, built in Rust
	  #+END_QUOTE
	- ### Installation
		- `sudo pacman -S fnm-bin`
	- ### Setup
- ## Oh-My-Tmux
  collapsed:: true
	- #tmux
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