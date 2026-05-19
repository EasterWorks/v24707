Modify your OrcaSlicer MACHINE START Gcode to the following:

```M104 S0 ; Stops OrcaSlicer from sending temp waits separately```
```M140 S0```
```PRINT_START EXTRUDER=[first_layer_temperature] BED=[first_layer_bed_temperature]```


Modify your OrcaSlicer MACHINE END Gcode to the following:

```PRINT_END```

Please continue to the next text file, "Pre-Flight Checks".
