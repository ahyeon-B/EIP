# 기억장치 관련 용어

### 스레싱(Thrashing)

- 프로세스 처리 시간보다 페이지 교체 시간이 더 많아지는 상태
- 전체 시스템 성능 저하 -> 다중 프로그래밍 다발 시 스래싱 발생
- 방지 방법

  1. 다중 프로그래밍 적정 수준 유지
  2. 일부 프로세스 중단
  3. 페이지 부재 빈도 조절
  4. 워킹 셋 유지

---

### 지역성(Locality)

- 프로세스 실행 간 주기억장치 참조 시 일부 페이지만 집중 참조
- 시간 구역성
  - 한 페이지를 일정 시간동안 집중적으로 액세스
  - 반복/순환(Loop), 스택(Stack), 부 프로그램(Sub Routine)
- 공간 구역성
  - 프로그램 실행 시 인접한 페이지들도 집중 참조
  - 배열순회(Array Traversal), 순차적 코드 실행

---

### 워킹 셋(Working Set)

- 일정 시간동안 자주 참조하는 페이지들을 주기억장치에 상주시켜 페이지 부재 및 교체 현상을 최소화
- 기억장치 사용 안정화

---

### 페이지 부재

- 프로세스 실행 중 필요한 페이지가 주기억장치에 누락(부재)
