## 项目描述

本项目是一个书法字体风格识别器，通过输入图片，识别出图片中的书法字体风格。项目包含以下文件：
- `0_setting.yaml`：配置文件，包含书法字体风格列表、图片调整大小的目标尺寸等设置。
- `1_Xy.py`：预处理图像、生成训练和测试数据集。
- `2_fit.py`：使用LazyClassifier评估多个分类模型，选择F1分数最高的模型并保存。
- `3_predict.py`：创建一个简单的图形用户界面，用户可以选择图像，程序会显示预测的书法字体风格。
- `util.py`：包含一些辅助功能，例如图像预处理、保存和加载文件等。

## 项目运行效果截图
<img src="https://github.com/LiuEhe/Calligraphy-Style-Recognition/blob/main/%E6%95%88%E6%9E%9C%E5%9B%BE/1.jpg" width="150" height="187.5"><img src="https://github.com/LiuEhe/Calligraphy-Style-Recognition/blob/main/%E6%95%88%E6%9E%9C%E5%9B%BE/2.jpg" width="150" height="187.5"><img src="https://github.com/LiuEhe/Calligraphy-Style-Recognition/blob/main/%E6%95%88%E6%9E%9C%E5%9B%BE/3.jpg" width="150" height="187.5"><img src="https://github.com/LiuEhe/Calligraphy-Style-Recognition/blob/main/%E6%95%88%E6%9E%9C%E5%9B%BE/4.jpg" width="150" height="187.5"><img src="https://github.com/LiuEhe/Calligraphy-Style-Recognition/blob/main/%E6%95%88%E6%9E%9C%E5%9B%BE/5.jpg" width="150" height="187.5">


## 功能

1. 预处理图像并生成训练和测试数据集。
2. 使用LazyClassifier评估多个分类模型，选择F1分数最高的模型并保存。
3. 创建一个简单的图形用户界面，用户可以选择图像，程序会显示预测的书法字体风格。


## 说明
 
  本项目采用传统的机器学习方法，预测准确率在0.7左右徘徊。仅作学习参考用。

## 依赖

- Python
- Scikit-learn
- LazyPredict
- OpenCV
- PIL
- Tkinter
- PyYAML

## 使用

1. 确保已安装所有依赖库。
2. 运行 `1_Xy.py` 生成训练和测试数据集。
3. 运行 `2_fit.py` 评估多个分类模型并保存最佳模型。
4. 运行 `3_predict.py` 启动图形用户界面，选择图像进行预测。

## 注意

- 请点击  [notion](https://liuehe.notion.site/79d73daae145425e9c513dee39b10d84) ,选择  `1.书法体识别`  下载数据。
- 由于序列化数据超过100MB，文件未上传，请运`1_Xy.py`得到，或者前往[notion](https://liuehe.notion.site/79d73daae145425e9c513dee39b10d84)下载。
- 请按照配置文件 `0_setting.yaml` 中的设置生成相关的文件夹，和放置文件位置。
- 请确保已安装所有依赖库。

#######################################################################
## V1.1

### Hog优化

1.使用特征提取方法，将数据特征提取，优化数据集，提升准去率和效率

2.请将1_Xy.py中的 
```
from util import ···
```        
修改为

```
from util_hog import ···
```    
重新运行代码，得到新数据，运行 `2_fit.py` 评估多个分类模型并保存最佳模型。

### VGG16优化

1.使用深度学习VGG16模型提取将数据特征，优化数据集，提升准去率和效率

2.请将1_Xy.py中的 
```
from util import ···
```        
修改为

```
from util_vgg16 import ···
```    
重新运行代码，得到新数据，运行 `2_fit.py` 评估多个分类模型并保存最佳模型。

## 结论

模型得到优化，准确率得到提升，效率提高.
