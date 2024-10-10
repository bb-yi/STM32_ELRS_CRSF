# STM32 ELRS CRS-F Protocol Receiver

## 项目介绍

使用 STM32 接收 ELRS 接收机 (CRSF 协议) 的数据，采用串口空闲中断接收方式。

## 使用说明

1. **文件添加**  
   将 `user` 文件夹下的 `elrs.c` 和 `elrs.h` 文件添加到你的工程中。

2. **串口配置**

    - 在 STM32CubeMX 中打开串口 (示例工程中使用的是串口 2)。
    - 配置波特率为 420000。
    - 启用 DMA 通道。
    - 生成代码。

3. **函数构成**

    - 将 `ELRS_UARTE_RxCallback()` 函数添加到串口空闲中断的回调函数中。
    - 在主函数开头调用 `ELRS_Init()`。

4. **数据访问**  
   可以调用 `elrs_data` 结构体中的各种数据，详细信息请查看 `elrs.h` 文件。

## 参考视频

[观看视频](https://www.bilibili.com/video/BV1c82kYjEmX)
