# gini-car
---
# 딥러닝 기반 이미지 분석을 통한 안전 운전 보조 시스템
---
## Table of Contents
+ background
+ Quick Overview
+ Description
+ reference
+ idea
+ install
+ usage
+ plus
+ Improvements
----

## background
운전자 사고가 언제 가장 많이 발생하는지 조금만 고민해보면, 대게 초보운전일 때 사고가 발생한다는 것을 알 수 있다. 실제로 미국국립보건원에 의하면 [운전자 사고, 면허취득 3개월 이내 최대치](https://terms.naver.com/entry.naver?docId=5664483&cid=60296&categoryId=60311)라고 발표하였으며, 
우리나라의 경우 운전면허의 간소화로 인해 초보운전 교통사고 비율이 상당히 높다는 것은 모두가 다 아는 사실이다. 지니카는 이 문제에 기반하여, 기술적으로 초보운전자를 보조해주고자 이 프로젝트를 시작하였다.  

(목차 제거 , 내용 수정 및 추가)

## Quick Overview
주간 주행 인식
 + 동영상 추가 
 
 (회의에서 나온대로 시각적 효과 추가)
 
 (이 창을 통해 어떤 결과물이 나왔는지 처음부터 시각적으로 강조 이후 본문에 야간, 사고 영상 추가)
 
 ## Description
카메라를 통해 얻은 비디오 데이터에서 연속적인 이미지 프레임을 추출하고 연속적인 이미지의 변화에 따른 관계 추론을 통해 주변 상황을 이해할 수 있습니다. 
예를 들어, 전방 카메라의 이미지에서 앞 차량의 크기가 커진다면 시스템은 앞 차와의 차량 간격이 가까워지고 있음을 알고 속도를 줄이게 할 수 있습니다. 
또한 우측으로 차선 변경이 필요한 경우에는 우측 앞, 뒤 차량의 크기 변화에 따라 적정 속도를 유지하며 안전하게 차선 변경을 유도할 수 있습니다.

(내용 수정 및 추가)
 
 
 ## idea
 이 프로젝트는 Temporal Relational Reasoning in Videos에서 시작 되었는데
 논문에서 소개해준 Temporal Relation Network (TRN)라는 모듈을 이용해, 기존 CNN 모델에 plug-and-play 방식으로 쉽게 활용하여
 비디오 데이터에서 시간적인 관계를 추론하고 학습할 수 있다.
 
 
 ![참고 이미지](https://user-images.githubusercontent.com/29950822/144726509-b7b8ae49-266e-4fa9-b330-e72f34dfa960.png)
 
 논문에서 2, 3, 4개의 프레임을 묶어서 CNN에 넣어 동영상의 시간에 따른 관계를 추론하는데,
 
 이 방법을 이용해 차량의 가까워짐, 멀어짐, 사고가 발생하는 순간 등을 쉽게 파악할 수 있어
 초보자가 운전을 하는데 있어서 보조의 역할로 이용한다면, 초보운전 사고를 줄일 수 있는 긍정적인 효과를 가져올것다 
 (내용 수정 및 추가)
 
 ## install
  + install 관련 코드 추가
  
 ## usage
  + 사용 방법에 관한 코드 추가 
  
 ## realization
  + 야간 주행 영상 추가
  + 사고 인식 영상 추가
 
 (loss 값을 보여 주면서 어느 정도 정확성을 보여주었는지 추가해도 좋을거 같다고 생각합니다, 혹은 사용한 모델(pretrain, rsenet 등)이 어떤것인지 소개)
 
 ## plus(적용 가능한 추가 레이블 설명 또는 추가적인 활용성)
  + 횡단보도 (보행자에 대한 label)
  + 급정거, 급발진 (위험한 상황에 대한 label)
  + 비나 눈 자연재해와 같은 레이블
  +
  
  
  
  + 사고 발생시 경고 음이 실제로 발생?
  + 

## Improvements
 + 정확도 향상
 + 추가적인 데이터의 필요성
 
## reference
[Temporal Relational Reasoning in Videos](https://arxiv.org/pdf/1711.08496.pdf)

[논문 리뷰](https://medium.com/@parkjh688/%EB%85%BC%EB%AC%B8-%EB%A6%AC%EB%B7%B0-%EA%B4%80%EC%B0%B0%ED%95%98%EA%B3%A0-%EC%B6%94%EB%A1%A0%ED%95%B4%EC%A3%BC%EB%8A%94-neural-nets-5bcadedf59cb)
 
 
