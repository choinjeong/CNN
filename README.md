# CNN

###프로젝트 개요
-이 프로젝트는 실내 인테리어 이미지 데이터셋을 활용하여 CNN(Convolutional Neural Network) 모델을 훈련하여 다양한 룸 타입을 구분하는 것을 목표로 합니다. 이를 통해 각 이미지가 침실, 거실, 부엌, 다이닝 룸 또는 화장실 5개 클래스 중 어디에 속하는지 자동으로 이미지를 식별할 수 있게 됩니다.

###데이터 소스
-데이터셋은 직접 웹 크롤링 및 Kaggle, image.csv에서 수집되었습니다. 수집된 이미지 데이터는 주요 실내 인테리어 환경을 다양하게 포함하고 있으며, 다음 단계의 모델 훈련을 위해 준비되었습니다.
-약 1만 2천 개의 데이터와 5개 클래스

###CNN 주요 특징
- 합성곱 레이어(Convolutional Layers)
- 풀링 레이어(Pooling Layers)
- 자동 특징 추출(Automatic Feature Extraction)
- 전이 학습(Transfer Learning)
- 깊은 신경망(Deep Networks)

###분석 결과
-정확도(Accuracy)는 0.55, loss는 1.11로 지표를 통해 해당 모델의 결과를 알 수 있었습니다. 모델의 성능을 보다 쉽게 이해하기 위해 시각화를 통해 알아보았습니다.

(시각화)

###분석 한계
-본 프로젝트에서 이미지 분류를 하기 위해서 사용한 분석 모델은 CNN이다. 우선적으로 직접 ConvNet2D를 여러개 쌓아서 모델을 구축하였다. 그렇기 때문에 보다 정교한 모형을 구축하는 데 시간이 많이 소요되었고 데이터셋의 양의 한계로 낮은 정확도를 보완하기 위해 사전학습된 모델 중 MobileNet을 사용하기로 했습니다. MobileNet은 경량화된 딥러닝 신경망 아키텍처로, 모바일 및 임베디드 디바이스에서 효율적으로 실행될 수 있도록 설계된 특징을 갖고 있습니다. 

###MobileNet 주요 특징
- 경량화된 아키텍처
- 깊이 분리 합성곱(Depthwise Separable Convolution)
- 네트워크의 확장성 : width multiplier , resolution multiplier

###분석 결과
loss         :  0.45
accuracy     :  0.95
precision    :  0.88
recall       :  0.86
prc          :  0.94

(시각화-그래프)

기존에 구현한 모델보다 loss(1.11→0.45)나 accuracy(0.55→0.95) 측면에서 훨씬 더 좋은 결과를 보이고 있습니다. 

(시각화-예측사진)

###참고
[1] https://arxiv.org/pdf/1704.04861v1.pdf
