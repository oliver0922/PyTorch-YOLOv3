# Udacity Self Driving Car Dataset 으로 YOLOv3 학습하기


## 1. Clone github repository  

git을 clone을 해준다.   
![image](https://user-images.githubusercontent.com/69920975/122338777-1da1c480-cf7b-11eb-93e1-7a06963f8c27.png)

 
## 2. Install Packages  
requirements.txt를 실행시켜 내부에 있는 library들을 설치해준다  

## 3. Download pretrained weights  
이미 학습된 pretrained된 모델을 사용한다   
![image](https://user-images.githubusercontent.com/69920975/122344276-94da5700-cf81-11eb-8d9b-176d464a8e46.png)  

## 4. Customize Dataset  
class 개수에 따라서 다음과 같이 숫자를 변경해준다(여기서는 class가 11개이므로 11을 사용)  
![image](https://user-images.githubusercontent.com/69920975/122344555-e387f100-cf81-11eb-8a9f-1e3f55eb2331.png)

## 5. Prepare Dataset  
!curl -L "https://public.roboflow.com/ds/zzytNXAeGI?key=5D2xJK4vLz" > roboflow.zip; unzip roboflow.zip; rm roboflow.zip
위의 코드를 사용해서 dataset을 다운로드 해준다. 
![image](https://user-images.githubusercontent.com/69920975/122345125-7759bd00-cf82-11eb-946f-dfce0c0e98be.png)  

아래와 같이 Dataset을 skitlearn의 train_test_split 함수를 사용하여 8:2로 train set과 test set으로 분할해준다.
![image](https://user-images.githubusercontent.com/69920975/122345251-9e17f380-cf82-11eb-97c5-38b3b5910fa0.png)    

## 6. Train  
train.py를 아래와 같이 실행시킨다  
![image](https://user-images.githubusercontent.com/69920975/122345843-4463f900-cf83-11eb-8561-ddaf6ed9e0ab.png)  

## 7. Tensorboard 관찰 
![image](https://user-images.githubusercontent.com/69920975/122345932-5f366d80-cf83-11eb-8618-129478178a1d.png)
![image](https://user-images.githubusercontent.com/69920975/122345967-6b222f80-cf83-11eb-838b-e5547a78f0b5.png)
![image](https://user-images.githubusercontent.com/69920975/122346003-75442e00-cf83-11eb-9bb6-ebe0206256dd.png)



