# 17. 소스코드 관리

- 소스코드 관리 시스템은 여러 기능을 함
  - 변화를 관찰하며 기록함
  - 누가 이 코드를 바꿨는가?
  - 버전의 차이는 무엇인가?
  - 이번 릴리즈에서 코드를 몇 줄 바꿨는가?
- 소프트웨어 릴리즈를 구분할 수 있음
- 롤백이 가능함
- 브랜치 관리가 가능함
- 아카이빙
- 여러 사용자가 동시에 작업이 가능함

## 소스코드 관리와 빌드

- 제품 빌드가 자동화 될 수 있음
- 반복 가능함

## 소스관리시스템을 사용하지 않는다면

- 부끄러워 하라!

# 18. 디버깅

- 아무도 완벽한 소프트웨어를 작성하지 못한다.
- 하루에 대부분을 디버깅하는데 보낼지도

## 디버깅의 심리

- 버그를 유발한 사람을 비난하기보단 문제를 해결하려 하자.

## 디버깅의 사고방식

- 한 발자국 뒤로 물러서서
- 근시를 조심하며
- 문제의 근본적인 원인을 발견하려 노력하라

## 어디에서 시작할까

- 컴파일의 경고레벨
- 정확한 관찰이 필요
- 제 삼자의 버그 보고서는 정확도가 떨어진다 -> 실제 버그 재현을 보는것도 좋은 방법
  - 버그 보고자 인터뷰가 필요: 어떤 상황에서 어떤 액션을 했을 때 버그가 발생하는지?
  - 엣지 테스트가 더 철저할 필요가 있음

## 디버깅 전략

- 데이터를 가시화하라 (디버거에서 왓쳐?)
- DDD 디버거? (뭔지 모르겠음)

## 트레이싱

- 데이터가 변화는 과정을 살펴보라
- 동시성, 이벤트 기반 프로그램이라면 트레이싱 로그가 도움이 된다

## 고무오리

- 누군가에게 설명한다.
- 설명하려면 생각만으로 지나친 것들을 알아차리게 된다.

## 제거과정

- OS, 라이브러리 등 외부 프로그램에서 버그가 있을 수 있다
- 하지만 처음부터 이런걸 가정할 필요는 없다
- '발굽모양을 보면 말부터 생각해야지, 얼룩말부터 생각하지 말자' -> 나부터 다시 확인해보자

## 놀람의 요소

- 모든 경계조건을 테스트하라
- 버그를 마주치면, 단위 테스트를 수정해야할지도 고려하라, 테스트 자체가 잘못되었을 수 있다
- 버그 유발 값이 이미 전부터 전달되었다면 매개변수 검증도 고려하라
- 버그 분석을 위한 로깅과 로깅 분석도 고려하라
- 버그를 팀원과 공유하라, 다른 팀원이 실수했거나 실수할 일을 줄인다
