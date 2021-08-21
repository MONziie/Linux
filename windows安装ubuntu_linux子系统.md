重装的时候，又忘了安装步骤，悲伤的记忆力...
Ubuntu LTS（长期支持 longterm support）做下笔记
Microsoft store也有很多宝藏啊，还不用找开源镜像，nice！

安装步骤链接参考：
https://zhuanlan.zhihu.com/p/97942331
https://www.jb51.net/article/189243.htm


1、控制面板 -> 程序 -> 选择启用或关闭Windows功能 -> 勾上 适用Linux的Windwos子系统 -> 确定 -> 重启电脑
2、在 设置 -> 更新和安全 -> 开发者选项 中切换到开发人员模式
3、打开windows商店，搜索 ubuntu，安装ubuntu
4. 设置国内阿里镜像数据源

  # 1.切换为超级管理员root
  sudo su 
  # 2.编辑数据源配置文件
  vim /etc/apt/sources.list

  # 3.  i 插入以下内容
  deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse
  deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse
  deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse

  # 4. Esc -> :wq 保存退出

  # 5.更新配置
  apt-get update
  
  
  
  
