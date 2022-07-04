tags:: #macOS #manjaro 
label:: package

- ## Installation
	- `sudo brew install neovim` #macOS
	- `sudo pacman -S neovim` #manjaro
- ## Config
	- ```sh
	  set tabstop=4                        
	  set shiftwidth=4          
	  set expandtab
	  imap jk <Esc>
	  
	  "keep visual mode after indent
	  vnoremap > >gv
	  vnoremap < <gv
	  ```
-
-