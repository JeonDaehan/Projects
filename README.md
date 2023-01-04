# Surface_Crack_Detection
My_Projects_Data_Analyst

## 1. Teaming
전대한

## 2. Data set
출처 : kaggle.com/
구성 : 변수, 레이블, 데이터수 등 전반적인 설명

## 3. Development
1) 목표 : CNN모델 정확도 99% 이상
2) 프로젝트 소스 : 코드작성 파일명(jupyter notebook, pycharm)
3) 개발 환경
Colab (GPU사용)
설치모듈 : numpy, pandas, matplotlib, tensorflow, os, glob, shutil, random, cv2, google.colab, zipfile, datetime
## 4) 모델 아키텍처 및 선정 이유
CNN구조 : C-P-Drop-C-P-Drop-C-P-Drop-F-Drop-D
기존 learning_rate(0.0001)에서 발견된 과적합 문제를 해결하기 위해 lr를 0.00001로 설정
"이미지 처리를 위해 CNN을 사용함"

## 5) 결과

## 훈련(training)
## C-P-C-P-C-P-F-D-D
lr 0.0001 => loss: 0.0102 - accuracy: 0.9969 - val_loss: 0.0237 - val_accuracy: 0.9930 과적합 
lr 0.00001 => loss: 0.0317 - accuracy: 0.9905 - val_loss: 0.0390 - val_accuracy: 0.9944 

## C-P-C-P-F-D-D 
lr 0.0001 => loss: 0.0146 - accuracy: 0.9956 - val_loss: 0.0103 - val_accuracy: 0.9966
lr 0.00001 => loss: 0.0482 - accuracy: 0.9854 - val_loss: 0.0130 - val_accuracy: 0.9986

## 평가(evaluate)
## C-P-C-P-C-P-F-D-D
lr 0.00001 [0.04126840457320213, 0.9888749718666077] 정확성과 과적합이 없음
lr 0.0001 [0.03228703513741493, 0.9911249876022339] 과적합


## C-P-C-P-F-D-D
lr 0.00001 [0.13723982870578766, 0.9537500143051147] 정확성이 떨어짐.
lr 0.0001 [0.019934188574552536, 0.9948750138282776] 과적합

### 위의 실험을 통해 최종적으로 모델의 정확성이 가장 높았던 "C-P-C-P-C-P-F-D-D"모델로 채택하고, 과적합이 최소화 되었던 lr = 0.00001로 설정하여 99%의 모델을 만들었다. 


## 6) 프로젝트 진행 시 시행 착오 및 문제점
Colab 작업환경이 아닐 시 개인 pc의 문제로 작업환경이 이루어지기 어려웠다.
매 작업마다 모델을 다르게 설계하여 최종후보 4개를 선별하는 과정에서 많은 시간이 소요되었다 (약 1시간)
