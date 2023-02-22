## 环境安装
具体操作见https://blog.csdn.net/HUASHUDEYANJING/article/details/126238110
- 1 激活环境
```
conda activate polarnet
```
- 2 安装pytorch
```
conda install pytorch torchvision cudatoolkit=11.3 -c pytorch
```
- 3 pytorch >= 1.8.0 安装pytorch-scatter
```
conda install pytorch-scatter -c pyg
```
## 下载代码
- 1 下载代码
```
git clone https://github.com/huashu996/PolarSeg.git
cd PolarSeg
pip install -r requirement.txt
pip install vispy
pip install matplotlib
```
- 2 semantic-kitti-api官方工具包
```
git clone https://github.com/AbangLZU/semantic-kitti-api.git
cd semantic-kitti-api
pip install -r requirements.txt
#可视化
python visualize.py --dataset /path/to/your/kitti/dataset --sequence 00
```
## 运行代码
- 1 训练
```
python train_SemanticKITTI.py --data ./data/kitti/dataset
```
- 2 验证
```
python test_pretrain_SemanticKITTI.py -d ./data/kitti/dataset/ -p ./pretrained_weight/SemKITTI_PolarSeg.pt
```
