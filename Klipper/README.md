[中文版点我](./README.chs.md)

# Klipper setup

The config here is just the setup I'm using.

## Installing

- Install [toolchanger extension](https://github.com/viesturz/klipper-toolchanger/)
- Use the config as a guide for your own config

## Orca Slicer config

### Printer settings
- Cooling tube length: 15
- Cooling tube position: 35
- Filament parking position: 35
- Enable filament ramming: false
- Change filament G-code:
```
M104 T[next_extruder] S[new_filament_temp]
T[next_extruder]
```
- Start Gcode:
```
M104 S0
M140 S0
PRINT_START EXTRUDER=[nozzle_temperature_initial_layer] BED=[bed_temperature_initial_layer_single] CHAMBER=[chamber_temperature] MESH_MIN={adaptive_bed_mesh_min[0]},{adaptive_bed_mesh_min[1]} MESH_MAX={adaptive_bed_mesh_max[0]},{adaptive_bed_mesh_max[1]} MESH_ALGO=[bed_mesh_algo] MESH_PROB_COUNT={bed_mesh_probe_count[0]},{bed_mesh_probe_count[1]} TOOL=[initial_extruder]
```

### Filament settings
- Delay after unloading: 2
