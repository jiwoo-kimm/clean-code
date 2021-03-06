# 2장 | 이상한 나라의 객체
🔥 소프트웨어 설계에서의 객체

<br>

## 💻 객체, 그리고 소프트웨어 나라

### 객체

- 객체란 **식별 가능한 개체 또는 사물**이다.
- 객체는 **구체적인 사물**일 수도 있고 **추상적인 개념**일 수도 있다.
- 객체는 구별 가능한 __식별자__, 특징적인 __행동__, 변경 가능한 **상태**를 가진다.
- 소프트웨어 안에서 객체는 저장된 상태와 실행 가능한 코드를 통해 구현된다.

### 상태

- 상태를 이용하면 과거의 모든 행동 이력을 기억하지 않고도 행동의 결과를 쉽게 예측할 수 있다.
- 상태는 특정 시점에 객체가 가지고 있는 **정보의 집합**으로 객체의 **구조적 특징**을 표현한다.
- 상태는 단순한 값과 객체의 조합으로 표현할 수 있다.
  - **프로퍼티(property)**: 객체의 상태를 구성하는 모든 정적인 특징
    - **링크(link)**: 객체 사이의 의미 있는 연결
    - **속성(attritbute)**: 객체를 구성하는 단순한 값
  - **프로퍼티 값(property value)**: 시간에 따라 변화하는 동적인 값

### 행동

- 행동은 외부의 요청 또는 수신된 메시지에 응답하기 위해 동작하고 반응하는 활동이다.
- 행동의 결과로 객체는 **자신의 상태를 변경**하거나 **다른 객체에게 메시지**를 전달할 수 있다.
- 객체는 행동을 통해 다른 객체와의 **협력**에 참여하므로 행동은 **외부에 가시적**이어야 한다.

### 캡슐화

- 객체는 **상태**를 외부로 노출하지 않는다.
- 객체가 외부에 노출하는 것은 **행동**뿐이며, 외부에서 객체에 접근할 수 있는 유일한 방법 역시 행동뿐이다.
- 상태를 잘 정의된 행동 집합 뒤로 캡슐화하는 것은 객체의 자율성을 높이고 협력을 단순하고 유연하게 만든다.

### 식별자

- 식별자는 어떤 객체와 다른 객체를 구별하는 데에 사용되는 특정한 프로퍼티다.
- **단순한 값**, 즉 객체가 아닌 것은 식별자를 가지지 않는다. 따라서 **동등성(equality)** 을 검사한다.
- **객체**는 상태가 변경될 수 있기 때문에 식별자를 통한 **동일성(identical)** 을 검사한다.

<br>

## 💻 행동이 상태를 결정한다.

- 객체를 설계할 때 **상태보다는 행동**에 초점을 맞춰야 한다.
- 어플리케이션에 필요한 **협력**을 생각하고, 협력에 참여하는데 필요한 **행동**을 생각한 후, 행동을 수행할 **객체**를 선택하는 방식으로 설계해야 한다.

<br>

## 💻 은유와 객체

- 객체지향은 현실의 **모방**과 **추상화**라기 보다는, **은유(metaphor)** 라고 할 수 있다.
- 소프트웨어 객체는 현실 객체가 가지지 못한 **능동적**인 능력을 추가로 보유하게 된다.
- 객체지향 설계는 현실의 구조와 특성을 정확하게 반영하거나 현실에 한정지어질 필요가 없다.

<br>

## 📝 느낀점

객체를 설계할 때 상태가 아닌 행동과 책임을 중심으로 생각해야 한다는 것을 제대로 느낄 수 있었다. 나는 여태 객체가 가져야 할 값들을 UML로 표현하고 그에 따라서 클래스를 설계했다. 그 후 기능을 생각하고 구현하기 시작하면서 코드를 적는 방식으로 프로그램을 설계해왔던 것이다. 이 때 실제로 작업할 때도 느꼈지만, 이런 방식으로는 객체의 행동을 거시적으로 바라 보기가 어렵기 때문에 결국 협력에도 적합하지 않은 객체가 탄생하게 된다. 따라서 앞으로 어플리케이션을 만들 때는 *협력*, *행동*, 그 다음 *상태* 순서로 생각하고 설계를 하도록 노력해야겠다.
