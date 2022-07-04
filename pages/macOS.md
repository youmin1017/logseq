- ## macOS Package Manager [[Homebrew]]
- ## Packages
	- query-table:: true
	  [query-table:: true
	  #+BEGIN_QUERY
	  {:title "All page tags"
	  :query [:find ?tag-name
	          :where
	          [?tag :block/name ?macOS]]
	  }
	  #+END_QUERY](#+BEGIN_QUERY
	  {:title "All page tags"
	  :query [:find ?tag-name
	          :where
	          [?tag :block/name ?tag-name]]
	  :view (fn [tags]
	        [:div
	         (for [tag (flatten tags)]
	           [:a.tag.mr-1 {:href (str "#/page/" tag)}
	            (str "#" tag)])])}
	  #+END_QUERY)
- ## Configs
	- [[ssh]]
-