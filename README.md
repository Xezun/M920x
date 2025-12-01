OpenCore EFI for Lenovo ThinkCentre M920x-N000 10S4

# 硬件配置

| 类别 | 内容 | 备注 | 
|:-:|:-|:-|
| 型号 | 10S4 | 国行 | 
| 芯片组 | Q370 | Lenovo |
| 处理器 | Intel(R) Core(TM) i9-9900T CPU @ 2.10GHz | 正显版 |
| 核显 | Intel(R) UHD Graphics 630 | 支持 Metal 3 | 
| 有线网卡 | Intel(R) Ethernet Connection (7) I219-LM | - |
| 无线网卡 | BCM943602CS | 三天线，蓝牙4.2版 |
| 独显 | AMD Radeon RX 560 4G | 宝龙达 |
| 声卡 | Realtek High Definition Audio | ALC235 |
| SSD1 | WD_BLACK SN770 2TB | macOS |
| SSD2 | WD_BLACK SN770 2TB | Windows 10 |

# BIOS 设置

- 先恢复默认：Exit -> OS Optimized Defaults [Enabled] -> Load Optimal Defaults
- 关闭安全启动：Security -> Secure Boot -> Secure Boot -> Disabled
- 关闭 CFG 锁：可以在 OpenCore 引导页面，按空格选择 “Unlock CFG” 重启即可。

# 软件版本

| 类别 | 版本 | 备注 |
|:-:|:-:|:-:|
| OpenCore | 1.0.6 | - |
| macOS | 15.7.2 | - |
| OpenCore Legacy Patcher | 2.4.1 | - |

# 驱动情况

- 主板：Q370 主板，注入通用的 ACPI 即可
- 处理器：免驱原生支持
- 核显：使用 0x3E980003 仅作加速用
- 独显：免驱，开启硬件加速，降低功耗，待机功耗15W左右，待机温度55摄氏度左右
- 声卡：定制 layoutID = 20 双头耳机和单头2in1耳机都可用
- 网卡：白果拆机卡找回旧驱动，隔空、随航、接力支持且稳定
- 硬盘：西数对 macOS 兼容性较好

# 已知问题

- 不支持“私有Wi-Fi地址”，应该是由于网卡用的是旧版驱动。
- iStat Menus 传感器中，无法显示核显温度，主列表中，没有 GPU 表盘，详细列表中，“显卡”的温度，实际是独显的温度。
- Asphalt8 运行中，切换音频输出，DP音频-内置扬声器，会导致游戏声音异常，必须重启应用，应该是应用问题。
- 双头耳麦，正常使用，只有 Siri 应用“不能连接麦克风”；二合一耳麦，一切正常。

