# Hierarchical Optical Flow Attention Model (HOFAM)
HOFAM: Hierarchical Optical Flow Attention Model for Cross Scene Foreground Detection


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



