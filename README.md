# ocr_recognition
验证码识别,该模型是基于xlvector编写的一段识别数字的代码上进行加工,验证码内容包含了大小字母以及数字,采用lstm+warp-ctc+cnn达到不分割字符而识别验证码内容～
#几点说明：
  1. 该模型是基于mxnet框架训练而来，基于环境为ubuntu 14，支持GPU和CPU两种模式，如果要运行该代码，需要具备如下软件支持：
     1. opencv
     2. openblas
     3. torch
     4. cmake
     5. mxnet
     6. warp-ctc
     7. python2.7
     8. gcc(如果版本太低，要么去掉warp-ctc对应mk目录下的std11标识符，改为std0即可)
  2. 对于代码的相应的描述：
     ocr_train.py     为训练模型文件,可以微调模型
     ocr_predict.py   训练好的模型进行训练
     lstm_model.py    分装的mx.model，值实现了前馈网络.
     generator.py     该代码自动生成验证码(为了节约时间，直接摘自网络，再次鸣谢作者).
     lstm.py          ctc算法处理数据
 
  3.效果
  
