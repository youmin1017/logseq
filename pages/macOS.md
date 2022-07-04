- ## macOS Package Manager [[Homebrew]]
- ## Packages
	- #+BEGIN_QUERY
	  {:title "All pages have a *macOS* tag"
	   :query [:find ?name
	         :in $ ?tag
	         :where
	         [?t :block/name ?tag]
	         [?p :block/tags ?t]
	         [?p :block/name ?name]]
	   :inputs ["macOS"]
	   :view (fn [result]
	         [:div.flex.flex-col
	          (for [page result]
	            [:a {:href (str "#/page/" page)} (clojure.string/capitalize page)])])}
	  #+END_QUERY
- ## Configs
	- [[ssh]]
-