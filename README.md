OpenCore EFI for Lenovo ThinkCentre M920x-N000

# 硬件配置

| 类别 | 内容 | 备注 | 
|:-:|:-|:-|
| 型号 | 10S4 | 国行 | 
| 芯片组 | Q370 | Lenovo |
| 处理器 | Intel(R) Core(TM) i9-9900T CPU @ 2.10GHz | 正显版 |
| 核显 | Intel UHD Graphics 630 | 支持 Metal 3 | 
| 无线 | BCM943602CS | 三天线，蓝牙4.2版 |
| 独显 | AMD Radeon RX 560 4G | 宝龙达 |
| 声卡 | Realtek High Definition Audio | ALC235 |
| SSD1 | WD_BLACK SN770 2TB | macOS |
| SSD2 | WD_BLACK SN770 2TB | Windows 10 |

# BIOS 设置

关闭安全启动即可

# 软件版本

| 类别 | 版本 | 备注 |
|:-:|:-:|:-:|
| OpenCore | 1.0.5 |  |
| macOS | 15.7.1 |  |
| OpenCore Legacy Patcher | 2.4.1 |  |
|  |  |  |

# 驱动情况

- 主板：已解锁 CFG_LOCK
- 处理器：免驱原生支持
- 核显：使用 0x3E980003 仅作加速用
- 独显：免驱，开启硬件加速，降低功耗，待机温度在55摄氏度以下
- 声卡：定制 layoutID = 20 双头耳机和单头2in1耳机都可用
- 网卡：白果拆机卡找回旧驱动，隔空、随航、接力支持且稳定
- 硬盘：西数对 macOS 兼容性较好

