# Event-based-data
- [Event-based Vision: A Survey](https://arxiv.org/pdf/1904.08405)

## Abstract
- 일반적인 frame camera와 event camera의 차이
  - frame camera는 고정된 속도로 이미지를 캡쳐하는 카메라
  - event camera는 픽셀 당 밝기 변화를 비동기적으로 측정하는 카메라
    - 밝기 변화의 시간, 위치 및 신호를 인코딩하는 event stream 출력
    - 바이오에서 영감을 받은 카메라
    - 마이크로 세컨드 단위의 높은 시간 해상도를 가짐
    - 140dB 대 60dB의 매우 높은 dynamic range를 가짐
    - 전력 소비가 낮고, 픽셀 대역폭이 높음 (kHz 단위)
    - 모션 블러가 줄어든다는 장점이 있음
- 논문의 목표
 - event camera의 작동원리
 - 사용가능한 실제 센서들
 - 저수준(기능 감지 및 추적, 광학 흐름)에서 높은 수준(재구축, 세분화, 인식)의 event camera 제시
 - SNN과 같은 새로운 센서를 위한 특수 프로세서를 포함하여 event를 처리하기 위해 개발된 기술에 대해 논의

### index term
- Event camera
- Bio-lnspired vision
- Asynchronous sensor
- Low latency
- High dynamic range
- Low power

## Applications
- Event camera는 실시간 상호 작용 시스템(로봇 공학, 웨어러블 전자 장치), 조명이 제어되지 않는 조건, 대기시간이나 전력이 중요한 곳에서 이점을 제공한다.
- 물체/제스처 인식, 감시 및 모니터링, 물체 추적 등에 사용됨

## Principle of operation of event cameras
- 30fps와 같이 외부 시계에 의해 지정된 속도로 전체 이미지를 획득하는 표준카메라 (frame-based camera)
- 모든 픽셀에 대해 장면의 밝기 변화에 비동기적이고 독립적으로 반응하는 DVS (event-based camera)
- 디지털 'event' 또는 'spikes'의 가변 데이터 속도 시퀀스를 카메라의 출력으로 함
- 각 event는 특정 시간에 픽셀에서 미리 정의된 크기의 밝기(로그 강도)의 변화를 나타냄

### figure.1
![image](https://github.com/mjkim0819/BCML_STUDY/assets/108729047/96ed00f6-dff2-4246-97e1-6e23450dda08)
- 이벤트 기반 동적 비전 센서(DVS)와 동일한 픽셀 배열의 프레임 기반 액티브 픽셀 센서 (APS)로 구성된 DAVIS 카메라의 요약
  - 각 픽셀에서 동일한 포토다이오드 공유
- 
