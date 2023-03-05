자연어 처리 분야에는 2가지 기반의 모델이 있습니다

1. 통계 기반
2. neural network 기반

이번에 읽은 A Neural Probabilistic Language Model라는 논문은 neural network 기반 언어 모델을 처음으로 제안한 논문 중 하나입니다. 이전의 언어 모델은 n-gram과 같은 통계 기반 모델이 대부분이었지만, 이 논문에서는 단어 시퀀스를 다루기 위해 신경망 모델을 사용하였습니다.

## 논문 요약
이 논문은 단어 시퀀스의 확률 분포를 추정하기 위한 뉴럴 네트워크 모델인 Neural Probabilistic Language Model (NPLM)을 제안합니다. NPLM은 단어 시퀀스를 입력받아 다음 단어를 예측하는 작업을 수행하며, 각 단어의 확률을 출력합니다. 이 모델은 단어들을 distributed representation으로 표현하고, 이를 통해 단어 간 유사도를 계산합니다. 또한, 이 모델은 n-gram 방식과는 달리 이전에 나온 모든 단어를 고려하며, 이를 위해 feedforward neural network를 사용합니다.

NPLM은 backpropagation 알고리즘을 사용해 학습되며, 학습 과정에서 noise-contrastive estimation(NCE)을 사용하여 빠른 학습을 가능하게 합니다. 실험 결과, NPLM은 기존 n-gram 모델들과 비교해 좋은 성능을 보여주며, 또한 NPLM이 학습한 distributed representation이 다른 자연어 처리 작업에서도 좋은 성능을 보인다는 것을 보여줍니다.
