# mge51101-20196018

```
Name: YoungJun Choo  
Student No.: 20196018  
School: Business Analytics  
E-mail: gkdlfnddy@unist.ac.kr  

```

kaggle deepfake data 분석 

# Introduction
Nowadays, youtube generates many videos. someone makes fake vidoes and voices for their benefits. and it makes many problems in society. evenif they makes president fake videos. Therefore, it is very important technology. we research fake video detecting algorithm.

Recently, Deep Neural Networks is a paradigm. It solve many difficult problems such as NLP, S2S, Image Detection, Voice Recognition, MOT, GAN. In this paper, We use Two technology Image detection and Voice Recognitio. Because, it can relate with video analysis.

Many researchers publish noticeable papers about the CNN. For example, MTCNN can detect face, Batch normalization can allow to use high learning rate, Inception block can extract complicate feature. To apply CNN algorithm for deepfake detection, we need to answer following questions:

- Can we extract face from video without error?
- Can we get voice information from video?
- Can we detect fake or not by using face and voice information?

Solving above questions makes improvemtent about fake detection algorithm. In this paper, actually we don't have remarkable achievements. Because, this paper is an intermediate process of algorithm development. Therefore, we focus on applying algorithm and experiment algorithm. The brief contributions can be summarized as follows:

- To extract face image, we use MTCNN algorithm and we consider error situation. so we can extract face from video without error.
- To extract voice information, we use moviepy packacage. It allow to extract voice information from video.
- To detect fake or not, we use CNN algorithm, inception block, Batch normalization, Sigmoid activation function for last activation function.

Finally, we have a disscution about our experiment and future works.

# Related work

The literacture on image detection and voice recognition and CNN algorithm is vast and span. So, we focus on recent research about Deep Neual Networks.

# Method

(Detail about face & voice extracting method)

<img src="./image/extractingmethod.png" width="70%" height="70%" style="float:left">

(Detail face extraction algorithm)

<img src="./image/Faceextractiondetail.png" width="50%" height="50%" style="float:left">


(One Image fake detection Algorithm)

<img src="./image/oneimageAlgorithm.png" width="50%" height="50%" style="float:left">


(Voice fake detection Algorithm)

<img src="./image/VoiceCNNalgorithm.png" width="50%" height="50%" style="float:left">

(Last CNN Algorithm)

<img src="./image/lastCNNalgorithm.png" width="50%" height="50%" style="float:left">


(Overall structure)

<img src="./image/Video분석전체구조.png" width="80%" height="80%" style="float:left">


# Result

# Conclution


