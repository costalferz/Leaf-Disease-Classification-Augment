## Requirement
We run code in Google Colab
- Python 3.10.12
- PyTorch 2.0.1
- NVIDIA Tesla T4

## Dataset
Here we have use Durian Leaf Disease dataset. The dataset original consists of 420 healthy and disease leaf images divided into 4 class by disease.

Dataset can be found [here](https://universe.roboflow.com/new-workspace-7ly0p/durian-diseases)

The classes uses in dataset are:
- Leaf Spot
- Algal Leaf Spot
- Leaf Blight 
- No Disease


![Alt text](https://media.discordapp.net/attachments/1142698914307379311/1180798004303765504/image.png)

## Augmentation

durian plant disease with augmentation by rotation and cutout methods in roboflow 
90° Rotate: Clockwise, Counter-Clockwise, Upside Down
Cutout: 7 boxes with 15% size each

Dataset Split: Train 70 %, Valid 15 %, Test 15 %


> Dataset No Augmentation can be download [here](https://app.roboflow.com/ds/jcFfz9CvlR?key=OZ6mrOsC6S).

> Dataset Augmentation can be download [here](https://app.roboflow.com/ds/8Hw98Eauea?key=xIrYoWnUZ4).


## Train Model

Train VGG16, EfficientNet_b2, ResNet18 Pre-trained models with IMAGENET1K_V1

75 Epoch with Data_No_Augment and 25 Epoch with Data_Augment

> Output of training is given below

Epoch 73/74
train Loss: 0.0003 Acc: 1.0000
valid Loss: 0.0464 Acc: 1.0000

Epoch 74/74
train Loss: 0.0004 Acc: 1.0000
valid Loss: 0.0424 Acc: 1.0000

Training complete in 2m 43s
Best val Acc: 1.000000

## Evaluation
Evaluation With Accuracy, weighted F1-Score

| Model   | Augmentation | Accuracy  | F1 Score  | 
| ------------- | ------------- | ------------- | ------------- | 
| ResNet18  | No Augmentation  | 94.12% | 0.9399 |
|   | Augmentation  | 97.06% | 0.9706 | 
| VGG16  | No Augmentation  | 89.71% | 0.8976 |
|   | Augmentation  | 94.12% | 0.9421 | 
| EfficientNet B2  | No Augmentation  | 90.20% | 0.9025 |
|   | Augmentation  | 92.16% | 0.9217 | 