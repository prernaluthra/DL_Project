# Deep Learning Project Fall 2021

## 1. Deep_Learning_Project_Fall_2021.ipynb
This file primarily contains the code for running BRATS2021 Dataset with VGG16, ResNet50 or EfficientNetB3

### Kaggle Notebook
We primarily ran the code as a Kaggle Notebook. 
The code can also be found here: https://www.kaggle.com/prernaluthra/dl-project

### Data Sources
1. We used the BRATS2021 dataset available here: https://www.kaggle.com/c/rsna-miccai-brain-tumor-radiogenomic-classification
2. Weights of the models: VGG16, ResNet50, EfficientNetB3

### How to run the code?
1. You can either clone the kaggle notebook OR you can clone this github repo ( specifically file Deep_Learning_Project_Fall_2021.ipynb)
2. Go to file `Deep_Learning_Project_Fall_2021.ipynb`
3. In the code cell `[In 132...]` of the notebook, you'll see the line
```
root_dir = '../input/rsna-miccai-brain-tumor-radiogenomic-classification/'
```
Replace this line so that it points to the path to BRATS2021 Dataset (as indicated in Data Sources Section).
3. Pick a model you would like to run (eg. VGG16). Make sure you add appropriate imports for it. Note that imports for VGG16, ResNet50, EfficientNetB3 are allready present.
3. In `Build Model` Section ( or `[In 139...]` code cell), you'll see the line
```
model = VGG16(include_top=False,weights=weights_path)
```
Repace this line with the model you would like to run. 
4. In the same code cell as above (3.), you'll see the line
```
model = Model(model.inputs, outputs, name="VGG16")
```
Repace this line with the model you would like to run. It should be the same as what you picked in 3.
5. In `Train Model` Section ( or `[In 140...]` code cell), you'll see the line
```
model = build_model("../input/vgg16-weights/vgg16_weights_tf_dim_ordering_tf_kernels_notop.h5")
```
Repace this line with the path to weights of the appropriate model you chose in 3. and 4.
6. You should be all set!
