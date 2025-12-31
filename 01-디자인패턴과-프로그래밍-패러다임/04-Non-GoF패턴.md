## 비-GoF 패턴 정리

> 비-GoF 패턴은 GoF 23 디자인 패턴에 포함되지는 않지만,  
> 실무·프레임워크·언어·아키텍처 수준에서 반복적으로 사용되는 설계 방식이다.

---

### 1. 아키텍처 패턴 (Architectural Pattern)
애플리케이션 **전체 구조와 레이어 분리**에 초점을 둔다.

#### MVC (Model–View–Controller)
- 애플리케이션을 Model / View / Controller로 분리
- 역할 분리를 통한 유지보수성과 확장성 향상

#### MVP (Model–View–Presenter)
- MVC에서 Controller 대신 Presenter 사용
- View와 Presenter가 1:1로 강하게 결합

#### MVVM (Model–View–ViewModel)
- ViewModel을 통해 View 추상화
- Data Binding 기반, 테스트 용이

#### Layered Architecture
- Presentation / Business / Persistence 계층 분리
- 전통적인 엔터프라이즈 구조

#### Hexagonal Architecture (Ports & Adapters)
- 외부 시스템과의 결합 최소화
- 테스트와 확장성에 유리

---

### 2. 엔터프라이즈 패턴 (Enterprise Pattern)
대규모 시스템에서 **비즈니스 로직 관리와 데이터 접근**을 구조화한다.

#### Service Layer
- 비즈니스 로직을 서비스 계층에 집중
- Controller와 도메인 로직 분리

#### Repository Pattern
- 데이터 접근 로직을 추상화
- 도메인 모델과 DB 분리

#### Data Mapper
- 객체와 데이터베이스 간 매핑 로직 분리
- ORM의 개념적 기반

#### Active Record
- 객체가 데이터 접근 책임을 직접 가짐
- 소규모 시스템에 적합

---

### 3. 의존성 관리 패턴
객체 간 **결합도를 낮추기 위한 구조적 접근**이다.

#### Dependency Injection (DI)
- 객체가 의존성을 직접 생성하지 않음
- 외부에서 주입받아 결합도 감소

#### Inversion of Control (IoC)
- 제어 흐름을 프레임워크가 담당
- DI는 IoC의 구현 방식 중 하나

---

### 4. 언어·플랫폼 특화 패턴
특정 언어의 기능을 활용한 패턴이다.

#### Module Pattern
- 모듈 단위로 코드 구성
- 전역 변수 오염 방지

#### Revealing Module Pattern
- 공개할 멤버만 노출
- JavaScript의 클로저 기반 패턴

#### Callback / Promise / Async Pattern
- 비동기 처리 흐름 제어
- JavaScript 환경에서 필수적

---

### 5. UI / 상태 관리 패턴
프론트엔드에서 **상태 흐름과 UI 업데이트**를 관리한다.

#### Flux / Redux
- 단방향 데이터 흐름
- 상태 예측 가능성 강화

#### Observer 기반 상태 관리
- 상태 변경 시 자동 UI 반영
- 반응형 UI 구조

---

### 한 줄 요약

- **비-GoF 패턴**은 객체 단위가 아닌 **시스템·레이어·플랫폼 수준의 설계 방식**
- **GoF 패턴**은 “객체를 어떻게 설계할 것인가”
- **비-GoF 패턴**은 “시스템을 어떻게 나눌 것인가”