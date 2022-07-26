- ## Installation
	- `sudo brew install neovim` #macOS
	- `sudo pacman -S neovim` #manjaro
- ## Config
	- ```vimscript
	  set tabstop=4       " The width of a TAB is set to 4.
	                      " Still it is a \t. It is just that
	                      " Vim will interpret it to be having
	                      " a width of 4.
	  
	  set shiftwidth=4    " Indents will have a width of 4
	  
	  set softtabstop=4   " Sets the number of columns for a TAB
	  
	  set expandtab       " Expand TABs to spaces
	  imap jk <Esc>
	  
	  "keep visual mode after indent
	  vnoremap > >gv
	  vnoremap < <gv
	  ```
-
-