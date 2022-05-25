Install Debug Tools
====================

1 Install CP2102 Driver  
-----------------------

Plug the USB-to-UART cable CP2102 to the PC, unzip **CP2102WIN7.rar** on Windows, then click **preInstaller.exe** to install

.. figure:: ./image/EM3288_Android9_11.png
   :alt: Install CP2102

.. figure:: ./image/EM3288_Android9_12.png
   :alt: Install successful
      
Now the device will be listed under *Device Manager -> PORTS* with unique serial port assigned

.. figure:: ./image/EM3288_Android9_13.png
   :alt: serial port path

2 Install Rockchip Driver Assistant
-------------------------------------

Path :file:`Release_DriverAssitant/DriverInstall.exe`

.. figure:: ./image/EM3288_Android9_14.png
   :alt: RK_Driver_Assitant_install-1
   :width: 300px
   
.. figure:: ./image/EM3288_Android9_15.png
   :alt: RK_Driver_Assitant_install-2
   :width: 300px

After the installation is complete,connect the board and PC with Micro USB cable (USB powered), in *Computer Management* can see the following information:

.. figure:: ./image/EM3288_Android9_16.jpg
   :alt: serial port path

3 Install Serial Terminal Tool
-------------------------------

The serial terminal **SecureCRT** is used for debugging. It can be used directly after decompression. 
Open **SecureCRT.exe** after copy to PC :file:`tools/windows/SecureCRT.exe`, then click the icon *Quick Connect* to config

.. figure:: ./image/EM3288_Android9_17.png
   :alt: SecureCRT UI

.. figure:: ./image/EM3288_Android9_18.png
   :alt: Quick Connect

Set the parameters as follow:

- Protocol: Serial
- Port: To be specified by user PC
- Baud rate: 115200
- Please check **XON/XOFF** but not **RTS/CTS**
- Check *Save* session

.. figure:: ./image/EM3288_Android9_19.png
   :alt: Set the parameters

After all, click *connect*

.. figure:: ./image/EM3288_Android9_20.png
   :alt: Connect Serial
 
.. note:: 

 If open more than one serial terminal tools, and they use the same serial port, there will be reported **the port is busy**.
 **Solution**: Turn off the serial tool that unnecessary.
