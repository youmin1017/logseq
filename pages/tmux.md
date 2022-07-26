- ## Installation
	- `brew install tmux` #macOS
- ## Oh-My-Tmux
	- ```bash
	  # install
	  git clone https://github.com/gpakosz/.tmux.git ~/.oh-my-tmux
	  ln -s -f ~/.oh-my-tmux/.tmux.conf ~/.tmux.conf
	  cp ~/.oh-my-tmux/.tmux.conf.local ~/.tmux.conf.local
	  
	  # .tmux.conf.local
	  tmux_conf_theme_left_separator_main='\uE0B0'
	  tmux_conf_theme_left_separator_sub='\uE0B1'
	  # tmux_conf_theme_right_separator_main='\uE0B2'
	  # tmux_conf_theme_right_separator_sub='\uE0B3'
	  ```