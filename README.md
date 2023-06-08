# errorGuide
## 2023/06/08

- ORA-01950 : 테이블스페이스 'USERS'에 대한 권한이 없습니다.
![image](https://github.com/EunJi9739/errorGuide/assets/133085347/9dcd18bf-828a-4425-9081-99a55175b231)
    - 발생 경로
        - 국비 과정 통합구현 시험 연습 중 ARC에서 API 테스트할 때 발생.
    - 해결 방법
        - ALTER USER 유저명 DEFAULT TABLESPACE USERS QUOTA UNLIMITED ON USERS;
    - 원인
        - 사용하고 있는 DB 계정에 생성 권한은 있으나, 할당량 권한이 주어지지 않아서 발생한 문제.
