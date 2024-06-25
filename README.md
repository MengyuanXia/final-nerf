# NeRF

NeRF is used to reconstruct 3D scenes from images of single or multiple perspectives and synthesize new perspectives.

## Installation

```
cd final-nerf
pip install -r requirements.txt
```

<details>
  <summary> Dependencies (click to expand) </summary>
  
  #### Dependencies
  - torch
  - torchvision
  - matplotlib
  - numpy
  - imageio
  - imageio-ffmpeg
  - configargparse
  - tensorboard
  - ...
</details>


## Usage

### Data
You can run on your own real data or download data.

The configuration of the environment of colmap is referred to [this blog](https://zhuanlan.zhihu.com/p/397053413).

Dataset structure:
```                                                                                           
├── data                                                                                                                                                                                                       
│   ├── nerf_llff_data ── flower                                                                                                                                                                                                                                                                                                          
|   ├── nerf_synthetic ── lego
|   | ...
```
---
### Train
```
python run_nerf.py --config configs/{DATASET}.txt
```
Example:Train a low-res `lego` NeRF:
```
python run_nerf.py --config configs/lego.txt
```
After training for 100k iterations, you can find the following 
[video](https://pan.baidu.com/s/1O-IkVx8f5J5onH82A8JTKQ?pwd=4321) 
and [checkpoints](https://pan.baidu.com/s/1x-ixeoKglLPDc5cBQiugLA?pwd=2121).

---

### Test
```
python run_nerf.py --config configs/{DATASET}.txt --render_only
```

