# FashionMNIST_Colab — 3D어패럴캐드 ANN 실습용 노트북

금오공대 소재디자인공학과 **3D어패럴캐드** 수업(ch1.5 인공신경망 사례)에서 쓰는 Colab 노트북입니다.
TensorFlow 공식 튜토리얼 **「기본 분류: 의류 이미지 분류」 한국어판**을 그대로 보관한 것으로,
원본 링크가 바뀌거나 사라져도 수업이 끊기지 않도록 이 저장소에 사본을 둡니다.

## 열기

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/cfms-lab/FashionMNIST_Colab/blob/main/classification.ipynb)

- Colab 링크: https://colab.research.google.com/github/cfms-lab/FashionMNIST_Colab/blob/main/classification.ipynb
- 구글 계정으로 로그인한 뒤 **런타임 → 모두 실행 (Ctrl+F9)**.
  처음 실행할 때 "이 노트북은 Google에서 작성하지 않았습니다" 경고가 뜨면 **무시하고 계속하기**.
- 수정한 내용을 남기려면 **Drive로 복사** 버튼으로 내 드라이브에 사본을 만든 뒤 작업합니다.

## 실행 확인 기록

| 날짜 | Colab 환경 | 결과 |
|---|---|---|
| 2026-10-15 | Python 3.13, TensorFlow 2.21.0, CPU | 전체 셀 오류 없이 실행. 10 epoch 약 70초, 테스트 정확도 0.8862 |
| 2026-10-15 | 위와 같음, 은닉층 Dense(128)→Dense(28) | 테스트 정확도 0.8603 (수업 실습 ①) |

내년 수업 전에 한 번 더 "모두 실행"해 보고 이 표에 한 줄 추가하면 됩니다.

## 수업에서 바꿔 보는 값

| 셀 | 바꾸는 값 | 뜻 |
|---|---|---|
| `model = tf.keras.Sequential([...])` | `Dense(128, ...)`의 128 | 은닉층 노드 수 |
| `model.fit(train_images, train_labels, epochs=10)` | 10 | 전체 데이터를 반복 학습하는 횟수 |
| `img = test_images[1]` | 1 | 예측해 볼 테스트 이미지 번호 |

고친 셀부터 다시 실행: **런타임 → 셀 및 하위 셀 실행 (Ctrl+F10)**.

## 출처와 라이선스

- 원본: TensorFlow 문서 한국어 번역 저장소 `tensorflow/docs-l10n`
  `site/ko/tutorials/keras/classification.ipynb`
  (웹: https://www.tensorflow.org/tutorials/keras/classification?hl=ko)
- 노트북 코드: Apache License 2.0 (Copyright 2018 The TensorFlow Authors). 노트북 첫 셀의 라이선스 문구를 그대로 두었습니다.
- Fashion-MNIST 데이터: Zalando Research, MIT License (https://github.com/zalandoresearch/fashion-mnist)
