초안 작성 참고: [글쓰기 초안 작성하기](https://jwleepro.github.io/document_manage/writing_simple_bestpractice.html)

# 데이터 웨어하우스(Data Warehouse)와 데이터 레이크(Data Lake)
1. 글의 목적을 한 문장으로 정한다.
   > “이 글을 다 읽은 사람이 딱 하나만 기억한다면 무엇을 기억했으면 좋겠는가?”
   - 이 글의 목적은 데이터 웨어하우스와 데이터 레이크의 특징을 파악하고 용도에 맞게 쓰기 위해서다
   - 이 글을 읽은 사람은 데이터 웨어하우스와 데이터 레이크를 어떤 상황에서 사용할 것인지 설명할 수 있었으면 좋겠다
<br>

2. 독자가 읽고 나서 무엇을 이해해야 하는지 정한다.
   > Data Warehouse와 Data Lake는 왜 따로 존재하는가? 와 같은 질문을 4개만 만들어 보자
   1. 둘 다 데이터를 저장하는데 왜 Data Warehouse와 Data Lake를 구분해서 사용하는가?
   2. Data Warehouse, Data Lake는 어떤 상황에서 필요한가?
   3. Data Warehouse, Data Lake를 같이 사용할 수 있는가?
   4. Data Warehouse와 Data Lake는 각각 무엇을 잘하고 무엇을 잘하지 못하는가?
   5. 운영 DB, Data Warehouse, Data Lake를 함께 사용하는 간단한 예시는 무엇인가?
<br>

3. 조사한 자료에서 핵심 질문을 뽑는다.
   > 자료를 질문에 연결하기
   1. 둘 다 데이터를 저장하는데 왜 Data Warehouse와 Data Lake를 구분해서 사용하는가?

      **답변:**  
        [내가 생각하는 핵심 답]  
      Data Warehouse는 사전에 사용 목적과 구조를 정하고 저장해서 조회나 분석에 강점이 있고,  
      Data Lake는 다양한 형태의 데이터를 먼저 저장하고, 나중에 사용 목적과 구조를 결정할 수 있다.  
      따라서 서로 다른 목적에 최적화되어 있기 때문에 구분해서 사용한다.
      <br>  
        [설명에 필요한 내용]  
      - Data Warehouse는 기간별 양품 수량, 불량률, 설비 온도와 같이 사전에 정해진 양식의 데이터를 대용량으로 저장한다.
      
 
---
## 참고자료
