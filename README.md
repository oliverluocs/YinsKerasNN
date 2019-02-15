# YinsKerasNN
This package uses Keras as framework which provides a high-level neural networks API developed with a focus on enabling fast experimentation.

## Information

Information:
- Package: YinsKerasNN
- Type: Package
- Title: Yin's Version of Neural Network through Keras Framework
- Version: 0.1.0
- Author: Yiqiao Yin
- Maintainer: Yiqiao Yin <eagle0504@gmail.com>
- Description: This package uses Keras as framework which provides a high-level neural networks API developed with a focus on enabling fast experimentation.
- License: GPL-2
- imports: quantmod,stats,xts,TTR,knitr,keras
- Encoding: UTF-8
- LazyData: true

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

Basic working knowledge of using *R* and *RSTudio*. Please also have **kears** and **knitr** packages installed.

### Installing

The installation of this package is simple. We recommend to use *devtools* to install from Github.

```
# Install Packge using devtools
devtools::install_github("yiqiao-yin/YinsKerasNN")
```

### Usage

Inputs are the following:
-  **x = x**: This is the explanatory variable. Usually it is in the form of a matrix or a data frame.
-  **y = y**: This is the response variable, i.e. labels. This is usually a column of vectors. 
-  **cutoff = .9**: The script will y and x together in one single data frame and use this cutoff to separate out a held-out test set. The ratio of 0.9 means the script takes first 90% of the observations as training and leave the last 10% of the observations as testing. The Kears Neural Network function will uses training set to conduct K-fold cross validation.
-  **validation_split = 0.1**: Default value for validation_split is 0.1 which means validation data used the last 10% of the training data after the cut of using **cutoff**. This way we have training set, validating set, and test set.
-  **batch_size = 128**: This refers to a set of N samples. A batch generally approximates the distribution of the input data better than a single input. The larger the batch, the better the approximation; however, it is also true that the batch will take longer to process and will still result in only one update.
-  **l1.units = 256**: The number of hidden units for the first hidden layer.
-  **l2.units = 128**: The number of hidden units for the second hidden layer.
-  **l3.units = 64**: The number of hidden units for the third hidden layer.
-  **epochs = 30**: Epoch: an arbitrary cutoff, generally defined as "one pass over the entire dataset", used to separate training into distinct phases, which is useful for logging and periodic evaluation. 

## Soft Threshold

This package is the first package I publish in the field of deep learning. The Kears framework allows me to constructs a three-layer neural network. Though the number of layers are pre-defined, the number of hidden units for each layer and the epochs are soft thresholds and should be considered tuning parameters.

## Example

An example usage of this package can refer to the following.

```
# For example
YinsKerasNN::YinsKerasNN(x, y, cutoff = 0.8)
```

## Built With

* [Yiqiao Yin's Research](https://yinscapital.com/research/): We conduct research at Yin's Capital and we develop packages for trading algorithms.
* [Keras R Interface](https://keras.rstudio.com/): I used this site as code source for Kears R interface. 

## Contributing

Yiqiao Yin (myself) is the sole owner and manager for this package. The origin of author's inspiration of developing this package comes from his experience in statistical machine learning and stock market. For story, please click [here](https://github.com/yiqiao-yin/Statistical_Machine_Learning/blob/master/Story.md).
