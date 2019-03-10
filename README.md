# Face-Recgonition <br/>

This Project contains human face recognition using various algorithms such as PCA, LDA, simple feed forward NN, ConvNet.<br/>
PCA, LDA have been implemented using numpy. Both of these algorithms have been implemented in Detail. Not the direct scikit-<br/>
learn or some other APIs are used for these.<br/>

Feed forward NN and Convnets are implemented using Tensorflow 2.0 API. This was coded in Google Colab. Trained on GPU runtime.<br/>
<br/>
# Data and PreProcessing<br/>

The dataset contains 40 different persons' images. 10 images per person. So in total 400 images.<br/>
Out of which 60% i.e 240 images were taken as part of training set and rest 40% images were considered test set.<br/>
Image normalization is a must<br/>
<br/>
# Observations<br/>

PCA, LDA seems to perform better as compared to the simple feed forward Neural Network and ConvNet. <br/>
This is mainly due to dataset containing less number of images. So its generally advisable to use some traditional ML<br/>
techniques instead of "Deep" Neural Nets in such cases. <br/>
<br/>
ConvNets performed better than the traditional feed forward neural network as its an image data so shape of the data,<br/>
location invariance are preseved by the ConvNets<br/>
<br/>
#  Few Important Points <br/>
 1- Image normalization is a must; Otherwise your neural networks wont learn. I was having the same issue initially😊<br/>
    best way to normalize should be x-mean(x)/std(x) ; you can also use min-max normalization<br/>
 2- Before applying convnet, its better to resize the images into a squared size image<br/>
 3 - Dont use Too many layers, or too many filters when the data is not huge. Otherwise it will overfit.<br/>
 4 - Batch size >1 is much prefered i.e mini batch gradient descent; stochastic one might be a bit flaky,<br/>
     You might need to run it for more epochs.<br/>
