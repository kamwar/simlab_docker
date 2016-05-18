# simlab_docker
Docker for simLAB

Run docker with usb support:
```
docker run  -it --privileged -v /dev/bus/usb:/dev/bus/usb kamwar/simlab
```

start simLAB for virtual SIM. No simtrace nor pc/sc reader is needed for editing:
```
#python mim/mim_soft.py
```
