#使用说明

## VPN的使用
Windows下VPN的配置请自行上网搜索，相关参数如下：
* 用户名：xxx
* 密码：xxx
* VPN类型：PPTP
* 服务器地址：xxx.xxx.xx.xxx
> 目前VPN不支持MacOS及无线网络

## 服务器的使用
####1 下载并安装Xshell5（可选）
直接网上安装即可
####2 登录服务器
通过ssh命令登录服务器，图所服务器ip为xxx.xxx.xx.xx
登录命令：
>ssh username@xxx.xxx.xx.xx

随后输入密码即可。

## 服务器端的环境搭建
#### 1 本地安装python
下载并解压python
> wget https://www.python.org/ftp/python/3.5.2/Python-3.5.2.tgz
> tar -xzf Python-3.5.2.tgz 

本地编译并安装python
> cd Python-3.5.2/
> mkdir -p ~/software/python35
> ./configure --prefix="/home/dingzheng/software/python35"
> make
> make install

创建虚拟环境
> cd ~/software
> virtualenv vpy35

选择本地的python解释器
> virtualenv -p /home/dingzheng/software/python35/bin/python3.5

使用虚拟环境
> source ~/software/vpy35/bin/activate

退出虚拟环境
> deactivate

####2 相关依赖的安装
在使用虚拟环境的基础上，使用pip进行包的安装，以TensorFlow为例
> pip install tensorflow-gpu

安装完毕之后可以尝试导入该包，测试是否安装正确
> python -c "import tensorflow"

如有任何疑问，可以随时联系我，微信邮件均可。




