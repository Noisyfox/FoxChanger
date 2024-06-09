[English](./README.md)

# Klipper配置

这些只是我在用的配置，经供参考。

## 安装

- 安装 [klipper toolchanger 插件](https://github.com/viesturz/klipper-toolchanger/)
- 参照我的配置来设置你的打印机

## Orca Slicer配置

### 打印机设置
- 喉管长度: 15
- 喉管位置: 35
- 耗材停靠位置: 35
- 启用耗材尖端成型: false
- 耗材丝更换 G-code:
```
M104 T[next_extruder] S[new_filament_temp]
T[next_extruder]
```
- 打印机起始 Gcode:
```
M104 S0
M140 S0
PRINT_START EXTRUDER=[nozzle_temperature_initial_layer] BED=[bed_temperature_initial_layer_single] CHAMBER=[chamber_temperature] MESH_MIN={adaptive_bed_mesh_min[0]},{adaptive_bed_mesh_min[1]} MESH_MAX={adaptive_bed_mesh_max[0]},{adaptive_bed_mesh_max[1]} MESH_ALGO=[bed_mesh_algo] MESH_PROB_COUNT={bed_mesh_probe_count[0]},{bed_mesh_probe_count[1]} TOOL=[initial_extruder]
```

### 耗材丝设置
- 卸载后延迟: 2
