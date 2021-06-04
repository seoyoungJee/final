# Manners Maketh Man
### Members    
강하영, 강진, 김해린, 지서영, 유수정
    

## 1. Introduction 
해당 프로젝트는 **모션인식을 이용한 어린이 언어습관 교정 게임**이다. 어린이가 존댓말, 감사표현 등 상황에 맞는 언어 습관을 구사할 수 있도록 모션 인식 기술을 이용해 게임으로 재미있게 공부할 수 있도록 돕는다. 빙고게임이라는 게임 포맷을 사용함으로써 어린이가 빙고판을 채워나가는 성취감을 주어 학습효과를 더욱 향상시키고자 한다.   


## 2. Background & Objective

### 2.1 Target User
> 6-7세의 어린이를 대상으로 함. 초등학교 입학 전 필요한 올바른 언어에 대한 학습을 할 수 있는 프로그램이므로 미취학 아동 중 글을 읽을 수 있는 나이인 6-7세의 어린이로 설정했다. 

### 2.2 Their Problems
>바른 언어습관 형성을 위해서는 공동체 속에서 학습하는 것이 필요하다. 과거에는 대가족을 형성해 많은 가족 구성원이 함께함으로써 예절을 배울 기회가 많았다면 현재는 점점 핵가족화 되어가 예절교육에 소홀해지는 경향이 있고, 더욱이 현재 Covid-19와 같은 펜데믹상황이 발생하여 사회적 거리두기로 인해 공동체를 이루는 것이 어려워졌다. 따라서 어린이들이 다양한 상황에 따른 바른 언어 습관을 형성할 수 있도록 돕는 새로운 방법을 고안했다.
### 2.3  Project Goal
>Kinect V2와 pygame을 이용한 모션인식 게임을 통해 어린이가 직접 몸을 움직이면서 다양한 상황에 해당하는 올바른 언어예절을 학습을 할 수 있는 빙고게임을 개발한다.


## 3. Main Function
### 3.1 Bingo Game
1. 3x3 빙고판을 채우는 것이 과제다. 각각의 빙고 칸마다 각기 다른 스토리로 언어예절 게임이 존재한다.
2. User가 선택한 칸에 해당하는 게임의 문제를 읽고 지시사항대로 모션을 취한다.  
  
<img src="/image/빙고판.PNG" width="50%" height="50%"><img src="/image/게임.PNG" width="50%" height="50%">  
  
3. 정답맞추기에 성공하면 정답화면으로 넘어간다.
4. 빙고판에 동그라미가 표시되고 같은 방식으로 다른 게임들을 진행해 빙고판을 완성한다.  

<img src="/image/정답.PNG" width="50%" height="50%"><img src="/image/빙고판2.PNG" width="50%" height="50%">
### 3.2 Motion in Game
1. Kinect V2 카메라를 통해 사람 몸의 Joint를 인식한다.  
2. 게임별로 사용되는 Joint가 각각 다른데 미리 설정한 Joint가 정해진 위치에 닿으면 정답 유무를 인식하는 알고리즘을 적용한다.
3. 이를 통해 여러 정답 선택지들을 마우스가 아닌 Body Joints를 사용해 정답을 선택한다.  
Ex) 손, 팔꿈치, 무릎, 머리 등  

<img src="/image/손.PNG" width="50%" height="50%"><img src="/image/무릎.PNG" width="50%" height="50%">

## 4. Demonstration Video

## 5.설치 단계
### 5.1 Kinect for Windows SDK v2 설치

설치 과정 
[Microsoft Download Center](https://www.microsoft.com/ko-kr/download/)에서 설치 파일 [Kinect for Windows SDK v2](https://developer.microsoft.com/ko-kr/windows/kinect/)을 다운 받는다. 
<img src="/image/download(1).png" width="50%" height="50%">

최신버전 사용을 추천합니다.

시스템 요구 사항:

지원되는 운영 체제 (Embedded 8 Standard, Windows8, Window 8.1)(사용자:Window10, 64-bit)
- 권장 하드웨어 구성 : 64-bit (x64) 프로세서 / 4 GB 메모리 (이상) / Physical dual-core 3.1 GHz (2 logical cores per physical) 이상 프로세서 /  Kinect for Windows v2 센서 전용 USB 3.0 controller*/ DX11 capable graphics adapter** / 전원 허브 및 USB 케이블이 포함 된 Microsoft Kinect v2 케이블

<img src="/image/kinect%20hardware.png" width="50%" height="50%">

- Softerware 요구 사항:
  - Visual 2012 또는 [Visual Studio2013](https://www.microsoft.com/ko-kr/download/details.aspx?id=40784) 

설치 진행 순서 상세 :
  1. kinect 센서가 컴퓨터 USB 포트에 연결되어 있지 않은지 확인합니다.
  2. 다운로드 위치에서 KinectSDK_v2.0_1409-Setup.exe를 두 번 클릭합니다.

<img src="/image/download%20(2).png" width="50%" height="50%"><img src="/image/download%20(3).png" width="50%" height="50%">

  4. 설치가 완료되면 Kinect 센서가 전원 허브에 연결되어 있고 전원 허브가 콘센트에 연결되어 있는지 확인합니다. 전원 허브의 USB 케이블을 PC의 USB 3.0 포트에 연결합니다. 드라이버 설치가 자동으로 시작됩니다.
  5. 드라이버 설치 후 장치 관리자를 실행하여 확인할 수 있으며 장치 목록에 "KinectSensor Device"가 존재합니다.

<img src="/image/download(4).jpeg" width="50%" height="50%"><img src="/image/download(5).jpeg" width="50%" height="50%">

<img src="/image/download(6).jpeg" width="50%" height="50%">

  6. 실행된 Kinect for Window에 위와 같이 체크가 되어 있어야 합니다. (USB Controller의 느낌표가 표시되어 있지만 사용하는데 문제는 없습니다.)
  7. 설치가 완료되었습니다.
