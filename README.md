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
Implementation of the code is in the `main.py` module.
##### Run
Run the following command to run the project:
```
python main.py
```

### Optimization of parameters
#### Trial 1
If the parameter set are as follows:
```
keep_probability = 0.8
learning_rate = 1e-3
epochs = 35
batch_size = 16
kernel_initializer=tf.truncated_normal_initializer(stddev=0.01),
```

Then the following cross-entropy losses are reported:
```
Epoch 0 cross entropy: 0.4159979820251465
Epoch 1 cross entropy: 0.20233970880508423
Epoch 2 cross entropy: 0.12811613082885742
Epoch 3 cross entropy: 0.18717120587825775
Epoch 4 cross entropy: 0.10593946278095245
Epoch 5 cross entropy: 0.12027303129434586
Epoch 6 cross entropy: 0.09569086879491806
Epoch 7 cross entropy: 0.08572504669427872
Epoch 8 cross entropy: 0.06541970372200012
Epoch 9 cross entropy: 0.04470018297433853
Epoch 10 cross entropy: 0.06306686997413635
Epoch 11 cross entropy: 0.07552369683980942
Epoch 12 cross entropy: 0.041253332048654556
Epoch 13 cross entropy: 0.03667908161878586
Epoch 14 cross entropy: 0.06924770027399063
Epoch 15 cross entropy: 0.10168122500181198
Epoch 16 cross entropy: 0.0723799616098404
Epoch 17 cross entropy: 0.020970353856682777
Epoch 18 cross entropy: 0.07346542179584503
Epoch 19 cross entropy: 0.025937270373106003
Epoch 20 cross entropy: 0.018273258581757545
Epoch 21 cross entropy: 0.06656047701835632
Epoch 22 cross entropy: 0.02845245972275734
Epoch 23 cross entropy: 0.015441633760929108
Epoch 24 cross entropy: 0.015483175404369831
Epoch 25 cross entropy: 0.049823980778455734
Epoch 26 cross entropy: 0.03239881619811058
Epoch 27 cross entropy: 0.034569740295410156
Epoch 28 cross entropy: 0.029049750417470932
Epoch 29 cross entropy: 0.06146091967821121
Epoch 30 cross entropy: 0.014159000478684902
Epoch 31 cross entropy: 0.02383291721343994
Epoch 32 cross entropy: 0.03356606513261795
Epoch 33 cross entropy: 0.02050946094095707
Epoch 34 cross entropy: 0.03675944358110428
```

#### Trial 2
If the parameter set are as follows:
```
keep_probability = 0.5
learning_rate = 1e-4
epochs = 35
batch_size = 16
kernel_initializer=tf.truncated_normal_initializer(stddev=0.01),
```

Then the following cross-entropy losses are reported:
```
Epoch 0 cross entropy: 0.6341592073440552
Epoch 1 cross entropy: 0.31032174825668335
Epoch 2 cross entropy: 0.12776413559913635
Epoch 3 cross entropy: 0.16670547425746918
Epoch 4 cross entropy: 0.057985249906778336
Epoch 5 cross entropy: 0.11389415711164474
Epoch 6 cross entropy: 0.1323574036359787
Epoch 7 cross entropy: 0.04458057880401611
Epoch 8 cross entropy: 0.11291152983903885
Epoch 9 cross entropy: 0.08162795007228851
Epoch 10 cross entropy: 0.08123179525136948
Epoch 11 cross entropy: 0.046508293598890305
Epoch 12 cross entropy: 0.05531691387295723
Epoch 13 cross entropy: 0.042440008372068405
Epoch 14 cross entropy: 0.02731557935476303
Epoch 15 cross entropy: 0.0331728495657444
Epoch 16 cross entropy: 0.034475963562726974
Epoch 17 cross entropy: 0.02987908199429512
Epoch 18 cross entropy: 0.07515966892242432
Epoch 19 cross entropy: 0.054252296686172485
Epoch 20 cross entropy: 0.0401657298207283
Epoch 21 cross entropy: 0.04614529758691788
Epoch 22 cross entropy: 0.037293799221515656
Epoch 23 cross entropy: 0.027658971026539803
Epoch 24 cross entropy: 0.03902638331055641
Epoch 25 cross entropy: 0.034843336790800095
Epoch 26 cross entropy: 0.04926333576440811
Epoch 27 cross entropy: 0.030499914661049843
Epoch 28 cross entropy: 0.01810084655880928
Epoch 29 cross entropy: 0.045558955520391464
Epoch 30 cross entropy: 0.0473208874464035
Epoch 31 cross entropy: 0.015265390276908875
Epoch 32 cross entropy: 0.03306800127029419
Epoch 33 cross entropy: 0.02118477039039135
Epoch 34 cross entropy: 0.037661585956811905
```

