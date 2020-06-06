# mge51101-20196018

```
Name: YoungJun Choo  
Student No.: 20196018  
School: Business Analytics  
E-mail: gkdlfnddy@unist.ac.kr  

```

kaggle deepfake data 분석

# Introduction
Nowadays, youtube generates many videos. someone makes fake videos and voices for their benefits. and it makes many problems in society. they make even president fake videos. Therefore, it is a very important technology. we research fake video detecting algorithm.

Recently, Deep Neural Networks is a paradigm. It solves many difficult problems such as NLP, S2S, Image Detection, Voice Recognition, MOT, GAN. In this paper, We use Two technology Image detection and Voice Recognition. Because it can relate to video analysis.

Many researchers publish noticeable papers about CNN. For example, MTCNN can detect faces, Batch normalization can allow using a high learning rate, Inception block can extract complicate feature. To apply the CNN algorithm for deepfake detection, we need to answer the following questions:

- Can we extract face from video without error?
- Can we get voice information from the video?
- Can we detect fake or not by using face and voice information?

Solving the above questions makes improvements about fake detection algorithm. In this paper, we don't have remarkable achievements. Because this paper is an intermediate process of algorithm development. Therefore, we focus on applying algorithms and experiment algorithms. The brief contributions can be summarized as follows:

- To extract the face image, we use the MTCNN algorithm and we consider error situations. so we can extract face from video without error.
- To extract voice information, we use moviepy package. It allows to extract voice information from the video.
- To detect fake or not, we use the CNN algorithm, inception block, Batch normalization, Sigmoid activation function for the last activation function.

Finally, we have a discussion about our experiment and future works.

# Related work

The literature on image detection and CNN algorithm is vast and span. So, we focus on recent research about Convolution Neural Networks. To detect the face,  some of the CNNs based face detection approaches have been proposed in recent years. Yang et al. [11] train deep convolution neural networks for facial attribute recognition to obtain a high response in face regions which further yield candidate windows of faces. However, due to its complex CNN structure, this approach is time costly in practice. Li et al. [19] use cascaded CNNs for face detection, but it requires bounding box calibration from face detection with the extra computational expense and ignores the inherent correlation between facial landmarks localization and bounding box regression. To overcome the previous problem MTCNN is suggested and it shows high performance we use this algorithm for face detection.

To detect fake, feature extraction algorithm is also important. Many researchers know it is important and publish many papers. Residual bock is proposed to alleviate gradient descent with low parameters. For the same reason, the Densely block is designed and it has an additional advantage about preservation images minor characteristics. Google develops inception block. this algorithm's advantages are dimension reduction and extraction of non-linear features. We apply this inception block. 

[11] S. Yang, P. Luo, C. C. Loy, and X. Tang, “From facial parts responses to
face detection: A deep learning approach,” in IEEE International Conference on Computer Vision, 2015, pp. 3676-3684.
[19] H. Li, Z. Lin, X. Shen, J. Brandt, and G. Hua, “A convolutional neural
network cascade for face detection,” in IEEE Conference on Computer
Vision and Pattern Recognition, 2015, pp. 5325-5334.
mtcnn: Zhang et al, Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks, 2016

# Method

 In this section, we will have a comprehensive explanation of MTCNN, Face extraction algorithm, one image analysis algorithm, Voice analysis algorithm, last analysis algorithm and overall structure.

In the MTCNN Section, we refer to MTCNN and just apply it to our model for extracting face. This method consists of P-Net(Proposed Network), R-Net(Refinement Network), O-Net(Output Network). Each Network has its own functions. P-Net proposes candidates of windows about face classification by using input(12x12x3), bounding box regression, facial landmark location. The highly overlapped information is merged by NMS. After this information becomes R-Net input data(24x24x3). It is working similarly to P-Net, but R-Net analysis more detailly. R-Net’output data becomes O-Net’input data(48x48x3). O-Net analyzes a similar way and makes a more detailed output. This initial input image has a pyramid structure(200X160X3, 100X66X3, 30X20X3).

<img src="./image/extractingmethod.png" width="70%" height="70%" style="float:left">

(Figure 1 MTCNN 3 key methods with pyramid input)

In the Face extraction algorithm Section, we make this algorithm to extract face image from video. MTCNN can extract face 95%, so we need to consider the error situations. In figure 2, this algorithm considers the error so we can get input data. We use CV2 video capture functions for capturing images. MTCNN detects Face from the captured image. If we detect 10 images, these become input data(10,256,256,3).

<img src="./image/Faceextractiondetail.png" width="50%" height="50%" style="float:left">

(Figure 2 Face extraction algorithm)

In the One Image fake detection Algorithm, to analyze face data for detecting fake or not like figure 3. We apply inception, Batch normalization, Maxpooling. Before connecting to the FC layer. Lastly, we reduce nodes to concatenate 10 images data and voice data.

<img src="./image/oneimageAlgorithm.png" width="50%" height="50%" style="float:left">

(Figure 3 one image analysis algorithm)

In the Voice fake detection Algorithm, to analyze voice information, we apply mainly the 1D convolution layer like Figure 4. 

<img src="./image/VoiceCNNalgorithm.png" width="50%" height="50%" style="float:left">

(Figure 4 Voice fake detection Algorithm)

In theLast CNN Algorithm, the Last CNN algorithm's main function is that we concatenate 11 outputs from image and voice. To calculate loss value, we make the last value 0(Real) or 1(Fake).

<img src="./image/lastCNNalgorithm.png" width="50%" height="50%" style="float:left">

(Figure 5 Last CNN Algorithm)

Now, we can understand how each algorithm work to detect video fake. We are coding like figure 6. This jupyter code is downloaded from https://github.com/Chooyoungjun/mge51101-20196018/tree/master/deepfakedetection/code.

<img src="./image/Video분석전체구조.png" width="80%" height="80%" style="float:left">

(Figure 6 Overall structure)

# Result
In the result section, we will explain about Loss function and Test Result. 
### Loss function
We use the Binary Crossentropy loss as a criterion. It is computed as:

![equation](https://latex.codecogs.com/gif.latex?-%5Cfrac%7B1%7D%7BN%7D%5Csum_%7Bi%3D1%7D%5EN%20%5By_i%20%5Clog%28%5Chat%7By%7D_i%29&plus;%281-y_i%29%20%5Clog%281-%5Chat%7By%7D_i%29%5D)

This loss function can calculate large value when the prediction is wrong. For example, the ground truth is 0 and the prediction value is 0.9. The loss is 1. If the prediction value is 0.99, the loss is 2. If the prediction value is 0.1, the loss is 0.0457. Likewise, this loss function can calculate the exact loss value for training. That is why we choose this loss function.
### Test Result
In this project, the loss function is criterion and metrics. This information can check the [Kaggle evaluation]( https://www.kaggle.com/c/deepfake-detection-challenge/overview/evaluation, "kaggle link"). 
In my cases, the loss value is 0.6974. it isn’t a good performance. We will discuss results and future works in the conclusion section.
# Conclusion


