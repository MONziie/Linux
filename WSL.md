

## WINDOWS-LINUX双系统
### WSL下安装docker

<p>
手动操作;
1.启用适用子系统
以管理员身份打开 PowerShell 并运行：
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
重启计算机

2 安装WSL2之前启用虚拟机功能：
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
重启

3 下载内核更新包UPDATE windows: 运行

4 设置wsl2为默认版本：wsl --set-default-version 2

5 安装Linux分发版：Microsoft store

6.Ubuntu for WSL 1升级成Ubuntu for WSL 2:(powershell)
wsl.exe --set-version Ubuntu-20.04 2
(需要几分钟等待)

7 查看已安装WSL的版本：(powershell)
wsl.exe -l -v

wsl  --set-default ubantu . 

系统--设置--更多存储设置--保存到C盘

安装Docker
setting:
在 "设置" "常规" 中选中 "使用基于 WSL 2 的引擎" > General
 "设置 > 资源 > WSL 集成"，从已安装的 WSL 2 分发中选择要启用 Docker 集成。
 
1.docker run -d -p 80:80 docker/getting-started
2.new repository
docker run -name repo alpine/git clone\https://github.com/docker/getting-started.git
3.build the image
cd getting-started docker build -t docker101tutorial
4. run the contianer
docker run -d -p 80:80 \ --name docker-tutorial docker101tutorial

要确认是否已安装 Docker，请打开 WSL 分发 (例如 Ubuntu) 并通过输入以下内容来显示版本和版本号： docker --version
使用以下方法运行简单的内置 Docker 映像，测试安装是否正常： docker run hello-world

创建虚拟环境：
https://docs.microsoft.com/zh-cn/windows/python/web-frameworks#hello-world-tutorial-for-django

ctrl-D/exit()结束环境


VS
https://code.visualstudio.com/docs/remote/containers-tutorial

https://docs.microsoft.com/zh-cn/windows/dev-environment/docker/overview

https://docs.microsoft.com/zh-cn/windows/python/web-frameworks#hello-world-tutorial-for-django


</p>



文档：
https://docs.microsoft.com/zh-cn/windows/dev-environment/overview

centos镜像:
http://isoredirect.centos.org/centos/8/isos/x86_64/#http://isoredirect.centos.org/centos/8/isos/x86_64/#
centos:安装图解：
https://zhuanlan.zhihu.com/p/85807189

centos下离线安装docker:
https://zhuanlan.zhihu.com/p/349055854


Linux教程：
https://zhuanlan.zhihu.com/p/351483036
