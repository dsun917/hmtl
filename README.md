---
description: 'https://github.com/donglee-afar/logdeep'
---

# Learning

To see whether the current available data can draw a concrete decision boundary between normal data and abnormal data. Given a large and diverse set of training data, a good deep learning model will significantly outperform non-deep learning algorithms.

## 

## Density Estimation

Model p\(x\) from data, identify unusual users by checking which have p\(x\) &lt; \epsilon

### Gaussian Mixture Model

#### Gaussian Distribution

With assumption the feature follow Gaussian distribution, we can do parameter estimation with samples using maximum likelihood estimation. 

#### Multivariate Gaussian Distribution 

Do not model p\(x1\), p\(x2\) separately, model p\(x\) all in one go. 

Automatically captures correlations between features using covariance matrix.

#### Maximum Likelihood

Assume the data points are sampled from a probability density function

$$
f_{\theta} (x)
$$

theta is unknown, to be found from data.  

$$
L(\theta) = f_{\theta} (x^{1}) f_{\theta} (x^{2})...f_{\theta} (x^{N})
$$

$$
\theta^{*} = argmax_{\theta} L(\theta)
$$

### One-class SVM

### PCA

Project features to some dimension which can differentiate the data very much.

### Isolated Forest 

Use tree like structure to split data

#### Construct a fully random binary tree

* Choose attribute j at random
* Choose splitting threshold theta uniformly from \[min, max\]
* until every data point is in its own leaf



### Outlook: Auto-encoder

Train: Training data, encoder, code, decoder, training data \(as close as possible\)

Test: normal data, encoder, code, decoder, can be reconstructed 

Test: anomaly data, encoder, code, decoder, can not be reconstructed \(Large reconstruction loss\)



## Evaluation

Assume we have some labeled data, of anomalous and non-anomalous examples \(y = 0 if normal, y = 1 if anomalous\). 



## Anomaly Detection vs Supervised Learning

Choose anomaly detection with very small number of positive examples \(0-20 is common\) and large number of negative examples.

Many different "types" of anomalies. Hard for algorithms to learn from positive examples what the anomalies look like; future anomalies may look nothing like any of the anomaly examples we've seen so far. Anomaly samples can not be treated as a class because it variate a lot. 

Choose supervised learning with a large number of positive and negative examples.

 Enough positive examples for algorithms to get a sense of what positive examples are like, future positive examples likely to be similar to ones in the training set.

##  Features

### Feature Transformation

For non-Gaussian model, play with different transformations log\(x\) for the data to make it gaussian.

### Feature Selection

Choose features that might take on unusually large or small values in the event of an anomaly.

Such as memory use of computers, number of disk accesses/sec, CPU load, network traffic, and combinations of them

### Polluted

A little bit of training data is an anomaly.



## Error Analysis

## DeepLog



