# simlab_docker
Docker for simLAB - SIM UICC card editor and SIM/SAT simulator.
Docker includes pcsc support.

Run docker with usb support:
```
docker run  -it --privileged -v /dev/bus/usb:/dev/bus/usb kamwar/simlab
```

To start simLAB with virtual SIM just run the following command in docker shell
```
#python mim/mim_soft.py
```
No additional hardware is needed for virtual SIM editing.

To start simLAB with live SIM, connect any PC/SC card reader.
```
#python mim/mim_live.py
```

For MitM functionality, simtrace must be connected.
