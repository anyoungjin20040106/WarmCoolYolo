# WarmCoolYolo

이 프로젝트는 YOLO의 분류 기능을 활용하여 사진 데이터를 분석하고, 사용자의 피부 톤을 쿨톤 또는 웜톤으로 분류하는 딥러닝 모델입니다. 이 모델은 메이크업 추천 등 다양한 응용 프로그램에서 활용될 수 있습니다.

## 프로젝트 개요

- **목적**: 사용자 사진 데이터를 기반으로 피부 톤을 분류하여 메이크업 추천 서비스 등에 활용
- **데이터 출처**: ShowMeTheColor GitHub Repository
- **사용 기술**:
  - 딥러닝 프레임워크: YOLO
  - 프로그래밍 언어: Python

## 데이터셋

- **데이터 출처**: ShowMeTheColor에서 제공하는 이미지 데이터
- **데이터 구조**:
  - 이미지가 겨울 쿨톤, 여름 쿨톤, 봄 웜톤, 가을 웜톤으로 라벨링되어 있으며, 학습 데이터와 검증 데이터로 분리하여 사용

## 모델 구조

- **기본 모델**: YOLO를 기반으로 한 Convolutional Neural Network (CNN)
- **전이 학습**: 미리 학습된 YOLO 모델을 활용하여 학습 가속화
- **출력**: Softmax 함수를 사용하여 겨울 쿨톤, 여름 쿨톤, 봄 웜톤, 가을 웜톤으로 확률값 반환

## 주요 파일 구조

```
.
├── warmcoolmodel.pt               # 학습된 YOLO 모델 파일
├── train.ipynb            # 모델 학습 스크립트
└── README.md              # 프로젝트 설명
```

## 결과 예시

- **봄 웜톤 이미지**:
  - 모델이 90% 확률로 봄 웜톤으로 분류
- **여름 쿨톤 이미지**:
  - 모델이 95% 확률로 여름 쿨톤으로 분류
- **가을 웜톤 이미지**:
  - 모델이 90% 확률로 가을 웜톤으로 분류
- **겨울울 쿨톤 이미지**:
  - 모델이 95% 확률로 겨울울 쿨톤으로 분류

---