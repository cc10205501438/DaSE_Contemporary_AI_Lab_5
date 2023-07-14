# Readme
## 环境
python3.9

## 目录结构
├─baseline                  不使用预训练模型的baseline
│ ├─baseline.py
│ ├─model.py
│ └─data_utils.py
├─data                      训练数据-文本和图像
├─label                     训练数据-标签    
│ ├─test_without_label.txt
│ └─train.txt
├─output                    输出(预测测试集)
├─main.py                   主函数    
├─data_utils.py             数据处理模块
├─model.py                  多模态模型构建
├─figs.ipynb                部分图表

## 安装
```bash
pip install -r requirements.txt
```

## 查看可调整参数
```bash
python ./main.py -h
```

## 训练
多模态融合模型
```bash
python ./main.py
```

消融实验(仅图像)
```bash
python ./main.py --image_only
```

消融实验(仅文本)
```bash
python ./main.py --text_only
```

## 预测测试集

```bash
python ./main.py --do_test
```

## 其他
训练baseline模型
```bash
python ./baseline/baseline.py
```


## 使用的库
nltk==3.6.5
numpy==1.20.3
opencv_python==4.6.0.66
pandas==1.3.4
Pillow==9.2.0
scikit_learn==1.1.1
torch==1.11.0
transformers==4.18.0