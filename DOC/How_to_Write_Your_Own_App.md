## APP固件编写指南

UARTCAN固件由xboot + app组成，xboot出厂刷入，固件不公开。app固件公开发布，
[下载链接](https://github.com/xjtuecho/UARTCAN/tree/master/HEX)

### ROM分配

MCU FLASH存储空间共64kB，起始地址0x08000000，长度0x10000

xboot占用开始的16kB，起始地址0x08000000，长度0x4000

app占用剩下的48kB，起始地址0x08004000,长度0xC000

### MDK额外设置：
1. Alt+F7打开项目属性，Target标签下，IROM1，Start填0x8004000,Size填0xC000
2. 修改中断向量表地址，system_stm32f10x.c中，将VECT_TAB_OFFSET宏内容改为0x4000
   #define VECT_TAB_OFFSET  0x4000
   也可以在app的main函数中调用以下API设定app中断向量表地址
   NVIC_SetVectorTable(NVIC_VectTab_FLASH, 0x4000)

### 注意事项
1. 可以使用ST-LINK刷入自己的代码，这样做会破坏xboot，xboot破坏以后，app也无法再写入，
   需要自费返厂写入xboot，才能继续使用官方固件。
2. app写入方法请参考UARTCAN用户手册

## UARTCAN主要硬件
- MCU：STM32F103C8T6
- CAN：TJA1050T
- LDO：XC6206

## MCU GPIO分配
- PA9： UART_TX
- PA10：UART_RX
- PA11：CANRX
- PA12：CANTX
- PB12：LED
- PC13：KEY

                                                   by ECHO Studio 2016.11.27

