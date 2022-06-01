# 人工智慧
- [Hung-yi Lee](https://www.youtube.com/c/HungyiLeeNTU)

# 人工智慧的應用
- 智慧金融
  - [人工智慧與金融應用](https://www.ibm.com/blogs/think/tw-zh/2019/09/27/aifinance/) 
- 智慧城市
- 智慧醫療
- 智慧農業
- 智慧工業
- 資訊安全 

## CNN的應用
- ImageNet
  - [ImageNet Dataset | Papers With Code](https://paperswithcode.com/dataset/imagenet) 
  - [Image Classification on ImageNet](https://paperswithcode.com/sota/image-classification-on-imagenet)
## RNN的應用
## GAN的應用

- [【機器學習2021】生成式對抗網路 (Generative Adversarial Network, GAN) (一) – 基本概念介紹](https://www.youtube.com/watch?v=4OWp0wDu6Xw)
- [DEEPfake]()
  - [Deepfake技術親手實驗　感受深度造假影片威力](https://www.netadmin.com.tw/netadmin/zh-tw/technology/DCF13461B4D24363A7BBE6CE61A19788)
  - [Deep Learning for Deepfakes Creation and Detection: A Survey](https://arxiv.org/abs/1909.11573)
  - [Face2face ](https://towardsdatascience.com/face2face-a-pix2pix-demo-that-mimics-the-facial-expression-of-the-german-chancellor-b6771d65bf66)
## Deep reinforcement Learning的應用
- [Deep Reinforcement Learning: Neural Networks for Learning Control Laws](https://www.youtube.com/watch?v=IUiKAD6cuTA)
- [A friendly introduction to deep reinforcement learning, Q-networks and policy gradients](https://www.youtube.com/watch?v=SgC6AZss478)
- [MIT 6.S091: Introduction to Deep Reinforcement Learning (Deep RL)](https://www.youtube.com/watch?v=zR11FLZ-O9M)
- [Process manufacturing optimization using AI with the Project Bonsai reinforcement learning toolchain](https://www.youtube.com/watch?v=Wh9ekBhU86U)

# 人工智慧開發環境: Google Colab   Tensorflow PyTorch [YOUYUBE](https://youtu.be/ObyCftNJ9Fw)

## Tensorflow 
- [(Hands-on Machine Learning with Scikit-Learn, Keras, and TensorFlow, 2/e)]()
  - [精通機器學習｜使用 Scikit-Learn , Keras 與 TensorFlow, 2/e  Aurélien Géron 著 賴屹民 譯](https://www.tenlong.com.tw/products/9789865024345?list_name=srh)
  - [github](https://github.com/ageron/handson-ml2)
- [Tensorflow ](https://www.tensorflow.org/)
  - [TensorFlow tutorials](https://www.tensorflow.org/tutorials) 
    - [Convolutional Neural Network (CNN)](https://www.tensorflow.org/tutorials/images/cnn) 

```python
import tensorflow as tf

x = tf.constant([[1., 2., 3.],
                 [4., 5., 6.]])

print(x)
print(x.shape)
print(x.dtype)
```
## PyTorch
- [教科書Deep Learning with Pytorch](https://www.manning.com/books/deep-learning-with-pytorch)
  - [核心開發者親授！PyTorch 深度學習攻略](https://www.tenlong.com.tw/products/9789863126737?list_name=srh)
  - Eli Stevens、Luca Antiga、Thomas Viehmann 著 黃駿 , 施威銘研究室 監修
  - [github](https://github.com/deep-learning-with-pytorch/dlwpt-code)
- [PYTORCH TUTORIALS](https://pytorch.org/tutorials/index.html)
- [PYTORCH - YOUTUBE SERIES](https://pytorch.org/tutorials/beginner/introyt.html)
- [PyTorch Examples](https://github.com/pytorch/examples)
```PYTHON
import torch
x = torch.rand(5, 3)
print(x)
```
### [LEARN THE BASICS](https://pytorch.org/tutorials/beginner/basics/intro.html)
- [TENSORS](https://pytorch.org/tutorials/beginner/basics/tensorqs_tutorial.html)
```
import torch
import numpy as np

data = [[1, 2],[3, 4]]
x_data = torch.tensor(data)
x_data

shape = (2,3,)
rand_tensor = torch.rand(shape)
ones_tensor = torch.ones(shape)
zeros_tensor = torch.zeros(shape)

print(f"Random Tensor: \n {rand_tensor} \n")
print(f"Ones Tensor: \n {ones_tensor} \n")
print(f"Zeros Tensor: \n {zeros_tensor}")
```
# 大學部上課影片

### 20220518
- [AI 第一堂課](https://youtu.be/rLx7wMWAH7g)
- [What can AI do today? ](https://youtu.be/HxfMbrolH4g)

### 20220525
- [神經網路與邏輯閘]
### 20220601
- [具有學習能力的神經網路1.誤差函數]()
