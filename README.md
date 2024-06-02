# 오픈소스SW개론
## readme파일 만들기 연습

### 1. top 명령어

#### 설명
top 명령어는 시스템의 실시간 성능 모니터링 도구로, 현재 실행 중인 프로세스의 정보를 실시간으로 보여줌
- 실시간으로 시스템의 CPU, 메모리 사용량 등을 모니터링
- 인터페이스 커맨드 키를 제공함
- 프로세스를 정렬하거나 필터링할 수 있음

### top 명령어를 실행한 모습
![top 명령어](https://github.com/jwchoi423/opensource/blob/main/top%20%EB%AA%85%EB%A0%B9%EC%96%B4.PNG)

![top 명령어1](https://github.com/jwchoi423/opensource/assets/115212670/ced7adc8-ec7b-424f-8dec-0d0b1d0b6071)
#### 첫 번째 줄
현재 시간, 서버가 구동된 후 지난 시간, 유저의 수, CPU가 수행하는 작업의 양의 이동 평균(1분/5분/15분)
#### 두 번째 줄
전체 프로세스의 수, 실행/대기/종료/좀비 상태의 프로세스의 수
###### 여기서 좀비 상태는 상위 프로세스가 먼저 종료되어 '/(루트)' 프로세스에 닿을 수 없는 상태의 프로세스이다.
#### %Cpu(s) 줄
이 줄들에서는 CPU 사용률과 비율을 표시한다.

us : 프로세스의 유저 영역에서의 CPU 사용률

sy : 프로세스의 커널 영역에서의 CPU 사용률

ni : 프로세스의 우선순위(priority) 설정에 사용하는 CPU 사용률

id : 사용하고 있지 않는 비율

wa : IO가 완료될때까지 기다리고 있는 CPU 비율

hi : 하드웨어 인터럽트에 사용되는 CPU 사용률

si : 소프트웨어 인터럽트에 사용되는 CPU 사용률

st : CPU를 VM에서 사용하여 대기하는 CPU 비율

#### 마지막 두 줄
![top 명령어2](https://github.com/jwchoi423/opensource/blob/main/top%20%EB%AA%85%EB%A0%B9%EC%96%B42.PNG)

Mem : RAM의 메모리 영역

Swap : 디스크를 메모리처럼 이용하는 Swap 메모리 영역
###### Swap은 일반적으로 Mem이 가득 찼을 때 사용하며, 이 영역은 디스크이므로 RAM 메모리보다 속도가 느리다.
total : 총 메모리 양

free : 사용가능한 메모리 양

used : 사용중인 메모리 양

---
### top 명령어 사용 방법 및 설명

#### 기본 top 명령어 실행
`~$ top`

#### top 명령어 -옵션
`~$ top -u [User_name]` : 특정 사용자 소유의 프로세스만 표시

#### top 내에서 커맨드 키
`Shift키 + p` : CPU 사용률 기준으로 정렬

`Shift키 + m` : 메모리 사용률 기준으로 정렬

`Shift키 + t` : 프로세스 실행 시간 기준으로 정렬

`q` : top 명령어 종료
