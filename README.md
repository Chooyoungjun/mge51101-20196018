# mge51101-20196018

```
Name: YoungJun Choo  
Student No.: 20196018  
School: Business Analytics  
E-mail: gkdlfnddy@unist.ac.kr  

```


• upload your plan on GitHub (use markdown)
my plan is predict deepfake about voice and face so i will use kaggle data

교수님 한테 이미 보여 드렸는데 그때 받은 코맨트 대로 수정 하고 있는 중입니다. 

목표는 이번 학기동안 공부해서 학습이 되고 페이크를 예측 하는 것 입니다. 

데이터를 받고 하는데 시간이 많이 걸리는데 이미 그런 과정은 완료를 해서 분석을 어떻게 해야 할지에 대해서만 

고려하면 될 것 같습니다. 

참고 하실만한 자료를 공유 해 주시면 감하겠습니다. 
 

kaggle deepfake data 분석 

Voice & Video data

• What is your goal? Why this is important problem?

purpose nowadays fake videos are damaging many people 

becase of Technology (Deeplearning, GAN ....)

That technology makes fake videos so sophisticated that it is difficult for humans to distinguish them.

• Explain your Data Science problems in detail

1. Video data is consist of 2 part color(R,G,B) and Time that is why it need high dimensional analysis
2. 3D conv Tech is not verified and hard to filter analysis point
3. Fake is consist of Two part (Video or Voice) but we don't know what fake is applied
4. Voice Detection need anothor Tech (actually i don't know so i need to study.)
5. computing resource is not enough 

• How to evaluate your model empirically? What is your metric?
In this case It  just distinguish Fake or Not so 
I use BinaryCrossentropy it is suitable for this case 
because it can detect more sensitively especially between 1 and 0

![equation](https://latex.codecogs.com/gif.latex?-%5Cfrac%7B1%7D%7BN%7D%5Csum_%7Bi%3D1%7D%5EN%20%5By_i%20%5Clog%28%5Chat%7By%7D_i%29&plus;%281-y_i%29%20%5Clog%281-%5Chat%7By%7D_i%29%5D)
![equation](http://latex.codecogs.com/gif.latex?O_t%3D%5Ctext%20%7B%20Onset%20event%20at%20time%20bin%20%7D%20t)
![equation](http://latex.codecogs.com/gif.latex?s%3D%5Ctext%20%7B%20sensor%20reading%20%7D) 
![equation](http://latex.codecogs.com/gif.latex?P%28s%20%7C%20O_t%20%29%3D%5Ctext%20%7B%20Probability%20of%20a%20sensor%20reading%20value%20when%20sleep%20onset%20is%20observed%20at%20a%20time%20bin%20%7D%20t)
• Describe [ what is, how to gather, difficulty of ] your data concretely
Video data 500GB is on kaggle[kaggle](https://www.kaggle.com/c/deepfake-detection-challenge/data, "kaggle link") website 
for gathering it is down through the Internet
also data each data make Time Serial Image data and Voice data for Learning 
it take almost 1 month
• Read the issues in your GitHub and revise your proposal 
