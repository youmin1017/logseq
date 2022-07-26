tags:: #sandbox #cgroup

- [Manual](http://www.ucw.cz/moe/isolate.1.html#_name)
- ## Installation
	- #ubuntu
	  ```bash
	  sudo apt update
	  sudo apt-get install -y --no-install-recommends git libcap-de make
	  git clone https://github.com/judge0/isolate.git /tmp/isolate
	  cd /tmp/isolate
	  make -j$(nproc) install
	  rm -rf /tmp
	  ```
- ## Environment
	- #+BEGIN_CAUTION
	  `ioi/isolate` using [[cgroup]] ^^v1^^, if your system using `cgroupv2` you should switch it to ^^v1^^
	  #+END_CAUTION
	- ((62c05dd6-3671-447d-8e39-3d681ce6d1b1)) #linux
	  id:: 62c059db-bbd6-481e-b46b-8aeecd4b9abb
	- ((62c041ba-86d6-436b-b8c0-9ff0be20f9e8))  #macOS
- ## Docker
	- #Docker
	- #+BEGIN_NOTE
	  使用來自^^judge0^^的[compilers](https://hub.docker.com/r/judge0/compilers)image ，這個Image以經打包好了許多的compilers, such as `gcc`, `g++`, `rustc`, etc.
	  #+END_NOTE
	- 在執行容器時因為^^isolate^^需要用到[[cgroup]]，因此引此需要加上`--privileged`這個Flag
- ## Create Sandbox
	- `isolate --cg --b <box-id> --init`
- ## Run Program
	- ```bash
	  isolate --cg --silent --meta meta.txt --box-id 0 \
	          --time 2.0 --extra-time 0.5 --wall-time 5.0 \
	          --stack 64000 --processes=30 --cg-mem 128000 \
	          --no-cg-timing --fsize 1024 \
	          -E LANG -E LANGUAGE -E LC_ALL -E PATH\
	          --dir '/etc':'noexec' \
	          --run -- `which g++` program.cpp
	  ```
	- ```bash
	  isolate --cg --silent --meta meta.txt --box-id 0 \
	          --time 2.0 --extra-time 0.5 --wall-time 5.0 \
	          --stack 64000 --processes=30 --cg-mem 128000 \
	          --no-cg-timing --fsize 1024 --stdin stdin.txt --stdout output \
	          -E LANG -E LANGUAGE -E LC_ALL \
	          --dir '/etc':'noexec' \
	          --run -- a.out
	  ```
- ## Test C Programe
	- ```c
	  #include<stdlib.h>
	  #include <unistd.h>
	  
	  int main() {
	      void* buf = malloc(1024 * 1000); // 1000kb
	      usleep(3 * 1000 * 1000);         // 3s
	  }
	  ```
-
- ## References
  collapsed:: true
	- [自研沙箱Isolate学习](https://juejin.cn/post/6927151461625233416)
	- [isolate Sandbox 使用](https://tracyliu1220.github.io/2020/09/22/2020-09-22-Sandbox-ioi-isolate/)
-