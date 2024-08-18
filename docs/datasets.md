# Prepare Datasets
Currently supported datasets: Occ3D-nuScenes.

## Occ3D-nuScenes
Download nuScenes V1.0 full from [here](https://www.nuscenes.org/download) to `data/nuscenes`, nuScenes-lidarseg from [here](https://www.nuscenes.org/download), GTs of Occ from [here](https://github.com/Tsinghua-MARS-Lab/Occ3D).

Create the pkl file:
```python
python tools/create_pkl.py
```
Generate the 2D semantics of BEV images using lidar:
```python
python tools/gen_seg_from_lidar.py
```

Download pretrained model weights from [here](https://github.com/pmj110119/storage/releases/download/v1/bevdet-stbase-4d-stereo-512x1408-cbgs.pth) to `./checkpoints/`.

Folder structure
```
├── data/
│   ├── nuscenes/
│   │   ├── gts/  # GTs of Occ3d
│   │   ├── maps/
│   │   ├── samples/
│   │   ├── sweeps/
|   |   ├── fusionocc-nuscenes_infos_val.pkl
|   |   ├── fusionocc-nuscenes_infos_train.pkl
|   |   ├── img_2d_seg
|   |   ├── lidarseg
|   |   │   └── v1.0-{mini, test, trainval}
|   |   └── v1.0-{mini, test, trainval}
|   |       ├── Usual files (e.g. attribute.json, calibrated_sensor.json etc.)
|   |       ├── lidarseg.json
|   |       └── category.json (the category.json from
                               nuScenes v1.0 is overwritten.)
```