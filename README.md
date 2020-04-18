# mge51101-20196018

```
Name: YoungJun Choo  
Student No.: 20196018  
School: Business Analytics  
E-mail: gkdlfnddy@unist.ac.kr  

```

kaggle deepfake data 분석 

Voice & Video data

• What is your goal? Why this is important problem?

first purpose nowadays fake videos are damaging many people 

becase of Technology (Deeplearning, GAN ....)

second purpose is to have a better score than kaggle first place 0.19170. I would like to do so and issue paper.

In order to achieve the best score, I am studying the code from ranking 1st to 5th and planning development in my own way.

That technology makes fake videos so sophisticated that it is difficult for humans to distinguish them.

• Describe [ what is, how to gather, difficulty of ] your data concretely

Video data almost 500GB is on [kaggle](https://www.kaggle.com/c/deepfake-detection-challenge/data, "kaggle link") website for gathering it ,i download videodata through the Internet. and then i make preprocessing code for traing. for example, 255x255 face extract and voice data extract.

it take almost 1 month...

training data video is almost (4000*50)200000 videos

each video has explaination about it is fake or not.. and if it is fake, additional information origin video is added 

but it isnt explain about kind of fake (voice? video?)

many kind of people is provided (black, white, brown, man,woman, older people, younger..)

some video show more than two people..

• Explain your Data Science problems in detail

1. Video data is consist of 2 part color(R,G,B) and Time that is why it need high dimensional analysis
2. 3D conv Tech is not verified and hard to filter analysis point
3. Fake is consist of Two part (Video or Voice) but we don't know what fake is applied
4. Voice Detection need anothor Tech (actually i don't know so i need to study.)
5. computing resource is not enough 

Detail image is below 

![realimage](deepfakedetection/sample/real.jpg)
![fakeimage](deepfakedetection/sample/fake.jpg)

more detail about image 
what is part of fake? eye.. 

below image show more detail about fake

![realdetailimage](deepfakedetection/sample/realdetail.jpg)
![fakedetailimage](deepfakedetection/sample/fakedetail.jpg)

So we neet to detect this kind of fake 
Actually it is not difficult part because we can detect by our eyes.
Detection algorithm can detect fake batter than human, so it is very hard technique

And Voice fake is also exist actually i dont know exactly how to detect voice i will learn and develop by your class and self study during this semaster

• How to evaluate your model empirically? What is your metric?

In this case It  just distinguish Fake or Not so I use BinaryCrossentropy it is suitable for this case because it can detect more sensitively especially between 1 and 0

![equation](https://latex.codecogs.com/gif.latex?-%5Cfrac%7B1%7D%7BN%7D%5Csum_%7Bi%3D1%7D%5EN%20%5By_i%20%5Clog%28%5Chat%7By%7D_i%29&plus;%281-y_i%29%20%5Clog%281-%5Chat%7By%7D_i%29%5D)

Above formula for back propagation loss value

Evaluation Matrix is F1 score 

Threshold about fake dection is 0.5 but it can be changed by result

![equation](https://latex.codecogs.com/gif.latex?F1%20score%20%3D%202%5Ctimes%20%5Cfrac%7BPrecision%5Ctimes%20Recall%7D%7BPrecision&plus;%20Recall%7D)




• Feasibility

now what i do 

first, extract 10 Face by using MTCNN from each video 

second, resizing 255,255,3 

third, extract 1 voice data by using moviepy editor

fourth, make a network. I try many times now using multi input and 2dconv instead of 3dconv and ensamble of each result

fifth, leaning start using Adam optimizer and BinaryCrossentropy loss fuction

sixth, now fail... so try again with your comment i think 


