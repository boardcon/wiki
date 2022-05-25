Install Debug Tools
====================

1 Install CP2102 Driver  
-----------------------

Plug the USB-to-UART cable CP2102 to the PC, unzip **CP2102WIN7.rar** on Windows, then click **preInstaller.exe** to install

.. figure:: ./image/EM3566_SBC_Android11_figure_17.png
   :alt: Install CP2102
   :width: 472px

.. figure:: ./image/EM3566_SBC_Android11_figure_18.png
   :alt: Install successful
      
Now the device will be listed under *Device Manager -> PORTS* with unique serial port assigned

.. figure:: ./image/EM3566_SBC_Android11_figure_19.png
   :alt: serial port path

2 Install Rockchip Driver Assistant
-------------------------------------

Path :file:`DriverAssitant_v5.1.1/DriverInstall.exe`

.. figure:: ./image/RK_Driver_Assitant_install-1.png
   :alt: RK_Driver_Assitant_install-1
   :width: 300px
   
.. figure:: ./image/RK_Driver_Assitant_install-2.png
   :alt: RK_Driver_Assitant_install-2
   :width: 300px

After the installation is complete, connect the board and PC with Micro USB cable and press the **Recover** key and hold then power the board, in *Computer Management* can see the following information:

.. figure:: ./image/EM3566_SBC_Android11_figure_22.png
   :alt: serial port path

The WINDOW will pop up *found New Hardware Wizard* dialog box, choose to install from the specified location, and then select :file:`/DriverAssitant_v5.11/DriverAssitant_v5.1.1/ADBDriver`.

After the installation is complete in *Computer Management* can see the following information:

.. figure:: ./image/EM3566_SBC_Android11_figure_23.png
   :alt: installation complete

3 Install Serial Terminal Tool
-------------------------------

The serial terminal **SecureCRT** is used for debugging. It can be used directly after decompression. 
Open **SecureCRT.exe** after copy to PC :file:`tools/windows/SecureCRT.exe`, then click the icon *Quick Connect* to config

.. figure:: ./image/EM3566_SBC_Android11_figure_24.png
   :alt: SecureCRT UI

.. figure:: ./image/EM3566_SBC_Android11_figure_25.png
   :alt: Quick Connect

Set the parameters as follow:

- Protocol: Serial
- Port: To be specified by user PC
- Baud rate: 1500000
- Please check **XON/XOFF** but not **RTS/CTS**
- Check *Save* session

.. figure:: ./image/EM3566_SBC_Android11_figure_26.png
   :alt: Set the parameters

After all, click *connect*

.. figure:: ./image/EM3566_SBC_Android11_figure_27.png
   :alt: Connect Serial
 
.. note:: 

 If open more than one serial terminal tools, and they use the same serial port, there will be reported the port is busy.
 **Solution**: Turn off the serial tool that unnecessary.
