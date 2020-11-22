# E28_GANomaly_detection

# 정상-이상 데이터의 anomaly score 분포 시각화

![Screenshot from 2020-11-22 20-12-28](https://user-images.githubusercontent.com/39249809/99902189-39076280-2cff-11eb-87e3-f03ae110aa6a.png)


# 테스트셋 이상감지 정확도(%) - 적절한 threshold에 따른 이상 감지율 계산


![Screenshot from 2020-11-22 20-12-35](https://user-images.githubusercontent.com/39249809/99902188-37d63580-2cff-11eb-83ff-7034eb3dee25.png)


# 이상감지 성공실패사례 제시

- CIFAR-10에서 특정 클래스, 6번 라벨 개구리(Frog)를 이상 데이터로 활용함
    1. 개구리(Frog) 6번 라벨링된 모든 이미지를 훈련 데이터에서 제거하고, 나머지 클래스로만 학습을 시킴
    2. 테스트 데이터를 6번 라벨(이상 데이터를 포함한) 형태로 구성하여 이상감지 성능을 평가하는 방식임
- 위 모델은 개구리는 학습되지 않은 데이터이므로, 테스트 데이터로 개구리가 나타나면 매우 특이한 상황이라고 가정하는 것임
    1. 위 시각화 자료에서 anormaly 데이터(6번 라벨)와 normal 데이터(나머지 라벨)간의 분포가 다른 것을 확인할 수 있음 