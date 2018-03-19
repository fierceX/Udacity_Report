# 项目说明
## 运行环境及库
- python 3.6
- Mxnet 1.1.0 (GPU版)
- numpy 1.13.1
- matplotlib 2.1.2
- multicoretsne
### Mxnet安装
具体安装教程参见Mxnet官网和  [Mxnet安装教程](http://zh.gluon.ai/chapter_preface/install.html)  
使用pip安装  
```
pip install mxnet
```
默认安装的是CPU版，若需要安装GPU版则
```
pip install mxnet-cu80
```
安装CUDA8版本
```
pip install mxnet-cu90
```
安装CUDA9版本  
### multicoretsne 安装  
参见multicoretsne项目[github](https://github.com/DmitryUlyanov/Multicore-TSNE)页面  
## 项目文件说明
- CNN_Text_Classification.ipynb  
    TextCNN模型训练脚本
- Data_utils.ipynb  
    数据预处理脚本
- test.ipynb  
    测试集测试脚本
- Data_Visualization
    数据可视化脚本
- data_vocab  
    数据词典文件
- label_vocab  
    分类标签词典
- params/0.8529723991507431_params  
    模型最终参数文件
- 20news-bydate.tar.gz  
    原始训练数据压缩文件

**注意**: 
-   运行训练脚本会覆盖生成新的词典文件，新的词典文件可能和保存的模型参数文件不对应，所以会影响测试脚本效果，若要重新训练，可以载入已经生成好的词典文件，也可以全部重新训练。  
-   训练过程中，会需要下载预训练词向量文件，需要一些时间，如果在国内下载速度过慢的话，可以设置环境变量`MXNET_GLUON_REPO`为`https://apache-mxnet.s3.cn-north-1.amazonaws.com.cn/`来加速下载。