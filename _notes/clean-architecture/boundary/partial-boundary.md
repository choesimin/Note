---
layout: note
title: Clean Architecture - 부분적 경계
date: 2023-11-28
---



[ 서론 ]

아키텍처 경계를 완벽하게 만드는 데는 비용이 많이 들며, 유지하는데도 엄청난 노력이 필요함
    쌍방향의 다형적 Boundary 인터페이스
    Input/Output 데이터구조
    두 영역을 독립적으로 컴파일하고 배포할 수 있는 컴포넌트로 격리하는데 필요한 모든 의존성 관리

애자일 커뮤니티의 많은 사람들은 YAGNI(You are not going to need it) 원칙을 위배하는 선행적인 설계를 탐탁치 않아함
“하지만 어쩌면 필요할지도”라는 생각이 들 수 있는데, 그렇다면 부분적 경계(partial boundary)를 구현해볼 수 있음
 
 
[ 결론 ]

아키텍처 경계를 부분적으로 구현하는 간단한 3가지 방법을 살펴보았는데, 방법은 많으며 3가지는 순전히 예시임
    마지막 단계를 건너뛰기: 독립적으로 컴파일 및 배포 가능 컴포넌트로 만들고, 단일 컴포넌트에 그대로 모아둠
    일차원 경계: 양방향 Boundary 인터페이스가 아닌 한방향만 경계를 인터페이스로 격리함
    파사드: Facade 클래스에 모든 서비스 클래스를 메소드 형태로 정의하고, 호출이 발생하면 해당 서비스 클래스로 전달함


각 접근법은 완벽한 형태의 경계를 담기 위한 공간으로써 적절하게 사용할 수 있는 상황이 서로 다름
또한 각 접근법은 해당 경계가 실제로 구체화되지 않으면 떨어질 수 있음
아키텍처 경계가 언제, 어디에 존재해야 할 지 그리고 그 경계를 완벽하게 혹은 부분적으로 구현할지를 결정해야 함

클린 아키텍처를 구현해봤던 사람이라면 비용이 적지 않음을 느낄 수 있을 것이다. 책에서도 이를 알고 있고, 다양한 지름길을 소개해주고 있다. 완벽하게 클린 아키텍처를 구현하는 것은 오버엔지니어링이 될 수 있으므로, 적절히 트레이드 오프를 하도록 하자.





---




# Reference

- Clean Architecture (도서) - Robert C. Martin
- <https://phantasmicmeans.tistory.com/entry/Clean-Architecture-24-%EB%B6%80%EB%B6%84%EC%A0%81-%EA%B2%BD%EA%B3%84>
- <https://ocwokocw.tistory.com/44>