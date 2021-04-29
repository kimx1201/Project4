# Project4

Section 4 Project 가이드라인
소요시간 : 7 min
이번 프로젝트의 목적은

내가 설정한 포지션에서 적합한 가설을 세우고 가설을 검증해본다.
가설 검증을 위한 딥러닝 파이프라인을 구축해보는 데 의의가 있다.
(파이프라인이 완벽하지 않아도 되며, 큰 가설의 일부(곁 가지)에 대한 검증을 목표로 해도 괜찮다.
더 나아가는 방향에 대해서는 이후 프로젝트를 통해서 연계해 나가도 좋다)

1. 관심데이터 선정 Plan A, Plan B
연구자에겐 가장 어려운 주제이다. "지금 무엇을 해야 할까?"
보통 초기 연구자는 연구실(회사)에서 하던 연구방향에서 +@를 구현하는 것이 대부분이다. (석사과정, 사원급)
우리는 아직 연구소가 없다.
이런 상황에서 연구주제를 정해야 하는데, 연구주제는 떠오르지 않고, 써보고 싶은 Method만 떠오르는 것이 아직 우리의 모습이다. 그렇기 때문에 연구주제를 정하기 위해서는 내가 취직하고 싶은 회사, 그 회사의 연구/사업 내용을 골라보고, 풀고자 하는 문제와 비슷한 데이터를 찾고, 그에 맞는 기술력을 키워보는 것을 목표로 한다.

예) 현대자동차, 소카 등의 자율주행차 관련 업무를 목표로 하고 있다면, 관련 기술을 시험해볼만한 내용이 있는 지 찾아보아야 한다.
예) 카카오, 네이버 등을 목표로 한다면 음성인식, 음성생성에 대한 데이터 셋을 찾아보면 좋다.
예) 네이버 웹툰 등을 목표로 한다면, GAN등의 생성모델과 보안(fingerprint recognition) 관련 딥러닝 기술을 적용해볼 데이터를 찾는 게 좋다.
예) airbnb와 같이 숙박업에서 근무하고 싶다면, 고객데이터의 통계분석이 필요하며, 추천시스템을 적용해 볼 수 있는 데이터를 찾는 것이 좋다.

추천데이터 :
피부암 진단

넷플릭스 영화와 드라마

한국 유튜브 통계

라면 평가

목소리 성별 분류

음악 레이블 데이터셋

2. 데이터 선정 이유 (단순히 관심있어서는 No. 내 취직방향에 대해서 고민해보기)
위의 예시와 같이 내가 선정한 데이터 그리고 그 데이터를 가공하면서 얻은 지식과 경험을 "어떤 회사에서 높이 살 수 있을까?", "어디 회사의 어느부분에 적용해 볼 수 있을까"를 생각해서 기록해본다.

3. 데이터를 이용한 가설
데이터를 선정함과 동시에 데이터를 통해서 내가 무엇을 해볼 수 있을 지 가설을 세우는 것이 중요하다.
쓸모있어야 한다. 데이터기반의 사고방식 (data-driven thinking/decision)에 대한 마음가짐을 Section1-2에서 배웠다. 이번에는 그것들을 심화시켜서 진짜 필요한 기술을 찾아볼 수 있는 생각을 해보자.
실제로는 쓸모 없을지 몰라도 적어도 내 생각에는 정말 쓸모있다고 생각하면 좋다.

4. 데이터 전처리
가설을 정했다면, 데이터의 가공을 시작해본다. 바로 적용이 될 수 있는 데이터도 있겠지만, 내가 전처리를 좀 해봐야 한다.

데이터의 정규화
노이즈 제거
outlier 제거
타겟 레이블(label or Ground Truth) 생성 혹은 선택 등이 필요하다.
5. 딥러닝 방식 적용
내가 가진 문제를 굳이 딥러닝을 적용해야 하는 지 확인할 필요가 있다.
신경망 첫 시간에 엄청 큰 검을 들고 스테이크를 썰던 이미지를 기억하는가?
딥러닝의 가정 큰 장점은 어려운 문제를 더 어렵게 풀지만, 그 결과가 끝내주게 좋았을 때에 있다.
성능을 올리지 못하는 딥러닝 기술이 의미가 있을까?

6. Chance Level이 넘는 지 확인 (if not) Plan B 적용
binary 문제 (0 아니면 1인 문제)를 해결하면 chance level이 0.5(50%)이다. 하나로 찍는 머신이 있다고 가정해도 보통 50%정도는 달성하기 때문이다.
내가 만든 문제가 MNIST처럼 10개의 classification문제를 푼다고 하면 chance level이 0.1(10%)인 것이다.
가장 전통적인 ML 혹은 기본적인 신경망에 넣고 학습/테스트를 해 보았을 때 chance 수준으로 나오는 문제라면 딥러닝을 적용했을 때 과연 잘 나올 수 있을 지 반문하며, 데이터를 다시 들여다 보거나 내 가설이 틀렸을 수 있다는 것을 확인할 수 있어야 한다.

7. CV 적용하기
모델을 만들어서 어느정도 성능이 나왔다면, CV을 통해서 일반화될 가능성이 있는 지 확인해보자. 5-fold, 10-fold로 수행해보면, 일반화가 어느정도 되는지 알 수 있고, 더불어 파라미터를 변경하면서 최적화까지 해볼 수 있다.

8. Requirements.txt 만들고, 학습된 모델은 저장해보자.
내가 만든 딥러닝 모델을 단 한번만 사용하지 않을 것이기 때문에 모델을 저장하고, 또 새로운 환경에서 바로 구현할 수 있도록 Requirements.txt를 만들어보자.
언제까지 colab만 쓸 수 없기 때문이다.

9. 재구현하기
위에서 만든 Requirements.txt 를 이용하여 가상공간(conda, jupyter lab 등) 및 독립된 pc에서 같은 프로젝트를 진행해보자.
재구현이 되지 않으면, 아무도 이 결과에 대해서 믿어줄 수 없다. 따라서 재구현 할 수 있도록 Seed를 고정하는 작업을 했는 지 돌아보자.
