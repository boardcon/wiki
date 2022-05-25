Android9
=========

3 Compile Source 
================

*Step 1,* unzip the source.

# tar zxvf EM3288_android_9.0.tar.bz2

*Step 2,* compile uboot

# cd sdk-9.0/uboot

# make clean

# make mrproper

# ./make.sh rk3288

*Step 3,* compile the kernel

# cd sdk-9.0/kernel

# make ARCH=arm rockchip_defconfig

# make ARCH=arm rk3288-evb-android-act8846-lvds-avb.img -j8

**kernel.img,** **resource.img** and **boot.img** are generated in
current directory.

*Step 4,* compile the android

# cd sdk-9.0

# source build/envsetup.sh

# lunch

Choose rk3288-userdebug

# make -j8

*Step 5,* Generated image file

# ./mkimage.sh

# cd rockdev/Image-rk3288

# ls

Images are generated in current directory.

4 Images Operation
==================

4.1 Pack Image
--------------

*Step 1,* copy all the files in Android directory **rockdev/Image** to
the windows **AndroidTool_Release_v2.65/rockdev/Image**

*Step 2,* enter **AndroidTool_Release_v2.65/rockdev/**, double-click to
run **mkupdate.bat.**

*Step 3,* the **update.img** will be generated in **rockdev** directory.

.. image:: media/image3.png
   :width: 5.77153in
   :height: 1.99792in

.. image:: media/image4.png
   :width: 5.77014in
   :height: 3.77778in

.. image:: media/image5.png
   :width: 5.77014in
   :height: 3.77778in

.. image:: media/image6.png
   :width: 5.6875in
   :height: 2.95833in

4.2 Unzip Firmware
------------------

Unzip Firmware in ubuntu.

*Step 1*, copy **update.img** to the android source directory
**RKTools/linux/Linux_Pack_Firmware/rockdev/**

*Step 2*, execute the following command

# cd RKTools/linux/Linux_Pack_Firmware/rockdev/

# chmod 777 unpack.sh

# ./unpack.sh

# ls output/

# ls output/Image/

.. image:: media/image7.png
   :alt: aaaa_WPS图片
   :width: 5.51875in
   :height: 4.26944in

The unzip files will be generated in **output** directory.

.. image:: media/image8.png
   :alt: bbbb_WPS图片
   :width: 5.575in
   :height: 1.58819in

Unzip Firmware in windows.

*Step 1*, copy **update.img** to the windows directory
**AndroidTool_Release_v2.65/rockdev/**

*Step 2*, open Command Prompt then execute the following command in CMD

# RKImageMaker.exe -unpack ./update.img ./

.. image:: media/image9.png
   :width: 5.77014in
   :height: 2.25972in

After unzip the file to get boot.bin and firmware.img

.. image:: media/image10.png
   :width: 5.70833in
   :height: 3.3125in

*Step 3*, execute the following command in CMD to unzip **firmware.img**

# AFPTool.exe -unpack firmware.img ./

.. image:: media/image11.png
   :width: 5.77014in
   :height: 4.05347in

The unzip files will be generated in
**AndroidTool_Release_v2.65\rockdev\Image**

directory

.. image:: media/image12.png
   :width: 5.21875in
   :height: 3.27083in

.. _install-tools-1:
