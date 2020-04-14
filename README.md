# SOLOv2
The code is an unofficial pytorch implementation of [SOLOv2: Dynamic, Faster and Stronger]
(https://arxiv.org/abs/2003.10152)

based on https://github.com/Epiphqny/SOLOv2

## Install
Please check [SOLOv1](https://github.com/WXinlong/SOLO/blob/master/docs/INSTALL.md) for installation instructions.

## Training
Follows the same way as SOLOv1.

single GPU: 
```
python tools/train.py configs/solov2/solov2_r50_3x.py
```
multi GPU (for example 8): 
```
./tools/dist_train.sh configs/solov2/solov2_r50_3x.py 8
```

## Eval
Follows the same way as SOLOv1.

single GPU: 
```
python tools/test_ins.py configs/solov2/solov2_r50_3x.py work_dirs/solo_r50_3x/latest.pth --show --out results_solo.pkl --eval segm
```

## Visual
Follows the same way as SOLOv1.

single GPU: 
```
python tools/test_ins_vis.py configs/solov2/solov2_r50_3x.py  work_dirs/solo_r50_3x/latest.pth --show --save_dir  work_dirs/vis_solo
```


## Weights
链接：https://pan.baidu.com/s/1tj-E63y5P__nzVFoAKAk4w 
提取码：14r4 

## Results
After training 36 epochs(3x) on the coco dataset using the resnet-101 backbone, the mAP is 37.2 on COCO val-dev2017 dataset. In the original paper, the model achieves 38.8 after 72 epochs(6x).

<img src="AP.png">

## Visualization（1 epoch)

<img src="solov2.png" width="2000">
