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
+ 기존 learning_rate(0.0001)에서 발견된 과적합 문제를 해결하기 위해 lr를 0.00001로 설정

"이미지 처리를 위해 CNN을 사용함"
## 5) 프로젝트 진행 시 시행 착오 및 문제점

프로젝트 개선 사항
