+# 서울시 생활 정보 기반 대중교통 수요 분석 
---
## 프로젝트 개요 
- 주제 : 버스 노선 추가가 필요한 서울 시 내 자치구 선정
- 데이터 : 생활이동 정보, 버스 정보, 구별 거주 인구 정보
- 데이터 출처 : <https://data.seoul.go.kr/dataVisual/seoul/seoulLivingMigration.do>
- 목표 : 가설 수립, 단변량/이변량 분석, 검증, 인사이트 도출
---
## 데이터 소개
![image](https://github.com/user-attachments/assets/35af67dc-7174-44b2-b91b-ab0660d8f2f1)
---
## 문제 해결 프로세스 
![image](https://github.com/user-attachments/assets/9abdf435-2b47-45f9-a70c-42641c6fff1a)
---
### 가설 수립 
- 가설 1 : 총 이동인구가 많으면, 노선 추가가 필요할 것이다.
- 가설 2 : 평균 이동 시간이 긴 자치구와 인접하게 있으면 버스이용이 많아 노선이 필요할 것이다.
- 가설 3 : 상가가 많이 발달하여 승하차 평균 승객이 많으면서, 정류장이 없는 지역에 정류장 추가가 필요할 것이다.

--- 
## 단변량 분석
- **노선수**
![image](https://github.com/user-attachments/assets/6ca219c7-d3a7-490c-9766-68f675f6718a)
---
- **정류장 수**
![image](https://github.com/user-attachments/assets/cfcde39d-85ca-422e-8682-0ca769af23ea)
---
- **총 이동 인구 수**
![image](https://github.com/user-attachments/assets/a09fee3b-7288-4e32-b906-a5246c0b7ddc)
---
## 이번량 분석
- **X: 업종별(학원) -> Y: 정류장수**

![image](https://github.com/user-attachments/assets/a18ecbea-1f4e-4d67-917c-a64cdd2e1665)
---
- **X: 정류장 수 -> Y: 노선 수**
![image](https://github.com/user-attachments/assets/dead982d-cbde-4d23-b7d8-7a0447f86ab6)
---
- **X: 인구대비 이동인구 비율 -> Y: 노선 수**
![image](https://github.com/user-attachments/assets/abc7237d-6292-47d5-af3e-7c706142e96e)
---
- **관계 분석**
> - X: 업종별(학원) -> Y: 정류장수
>>PearsonRResult(statistic=0.3173004692109239, pvalue=0.12221794393316736)

> - X: 정류장 수 -> Y: 노선 수
>>PearsonRResult(statistic=0.2723983334002758, pvalue=0.18772533029186592)

> - X: 인구대비 이동인구 비율 -> Y: 노선 수
>>PearsonRResult(statistic=0.5126875030156735, pvalue=0.008779215599459614)


> - Y와의 관계를 그룹으로 정리
>>강한 관계의 x : 인구대비 인동 인구 비율 -> 노선수

>>중간 관계의 x : 세대당 인구 수 -> 승차 승객 수

>>약한 관계의 x : 업종별(학원) -> 정류장수
---
## 가설 검증 과정 
![image](https://github.com/user-attachments/assets/70c7f84d-8ac1-437b-9201-bb84eb0d4b1e)

- 학원가에는 정류장 수가 많을 것이라고 생각하였지만, 관계가 있지만, 강한 관계를 가지지 않는다.

- 정류장 수와 노선 수는 비례 관계가 있을 것이라 생각하였지만, 서로 강한 관계를 가지지 않는다.

- 인구 대비 이동인구의 비율과 노선 수는 관계가 있으며, 서로 강한 관계를 갖는다.
---
## 결론
![image](https://github.com/user-attachments/assets/5741a83d-2b7a-42ca-a53d-0f20d4bf0d20)
![image](https://github.com/user-attachments/assets/6c999830-b072-4952-82a4-c57d6a68f662)
> 관계들을 정리하여 보았을 때, 인구 대비 이동 인구와 노선수의 비율 계산해보면 **성북구, 동작구, 구로구** 의 순서로 나온 것을 확인할 수 있다. 인구 대비 이동 인구 수가 많다는 것은 외부 지역에서 유입과 유출이 많다는 것을 의미한다. 이는 노선의 밀집도가 높다는 것을 의미한다. 또한 실제 성북구에서 강남을 가기 위해서는 여러 번의 환승이 필요한 것을 확인할 수 있다. 이러한 점들을 해결하기 위하여 성북구에 노선의 추가 증설이 필요하다.


