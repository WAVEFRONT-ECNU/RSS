# 模块划分与分工

## 前处理

### WaveSlicer (MQC)
+ 用以按语句切分原始音频并输出(已实现)
+ 输出自动编号保存至缓存目录并输出内容日志
+ 输入和输出以接口实现，预留扩展能力
+ TODO 实时异步分析

### VoiceEnhancer (MZS)
+ 降噪
+ 语音信号增强
+ 电平标准化
+ 输入输出均为音频信号(wav进出就可以了)

## 机器学习部分 (BOTH)

### FeatureExtractor (*Important Module*)
+ 对前流程输出的语音进行信号处理和特征提取
+ 提取的型号为输入TensorFlow做准备

### TensorFlow
+ 训练模型
+ 目前计划每次输入两段特征进行相似度判断
+ 具体实现方式待进一步研究决定

## 后处理及最终文本输出

### Speech Recognition
+ 使用现有API实现
+ 将语音逐人拼接提交
+ 实现方式参考讯飞、阿里等主流语音识别平台SDK文档实现



# 开发时间表
+ 前处理部分二月上旬前完成
+ 机器学习部分二月底前完成（这个需要加紧完成）
+ 后处理，demo等在三月中旬前完成
+ 三月中旬亦需完成项目总结介绍、PPT等任务