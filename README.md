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
