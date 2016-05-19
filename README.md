# simlab_docker
Docker for simLAB - SIM UICC card editor and SIM/SAT simulator. Docker includes pcsc support.

Run docker with usb support:
```
docker run  -it --privileged -v /dev/bus/usb:/dev/bus/usb kamwar/simlab
```

Start simLAB for virtual SIM. No simtrace nor pc/sc reader is needed for SIM editing.
```
#python mim/mim_soft.py
```
