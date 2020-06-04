# Spine and vertebrae segmentation

## How to run

To run in the same environment as me, I recommend to import this folder and your data to 
[Google Drive](https://drive.google.com/)
and run notebooks from [Google Colaboratory](https://colab.research.google.com). The folder paths and imports are already
adjusted to Drive's folder structure. Google Colab has all required packages installed, only `nipype` for image
rotation needs to be installed.

Otherwise, `jupyter notebook` needs to be installed and this is the list of libraries used:

```
keras=2.3.1
tensorflow=2.2.0
nibabel=3.0.2
nipype=1.5.0
cv2=4.1.2
sklearn=0.22.2.post1
skimage=0.16.2
```

## Folder structure

```
.
+ data                  directory for data
|  + imgs               folder for image data
|  + masks              folder for mask data
|  + test               folder for test images (if needed)
|  + test_masks         folder for test masks (if needed)
+ saved_models          directory where trained models are saved
```

## Files
* models.ipynb - keras models
* functions.ipnyb - functions for data loading, saving, preprocessing, visualisations
* metrics.ipnyb - loss and metric functions
* spine-segmentation.ipynb - pipeline for training and predicting binary segmentation of 3D images 
* vertebrae-segmentation.ipnyb - pipeline for training and predicting multi-class segmentation of 3D images
* cross-validation.ipnyb - pipeline for cross validation

## Data
Data should be named in a way, when images and masks are sorted, they correspond to each other.

My implementation reads NifTy 3D images, which are then preprocessed and saved into .npy files.
