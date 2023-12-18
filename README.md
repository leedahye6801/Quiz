# 국가 자격 모의 테스트 자동 출제 시스템 개발[정보처리기사]

## 시스템 구성도
![image01](https://github.com/leedahye6801/Quiz/assets/119495348/3dc0df40-ce10-4562-9bce-41fcf6522e1d)

## 실행 환경
- 안드로이드 스튜디오
- 파이어베이스

## 실행 방법
![image02](https://github.com/leedahye6801/Quiz/assets/119495348/31f3bc89-320e-471f-86d1-8052af27f2a7)
<메인화면>
![image03](https://github.com/leedahye6801/Quiz/assets/119495348/8cb4df0e-ca34-4f67-ad12-3b1a0587ac29)
<과목 리스트 화면>
해당 과목의 유형별로 시험을 보게 된다.
![image15](https://github.com/leedahye6801/Quiz/assets/119495348/e06cd86a-23a8-45bb-8937-a77a96a22f54)
START QUIZ 버튼을 클릭시 시험이 시작된다.
![image04](https://github.com/leedahye6801/Quiz/assets/119495348/c557ad7b-b302-4eac-83c8-e481de800c63)

![image05](https://github.com/leedahye6801/Quiz/assets/119495348/6216400a-4e01-43ae-83a7-9e0e861932b8)
1. 로그인 (구글 계정)
2. 응시 과목 선택
3. START QUIZ 버튼을 통해 응시
4. 문제당 1분의 제한시간 안에 정답을 선택, 풀지 못할 때 EXT QUESTION 버튼을 통해 다음 문제로 전환( 이때, 선지를 선택할 수 없다.)
5. 결과 확인

## 동작 방법
![image06](https://github.com/leedahye6801/Quiz/assets/119495348/8a2d5602-33d4-4468-a456-c2969e7cabe9)

<전체적인 어플 화면 구성>

### 계정 데이터 저장
![image07](https://github.com/leedahye6801/Quiz/assets/119495348/5026a298-80b4-457b-a274-116f26b2c78e)
어플을 통해 구글 계정을 기반으로 로그인할 경우 파이어베이스-Authentication에 사용자의 계정
정보가 저장된다.

### 과목 리스트 데이터 저장
![image08](https://github.com/leedahye6801/Quiz/assets/119495348/e92fbee8-9f70-4e35-a3dc-961e96caf485)
파이어베이스-Storage에 과목 리스트 이미지 저장

### 문제 데이터 저장
![image09](https://github.com/leedahye6801/Quiz/assets/119495348/6a3447de-596c-45e8-9903-37cbab60b640)
![image10](https://github.com/leedahye6801/Quiz/assets/119495348/86b68f80-979b-440f-8107-64356a529f8f)
파이어베이스-Cloud Firestore에 문제 데이터를 입력했다.  
a. first: 1과목 소프트웨어 설계  
b. two: 2과목 소프트웨어 개발  
c. three: 3과목 데이터베이스 구축  
d. four: 4과목 프로그래밍 언어 활용  
e. five: 5과목 정보시스템 구축 관리  

questions 년도/회차/문제번호
기출문제를 기반으로 문제 데이터 번호를 지정하였다.  
ex) questions2011: 2020년 1회차 1번 문제

### 문제 랜덤 출제 기능
![image11](https://github.com/leedahye6801/Quiz/assets/119495348/b1b3fa0d-5b61-4fef-9eda-e03aa2fe4cc1)
![image12](https://github.com/leedahye6801/Quiz/assets/119495348/7bf9af45-849b-4c3f-af77-2368b20af80d)
랜덤으로 문제를 출제
개수는 30개로 지정하였지만 변경 가능

### 결과 데이터 저장
![image13](https://github.com/leedahye6801/Quiz/assets/119495348/8a3e5d6e-4cd9-43bb-ae59-270b52fc2410)
![image14](https://github.com/leedahye6801/Quiz/assets/119495348/dead24e8-8d7e-472e-826e-579a65bf4643)
파이어베이스\_Cloud Firestore에 과목별 결과 데이터(정답과 오답, 풀지않은 문제의 개수)가 저장된다.

## 참여자 명단
+ 송선섭
+ 이다혜
+ 한준혁
