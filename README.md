![logo](https://github.com/kamwar/simLAB/wiki/res/images/simLAB-logo.png)simLAB
=================
Docker for **simLAB** - SIM UICC card editor and SIM/SAT simulator.
Docker includes pcsc support.

Run docker with usb support
  ```
docker run  -it --privileged -v /dev/bus/usb:/dev/bus/usb kamwar/simlab
  ```

To start simLAB with virtual SIM use the following command in docker shell
  ```
#python mim/mim_soft.py
  ```
  No additional hardware is needed for virtual SIM editing.

To start simLAB with live SIM, connect any PC/SC card reader and use mim_live
  ```
#python mim/mim_live.py
  ```

>Note: For MitM functionality, simtrace must be connected.

Want to learn more? Detailed information can be found in the [simLAB wiki](https://github.com/kamwar/simLAB/wiki)
