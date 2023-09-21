# Mask-detect
对戴口罩的人脸检测模型，基于yolo进行改进，数据集手工标注补充，实现了一个识别照片中人们是否戴口罩的基础应用，同时还实现了一个简易的应用程序，方便观测
## 数据集介绍：

训练集（网上下载，选取2000张）

开源口罩佩戴检测数据集介绍:
https://zhuanlan.zhihu.com/p/103922982?utm_source=wechat_session
数据集百度云盘地址：
https://pan.baidu.com/share/init?surl=J8SwsZ9F5XFbUlHpEVQK3A

验证集（网上下载，选取300张，与训练集不同）

测试集（300张，自己人工标注）
![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/e7b2a393-aacf-4b84-9c27-7685b387e642)

## 训练过程：
在models文件夹下建立一个mask_yolov5s.yaml的模型配置文件，设定nc =2 表示这次训练的分类有两类：face和mask：

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/c6dc6943-0616-48fe-bcf0-d9b008529bba)

在mask_data.yaml设定训练集和验证集数据的地址路径（images和labels文件夹一一对应），设定好训练的类数（两类），类名（mask,face）

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/fe591778-b447-4805-8d1a-ff09b5018ccd)

## Loss变化:

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/532c39aa-6bb3-4517-ad3b-c1bad3f8f460)

## 测试结果：

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/9469eff7-b2dd-4cb4-8280-30ecaa7bc6d0)

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/50d594fc-1276-44ee-b5e0-688a526b63ad)

## 尝试加入qt界面：
在window.py里设定一个窗口主类，定义图片检测界面与UI:

点击“上传图片”：

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/deef4e08-9f9c-4e09-a4ee-53a5418df6d1)

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/081de275-bc31-48c3-892f-7edd84674dd9)

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/95dac27b-23ee-4ee7-8b16-53162ce9e61e)

以下结果：

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/8ba4ee5c-57f2-43ba-87b3-8b144d052481)

![image](https://github.com/yxyxnrh/Mask-detect/assets/82510221/93889d1b-4ff0-48d8-84a8-17fb562c6529)

