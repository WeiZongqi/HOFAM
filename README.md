# Robust Cross-Scene Foreground Segmentation in Surveillance Video

 We integrate dual modalities (foregrounds' motion and appearance), and then eliminating features without representativeness of foreground through attention-module-guided selective-connection structures. It is in an end-to-end training manner and to achieve scene adaptation in the plug and play style. Experiments indicate the proposed method significantly outperforms the state-of-the-art deep models and background subtraction methods in untrained scenes -- LIMU and LASIESTA.

****
## Introduction
Our work is based on our group accepeted work foreground segmentation model [STAM](https://www.mdpi.com/1424-8220/19/23/5142). Code uses Tensorflow 1.13, CUDN 10.1.

![Video Frame / Ground True / Optical flow / Foreground segmentation Result](https://weizongqi.github.io/HOFAM/show/test_0055.png)

## Structure
The structure of the proposed Hierarchical Optical Flow Attention Model (HOFAM).
![HOFAM](/show/hofam.png)

 Comparison to the baseline on DOTA for oriented object detection with ResNet-101. The figures with blue boxes are the results of the baseline and pink boxes are the results of our proposed CG-Net.
![Attention module in HOFAM](/show/atten.png)



## Experiment

|Method|Mean Dice|Recall|Precision|F-measure|
|:---:|:---:|:---:|:---:|:---:|
|HOFAM|0.9466|0.9661|0.9893|0.9776|

You need download [checkpoint](https://drive.google.com/file/d/1RodI2WjeG7X28T1kSTRppGmvSX95CUO8/view?usp=sharing) first, and place it in checkpoint/(here)


## dataset prepare
Refer to [selflow](https://github.com/ppliuboy/SelFlow) to calculate different optical flows
```sh
Merge vidoe frame + hierarchical optical flow + ground truth like dataset/demo_data/test_000155.png
```
Prepare and Generate tfrecode file
```sh
change data path and run tfrecode.py
```

## train and test

```sh
$ run main.py
```

## Ablation Results
Hierarchical optical flow (orange border) and foreground segmentation results.
![](/show/hop.png)

Visualization of Attention Module results.
![](/show/seg_atten.png)

Comparison results of foreground segmentation of
small objects with different losses.
![](/show/seg_loss.png)

## Cross-scene dataset Results
Comparison results of different model on crossscene dataset LIMU. Each column has five images and there are video frame, segmented results of HOFAM, PSPNet,
DeepLabV3+ and STAM, from left to right. Green: False Positive, Red: False Negative.
![](/show/seg_limu.png)

Comparison results of different Model on cross-scene
dataset LASIESTA.
![](/show/seg_la.png)
