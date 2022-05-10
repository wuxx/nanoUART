# nanoUART 用户手册
* [产品介绍](#产品介绍) 
* [产品特性](#产品特性) 
* [引脚定义](#引脚定义)
* [使用说明](#使用说明)
    * [接线](#接线)
	* [IO电平切换](#IO电平切换)
	* [串口工具使用](#串口工具使用)
* [FAQ](#faq)
	
# 产品介绍
nanoUART是MuseLab推出的TYPE-C接口的串口工具，尺寸2.2cmx1.7cm，最高可支持6Mbps波特率通信，支持流控，支持多种电平IO，包括5V/3.3V/2.5V/1.8V以及用户自定义电平VREF输入。

<div align=center>
<img src="https://github.com/wuxx/nanoUART/blob/master/doc/nanoUART-top.jpg" width = "500" alt="" align=center />
<img src="https://github.com/wuxx/nanoUART/blob/master/doc/nanoUART-bottom.jpg" width = "530" alt="" align=center />
</div>

# 产品特性
- 硬件全双工，最高支持6Mbps波特率通信
- 支持RTS/CTS硬件流控、支持常用的MODEM通信信号
- 支持多种IO电平
- TYPE-C接口，尺寸小巧，方便使用

## 引脚定义
正面|背面 |
----|---- |
GND | RI  | 
TX  | CTS |
RX  | DSR |
DTR | DCD |
RTS | VREF|
3V3 | 5V  |

说明1：提供5V/3.3V，可对外供电，5V供电电流最高500mA，3.3V输出电流最高300mA
说明2：VREF为外部参考引脚电平输入


# 使用说明

## 接线
串口使用方法：使用上和其他串口工具（PL2303, CH340, CP2102等）一致，信号为TX，RX。
串口接线说明：行业的默认规则是标记丝印是在哪块板子上，就表明是哪块板子TX或者RX。例如串口工具上标记的TX，表明是工具 "自己" TX，即串口工具的串口发送，应该接目标板上的丝印为RX的串口引脚（即目标板"自己"RX），即目标板接收。串口工具软件推荐使用sscom或者putty。
nanoUART|MCU |
----|----|
GND | GND | 
TX | RX  |
RX | TX  |

若发现串口无法正常使用，可以尝试以下方法定位排查：
自发自收测试：短接串口的TX RX，打开串口工具，随意发送一些数据，看是否有回显，若有回显，则说明串口工具本身硬件收发均没问题


## IO电平切换
可通过短接串口工具背部的短路桥来选择IO参考电平，默认内部提供四种IO电平，5V/3.3V/2.5V/1.8V，也可短路VREF，自行通过外部VREF引脚提供参考电平。


## 串口工具使用
推荐使用sscom或者putty连接串口使用。  
![sscom](https://github.com/wuxx/nanoUART/blob/master/doc/sscom.png)

# FAQ
