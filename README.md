# Monocular_Distance_Detect

Algorithm based on Yolo v5 to detect the front vehicles' distance

Modified based on [KinkangLiu](https://github.com/KinkangLiu/Monocular_Distance_Detect)

```
# Run
python estimate_distance.py --source YOUR_PATH\data\images\demo.mp4 --view-img
```

# The Video Demo

<img align="center" src="https://github.com/404nofound/Monocular_Distance_Detect/blob/main/test1.gif" alt="" width="640" height="360" style="display: inline; float: right"/>

## Output

```
label = label + ' ' + str('%.1f' % d[0]) + 'm ' + str(location)
```

`d0` denotes distance.

`location`: -1 means the targeted vehicle in the left; 0 in the center; 1 in the right.

## Important Parameters

```
def __init__(self):
    #自己相机的图像尺寸
    self.W = 1280
    self.H = 720
```

```
#相机高度
#关键参数，不准会导致结果不对
H = 0.4
```

```
#相机与水平线夹角, 默认为0 相机镜头正对前方，无倾斜
#关键参数，不准会导致结果不对
angle_a = 0
```

## Tips

- **Python3.8**

- **PyTorch version: 1.9.0**，PyTorch historical archive [Previous PyTorch Versions | PyTorch](https://pytorch.org/get-started/previous-versions/)

```
# CUDA 10.2
conda install pytorch==1.9.0 torchvision==0.10.0 torchaudio==0.9.0 cudatoolkit=10.2 -c pytorch
```
## Notes

GPU NVIDIA 3060 and above: **PyTorch version >= 1.11.0**
