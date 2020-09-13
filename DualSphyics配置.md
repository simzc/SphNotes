# 1 Markdown+坚果云笔记
## 1.1 坚果云笔记安装
下载地址：https://www.jianguoyun.com/
## 1.2 Markdown配置
必备软件：VS code
插件推荐： Markdown、Markdown AllInOne、Markdown Toc、Markdown Preview Enhanced

# 2 DualSphysics配置
## 2.1 配置背景
### 2.1.1 硬件配置
Ryzen 9 3950x + RTX 2080 Ti
### 2.1.2 软件配置
Win10专业版 + VS2019 + CUDA11.0
由于DualSPHysics_v5.0 IDE最高版本为vs2015，需在vs2019上安装v140（vs2015）编译工具
## 2.2 常见库配置
为后续使用，配置VTK库
[VS2019+cmake(3.15.3)+VTK(8.2.0)+配置完成后的demo演示
](https://blog.csdn.net/Pure_vv/article/details/102058609)

较低配置安装教程
[win10安装cuda9.0，cudann](https://blog.csdn.net/u013925378/article/details/91046639)
## 2.2 常见报错内容
```
nvcc fatal : Unsupported gpu architecture ‘compute_30‘ error MSB3721
```
原因：计算架构问题
[不同版本CUDA中nvcc编译器对计算架构支持不同；](http://arnon.dk/matching-sm-architectures-arch-and-gencode-for-various-nvidia-cards/)

对于不同架构的N卡，编译不同目标计算架构
https://www.pianshen.com/article/57121770090/
在CUDA11.0上会出警告旧版本计算架构会被淘汰

```
Error	LNK1104	cannot open file 'LibJVtkLib_x64_v142_Debug.lib'
```
原因：源码不提供'LibJVtkLib_x64_v142_Debug.lib'
解决方案：需安装v140编译工具

```

```
