강남대학교 데이터사이언스 전공 캡스톤디자인II 졸업작품

## 프로젝트 요약

### 1. 배경 

에브리타임 커뮤니티에는 학교에 관한 질문에 대답할 수 있는 AI챗봇 제작


### 2. 주최/주관

- 주최 : 강남대학교 산업데이터사이언스학부
- 주관 : 강남대학교 산업데이터사이언스학부

### 3. 데이터

- 데이터 : 에브리타임 게시글, 댓글, 공감수, 날짜 데이터

### 4. 일정 (UTC+ 9 (한국) 기준)

- 기간 : 2020년 9월 01일 00:00 ~ 2020년 11월 25일 18:00
- 학술제 : 2020년 11월 26일 ~ 12월 16일

## Change log

#### 1 ~ 5주차
* 졸업작품 신청서 작성
* 졸업작품 계획서 작성

#### 5주차 
* EDA : 데이터를 시각화 하여 탐색
* Data Processing : 한글을 제외한 특수기호 영어 숫자 등 제거
                    Konlpy를 이용한 명사, 동사, 형용사 추출
                    Tf-idf 를 통한 벡터화 및 Randomforest로 예측
                    
* Data Labeling : 강남대학교 사전 8개 구축 (0 - 기타, 1 - 행정, 2 - 교양, 3 - 교필, 4 - 복지, 5 - 경영, 6 - 글로벌, 7 - ict, 8 - 사범대)
                  사전단어가 2개 이상 있는 경우 질문으로 분류

#### 6주차
* 모델을 이용해 카테고리로 분류한 질문에 관련 단어가 나오면 미리 답변을 하는 봇을 제작
* 제대로 분류를 하지 못함 - data processing 다시 진행

#### 7주차
* EDA를 다시한번 진행 - 공감수가 많을수록 질문이 아니며 문장 길이가 길수록 질문이 아님
* data labeling에 조건을 추가 - 공감수가 2개 이상, 문장 길이가 140 이하는 label에서 제외 '?'이 들어간 문장을 찾음
* 모델을 decision tree, randomforest, xgboost를 사용한 결과 xgboost의 성능이 우수
* 
#### 8주차
* 불균형 클래스를 해결하기 위해 SMOTE 알고리즘을 통한 오버샘플링 진행 - 정확도 증가
* gridsearchcv를 통한 최적의 하이퍼파라미터 찾기, K-Fold 교차검증을 통해 일반화
* confusion metrix를 통해 모델평가 - 정밀도, 재현율, F1score 측정

#### 9주차
* AWS에 머신러닝 모델을 이용해 flask 웹서버 구축
* flutter로 채팅 UI 구축후 웹서버와 연동


