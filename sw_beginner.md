# 软件初级题
TinyMaix初体验

## 题目描述
你是否想象过在自己的常用单片机上运行神经网络模型来解决常规算法难以解决的复杂问题？   
在MCU上运行神经网络模型，是TinyML面临的典型挑战。    
Sipeed针对此类典型问题场景，推出了 [TinyMaix](https://github.com/sipeed/TinyMaix) 超轻量级TinyML推理框架，低至3KB flash，1KB sram占用，在经典Arduino ATmega328上都能运行MNIST手写数字识别模型！  

本题是软件组初级参与题，主要目的是让大家体验TinyMaix移植的便利性，参赛者仅需在自己熟悉的单片机平台上移植TinyMaix即可，  
具体要求如下：
1. 为TinyMaix增加任意一款不在当前[已测试列表](https://github.com/sipeed/TinyMaix/blob/main/benchmark.md)中的芯片的支持
2. 同一系列芯片算一种芯片，比如已移植STM32F411，那么STM32F401认为是同款芯片；STM32H7和STM32F7算不同系列芯片
3. 允许非单片机类的移植，比如A7，A53等内核的芯片，但此类芯片同厂家的同内核视为一种，即有人移植了A7的V3s后，再移植H3是无效的
4. 需测试芯片配置范围内可运行的模型的benchmark，从低到高为：
   1. mnist   2KB Flash,  2KB RAM    //初级手写数字识别(28x28x1)
   2. cifar  89KB Flash, 11KB RAM    //10分类小图(32x32x3)识别
   3. vww   227KB Flash, 54KB RAM    //2分类图像识别，mobilenet v1 0.25, 96x96x3 input
   4. mbnet 485KB Flash, 96KB RAM    //1000分类图像识别，mobilenet v1 0.25,128x128x3 input
5. 对于可运行vww例程以上配置的单片机，推荐使用[MaixHub](https://www.maixhub.com/)在线模型训练平台自助训练模型体验

## 提交内容
参赛者请在2022.10.31前提交结果。   
提交方式为，向TinyMaix仓库提交对应PR。提交格式参见 doc/porting/port_STM32F411.md   
需要投递简历的可以同时将简历投递至 support@sipeed.com, 标题为 "[秋季挑战赛]软件初级组 姓名"  

## 评比方法
满足基础要求者即为完赛。  

## 完赛记录
完赛者记录会在比赛期间及时更新到本节


