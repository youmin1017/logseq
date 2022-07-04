- ## macOS Package Manager [[Homebrew]]
- ## Packages
	- query-table:: true
	  #+BEGIN_QUERY
	  {:title "All page tags"
	  :query [:find ?tag-name
	          :where
	          [?tag :block/name ?macOS]]
	  }
	  #+END_QUERY
- ## Configs
	- [[ssh]]
-