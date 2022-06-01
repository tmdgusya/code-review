# Basic

## Log
- [ ] 로그 메세지만 보고 어떤 사유로 일이 진행되었거나, 예외가 발생했는지 알수 있는가? 
    - [ ] 개발자 말고 다른 사람도 행위를 추측할 수 있는 메세지인가?
- [ ] 로그를 파일 시스템으로 저장할 수 있게 만들었는가?
    - [ ] 저장할 수 있도록 만들었다면 저장 용량이 넘쳤을때 계획 혹은 몇일 단위로 보관할것인지 보관 정책은 수립했는가?
- [ ] 로그 메세지를 쉽게 보기 위한 모니터링 툴을 만들었는가?
    - [ ] 만들었다면 현재 예외가 발생했을때 검색하기 쉬운 구조인가?

# Spring Boot

# JPA

- [ ] JPA 변경감지의 원리에 대해서 알고 있는가?
    - [ ] 만약 EqualsAndHashCode 를 사용했다면 변경감지에 대한 부분을 생각했는가?
    - [ ] 어떤 상황에 동작하는가?

- [ ] `@Transactional` 어노테이션을 알고 있는가?
    - [ ] 읽기만 하는 부분에서 `readOnly` 옵션을 주고 있는가?
        - [ ] readOnly 옵션을 넣었을때 어떻게 다른지 아는가?
            - [ ] flush 가 안된다고 답변했다면 flush 는 무엇인지 아는가?
                - [ ] flushMode 에 대해서 아는가?
                
    - [ ] 동일 class 내에서 `@Transactional` 어노테이션이 작동하는가?
        - [ ] 만약 작동하지 않는다면 작동시킬 수 있는 방법이 있는가?
            - [ ] 작동시켰다면 그것이 Constructor Injection 일때의 문제는 없는가?

- [ ] 쓰기 지연 저장소에 대해서 아는가?
    - [ ] 어떤 쿼리들이 쓰기 지연 저장소에 저장되는지 아는가?
        - [ ] 어느시점에 쓰기 지연 저장소에 있는 쿼리가 쏘아지는지 아는가?

        - [ ] 쓰기지연저장소 구현체를 본적있는가?
            - [ ] 어떻게 쓰기 지연 저장소에 쿼리들이 저장되는지 구조를 아는가?

- [ ] Persistence Context 에 대해 알고 있는가?
    - [ ] 1차 캐시 2차 캐시를 알고 있는가?
        - [ ] 그렇다면 아래 상황에서 쿼리가 어떻게 발생할 것 같은가?
            ```java
            @Entity
            class Person {

                @Id
                Long id;

                @Column
                String name;

            }

            @Service
            class Service {

                private final PersonRepository personRepository;

                @Transactional
                public void test() {
                    Person person = personRepository.findByName("roach");

                    Person person2 = personRepository.findByName("roach");
                }

            }
            ```

- [ ] Paging 을 알고 있는가?
    - [ ] Paging Query 가 생성해주는 쿼리가 최적화된 쿼리라고 생각하는가?
        - [ ] 아니라면 어떻게 최적화 할 수 있는지 아는가?
    - [ ] offset 방식 (무한스크롤 또는 더보기) 방식에 대해서 알고 있는가?
        - [ ] 이를 구현하는 방법을 아는가?

- [ ] 
    