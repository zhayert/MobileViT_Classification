# MobileViT_Classification

This repository contains the code for the implementation of MobileViT in Pytorch. 

Paper: https://arxiv.org/pdf/2110.02178.pdf

## Pretrained models

Download pretraining weights files. Each model in the 'model.py' has a download address that provides pretraining weights, and download the corresponding pretraining weights based on the model you are using.

Set the '-- weights' parameter to the downloaded pretraining weight path in the "train.py".

## Datasets

I trained MobileViT with pretrained model in flower_photos and Caltech-256.

You can download flower_photos datasets from 

https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz

Or Caltech-256 datasets from 

https://data.caltech.edu/records/nyy15-4j048/files/256_ObjectCategories.tar?download=1

Please remember to set '-- data-path' to the decompressed datasets folder path in the 'train.py'.

If you want to use your own dataset, please arrange it according to the file structure of the flower classification dataset (i.e., one category corresponds to one folder). The 'num' in "train.py" and "predict.py" represents the number of categories in your own dataset.

After setting the path to the dataset and pretraining weights, you can use the 'train.py' to start training (the 'class_indices.json' file will be automatically generated during the training process)

## Training

Please execute the "train.py" for training.

## Predicting

Set the weight path model "weight_path" and predicted image path "img_path" can be used to make predictions using the predict.py.

Please execute the "predict.py" for predicting.
