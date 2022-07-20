- ## Installation
	- `brew install zsh` #macOS
- ## Config
	- ```zsh
	  # .zshrc
	  setopt autocd
	  autoload -Uz compinit && compinit
	  zstyle ':completion:*' matcher-list 'm:{a-z}={A-Z}'
	  ```