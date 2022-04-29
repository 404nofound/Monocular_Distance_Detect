# Monocular_Distance_Detect

Copied & modified from [KinkangLiu](https://github.com/KinkangLiu/Monocular_Distance_Detect)

```
# Run
python estimate_distance.py --source YOUR_PATH\data\images\demo.mp4 --view-img
```

https://user-images.githubusercontent.com/43553114/165961931-092e7ecd-569e-4153-a440-d15615b0a045.mp4

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
