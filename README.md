## 概述
UARTCAN是一款CAN接口调试工具。可以使CAN接口调试与串口调试一样方便。配合低成本的
USB转TTL数据线，可以将UARTCAN转化成一款USBCAN设备。

UARTCAN同样提供USB接口版本，USB接口版本与TTL接口版本操作完全相同。

上位机软件[超级终端](HOST/HyperTerminal.7z)，XP系统自带，Win7及以上系统点击下载。

### TERM模式
UARTCAN具备独特的TERM工作模式，借助超级终端等终端模拟软件，可以在PC上轻松进行
CAN接口调试。用户只需要学习少数几个命令，便可以轻松上手。

### PKT工作模式
UARTCAN同时具备PKT工作模式，该工作模式下，所有通讯数据按照16字节定长数据包来组织，
CRC数据校验保证了数据完整性，特别适合用户编程处理。该模式下用户还可以使用PC上
常见的CANTest软件来进行调试。

### BRIDGE工作模式
UARTCAN具备BRIDGE工作模式，该模式下使用简单的封包结构，便于用户编程处理。

## 主要特性
- 32位ARM处理器72M主频处理能力强大
- 独特的TERM工作模式无需专用上位机软件
- 精心设计的PKT工作模式便于用户二次开发
- CRC校验技术避免数据出错
- 兼容周立功CANTest软件
- BRIDGE模式支持透明转发
- 同时提供TTL版本和USB版本满足不同需求
- 体积小巧便携使用方便
- 支持固件升级
- 成本低廉

## 用户界面

- 短按按键LED指示工作模式
  1. 无闪烁：BRIDGE
  2. 闪一次：PKT
  3. 闪两次：TERM
- 长按按键切换工作模式

## 购买链接
- [USB版本](https://item.taobao.com/item.htm?spm=a1z10.1-c.w4004-9102396040.29.7db0abad4tIeu4&id=531094225355)
- [TTL版本](https://item.taobao.com/item.htm?spm=a1z10.5-c.w4002-9102396035.21.602f430flFQ0SU&id=531124016757)