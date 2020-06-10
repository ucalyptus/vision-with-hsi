# vision-with-hsi
Rebuilt pytorch wheels with Indian Pines and other HSI dataset support.

# Installation

```
pip install https://github.com/ucalyptus/vision-with-hsi/blob/master/torchvision-0.6.0a0+fdd8342-cp36-cp36m-linux_x86_64.whl?raw=true

```

# Usage

```
import torch
import torchvision

## Call the Dataset Class 
data_train = torchvision.datasets.IndianPines('./data',download=True,PATCH_LENGTH=2)

## Check the shapes
print(data_train.__getitem__(0)[0].shape)
print(data_train.__len__())


## Wrap it around a Torch Dataloader
train_loader = torch.utils.data.DataLoader(data_train,batch_size=16,shuffle=True, num_workers=2)
```
