# ossw #

### 220105 UPDATE

### LOGIC
##### 실시간 위치 표시 LOGIC ######
1. 버스 정류장마다 블루투스 모듈 설치, 버스에 블루투스 모듈 설치
2. 버스와 버스 정류장의 거리가 가까워지면 블루투스 연결 성공
   (각 정류장마다 다른 블루투스 모듈을 사용해 정류장마다 고유 숫자 반환)
▶ 반환된 숫자에 따라 지도에 버스 위치 표시

##### 잔여 좌석 표시 LOGIC #####
1. 탑승 시 NFC 태그하여 탑승자 식별,
   NFC 태그 시 1을 반환 해 1이 반환될 때마다 cnt에 누적
2. cnt를 버스 탑승 정원 수에서 차감하여 잔여 좌석 표시
3. 하차 시에도 NFC 태그 -> 이미 식별된 탑승자가 재태그를 했다면 2를 반환 
  ex) 반환 숫자가 2라면, cnt-1을 해줌
= 학생증 태그를 NFC로 대체

### 앱 구현
 1. 잔여 좌석 수 표시될 칸
  -> 아두이노를 이용해 입력되는 NFC 태그 횟수를 받아옴
 2. 현재 버스가 정차한 정류장 표시될 칸
  -> 버스 정류장마다 블루투스 모듈을 각각 설치해
      각 블루투스모듈이 연결 성공할 시 반환될 고유 숫자를 부여.
  -> 입력된 숫자 값에 따라 이전에 정차한 정류장을 앱을 통해 표시

##### 구현 계획
- 잔여 좌석 수 표시와 이전 정류장이 표시될 수 있도록 구현
-(시간이 된다면) 지도를 연동해서 실시간 위치를 지도 상에 표시 기능 추가

### 알아봐야 될 필요가 있는 것들
- 파이썬 or 자바로 앱 구현하는 방법
- 모듈을 통해 받아온 값, 즉 아두이노와 앱을 연동시키는 방법
- RFID 모듈 사용 방법 

### 오늘 한 것
RFID 모듈 이용해 사용자 식별 후 잔여좌석 수 시리얼 모니터에 출력

## -------------220106 UPDATE------------

### 앱 구현
안드로이드스튜디오 이용해 앱 개발하기로 결정

### 알아봐야 될 필요가 있는 것들
- 센서와 모듈을 통해 받아온 값, 즉 아두이노와 안드로이드 앱을 연동시키는 방법
- 학교 홈페이지에 업로드 되어있는 지도 이미지에 버스가 이동하고 있는 애니메이션 표시 방법

### 오늘 한 것

