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
; [toolchange_count]
M104 T[next_extruder] S[new_filament_temp] ; preheating the next toolhead

M204 S9000
{if toolchange_count > 1 && (z_hop_types[current_extruder] == 0 || z_hop_types[current_extruder] == 3)}
G17
G2 Z{z_after_toolchange + 0.4} I0.86 J0.86 P1 F10000 ; spiral lift a little from second lift
{endif}

T[next_extruder] X=[x_after_toolchange] Y=[y_after_toolchange] Z=[z_after_toolchange]

G1 X[x_after_toolchange] Y[y_after_toolchange] Z[z_after_toolchange] F12000 ; make gcode preview happy
```
- Start Gcode:
```
M104 S0
M140 S0
PRINT_START EXTRUDER=[nozzle_temperature_initial_layer] BED=[bed_temperature_initial_layer_single] CHAMBER=[chamber_temperature] MESH_MIN={adaptive_bed_mesh_min[0]},{adaptive_bed_mesh_min[1]} MESH_MAX={adaptive_bed_mesh_max[0]},{adaptive_bed_mesh_max[1]} MESH_ALGO=[bed_mesh_algo] MESH_PROB_COUNT={bed_mesh_probe_count[0]},{bed_mesh_probe_count[1]} TOOL=[initial_extruder]
```

### Filament settings
- Delay after unloading: 2
