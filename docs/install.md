# Installation Instructions
The enviroment is based on [BEVDet](https://github.com/HuangJunJie2017/BEVDet/blob/dev3.0/docker/Dockerfile).

**1. Conda Virtual Environment**
```shell
conda create -n fusionocc python=3.8 -y
conda activate fusionocc
```

**2. PyTorch**
```shell
pip install torch==1.10.1+cu113 torchvision==0.10.1+cu113  -f https://download.pytorch.org/whl/torch_stable.html
```

**3. MMCV, MMDet, MMSeg**
```shell
pip install mmcv-full==1.5.3 -f https://download.openmmlab.com/mmcv/dist/cu11.3/torch1.10.0/index.html
pip install mmdet==2.25.1 mmsegmentation==0.25.0
```

**4. Others**
```shell
pip install -r requirements.txt
```

**5. Intall FusionOcc**

```shell
git clone https://github.com/ShuoZhang-code/FusionOcc.git
cd FusionOcc
pip install -v -e .
```

