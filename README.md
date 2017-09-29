# Semantic Segmentation
### Introduction
In this project, you'll label the pixels of a road in images using a Fully Convolutional Network (FCN).

### Setup
##### Frameworks and Packages
Make sure you have the following is installed:
 - [Python 3](https://www.python.org/)
 - [TensorFlow](https://www.tensorflow.org/)
 - [NumPy](http://www.numpy.org/)
 - [SciPy](https://www.scipy.org/)
##### Dataset
Download the [Kitti Road dataset](http://www.cvlibs.net/datasets/kitti/eval_road.php) from [here](http://kitti.is.tue.mpg.de/kitti/data_road.zip). Extract the dataset in the `data` folder. This will create the folder `data_road` with all the training a test images.

It is also easier to download the VGG network directly from [here](https://s3-us-west-1.amazonaws.com/udacity-selfdrivingcar/vgg.zip). Otherwise, the helper functions will download that for you but it might be slower.

### Start
##### Implement
Implement the code in the `main.py` module indicated by the "TODO" comments.
The comments indicated with "OPTIONAL" tag are not required to complete.
##### Run
Run the following command to run the project:
```
python main.py
```
