<div align="center">
 
![image](https://user-images.githubusercontent.com/85033252/193809079-1786cdea-efe9-4508-b57a-2a1d14d6ebcb.png)
![](https://github.com/tenngs/anti-antisocial-AI/blob/main/Images/Anti_Anti-Social_AI.png)

</div>

<div align="center">

<h3> System to combat anti-social behaviours of fingernail biting and nose picking whilst using a computer<br>
 
</div>
 
<div align="center">
 
 ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white) &nbsp;&nbsp;&nbsp;&nbsp; ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) &nbsp;&nbsp;&nbsp;&nbsp; ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) &nbsp;&nbsp;&nbsp;&nbsp; ![Visual Studio Code](https://img.shields.io/badge/Visual%20Studio%20Code-0078d7.svg?style=for-the-badge&logo=visual-studio-code&logoColor=white)  &nbsp;&nbsp;&nbsp;&nbsp; ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
 
 ![](https://img.shields.io/badge/machine-learning-blue)  &nbsp;&nbsp;&nbsp;&nbsp;  ![](https://img.shields.io/badge/artificial-intelligence-blue)
 &nbsp;&nbsp;&nbsp;&nbsp; ![](https://img.shields.io/badge/teachable-machine-blue)
 
 </div>
 
<div align="center">
 
<h2> Table of Contents

</div>

- [Background](#background)
- [What does it do?](#what-does-it-do)
- [How does it do it?](#how-does-it-do-it)
- [Privacy](#privacy) 
- [Ethics and Biases](#ethics-and-biases)  
- [Let's have a look-see, shall we?](#lets-have-a-look-see-shall-we)
   - [Landing page](#landing-page)
   - [User monitoring](#user-monitoring)
- [How to use the system](#how-to-use-the-system)
- [Possible additions](#possible-additions)


## Background
This project’s viability is assessed by the general personal observation of the increase in ubiquitous computing and the reliance on computers especially in the lives of the young at present. It is further personally observed that the young increasingly manifest anti-social behaviours of nail biting and nose picking when utilising a computer. Hence, there is a need for additional tools to help people to reduce or remove these anti-social behaviours which this project aims to provide. 
<br>

## What does it do?
The system is designed to detect fingernail biting and nose picking behaviour from user's webcam feed by utilising a Machine Learning (ML) model and to "penalise" the user by playing a continuous and horrible sound until the user stops exhibiting these behaviours with a view of drawing attention to and correcting these behaviours. 

## How does it do it?
The most important part of the system is the ML model. Google's Teachable Machine (https://teachablemachine.withgoogle.com/) was utilised to produce the model by taking ~600 pictures of the author in each four system States. Head positioning in relation to the camera was varied in producing nose picking and fingernail biting events. Also included were positioning of fingers from both hands in various areas around the mouth and nose. In addition, photographs of Covered and Turned State were taken with varying material covering the lense and various distinct surroundings, respectively. The aim was to produce a varied range of photographs to train an accurate ML model.

Subsequently, the model was trained on the images, exported and tested. The results were convincing as the model was able to recognise all States with near 100% accuracy.

The definition and purpose of all system States are as follows:

1) Normal State (ie. != Nose Picking (NP) or fingernail biting (FB) or Turned or Covered)
2) NP & FB (prohibited behaviour occurs)
3) Turned State (where webcam is turned away from the user)
4) Covered State (where webcam is covered)

When States 2 (NP & FB), 3 (Turned), 4 (Covered) are recognised by the system, an extremely annoying and loud sound is played until the system decides that the user is exhibiting State 1 (Normal) behaviour. 

## Privacy
The ML model is hosted on Teachable Machine's servers and accessed via internet. Furthermore, all user image processing occurs in user's web browser.

Please note: No user images produced by user's webcam are ever transmitted over a network. Hence, no privacy issues arise from usage of the system.

## Ethics and Biases
The model is trained on the images of its author. As a result, the model will perform more accurately when utilised by a user depicting the same demographic characteristics as the author.   

## Let's have a look-see, shall we?
The project is deployed in AWS public cloud and can be accessed from https://dev.d2uanxqxa2fkp3.amplifyapp.com/
Please find below screenshots of landing page and user monitoring state. Please note that when a user is monitored, a red sign saying "Monitoring!" is flashing on the screen. 

<div align="center">

### Landing page<br>
  

 
![image](https://user-images.githubusercontent.com/85033252/193796620-96495834-458c-4209-b00f-f2e1b0d388ba.png)


  
### User monitoring<br> 
  

 
![image](https://user-images.githubusercontent.com/85033252/193797373-a52b505d-0e00-4836-8dcf-bdd3ca21d89f.png)

</div>

## How to use the system
First, navigate to the app's website of https://dev.d2uanxqxa2fkp3.amplifyapp.com/. Subsequently, please adjust your webcam so that your face is directly opposite of it. Webcams on top of monitors work well. Press "start monitoring" button and leave the app to monitor your behaviour. If you wish to stop monitoring yourself, simply press "stop monitoring" button or navigate away from the website.

## Possible additions
As discussed in Ethics and Biases section, the ML model is trained on photographs of its author and is thus biased towards authors' demographic characteristics. Ideally, photographs from as diverse as possible demographics could be added to the model's training set with a view of producing a model that is increasingly accurate when utilised by any person. This is something that I would like to do to experiment with the system further.



