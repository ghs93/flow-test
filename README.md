# 2023-01-11

## 오전

- 스크럼 회의 진행
    - 오전
        - 프론트는 유저 플로우 그리기
        - 백엔드는 요구사항 명세
    - 오후
        - 프론트 와이어 프레임 작성
        - 백엔드 ERD 기획 회의(기능 명세서 작성, ERD 작성)
- 요구사항 명세 회의 진행

## 오후

- 요구사항 명세 작성
    
    [요구사항 명세 ver 1.0](./2023-01-11%2002c43243e918405b9b0926f8daf19d37/%E1%84%8B%E1%85%AD%E1%84%80%E1%85%AE%E1%84%89%E1%85%A1%E1%84%92%E1%85%A1%E1%86%BC%20%E1%84%86%E1%85%A7%E1%86%BC%E1%84%89%E1%85%A6%20ver%201%200%20a392cfb6c13f45c48c9dd5a5e7bd0f07.md)
    
- ERD 기획 회의
    
    [ERD 기획 회의](2023-01-11%2002c43243e918405b9b0926f8daf19d37/ERD%20%E1%84%80%E1%85%B5%E1%84%92%E1%85%AC%E1%86%A8%20%E1%84%92%E1%85%AC%E1%84%8B%E1%85%B4%2073c4990953234df0ad40ead4b97fa912.md)

# 2023-01-10

## 오전

- 아이디어 컨설팅
    - 웹가이버
        - 가전, 가구, 수도 등 집안 가전, 가구에 문제가 생겼을 때 무작정 출장 서비스를 부르는게 아닌 화상 상담을 통해 문제를 진단 받고 간단히 해결할 수 있는 문제는 조언을 통해 해결하며, 출장이 필요한 경우엔 화상 상담 중 바로 가능한 날짜를 협의해서 예약을 잡는 서비스
- 기능 분류
    - 웹가이버 주제가 정해진 후 필요할 것 같은 큰 기능들 분류
        - 판매자, 사용자 분류
        - 화상 상담
        - 상담 예약 서비스
        - 실시간 상담 서비스
        - 결제 시스

## 오후

- 기능 상세 분류
- 필수 기능
    
    ### 판매자
    
    1. 화상 상담
        1. 방문 여부 체크
            1. 사용자가 출장 요청 누를 시
            2. 날짜, 시작시간, 종료시간 선택
    2. 예약 내역
        1. 상담 가능한 시간 지정
            1. 요일, 시작, 종료 선택
        2. 예약 요청 접수 시 5분이내 수락/거절
            1. 5분 초과 시 자동 거절
        3. 예약 취소 기능x
        4. 데이터
            1. 예약 시간
            2. 예약자 이름
            3. 사진
            4. 타이틀
            5. 내용
            6. 수락 식별자
    3. 실시간 매칭 수락
        1. 카카오택시 매칭 처럼 가까운 순으로 수락 뜸
            1. 매칭 페이지 열고 있을 경우에만 리스트 보임
            2. 5초~10초 단위로 리프레시
            3. 보여줘야할 것들
                1. 문의 제목
                2. 문의자 아이디
                3. 문의 내용
                4. 문의 사진
                5. 위치
                6. 상담료
        2. 카톡으로 수락 url 보내줌(플러스 친구)
    4. 리뷰 페이지
        1. 사용자가 작성한 리뷰를 볼 수 있다
        2. 리뷰에 댓글
    5. 결제
        1. 상담비 O 방문결제 X
    6. 판매자 프로필 페이지
        1. 마치 github readme 
        2. 수리사례 | 리뷰 토글
        3. 표시될 데이터
            1. 프로필 이미지
            2. 상호명
            3. 대표자명
            4. 영업시간
                1. 평일, 주말, 휴무일, 공휴일 여부
            5. 사업자주소
            6. 사업자등록번호
            7. 가게 설명
            8. 상담횟수
            9. 수리사례
                1. 이미지
                2. 글
                3. 상담내역 타이틀
            10. 리뷰(+총 리뷰수)
                1. 이미지
                2. 글
                3. 아이디
                4. 별점
                5. 상담내역 타이틀
                6. 대댓글
    7. 회원가입
        1. 성명
        2. 사업자등록번호
        3. 전화번호
        4. 주민번호 앞 7자리
        5. 카테고리
        6. 지역
        7. ID
        8. Password
        9. 상세주소
        10. 상호명

### 사용자

1. 화상 상담
    1. 출장 필요 시 출장 요청 버튼 클릭
2. 예약 하기
    1. 자신 위치 설정
    2. 상담하고 싶은 시간 선택
    3. 5분이내 수락/거절 여부 확인
    4. 예약 취소 가능(1일 전까지)
3. 실시간 매칭 요청
    1. 가까운 매장부터 실시간 매칭 요청
        1. 본인이 상담료 작성
        2. 문의 제목
        3. 문의 내용
        4. 문의 사진
        5. 현재 실시간 매칭중인 상담사 수 표시(매칭거리마다 달라짐)
    2. 수락 시 카톡으로 연락(플러스 친구)
4. 리뷰 작성
    1. 이용 완료된 서비스에 대한 리뷰 작성
        1. 사진
        2. 제목
        3. 내용
        4. 별점
5. 결제?
    1. 상담 종료 시 자동 결제
6. 서비스 내역(마이페이지)
    1. 이용 내역
    2. 리뷰 관리
7. 예약 현황
8. 회원가입
    1. 카드정보 입력
    2. 전화번호
    3. 주민번호 앞 7자리
    4. 아이디
    5. 비번
    6. 이름
