- [Manual](http://www.ucw.cz/moe/isolate.1.html#_name)
- #+BEGIN_CAUTION
  HOST請使用`ubuntu`，因為`ioi/isolate`使用 #[[cgroup]] 來限制記憶體、CPU等
  OR: You check your host is having `/sys/fs/cgroup/memory` and `/sys/fs/cgroup/cpuacct`
  #+END_CAUTION
- ## Docker Image
	- #+BEGIN_NOTE
	  使用來自^^judge0^^的[compilers](https://hub.docker.com/r/judge0/compilers)image ，這個Image以經打包好了許多的compilers, such as `gcc`, `g++`, `rustc`, etc.
	  #+END_NOTE
- ## Create Sandbox
	- `isolate --cg --b <box-id> --init`
- ## Run Program
	- ```bash
	  isolate --cg --silent --meta meta.txt --box-id 0 \
	          --time 2.0 --extra-time 0.5 --wall-time 5.0 \
	          --stack 64000 --processes=30 --cg-mem 128000 \
	          --no-cg-timing --fsize 1024 --stdin input --stdout output \
	          -E LANG -E LANGUAGE -E LC_ALL \
	          --dir '/etc':'noexec' \
	          --run -- a.out
	  ```
	-
- ## References
  collapsed:: true
	- [自研沙箱Isolate学习](https://juejin.cn/post/6927151461625233416)
	- [isolate Sandbox 使用](https://tracyliu1220.github.io/2020/09/22/2020-09-22-Sandbox-ioi-isolate/)