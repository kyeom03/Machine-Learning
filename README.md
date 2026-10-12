# 딥러닝 Advanced AI를 위한 FAQ

## 목차

- [0. ResNet / Skip Connection](#0-resnet--skip-connection)
- [1. GoogLeNet / Inception Module](#1-googlenet--inception-module)
- [2. SENet / SE Block](#2-senet--se-block)
- [3. Xception / Depthwise Separable Convolution](#3-xception--depthwise-separable-convolution)
- [4. CBAM](#4-cbam)
- [5. 구조 간 비교 질문](#5-구조-간-비교-질문)
- [6. Transformer / CNN 변형 모델](#6-transformer--cnn-변형-모델)

---

## 0. ResNet / Skip Connection

1. ResNet이 등장한 배경은 무엇인가요? https://chatgpt.com/s/t_6acc36a0a258819197baa1ae7c750826
2. 네트워크를 단순히 깊게 쌓으면 왜 성능이 오히려 떨어질 수 있나요? https://chatgpt.com/s/t_6acc37f42da88191ab8d22995130328e
3. Vanishing gradient 문제란 무엇인가요? https://chatgpt.com/s/t_6acc3854a2f081919510abddcdd49758
4. Skip connection이란 무엇인가요? https://chatgpt.com/s/t_6acc38f8b6d0819191ec3e8ad071d034
5. Skip connection은 입력 x를 어떤 방식으로 다음 블록에 전달하나요? https://chatgpt.com/s/t_6acc3956c59c8191b9757965d0ef6614
6. ResNet의 기본 아이디어를 수식으로 표현하면 어떻게 되나요? https://chatgpt.com/s/t_6acc399f13ac81918925adca2791214a
7. 일반적인 CNN 블록이 H(x)를 직접 학습하는 것과 ResNet이 F(x) = H(x) - x를 학습하는 것의 차이는 무엇인가요? https://chatgpt.com/s/t_6acc39fbd3848191a3e907d62d1d6c14
8. Residual learning이 학습을 쉽게 만드는 이유는 무엇인가요? https://chatgpt.com/s/t_6acc3a6378b08191a94c18d7237acf7f
9. Skip connection이 gradient flow에 주는 장점은 무엇인가요? https://chatgpt.com/s/t_6acc3ab7de848191a4c3b951256af7ea
10. ResNet은 깊은 네트워크에서 어떤 문제를 해결하기 위해 제안되었나요? https://chatgpt.com/s/t_6acc3aeb072c8191b5c2c441848ec3ab

## 1. GoogLeNet / Inception Module

1. Inception 모듈은 무엇인가요?
2. Inception 모듈에서 여러 크기의 convolution filter를 병렬로 사용하는 이유는 무엇인가요?
3. 1x1, 3x3, 5x5 convolution을 동시에 사용하는 장점은 무엇인가요?
4. 이미지나 feature map에서 다양한 scale의 정보를 추출해야 하는 이유는 무엇인가요?
5. Inception 모듈에서 1x1 convolution은 어떤 역할을 하나요?
6. 1x1 convolution이 연산량을 줄이는 원리는 무엇인가요?
7. 1x1 convolution이 단순히 크기만 줄이는 것이 아니라 channel mixing을 수행한다는 말은 무슨 뜻인가요?
8. GoogLeNet이 깊은 네트워크임에도 파라미터 수를 상대적으로 줄일 수 있었던 이유는 무엇인가요?
9. Inception 구조와 일반적인 sequential CNN 구조의 차이는 무엇인가요?
10. Inception 모듈의 장점과 한계는 무엇인가요?

## 2. SENet / SE Block

1. SENet이 해결하려고 한 문제는 무엇인가요?
2. CNN에서 channel이 의미하는 것은 무엇인가요?
3. 모든 channel이 동일하게 중요한 것은 아니라는 말은 무슨 의미인가요?
4. SE block에서 Squeeze 단계는 무엇을 수행하나요?
5. SE block에서 Global Average Pooling(GAP)의 역할은 무엇인가요?
6. GAP을 사용하면 feature map의 어떤 정보가 압축되나요?
7. SE block에서 Excitation 단계는 어떻게 작동하나요?
8. Excitation에서 fully connected layer와 sigmoid를 사용하는 이유는 무엇인가요?
9. SE block은 각 channel에 어떤 방식으로 가중치를 부여하나요?
10. SE block이 channel attention이라고 불리는 이유는 무엇인가요?
11. SE block은 spatial 위치 정보보다 어떤 정보에 더 집중하나요?
12. SE block을 기존 CNN에 쉽게 삽입할 수 있는 이유는 무엇인가요?
13. SE block이 성능을 향상시키는 핵심 원리는 무엇인가요?
14. SE block의 한계는 무엇인가요?

## 3. Xception / Depthwise Separable Convolution

1. Xception은 어떤 모델을 기반으로 발전한 구조인가요?
2. Xception의 핵심 아이디어는 무엇인가요?
3. Depthwise separable convolution이란 무엇인가요?
4. 일반 convolution과 depthwise separable convolution의 차이는 무엇인가요?
5. Depthwise convolution은 어떤 방식으로 수행되나요?
6. Depthwise convolution에서는 channel 간 상호작용이 일어나나요?
7. Pointwise convolution이란 무엇인가요?
8. 1x1 pointwise convolution은 depthwise convolution 이후 어떤 역할을 하나요?
9. Depthwise convolution과 pointwise convolution을 분리하면 어떤 장점이 있나요?
10. Depthwise separable convolution이 연산량을 줄이는 이유는 무엇인가요?
11. Xception은 Inception 구조를 어떻게 극단적으로 해석한 모델인가요?
12. Xception에서 중간 ReLU 비선형성을 제거한 이유는 무엇인가요?
13. Depthwise separable convolution이 모바일 및 경량 모델에서 자주 사용되는 이유는 무엇인가요?
14. Depthwise separable convolution의 단점은 무엇일 수 있나요?

## 4. CBAM

1. CBAM은 무엇을 위해 제안된 모듈인가요?
2. CBAM은 어떤 두 가지 attention으로 구성되어 있나요?
3. Channel Attention Module은 무엇을 학습하나요?
4. Spatial Attention Module은 무엇을 학습하나요?
5. Channel attention과 spatial attention의 차이는 무엇인가요?
6. CBAM에서 channel attention을 계산할 때 GAP과 Global Max Pooling(GMP)을 함께 사용하는 이유는 무엇인가요?
7. GAP은 어떤 정보를 반영하고, GMP는 어떤 정보를 반영하나요?
8. CBAM에서 channel attention은 feature map에 어떻게 적용되나요?
9. Spatial attention에서는 channel 방향으로 어떤 pooling을 수행하나요?
10. Spatial attention map은 feature map의 어떤 부분을 강조하나요?
11. Channel attention을 먼저 적용하고 spatial attention을 나중에 적용하는 이유는 무엇인가요?
12. CBAM이 SE block보다 확장된 점은 무엇인가요?
13. CBAM을 사용하면 네트워크가 어떤 정보를 더 잘 선택할 수 있나요?
14. CBAM의 장점과 추가 비용은 무엇인가요?

## 5. 구조 간 비교 질문

1. ResNet, SENet, CBAM은 모두 기존 CNN에 추가하거나 결합할 수 있는 구조입니다. 각각의 목적은 어떻게 다른가요?
2. ResNet은 feature를 더 잘 선택하는 모델인가요, 아니면 학습을 안정화하는 모델인가요?
3. SENet과 CBAM은 모두 attention을 사용합니다. 두 방법의 차이는 무엇인가요?
4. SENet은 channel attention만 사용하고, CBAM은 channel attention과 spatial attention을 모두 사용합니다. 이 차이가 왜 중요한가요?
5. Inception과 Xception은 모두 효율적인 convolution 구조를 고민한 모델입니다. 두 모델의 핵심 차이는 무엇인가요?
6. Inception의 병렬 convolution과 Xception의 depthwise separable convolution은 각각 어떤 방식으로 연산 효율성을 높이나요?
7. 1x1 convolution은 Inception, Xception, SENet 계열에서 각각 어떤 역할로 사용될 수 있나요?
8. Channel attention과 1x1 convolution은 모두 channel을 다룹니다. 둘의 차이는 무엇인가요?
9. Skip connection과 attention module은 모두 성능 향상에 기여하지만, 해결하는 문제는 어떻게 다른가요?
10. CNN 모델에서 성능 향상을 위해 사용되는 전략을 크게 나누면 어떤 것들이 있나요?

## 6. Transformer / CNN 변형 모델

### 6.1 Attention 메커니즘

1. Self-Attention, Cross-Attention, Scaled Dot-Product Attention, Multi-Head Attention이란 무엇인가요?
2. Positional Encoding은 어떻게 구현하나요?
3. Look-ahead Mask를 사용하는 이유는 무엇인가요?

### 6.2 CNN과 Transformer의 구조적 차이

4. CNN과 Transformer의 가장 큰 구조적 차이는 무엇인가요?
5. CNN은 local receptive field를 기반으로 합니다. 이것이 의미하는 바는 무엇인가요?
6. Transformer의 self-attention은 CNN의 convolution과 비교했을 때 어떤 장점이 있나요?
7. Vision Transformer(ViT)에서 이미지를 patch로 나누는 이유는 무엇인가요?
8. Patch embedding은 CNN의 convolution과 어떤 점에서 유사한가요?
9. Transformer는 왜 positional encoding이 필요한가요?
10. CNN은 위치 정보를 어떻게 자연스럽게 반영하나요?
11. Transformer는 global dependency를 잘 포착하지만, CNN보다 부족할 수 있는 점은 무엇인가요?

### 6.3 CNN-Transformer Hybrid 모델

12. CNN-Transformer hybrid 모델이 등장한 이유는 무엇인가요?
13. CNN과 Transformer를 결합하면 어떤 장점을 기대할 수 있나요?
14. CNN backbone 뒤에 Transformer encoder를 붙이는 구조는 어떤 목적을 가지나요?
15. Transformer 기반 vision 모델에서도 convolution이나 local window attention을 사용하는 이유는 무엇인가요?
16. Swin Transformer에서 window attention을 사용하는 이유는 무엇인가요?
17. ConvNeXt는 Transformer의 설계 철학을 CNN에 반영한 모델입니다. 이런 접근이 의미하는 바는 무엇인가요?

### 6.4 Inductive Bias와 데이터 규모

18. CNN의 inductive bias란 무엇인가요?
19. Transformer는 CNN보다 inductive bias가 약하다고 말하는 이유는 무엇인가요?
20. 데이터가 적은 경우 CNN이 Transformer보다 유리할 수 있는 이유는 무엇인가요?
21. 데이터가 충분히 큰 경우 Transformer가 강력한 성능을 보일 수 있는 이유는 무엇인가요?
