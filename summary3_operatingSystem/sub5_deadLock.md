# 교착 상태

### 정의

- 둘 이상의 프로세스들이 서로 점유하고 있는 자원을 요구하며 무한정 대기하고 있는 상태

---

### 교착 상태 필요 충분 조건

1. **상호 배제(Mutual Exclusion)** : 한 번에 한 개의 프로세스만이 공유 자원을 사용
2. **점유 및 대기(Hold and Wait)** : 최소한 하나의 자원을 점유하면서 다른 프로세스에 할당된 자원을 추가로 점유하기 위해 대기하는 프로세스 존재
3. **비선점(Non-preemption)** : 다른 프로세스에 할당된 자원은 끝날 때까지 강제로 선점 불가
4. **환형 대기(Circular Wait)** : 프로세스들이 원형으로 구성되어 있어 앞/뒤 프로세스 자원을 요구

---

### 교착상태 해결 방법

1. **예방(Prevention)**
   * 교착발생 4가지 조건 중 하나 이상을 사전에 제거하여 예방
2. **회피(Avoidance)**
   * 발생된 교착상태를 적절히 피해가는 방법
   * 은행원 알고리즘 : 은행에서 모든 고객의 요구가 충족되도록 현금을 할당하는 데서 유래
3. **발견(Detection)**
   * 교착상태에 있는 프로세스 및 자원을 발견/점검
4. **회복(Recovery)**
   * 교착상태 유발 프로세스 종료
   * 프로세스 내 할당된 자원 선점
