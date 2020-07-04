# covid19-chest-xray
This repository contains code and report for the COVID19 Chest XRay image classifications by using Deep Learning models. The problem is multilable classification problem in nature and hence we used Transfer Learning technique along with Focal loss as critarion. 
It is a multi label classification problem in nature. The dataset contains 3 classes ['COVID19', 'NORMAL', 'PNEUMONIA'].
The dataset is available here
https://drive.google.com/drive/folders/1-_XiDnOEloIdIUN7bpJbrUPalKv8Zn0m?usp=sharing
Data distribution is as follows: 
![data](https://user-images.githubusercontent.com/56000386/86512403-8a2fbc00-be1b-11ea-8e58-ff3b916004b3.PNG)

Batch size is 8 a batch example is shown as:
![batch](https://user-images.githubusercontent.com/56000386/86512436-c400c280-be1b-11ea-92e4-6ca94ce54c8b.PNG)

We used pretrained VGG16 model and replace its fully connected layers. The FC layer architecture is as follows. 
![fclayers](https://user-images.githubusercontent.com/56000386/86512496-412c3780-be1c-11ea-84e9-ef11969ad340.PNG)
Freezes all other layers except these FC layers and train this model on our dataset. 
The exparimental steps are as follows:
momentum = 0.9
learning rate = 0.001
optimizer = Stochastic Gradient Descent
critatrion = Focal Loss

and trained the model. 
The trained model can be found here:
https://drive.google.com/file/d/1X3plx3WiYD1R8CsDr-s2V7LXdMXFZve_/view?usp=sharing

The loss curve is: 
![loss curve](https://user-images.githubusercontent.com/56000386/86512550-a849ec00-be1c-11ea-947e-e151e08f8076.PNG)
The accuracy curve is:
![accuracy curve](https://user-images.githubusercontent.com/56000386/86512571-cadc0500-be1c-11ea-9816-66af40d97228.PNG)
The confusion matrices are:
![confusion matrix1](https://user-images.githubusercontent.com/56000386/86512579-d92a2100-be1c-11ea-8263-93fb6c6fa34d.png)
![confusion matrix2](https://user-images.githubusercontent.com/56000386/86512589-e1825c00-be1c-11ea-8814-057b43042d03.png)
![confusion matrix3](https://user-images.githubusercontent.com/56000386/86512594-eb0bc400-be1c-11ea-926c-98bcb906070e.png)
F1 score is:
![classification report](https://user-images.githubusercontent.com/56000386/86512605-f9f27680-be1c-11ea-8328-6fd9efceb072.PNG)

