# 软件优化题
TinyMaix卷王争霸赛

## 题目描述
典型神经网络模型最重要的算子是什么？是卷积！   
对卷积优化到极致是什么？是卷王！\狗头   

本题为软件优化题，就是希望各位卷王能压榨CPU的性能，使得[TinyMaix](https://github.com/sipeed/TinyMaix)更会**卷**积！

在以下题目中任选其一，评审的时候按照效果和完成度打分
1. 为TinyMaix增加mobilenetV2支持，即主要增加concat算子（涉及到模型转换脚本及tinymaix c代码，要求模型结构兼容）
2. 为TinyMaix增加目标检测例程，不局限于yolo，可以是自创架构，可以以人脸检测为例，要求速度>10fps @ 200M 等效主频
3. 以mobilenet v1 0.25 128x128为测试模型，以 对应架构O1 为基准，尝试优化执行速度，至少提高15%的执行速度
4. 为TinyMaix完善FP8支持，支持mobilenetV1运算出正确结果
5. 为TinyMaix增加一个新架构的加速，如xtensa的向量指令集，HiFi3/4/5 DSP指令集等，相对于原CPU执行速度至少减少25%推理时间
6. 其它任意值得优化的功能点

参赛者如果需要矽速的新硬件（RV64 C906 + RV32 E907 内核）进行架构相关的优化，可以发邮件到support@sipeed.com进行免费申请。   
注意申请硬件者需要先完成初级题以证明基础软件能力。  


## 提交内容
参赛者请在2022.10.31前提交结果。     
提交方式为，向TinyMaix仓库提交对应PR，包含 优化过程，测试结果，相关代码 等。
需要投递简历的可以同时将简历投递至 support@sipeed.com, 标题为 "[秋招挑战赛]软件优化组 姓名"  

## 评比方法
根据实际优化效果和优化的功能点意义进行评分。 

## 完赛记录
一等奖：lxowalle  为TinyMaix增加了ADD算子，mbnet/resnet支持   
二等奖：sunnycase 为TinyMaix优化了int8下的postprocess部分   
三等奖：nihui，为TinyMaix增加了X86 SSE2的架构优化   
        ganhailin 为TinyMaix增加了CSKYV2的架构优化   


