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
![screenshot_20171221-151714](https://www.google.co.kr/url?sa=i&url=https%3A%2F%2Fdatascience.stackexchange.com%2Fquestions%2F52144%2Fnegative-range-for-binary-cross-entropy-loss&psig=AOvVaw0QlK0VDgYFd2uQhS_EwJiM&ust=1585654159351000&source=images&cd=vfe&ved=0CAIQjRxqFwoTCNiT3JqMwugCFQAAAAAdAAAAABAD)
• Describe [ what is, how to gather, difficulty of ] your data concretely
Video data 500GB is on kaggle website 
[kaggle](https://www.kaggle.com/c/deepfake-detection-challenge/data, "kaggle link") 
for gathering it is down through the Internet
also data each data make Time Serial Image data and Voice data for Learning 
it take almost 1 month
• Read the issues in your GitHub and revise your proposal 
