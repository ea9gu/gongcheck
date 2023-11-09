# 📚 비가청 주파수를 활용한 수업 출석체크 앱, 공책

<br>

## 💫 공책
"공책"은 사용자의 휴대폰에서 발생하는 비가청 주파수를 이용하여 특정 공간과 시간에 있는 사람들만 출석 체크를 실시간으로 할 수 있습니다.
사용자가 해당 장소에 머물러 있어야만 출석을 인정받기 때문에 한 학생이 다른 학생을 위해 출석을 대신하거나, 임의로 출석을 조작하는 일을 획기적으로 줄입니다.

<br>

## 💫 서비스 흐름도
![image](https://github.com/ea9gu/flutter/assets/86945989/0938a18a-5359-4bb2-960c-f3c02d421cc4)

<br>

## 💫 구현 기능
<br>

### 교수용
+ 로그인 & 회원가입
<br>

+ 출석체크

![image](https://github.com/ea9gu/flutter/assets/86945989/d89ffd50-f3c6-4dcc-a961-0f46a610dc69)

<br>

+ 출석부 조회(날짜별, 학생별)

![image](https://github.com/ea9gu/flutter/assets/86945989/2a617fe5-b89a-43f2-9ac9-24764b3329a5)

<br>

+ 강좌추가

![image](https://github.com/ea9gu/flutter/assets/86945989/99b89a4b-7d0b-41a6-b14c-25f38e386cb6)

<br>

### 학생용

+ 로그인 & 회원가입

<br>

+ 출석체크

![image](https://github.com/ea9gu/flutter/assets/86945989/7901f8e3-adbe-4ac2-bc61-8de04d7e3632)

<br>

+ 출석부 조회(강좌별)

<br>

+ 기기등록

![image](https://github.com/ea9gu/flutter/assets/86945989/5b2892fc-22d1-4c45-bb05-ba0fca1c5fdb)

<br>

## 💫 시연 영상
https://youtu.be/GZO5QiaqNIw

<br>


## 💫 System Architecture

<img width="580" alt="architecture" src="https://github.com/ea9gu/server/assets/69420512/f675ffe0-1b93-47ea-a1ba-abcdca9b46fb">



## 💫 구현 API

### 로그인 & 회원가입 관련

|Method <br> |URL <br> |Description <br> |
|:---:|:---:|:---:|
|`POST`|/user/account/mylogin/|login|
|`POST`|/user/account/view_user_info/|view user information|
|`POST`|/user/account/signup/|회원 가입|
|`POST`|/user/account/password/change/|비밀번호 변경|
|`POST`|/user/account/password/reset/|비밀번호 리셋|


### 주파수 수신 & 발신 & 확인
|Method <br> |URL <br> |Description <br> |
|:---:|:---:|:---:|
|`GET`|/freq/generate-freq/|교수 출석 체크 시 주파수 생성 및 발생|
|`POST`|/freq/save-attendance/|학생 출석 체크 시 주파수 확인 및 출석 체크|


### 기기 등록 
|Method <br> |URL <br> |Description <br> |
|:---:|:---:|:---:|
|`POST`|/serial/save-device/|유효한 기기 등록|


### 수업 정보 
|Method <br> |URL <br> |Description <br> |
|:---:|:---:|:---:|
|`POST`|/class/create-and-enroll/|새로운 수업 등록|
|`POST`|/class/sutdent-course/|특정 학생이 듣는 모든 수업 정보 추출|
|`POST`|/class/prof-course/|특정 교수의 모든 수업 정보 추출|

### 출석 체크
|Method <br> |URL <br> |Description <br> |
|:---:|:---:|:---:|
|`POST`|/class/activate-signal/|수업 출석 체크 버튼 활성화|
|`POST`|/class/fix-attendance/|학생의 출석 체크를 교수가 임의로 변경 시 출석 정보 변경|

---




### 👋 Team Ea9gu

2022.09 ~ 2023.06

|김주연 <br> |김유민 <br> |장예서 <br> |
|:---:|:---:|:---:|
|Frontend<br>UI/UX|Frontend<br>UI/UX|Backend<br>DevOps|
