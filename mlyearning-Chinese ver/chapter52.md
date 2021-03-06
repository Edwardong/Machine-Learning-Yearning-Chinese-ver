## 52. 直接学习复杂的输出

图像分类算法输入图像 $x$，输出一个表示对象类别的整数。那么，算法可以输出描述图像的句子吗?

比如：

![32](https://raw.githubusercontent.com/AlbertHG/Machine-Learning-Yearning-Chinese-ver/master/md_images/32.png)

传统的监督学习算法学习函数 $h$：$X\rightarrow Y$，其中输出 $y$ 通常是整数或者实数。例如：


应用场景 | X | Y
---------|----------|---------
 垃圾邮件分类 | 邮件 | 垃圾邮件/不是垃圾邮件（0/1）
 图像识别 | 图片 | 整数标签
 房子价格预测 | 房子的特征 | 房子价格
 产品推荐 | 商品或者用户特征| 购买的机会


端到端的深度学习中最令人兴奋的发展之一是它可以让我们直接学习到比数字复杂得多的 $y$。在上面的图像字幕示例中，可以让神经网络输入图像 $x$ 并直接输出标题 $y$。

更多的例子：

应用场景 | X | Y | 例子引用
---------|----------|---------
 图像字幕 | 图片 | 文字 | Mao et al., 2014
 机器翻译 | 英文文本 | 法文文本 | Suskever et al., 2014  
 问答系统 | 问题文本 | 答案文本 | Bordes et al., 2015
 语音识别 | 音频 | 转录文本 | Hannun et al., 2015  
 文本转语音 | 文本特征 | 音频 | van der Oord et al., 2016
 
这是深度学习中的一个趋势：当你有正确的(输入、输出)标记对时，你就可以尝试去使用端到端学习技术，即使输出是一个句子、一个图像、音频或其他比单个数字更丰富的输出。