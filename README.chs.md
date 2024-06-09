# FoxChanger
Voron 2.4/Trident换头模组，类Prusa XL。

无需任何自制、定制金属件，完全由现成的标准五金件组成，且完全不需要后期加工。


# 硬件概览
本模组由以下3个部分组成:
- 换头模组: 换头机构和工具头停泊坞
- 压电热床: 基于压电蜂鸣器的热床归零传感器
- 喷嘴校准器: 基于微动开关的多头喷嘴偏移校准工具

## 换头模组
目前该换头机构基于Dragon Burner设计。理论上可以用在其它工具头上，但是需要注意空间限制。另外因为空间原因无法安装传统的调平传感器和Voron Tap，所以我用了一个和拓竹的P1/X1类似的压电热床传感器。

__请注意：所有商品链接只是为了举例，与本人没有任何利益关系！__（当然我现在在用的零件也是从这些链接里买的就是了）

- 原版 [Dragon Burner](https://github.com/chirpy2605/voron/tree/main/V0/Dragon_Burner)
- 一个稍微修改过的[Sherpa Zero ECAS extruder](https://www.printables.com/model/495935-sherpa-zero-ecas)，加厚了一点用来兼容市面上常见的第三方BMG挤出机齿轮组，而不需要打磨轴
- [Fly SHT-36 V2 CAN工具板](https://mellow-3d.github.io/fly-sht36_v2_general.html)
- 一个稍微修改过的[KayosMaker's CANboard_Mounts](https://github.com/KayosMaker/CANboard_Mounts)，加了一个用来固定线缆导向钢丝的槽
- X滑车端
  - 6\*8\*3(内径\*外径\*高) [黄铜粉末冶金含油轴承](https://item.taobao.com/item.htm?id=696124179286&skuId=4938962921704) (x3)
  - 2\*25(直径\*长) [不锈钢圆柱定位销](https://detail.tmall.com/item.htm?id=599565830368) (x4)
  - 1\*8(直径\*长) [不锈钢圆柱定位销](https://detail.tmall.com/item.htm?id=599565830368) (x4)
  - 0.3\*3\*5(线径\*外径\*长) [304不锈钢压簧](https://detail.tmall.com/item.htm?id=684011040182&skuId=4894464993901) (x4)
  - M3\*8 SHCS 螺丝 (x4)
  - M3\*12 SHCS 螺丝 (x4)
  - M3 热熔螺母 (x4)
- 工具头端
  - 1\*2\*8\*1(短边\*长边\*宽\*厚) [1/2角铁3MM孔](https://detail.tmall.com/item.htm?id=609920972548&skuId=5025597343138) (x2)
  - 6\*4\*8\*M3 [锥头定位销](https://item.taobao.com/item.htm?id=629688584816&skuId=4652635966160) (x3)
  - M3\*2\*5(螺纹\*长\*外径) [内螺纹圆铜柱](https://detail.tmall.com/item.htm?id=718349103139&skuId=5012741965543) (x4)
  - M3\*5 [平端内六角紧定螺丝](https://detail.tmall.com/item.htm?id=669353260796&skuId=5037115490335) (x2)
  - 3\*30(直径\*长) [不锈钢圆柱定位销](https://detail.tmall.com/item.htm?id=599565830368) (x2)
  - 6\*3(直径\*厚) [圆形磁铁](https://item.taobao.com/item.htm?id=650582587437&skuId=4683250052175) (x2)
  - M3\*6 FSHC 螺丝 (x5)
  - M3 热熔螺母 (x4)
- 工具头停泊坞
  - 3\*50(直径\*长) [不锈钢圆柱定位销](https://detail.tmall.com/item.htm?id=599565830368) (x2)
  - 6\*3(直径\*厚) [圆形磁铁](https://item.taobao.com/item.htm?id=650582587437&skuId=4683250052175) (x2)
  - 0.4\*5\*15(厚\*宽\*长) [301弹簧钢带](https://item.taobao.com/item.htm?id=617939955067&skuId=4529325587657)
  - [来自TapChanger的喷嘴堵头模具](https://github.com/viesturz/tapchanger/tree/f6a354f5bf93b9d8721f022794a41ad3e51c5828/Dock/Jigs)
  - [耐高温硅密封胶](https://detail.tmall.com/item.htm?id=631534616231&skuId=4504220328741)
  - M3\*6 FSHC 螺丝 (x2)
  - M3\*12 SHCS 螺丝 (x1)
  - M5\*10 BHCS 螺丝 (x1)
  - M3 热熔螺母 (x2)
  - M3 T型滑块钢珠螺母 (x1)
  - M5 T型滑块钢珠螺母 (x1)

注意：由于两边伸出来的锁定滑块，龙门架的左侧XY轴连接器需要开槽，或者和我一样用CNC的版本。

## 压电热床传感器
由4片20mm压电蜂鸣器和震动传感器模块做的热床归零传感器。

- [压电震动传感器](https://detail.tmall.com/item.htm?id=652122497796)
- 20mm 压电蜂鸣片 (x4)
- 6\*8\*3(内径\*外径\*高) [黄铜粉末冶金含油轴承](https://item.taobao.com/item.htm?id=696124179286&skuId=4938962921704) (x8)
- 6\*15(直径\*长) [光轴](https://detail.tmall.com/item.htm?id=680516964370&skuId=4882059537337) (x8)
- M3\*8 SHCS 螺丝 (x4)
- M3\*10 SHCS 螺丝 (x8)
- M3 热熔螺母 (x8)
- M3 T型滑块钢珠螺母 (x4)

## 喷嘴校准器

- 6mm 钢珠 (或者像我在用的[氮化硅陶瓷滚珠](https://item.taobao.com/item.htm?id=689926834804&skuId=5083796203976)) (x1)
- [欧姆龙 D2FC-f-7N 微动](https://item.taobao.com/item.htm?id=574796579888&skuId=3774524789330)，或者任意相同尺寸的微动 (x1)
- 6\*8\*3(内径\*外径\*高) [黄铜粉末冶金含油轴承](https://item.taobao.com/item.htm?id=696124179286&skuId=4938962921704) (x1)
