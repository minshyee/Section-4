# VaccinePass_Sentiment
2022년 1월, 정부가 방역 패스에 대한 조건을 변경, 새로 실시 하면서 방역 패스가 뜨거운 감자로 자리매김하였습니다.
## 1. Goal
뜨거운 감자였던 코로나 백신 패스에 관한 여론의 실태 조사 </br>
" 찬성자와 반대자의 진짜 비율은? " </br> </br>
현 시행에 대한 여론의 동향을 파악하고, </br>
후에 새로운 대안에 대한 근거 데이터로 사용이 가능할 정도의 신뢰도 있는 결과를 도출하는 것 </br>
## 2. Process
- Crawling
- Labeling
- Modeling
- Analysis

## 3. Data Set
[Total Data] 47089 rows × 1 columns 
- selenium을 사용한 naver news crawler
- 수만휘, Orbi 청소년 커뮤니티 댓글 수집
- 수작업으로 소수의 데이터 라벨링
    - 긍정 : 1 / 부정 : 2 / 중립 : 0 
    - Train Labeling Data (1208 * 2)

## 4. Modeling

[최종 모델] </br>
Korean BERT (Bidirectional Encoder Representations from Transformers)

<img src="https://user-images.githubusercontent.com/50479962/175188662-8d5cf8c0-32d3-4512-bb26-2b9c221aa87c.png" width="200" height="200"/>


|chennel Level|Best Train|Best Test|
|---|---|---|
|0.33|0.8718|0.8473|

## 5. Limit 
- 모집단의 한계, 표본도 너무 부족
- 댓글 데이터의 불균형성 (찬성댓글 극히 드뭄)
- labeling Data의 개수 부족

## 6. Plan to
- nltk vador를 이용 점수 계산? -> labeling
- 현재 이슈로 변경, 모델 비교 실험 추가
- 
