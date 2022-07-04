- #linux #cgroup
- [探索cgroup2](https://zhuanlan.zhihu.com/p/432112680)
- ## Switch cgroup version from v2 to v1
  id:: 62c05dd6-3671-447d-8e39-3d681ce6d1b1
	- ```bash
	  # Ref: https://stackoverflow.com/questions/70965770/unable-to-mount-memory-cgroup
	  # sudo vi /etc/default/grup
	  GRUB_CMDLINE_LINUX="cgroup_enable=memory systemd.unified_cgroup_hierarchy=0"
	  # sudo update-grub
	  # sudo reboot
	  ```
	- Then: You check your host is having `/sys/fs/cgroup/memory` and `/sys/fs/cgroup/cpuacct`
-