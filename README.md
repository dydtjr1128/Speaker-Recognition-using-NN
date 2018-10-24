# Speaker-Recognition-using-NN(화자 인식)
Speaker Recognition using Neural Network &amp; Linear Regression

## 화자 인식의 종류

### 화자 검증(Speaker Verification)
![image](https://user-images.githubusercontent.com/19161231/47407966-69831800-d798-11e8-99d3-f2eee7c8b69b.png)
![image](https://user-images.githubusercontent.com/19161231/47408073-d0083600-d798-11e8-8dc0-23bb62664bb4.png)

화자 검증은 저장한 화자의 음성과 입력 음성 사이의 유사도(Likelihood)를 이용하여 구한다. 
즉, 저장되지 않은 목소리, 즉, 사칭 목소리와  ‘유사도 간 비율(Δ)’을 측정한다. 그리고 사칭자 대비 신뢰할 수 있는 비율에 해당하는 ‘기준값(Θ)’에 따라 화자 일치 여부를 검증하게 된다. 이러한 과정으로 시스템은 이를 통해 등록되지 않은 목소리를 구별할 수가 있게 된다.


### 화자 식별(Speaker Identification)
![image](https://user-images.githubusercontent.com/19161231/47408080-d3032680-d798-11e8-92ce-c3a28712fe18.png)
![image](https://user-images.githubusercontent.com/19161231/47408093-e0201580-d798-11e8-9fff-e671183c5c5a.png)


화자식별은 미리 N명의 화자 모델(Voiceprint)을 등록한 시스템을 이용하여 화자 식별을 한다(그림3). 특정 사람이 시스템에 음성을 입력하면, 등록된 화자 모델을 검색해 음성과 가장 일치하는 화자를 찾게 된다. 

본 프로젝트에서는 화자 식별을 이용한 화자인식을 Neural Network를 이용하여 구현하였다.

## MFCC
![image](https://user-images.githubusercontent.com/19161231/47408156-165d9500-d799-11e8-8461-8c7699ea3ee4.png)

MFCC는 Mel Frequency Cepstrum Coefficient의 약자로서 음성인식 분야에서 널리 사용되는 알고리즘이다. 
MFCC는 소리의 특징을 추출하는 알고리즘으로서 입력받은 소리를 일반적으로 20ms-40ms정도의 작은 프레임으로 쪼개는 과정을 거치고 이러한 프레임들의 스펙트럼을 분석하여 특징을 추출하는 기법이다(그림 5). MFCC를 이용한 Features 추출은 음정이 변해도 어느 정도 일정하다는 장점이 있기 때문에 음성인식에 효과적인 알고리즘이다. 그림 6은 MFCC의 전체적인 과정이다.

![image](https://user-images.githubusercontent.com/19161231/47408174-2d9c8280-d799-11e8-8c18-a75dbe8fdba7.png)
