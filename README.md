# ChosunTruck
Euro Truck Simulator 2 autonomous driving solution

## Overview
In recent years, autonomous driving technology has become a big issue and we have studied the technology related to this.
It was developed in a simulator environment called Euro Truck Simulator 2 to study with real vehicles.
Because this simulator provides an environment similar to a real road, we determined it to be a good test environment.

```
g++ -o auto_drive main2.cpp IPM.cpp lineinder.cpp uinput.c `pkg-config opencv --cflags --libs` -std=c++11 -lX11 -Wall -fopenmp -O3 -march=native
```
