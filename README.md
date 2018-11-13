# ML-Class-Assignment
The assignment of machine learning course for post-graduates at BUAA EE, 2018.

**注：此稿为草稿，题目可能会有变动，最终内容将于11月14日确定。**

## 任务描述
本学期的机器学习大作业包括三个题目：手写数字识别、医学图像检测以及图像显著性检测，任选其一完成即可。由于难度不同，每题设置了不同的最高分：

1、手写数字识别：机器学习经典问题，在灰度图像中识别10类手写数字，属于分类问题。最高分90。

2、医学图像检测：利用彩色眼底图像判断是否患病，属于分类问题。最高分95。

3、图像显著性预测：在彩色图像中，预测人眼容易关注的区域（输出显著性图），属于回归问题。最高分100。

## 作业内容

1、在训练集上训练机器学习模型。

2、在测试集上测试模型的性能。

3、提交实验报告与模型代码。

## 题目一：手写数字识别

### 数据文件
* 训练数据集（10类，共6万个数字）：以bmp格式存储在**1-Digit-TrainSet.zip**。
* 测试数据集（10类，共1万个数字）：以bmp格式存储在**1-Digit-TestSet.zip**。

每个数据集中，每个文件名的第一个数字代表它的真实分类（label）。

![](/1-Digit-Example.png)

### 性能指标
测试集上的分类准确度。

## 题目二：医学图像检测

### 数据文件
* 训练数据集（2类，共1639幅图像）：以jpg格式存储在**2-MedImage-TrainSet.zip**。
* 测试数据集（2类，共250幅图像）：以jpg格式存储在**2-MedImage-TestSet.zip**。

![](/2-MedImage-Example.png)

每个数据集中，以disease开头的文件为患病图像，以normal开头的文件为无病图像。

### 性能指标
最基本的指标是测试集上的分类准确度。考虑到患病与无病样本数量不均等，且两种误判（无病判断成患病、患病判断成无病）带来的风险不同，因此为了全面反映分类器性能，还可以给出精确率、召回率或其他指标。

## 题目三：图像显著性预测

### 数据文件
* 训练数据集（共1600幅待检测图像及1600幅对应的显著图）：以jpg格式存储在**3-Saliency-TrainSet.zip**中。
* 测试数据集（共400幅待检测图像及400幅对应的显著图）：以jpg格式存储在**3-Saliency-TestSet.zip**中。

每个数据集中，待检测图像为人眼直接观察的彩色图像，保存在**Stimuli**文件夹；对应的显著图为相同尺寸的灰度图像，颜色越亮的区域代表显著性越强，保存在**FIXATIONMAPS**文件夹。考虑到图像内容可能对结果产生影响，每个数据集都包括20种不同类型的图像，存放在20个文件夹中（如**Action**，**Affective**，**Art**……），因此分析结果时，既可以给出总体性能，又可以对按类型进行分析。

![](/3-Saliency-Example.png)

### 性能指标

相关系数（CC）、归一化扫视路径显著性（normalized scanpath saliency，NSS），或其他衡量显著性图像相似程度的指标等。

## 数据获取

百度云盘下载：https://pan.baidu.com/s/1mOCFxATcCkHGbK8Vdtv5yQ

DropBox下载：https://www.dropbox.com/sh/i79cbllw6763zxg/AAA3-jPaRlYHMvsMyRbtRRmaa?dl=0

两种途径下载后文件相同，任选其一即可。

## 报告格式
作业报告格式包含：  
1、问题描述  
2、实验模型原理和概述  
3、实验模型结构和参数  
4、实验结果分析（包含训练集和测试集里的测试结果）,要求列举出一些**失败案例**并分析。  
5、总结  

## 作业提交
将模型代码、实验报告、测试结果打包，命名格式：学号_姓名_选题，第15周周二（12月18日）前发送至邮箱 tianyili@buaa.edu.cn。
