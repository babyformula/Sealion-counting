# Sealion-counting
Utilizing deep crowd network to classificate sealions &amp; recognise the population of each classification, with given dataset from NOAA satellite photographs. 

## 1.Description
### 1.1 Dataset
The dataset originate from NOAA, and could be obtained from [Kaggle](https://www.kaggle.com/c/noaa-fisheries-steller-sea-lion-population-count).<br>

It contains:<br>
* sample_submission.csv: an example valid submission file<br>
* Train/*.jpg: a set of training images, with each filename corresponding to a train_id<br>
* Train/train.csv: a list of ground-truth counts for each train_id<br>
* TrainDotted/*.jpg: copies of the training images with markings showing where each animal is (see below)<br>
* Test/*.jpg: a set of test images, with each filename corresponding to a test_id<br>

Here only several train pics were uploaded to this git because the whole dataset is quite a bit huge, and the validation and enhancement of this model was priority in this git. Definitely you can download the dataset from above link.<br>
### 1.2 Method
Basic method to achieve data preprocessing, classification, and crowd counting has already been realized in the Notebook file Deepcrowd_sealion.ipynb, and of course was written in python.<br>
Descriptions for each fuction in the Notebook file could also be found above their own section part.<br>

This model focuses on crowd network method to count sealions, and relies on following tools to operate:<br>
* Python 3.x
* Opencv 3.x
* Latest caffe
* Anaconda(optinal, you can choose to seperate the Jupyter file into python files and operate in your own way)

## 2.Practice
Recently(a month ago from creating this git) I have set up this model on an AWS GPU instance, dealing with 100 training pictures, and a lot of impovement and ensembling need to be done.<br>

Note, several lines need to be edited if you're trying to perform this model:<br>
* paths in the Jupyter file
* paths in models/crowdnet/train_val.prototxt
