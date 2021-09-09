### 영화 리뷰 속 스포일러 찾기
해당 프로젝트는 'IMDB 영화 스포일러 데이터셋'에서 스포일러가 포함된 영화 리뷰를 찾아내는 딥러닝 모델을 만드는 프로젝트 입니다. 리뷰 기능이 있는 영화 OTT 서비스에는 영화 재생 버튼 아래 영화 정보와 리뷰가 바로 노출되어 있는 경우가 많습니다. 고객들은 스포일러가 포함된 리뷰를 보기 원치 않을수도 있고, 보게되면 영화 보는 것을 꺼리게 될 수도 있습니다. 이를 방지하기 위해 자연어 처리를 이용해 스포일러가 포함된 리뷰를 걸러낼 수 있는 모델을 만들어보고자 했습니다. Word2Vec으로 사전 훈련된 벡터를 임베딩하고 ManhattanLSTM(이하 MaLSTM)을 활용해 모델을 생성했습니다.   


#### 데이터셋
IMDB Spoiler Dataset(Can you identify which reviews have spoilers to improve user experience?
https://www.kaggle.com/rmisra/imdb-spoiler-dataset?select=IMDB_reviews.json
