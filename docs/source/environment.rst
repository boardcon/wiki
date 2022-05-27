Compiler Environment
======================

1 Vmware10.0 + ubuntu16.04
--------------------------

Install Vmware10.0 in windows OS, and then install ubuntu16.04 in VMware
to compile. Please visit the official website http://www.ubuntu.com/ to
download and install ubuntu operating system.

.. Note::

 Android9 should be complied by ubuntu 64bit OS.

2 Install OpenJDK1.8
----------------------

.. code-block::

  sudo mkdir /usr/lib/java
  sudo tar zxvf java-8-openjdk-amd64.tar.gz –C /usr/lib/java/

Add the following information in the end of **/etc/profile**

| export JAVA_HOME=/usr/lib/java/java-8-openjdk-amd64
| export JRE_HOME=/usr/lib/java/java-8-openjdk-amd64/jre
| export CLASSPATH=.:$JAVA_HOME/lib:$JRE_HOME/jre/lib:$CLASSPATH
| export PATH=$JAVA_HOME/bin:$JRE_HOME/jre/bin:$PATH

.. code-block::

  source /etc/profile

Check JDK version
  
.. code-block::

   java -version

3 Install Tools
-----------------

- PC OS: ubuntu system
- Network: online
- Permission: root

.. code-block::

  sudo apt-get install build-essential
  sudo apt-get install zlib1g-dev
  sudo apt-get install flex
  sudo apt-get install libx11-dev
  sudo apt-get install gperf
  sudo apt-get install libncurses5-dev
  sudo apt-get install bison
  sudo apt-get install lsb-core
  sudo apt-get install lib32z1-dev
  sudo apt-get install g++-multilib
  sudo apt-get install lib32ncurses5-dev
  sudo apt-get install uboot-mkimage
  sudo apt-get install g++-4.4-multilib

