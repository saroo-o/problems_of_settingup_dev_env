# problems_of_settingup_dev_env
搭建开发环境可能遇到的问题及解决方案

## Linux虚拟机
### Virtualbox 6.1 & Ubuntu 18.04 & win10
- 设置共享文件夹
  首先在virtualbox虚拟机X上，点击“设置-共享文件夹”进行自定义设置win10的共享文件夹地址（我选了“自动挂载”和“固定分配”）。
  然后启动虚拟机X，在命令行终端输入：
  >  sudo adduser $USER vboxsf
  
  如果提示addUser: The group 'vboxsf' does not exist，则
  > sudo addgroup vboxsf
  
  后再
  > sudo adduser $USER vboxsf
  
  > sudo apt install virtualbox-guest-utils
  
  最后重启虚拟机，可以在/media/下发现sf_开头的自定义的文件夹名称。
  
- 参考
  [How to share a directory from host to guest machine in VirtualBox](https://askubuntu.com/questions/1121705/how-to-share-a-directory-from-host-to-guest-machine-in-virtualbox)