#### Trial 3
If the parameter set are as follows:
```
keep_probability = 0.5
learning_rate = 1e-4
epochs = 35
batch_size = 16
kernel_initializer=tf.random_normal_initializer(stddev=0.01),
```

Then the following cross-entropy losses are reported:
```
Epoch 0 cross entropy: 0.7080070972442627
Epoch 1 cross entropy: 0.6406339406967163
Epoch 2 cross entropy: 0.3742693066596985
Epoch 3 cross entropy: 0.21108479797840118
Epoch 4 cross entropy: 0.16506630182266235
Epoch 5 cross entropy: 0.14936479926109314
Epoch 6 cross entropy: 0.1192404180765152
Epoch 7 cross entropy: 0.11734238266944885
Epoch 8 cross entropy: 0.1583995372056961
Epoch 9 cross entropy: 0.1260288953781128
Epoch 10 cross entropy: 0.06402826309204102
Epoch 11 cross entropy: 0.1219969391822815
Epoch 12 cross entropy: 0.0837552398443222
Epoch 13 cross entropy: 0.05572331324219704
Epoch 14 cross entropy: 0.06275369971990585
Epoch 15 cross entropy: 0.033019665628671646
Epoch 16 cross entropy: 0.04543980211019516
Epoch 17 cross entropy: 0.05680057406425476
Epoch 18 cross entropy: 0.051619596779346466
Epoch 19 cross entropy: 0.06158866733312607
Epoch 20 cross entropy: 0.10007407516241074
Epoch 21 cross entropy: 0.07017311453819275
Epoch 22 cross entropy: 0.0244645606726408
Epoch 23 cross entropy: 0.0667419582605362
Epoch 24 cross entropy: 0.05968325585126877
Epoch 25 cross entropy: 0.05764343589544296
Epoch 26 cross entropy: 0.028973277658224106
Epoch 27 cross entropy: 0.048812706023454666
Epoch 28 cross entropy: 0.0246305949985981
Epoch 29 cross entropy: 0.03871047869324684
Epoch 30 cross entropy: 0.03261695057153702
Epoch 31 cross entropy: 0.03492679446935654
Epoch 32 cross entropy: 0.04025376960635185
Epoch 33 cross entropy: 0.030969437211751938
Epoch 34 cross entropy: 0.059104666113853455
```

[//]: # (Image References)
[trial1_1]: ./runs/trial_1/um_000001.png
[trial1_3]: ./runs/trial_1/um_000003.png
[trial1_9]: ./runs/trial_1/um_000009.png

[trial2_1]: ./runs/trial_2/um_000001.png
[trial2_3]: ./runs/trial_2/um_000003.png
[trial2_9]: ./runs/trial_2/um_000009.png

[trial3_1]: ./runs/trial_3/um_000001.png
[trial3_3]: ./runs/trial_3/um_000003.png
[trial3_9]: ./runs/trial_3/um_000009.png

### Image output
#### Trial 1
![Trial 1 Urban 1][trial1_1]

![Trial 1 Urban 3][trial1_3]

![Trial 1 Urban 9][trial1_9]

#### Trial 2
![Trial 2 Urban 1][trial2_1]

![Trial 2 Urban 3][trial2_3]

![Trial 2 Urban 9][trial2_9]

#### Trial 3
![Trial 3 Urban 1][trial3_1]

![Trial 3 Urban 3][trial3_3]

![Trial 3 Urban 9][trial3_9]

### Conclusion
Based on images above, we conclude that the first trial parameters are better suited for this project.

### Reference
The fully convolutional network used in this work is based on
[Fully Convolutional Networks for Semantic Segmentation](https://people.eecs.berkeley.edu/~jonlong/long_shelhamer_fcn.pdf) paper.