# Robust Cross-Scene Foreground Segmentation in Surveillance Video

 We integrate dual modalities (foregrounds' motion and appearance), and then eliminating features without representativeness of foreground through attention-module-guided selective-connection structures. It is in an end-to-end training manner and to achieve scene adaptation in the plug and play style. Experiments indicate the proposed method significantly outperforms the state-of-the-art deep models and background subtraction methods in untrained scenes -- LIMU and LASIESTA.

****
## Introduction
Our work is based on our group accepeted work foreground segmentation model [STAM](https://www.mdpi.com/1424-8220/19/23/5142). Code uses Tensorflow 1.13, CUDN 10.1.

![](https://weizongqi.github.io/HOFAM/show/test_0055.png)

## Results




## demo

You need download [checkpoint](https://drive.google.com/file/d/1RodI2WjeG7X28T1kSTRppGmvSX95CUO8/view?usp=sharing) first, and place it in checkpoint/(here)

```sh
$ run main.py
```

## train and test

```sh
1. If you want to train your own video dataset, you need to change your dataset same as dataset/demo_data/test_000155.png

2. Generate tfrecode file: change data path and run tfrecode.py

3. Change tfrecode file path in model.py line 137

4. Change train and test dataset in model.py  line 209 and 659

4. Change --phase(train or test) in main.py and run main.py
```



