## 简介

sdk-bsp-stm32h750-realthread-artpi 是 RT-Thread 团队对 ART-Pi 开发板所作的支持包，也可作为用户开发使用的软件SDK，让用户可以更简单方便的开发自己的应用程序。

ART-Pi 是 RT-Thread 团队经过半年的精心准备，专门为嵌入式软件工程师、开源创客设计的一款极具扩展功能的 DIY 开源硬件.

<img src="documents/figures/board_large.png" alt="image-20201009181905422" style="zoom:50%;" />

## 目录结构

```
$ sdk-bsp-stm32h750-realthread-artpi 
├── README.md
├── RealThread_STMH750-ART-Pi.yaml
├── debug
├── documents
│   ├── RT-Thread 编程指南.pdf
│   ├── UM5001-RT-Thread ART-Pi 快速上手.md
│   ├── UM5002-RT-Thread ART-Pi 开发手册.md
│   ├── UM5003-RT-Thread ART-Pi BT_WIFI 模块固件下载手册.md
│   ├── UM5004-RT-Thread ART-Pi 代码贡献手册.md
│   ├── board
│   └── figures
├── libraries
│   ├── STM32H7xx_HAL
│   ├── drivers
│   ├── rt_ota_lib
│   └── wlan_wiced_lib
├── projects
│   ├── art_pi_blink_led
│   ├── art_pi_bootloader
│   ├── art_pi_factory
│   ├── art_pi_wifi
│   └── industry_io_gateway
├── rt-thread
└── tools
```

- RealThread_STMH750-ART-Pi.yaml
  描述 ART-Pi 的硬件信息
- debug
  QSPI FLASH 下载算法等
- documents
  图纸，文档，图片以及 datasheets等
-  libraries
  STM32H7固件库，通用外设驱动，rt_ota固件库，wlan固件库等
-  projects
  示例工程文件夹，包含出厂程序，网关程序等
-  rt-thread
  rt-thread 源码
-  tools
  wifi 固件，BT 固件，rbl 打包工具等
## 使用

sdk-bsp-stm32h750-realthread-artpi 支持 RT-Thread Studio 和 MDK 开发

### RT-Thread Studio 开发


1. 打开 RT-Thread Studio 的包管理器,安装 ART-PI SDK 资源包

  <img src="documents/figures/sdk_manager.png" alt="sdk_manager" style="zoom: 67%;" />


2. 安装完成后 选择基于 BSP 创建工程即可
    <img src="documents\figures\creat_project.png" alt="image-20200926143024666" style="zoom:50%;" />

### MDK 开发
1. 在 [ART-Pi SDK仓库](https://github.com/RT-Thread-Studio/sdk-bsp-stm32h750-realthread-artpi) 下载 SDK

2. 进入工程目录。如：sdk-bsp-stm32h750-realthread-artpi\projects\art_pi_blink_led

3. 以管理员权限打开 windows 命令行 ，执行 mklink 命令，分别为 `rt-thread` 及 `libraries` 文件创建符号链接

   ```
   E:\project\sdk-bsp-stm32h750-realthread-artpi\projects\art_pi_blink_led>mklink /D rt-thread ..\..\rt-thread
   为 rt-thread <<===>> ..\..\rt-thread 创建的符号链接
   
   E:\project\sdk-bsp-stm32h750-realthread-artpi\projects>mklink /D libraries ..\..\libraries
   为 libraries <<===>> ..\..\libraries 创建的符号链接
   
   E:\project\sdk-bsp-stm32h750-realthread-artpi\projects>
   ```
4. 使用 [ENV](https://club.rt-thread.org/ask/question/5699.html) 工具执行 scons --target=MDK5 即可
   

## ART-Pi 交流平台

ART-Pi  是一个开源创意硬件平台，期待有更多的小伙伴能一起发现更多的乐趣，在使用过程中若您有任何的想法和建议，建议您通过以下方式来联系到我们。

RT-Thread [社区论坛](https://club.rt-thread.org/)。

ART-Pi 官方交流 QQ 群(1016035998)。

![qq_group](documents/figures/qq_group.png)

## 贡献代码

如果您对 ART-Pi 感兴趣，并有一些好玩的项目愿意与大家分享，欢迎给我们贡献代码，您可以参考 [ART-Pi 代码贡献手册](https://github.com/RT-Thread-Studio/sdk-bsp-stm32h750-realthread-artpi/blob/master/documents/UM5004-RT-Thread%20ART-Pi%20%E4%BB%A3%E7%A0%81%E8%B4%A1%E7%8C%AE%E6%89%8B%E5%86%8C.md) 。

