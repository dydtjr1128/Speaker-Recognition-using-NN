# Speaker-Recognition-using-NN(화자 인식)
Speaker Recognition using Neural Network &amp; Linear Regression

## 화자 인식의 종류

### 화자 검증(Speaker Verification)
<p align="center">
  <img src="https://user-images.githubusercontent.com/19161231/47408492-946e6b80-d79a-11e8-8ae1-8d118cbd65da.png">
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/19161231/47408073-d0083600-d798-11e8-8dc0-23bb62664bb4.png">
</p>
`화자 검증`은 저장한 화자의 음성과 입력 음성 사이의 유사도(Likelihood)를 이용하여 구한다. 
즉, 저장되지 않은 목소리, 즉, 사칭 목소리와  ‘유사도 간 비율(Δ)’을 측정한다. 그리고 사칭자 대비 신뢰할 수 있는 비율에 해당하는 ‘기준값(Θ)’에 따라 화자 일치 여부를 검증하게 된다. 이러한 과정으로 시스템은 이를 통해 등록되지 않은 목소리를 구별할 수가 있게 된다.


### 화자 식별(Speaker Identification)
<p align="center">
  <img src="https://user-images.githubusercontent.com/19161231/47408080-d3032680-d798-11e8-92ce-c3a28712fe18.png">
</p>
<p align="center">
  <img src="https://user-images.githubusercontent.com/19161231/47408093-e0201580-d798-11e8-9fff-e671183c5c5a.png">
</p>
`화자식별`은 미리 N명의 화자 모델(Voiceprint)을 등록한 시스템을 이용하여 화자 식별을 한다(그림3). 특정 사람이 시스템에 음성을 입력하면, 등록된 화자 모델을 검색해 음성과 가장 일치하는 화자를 찾게 된다. 

본 프로젝트에서는 화자 식별을 이용한 화자인식을 Neural Network를 이용하여 구현하였다.




## MFCC
<p align="center">  
  <img src="https://user-images.githubusercontent.com/19161231/47408767-984ebd80-d79b-11e8-9665-f6d895348234.png" width="60%">
</p>

`MFCC`는 Mel Frequency Cepstrum Coefficient의 약자로서 음성인식 분야에서 널리 사용되는 알고리즘이다. 
MFCC는 소리의 특징을 추출하는 알고리즘으로서 입력받은 소리를 일반적으로 20ms-40ms정도의 작은 프레임으로 쪼개는 과정을 거치고 이러한 프레임들의 스펙트럼을 분석하여 특징을 추출하는 기법이다. MFCC를 이용한 Features 추출은 음정이 변해도 어느 정도 일정하다는 장점이 있기 때문에 음성인식에 효과적인 알고리즘이다. 아래의 그림은 MFCC의 전체적인  과정이다.
사람마다 개개인의 고유한 DNA 및 지문을 가지고 있듯이, 각 사람마다 목소리의 고유 주파수, 진폭 등이 다르다는 특성(MFCC)을 이용하여 개인의 신분을 확인 할 수 있는 화자 인식이 가능하다.

<p align="center">  
  <img src="https://user-images.githubusercontent.com/19161231/47408769-98e75400-d79b-11e8-9599-93cc7bdb9b67.png" width="70%">
</p>

## Project Structure
<p align="center">
  <img src="https://user-images.githubusercontent.com/19161231/47409509-ec5aa180-d79d-11e8-9edf-c1c2de89a80a.png">
</p>

## Data Collection
<center>
  <table align="center">
    <tr>
      <th> Folder name </th>
      <th> Name </th>
      <th> Number of data </th>
    </tr>
    <tr>
      <td>0</td>
      <td>유인나</td>
      <td>20</td>
    </tr>
    <tr>
      <td>1</td>
      <td>배철수</td>
      <td>20</td>
    </tr>
    <tr>
      <td>2</td>
      <td>이재은</td>
      <td>20</td>
    </tr>
    <tr>
      <td>3</td>
      <td>최일구</td>
      <td>20</td>
    </tr>
    <tr>
      <td>4</td>
      <td>문재인</td>
      <td>20</td>
    </tr>
  </table>
</center>
