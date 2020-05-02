# ArgonOneRPI4Kali
## Argon One fan control for the Raspberry Pi 4 running Kali

This is a modified version of the original `argononed.py` file adapted to run on Kali distro on RPI4. The original failed as it depended upon an old version of python, and Kali has no `vcgencmd` package to track CPU temperature.

This version uses python3 and removes the dependency on `vcgencmd`. 

`argonone-config` updated with an option to return settings to default.


To get this working, be sure to:

  * remove "console=" entries in /boot/cmdline.txt file

  * add the following to /boot/config.txt:
  
    dtparam=i2c_arm=on
    
    dtparam=i2s=on
    
    dtparam=spi=on
    
    enable_uart=1
  

 
