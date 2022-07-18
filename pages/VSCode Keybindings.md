tags:: vscode

- [[macOS]] Binding
  collapsed:: true
	- ```json
	  // Place your key bindings in this file to override the defaults
	  [
	      {
	          "key": "cmd+k",
	          "command": "-workbench.action.terminal.clear",
	          "when": "terminalFocus && terminalHasBeenCreated || terminalFocus && terminalProcessSupported"
	      },
	      {
	          "key": "cmd+k",
	          "command": "workbench.action.navigateUp",
	          "when": "!inQuickOpen && !suggestWidgetVisible"
	      },
	      {
	          "key": "cmd+j",
	          "command": "workbench.action.navigateDown",
	          "when": "!inQuickOpen && !suggestWidgetVisible"
	      },
	      {
	          "key": "cmd+h",
	          "command": "workbench.action.navigateLeft",
	          "when": "!inQuickOpen && !suggestWidgetVisible"
	      },
	      {
	          "key": "cmd+l",
	          "command": "workbench.action.navigateRight",
	          "when": "!inQuickOpen && !suggestWidgetVisible"
	      },
	      {
	          "key": "cmd+l",
	          "command": "-expandLineSelection",
	          "when": "textInputFocus"
	      },
	      {
	          "key": "ctrl+j",
	          "command": "-editor.action.joinLines",
	          "when": "editorTextFocus && !editorReadonly"
	      },
	      {
	          "key": "ctrl+j",
	          "command": "-extension.vim_ctrl+j",
	          "when": "editorTextFocus && vim.active && vim.use<C-j> && !inDebugRepl"
	      },
	      {
	          "key": "ctrl+j",
	          "command": "workbench.action.quickOpenSelectNext",
	          "when": "inQuickOpen"
	      },
	      {
	          "key": "ctrl+n",
	          "command": "-workbench.action.quickOpenSelectNext",
	          "when": "inQuickOpen"
	      },
	      {
	          "key": "ctrl+k",
	          "command": "workbench.action.quickOpenSelectPrevious",
	          "when": "inQuickOpen"
	      },
	      {
	          "key": "ctrl+p",
	          "command": "-workbench.action.quickOpenSelectPrevious",
	          "when": "inQuickOpen"
	      },
	      {
	          "key": "ctrl+k",
	          "command": "-deleteAllRight",
	          "when": "textInputFocus && !editorReadonly"
	      },
	      {
	          "key": "ctrl+k",
	          "command": "-extension.vim_ctrl+k",
	          "when": "editorTextFocus && vim.active && vim.use<C-k> && !inDebugRepl"
	      },
	      {
	          "key": "ctrl+j",
	          "command": "selectNextSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "cmd+down",
	          "command": "-selectNextSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+k",
	          "command": "selectPrevSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "cmd+up",
	          "command": "-selectPrevSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+p",
	          "command": "-selectPrevSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+n",
	          "command": "-selectNextSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+l",
	          "command": "selectNextPageSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "cmd+pagedown",
	          "command": "-selectNextPageSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+h",
	          "command": "selectPrevPageSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "cmd+pageup",
	          "command": "-selectPrevPageSuggestion",
	          "when": "suggestWidgetMultipleSuggestions && suggestWidgetVisible && textInputFocus"
	      },
	      {
	          "key": "ctrl+t",
	          "command": "-editor.action.transposeLetters",
	          "when": "textInputFocus && !editorReadonly"
	      },
	      {
	          "key": "alt+j",
	          "command": "editor.action.moveLinesDownAction",
	          "when": "editorTextFocus && !editorReadonly"
	      },
	      {
	          "key": "alt+down",
	          "command": "-editor.action.moveLinesDownAction",
	          "when": "editorTextFocus && !editorReadonly"
	      },
	      {
	          "key": "alt+k",
	          "command": "editor.action.moveLinesUpAction",
	          "when": "editorTextFocus && !editorReadonly"
	      },
	      {
	          "key": "alt+up",
	          "command": "-editor.action.moveLinesUpAction",
	          "when": "editorTextFocus && !editorReadonly"
	      },
	      {
	          "key": "alt+r",
	          "command": "renameFile",
	          "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
	      },
	      {
	          "key": "enter",
	          "command": "-renameFile",
	          "when": "explorerViewletVisible && filesExplorerFocus && !explorerResourceIsRoot && !explorerResourceReadonly && !inputFocus"
	      },
	  ]
	  ```