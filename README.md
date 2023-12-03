## Dataset
Here we have use Durian Leaf Disease dataset. The dataset consists of 420 healthy and unhealthy leaf images divided into 4 categories by disease.

Dataset can be found [here](https://universe.roboflow.com/new-workspace-7ly0p/durian-diseases)

The classes uses in dataset are:
<pre>
1. Leaf Spot                                                      2. Algal Leaf Spot
3. Leaf Blight                                                    4. No Disease
</pre>

## Train Model

> Train VGG16,EfficientNet_b2, ResNet18 Pretrain-model(weight="IMAGENET1K_V1") 
> for 75 Epoch with Data_No_Augment and 25 Epoch with Data_Augment


Epoch 73/74
train Loss: 0.0003 Acc: 1.0000
valid Loss: 0.0464 Acc: 1.0000

Epoch 74/74
train Loss: 0.0004 Acc: 1.0000
valid Loss: 0.0424 Acc: 1.0000

Training complete in 2m 43s
Best val Acc: 1.000000

## Evaluation
Evaluation With Accuracy

| Model   | Augmentation | Accuracy  | F1 Score  | 
| ------------- | ------------- | ------------- | ------------- | 
| ResNet18  | No Augmentation  | 94.12% | 0.9399 |
|   | Augmentation  | 97.06% | 0.9706 | 
| VGG16  | No Augmentation  | 89.71% | 0.8976 |
|   | Augmentation  | 94.12% | 0.9421 | 
| EfficientNet B2  | No Augmentation  | 90.20% | 0.9025 |
|   | Augmentation  | 92.16% | 0.9217 | 