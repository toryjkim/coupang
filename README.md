# coupang 클론코딩 과제

## 목표

데레사 강사님께서 공유해주신 쿠팡 로그인 페이지 디자인을 참조해서 똑같은 사이트를 만들어보기

## 만들며 고려헀던 부분

1. 컨벤션: html, css를 작성할 때도 협업 및 추후 코드를 지속적으로 관리하기 위한 컨벤션이 있는지 알아보았습니다. 
=> 쿠팡의 로그인 페이지 소스코드를 검사해서 최대한 따르려 노력했습니다.
  - member라는 클래스 이름이 지속적으로 등장한다. 쿠팡 개발자만의 약속인듯 한데 어떤 의미를 가지고 있는지 정확하게 파악하지는 못했지만 페이지의 기능상 핵심 키워드를 뽑아서 클래스의 공통 이름으로 사용하는 것이라 유추했습니다. 로그인 기능을 보여주는 페이지이기 때문에 고객을 memeber로 표현해서 거의 모든 class 이름에 member가 포함되어 있습니다.
  - 페이지 내에서 하나의 커다란 기능을 단위로 분류했을 때 container가 최상위에 위치합니다.(ex. modal-container, member-container)
  - container 내부에 분할된 레이어가 존재합니다. (ex. member-header, member-main, member-footer)
  - 필요하다면 분할된 레이어를 wrapper로 감싸줍니다.(ex. member-wrapper : member-wrapper는 member-header, member-main, member-footer를 감싸는 wrapper입니다.)  
  ![image](https://user-images.githubusercontent.com/39623897/114306421-f3fd9480-9b16-11eb-855a-7272857ce1ee.png)
  - 독립적으로 사용하지 못하고 꼭 어딘가에 속해야 하는 요소들은 `부모__자식`으로 작명합니다. (ex. login__form login 이라는 독립적인 블록 아래  form 이라는 비독립적 요소가 딸려있습니다.- BEM 작성규정을 참조했습니다.)
  - 클래스로 css를 적용하지 않더라도 html을 구조화하기 위해 div 태그를 사용한다.


2. 쿠팡 코드를 분석하며 특이했던 부분:
  - 링크가 걸려있는 로고를 작성할 때, a 태그의 배경으로 coupang 이미지가 삽입되어있고 그 내부 요소로 img 태그를 다시 한번 작성해서 두 개의 겹쳐진 로고 이미지를 생성하고 있습니다.(왜 두개를 겹쳐놨는지 이유는 모르겠습니다.)  
    ![image](https://user-images.githubusercontent.com/39623897/114309996-1a75fc80-9b24-11eb-871b-925de6e81e04.png)

