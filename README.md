# ud18

A simple python3 script to dump the measured data of the Atorch ud18 USB meter
to the screen or optionally to a log file for further processing.

## Installation

Mainly required is the python3 serial library

``apt install python3 python3-serial``

## Usage

The connection to the UD18 is made over bluetooth. So you need to connect to the
UD18 over bluetooth first.

When the connection is made, a serial device is created, for example:

``/dev/rfcomm0``

To start the script and display data run:

``./ud18 -d /dev/rfcomm0``

Output should look like:

```
Voltage : 5.11V
Current : 0.22A
Power   : 1.1242W
Capacity: 83651mAh
Energy  : 524.79Wh
USB d-  : 0.06
USB d+  : 0.09
Time    : 96:21:57

Voltage : 5.11V
Current : 0.22A
Power   : 1.1242W
Capacity: 83651mAh
Energy  : 524.79Wh
USB d-  : 0.06
USB d+  : 0.08
Time    : 96:21:58
```

Logging to a file in csv format is also possible:

``./ud18 -d /dev/rfcomm -f logfile.csv``
