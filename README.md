# ROS
## ubuntu16.04 install ROS
   添加源
    
    sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
   设置秘钥
    
    sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116
   更新系统
    
    sudo apt-get update
   安装ROS
    
    sudo apt-get install ros-kinetic-desktop-full
   初始化ROS
    
    sudo rosdep init
    rosdep update
   初始化环境变量:
    
    echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc
    source ~/.bashrc
   安装python插件
    
    sudo apt-get install python-rosinstall      
   测试ROS
    
    roscore
    
## 官方系统的一些小bug
## change hostname

unable resolve host FriendlyELEC

      sudo vim /etc/hosts
      
      127.0.0.1	FriendlyELEC
      ::1		localhost ip6-localhost ip6-loopback
      ff02::1		ip6-allnodes
      ff02::2		ip6-allrouters
   
## language setting

perl: warning: Setting locale failed. <br>
perl: warning: Please check that your locale settings: <br>
LANGUAGE = (unset), <br>
LC_ALL = (unset), <br>
LC_TIME = "zh_CN.UTF-8", <br>
LC_MONETARY = "zh_CN.UTF-8", <br>
LC_ADDRESS = "zh_CN.UTF-8", <br>
LC_TELEPHONE = "zh_CN.UTF-8",<br>
LC_NAME = "zh_CN.UTF-8", <br>
LC_MEASUREMENT = "zh_CN.UTF-8", <br>
LC_IDENTIFICATION = "zh_CN.UTF-8", <br>
LC_NUMERIC = "zh_CN.UTF-8", <br>
LC_PAPER = "zh_CN.UTF-8", <br>
		
   安装 localepurge 管理语言文件
   
      sudo apt-get install localepurge
      
   选择我们想要的语言，例如 en_US.UTF-8 和 zh_CN.UTF-8。
   
      sudo locale-gen zh_CN.UTF-8 en_US.UTF-8
  
## install ROS package
	
	
## install opencv

参考 https://github.com/dj140/autocar <br>
有一处不同，Friend官方的lubuntu系统装不上opencv3.4，测试可以安装opencv3.2

	wget -O opencv.zip https://github.com/Itseez/opencv/archive/3.2.0.zip
	wget -O opencv_contrib.zip https://github.com/Itseez/opencv_contrib/archive/3.2.0.zip
编译方面也要改成3.2.0
