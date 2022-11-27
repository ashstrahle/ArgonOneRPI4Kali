# ArgonOneRPI4Kali
## Argon One fan control for the Raspberry Pi 4 running Kali

This repo contains modified versions of the original `argon1.sh` install script, and `argononed.py` file adapted to run on Kali distro on RPI4. 

## Installation

  1. Execute:
  ```
  sudo ./argon1.sh
  ```

  2. Remove "console=" entries in `/boot/cmdline.txt` file

  3. Add the following to `/boot/config.txt`:
  ```
        dtparam=i2c_arm=on
    
        dtparam=i2s=on
    
        dtparam=spi=on
    
        enable_uart=1
  ```
  4. Execute: 
  ```
  sudo ./argonone-config.sh
  ```
You're done!