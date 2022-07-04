- ## macOS Package Manager [[Homebrew]]
- ## Packages
	- #+BEGIN_QUERY
	  {:title "All blocks with tag project"
	   :query [:find (pull ?b [*])
	           :where
	           [?p :block/name "project"]
	           [?b :block/refs ?p]]}
	  #+END_QUERY
- ## Configs
	- [[ssh]]
-