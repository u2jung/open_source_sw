# open_source_sw

# top 명령어

 + 시스템의 현재 상태를 실시간으로 모니터링 할 수 있는 도구
 + 시스템의 리소스 사용현황, 각 프로세스의 CPU 및 메모리 사용량 등을 실시간으로 보여줌

**사용법**
 + 터미널에 'top'을 입력하고 엔터

**주요옵션**
  + -d[초] : 업데이트 주기를 지정
  + -u[사용자] : 특정 사용자의 프로세스만 보여줌
  + -p[PID] : 특정 프로세스의 PID를 지정하여 해당 프로세스만 보여줌
    
**인터페이스**
  + q :'top'종료
  + h : 도움말
  + k : 프로세스 종료
  + r : 프로세스 우선순위 변경

---
# ps 명령어

 + 현재 실행 중인 프로세스 목록을 보여줌
 + 다양한 옵션을 통해 원하는 프로세스 정보를 확인

**사용법**
 + 터미널에 'ps'를 입력하고 엔터
   
**주요옵션**
 + aux : 시스템의 모든 프로세스와 그 상세 정보를 보여 줌
     1. a : 터미널에 연결된 모든 사용자 프로세스를 포함
     2. u : 사용자 기반 포맷으로 출력
     3. x : 터미널에 종속되지 않은 프로세스도 포함
 + -e 또는 -a : 모든 프로세스를 표시
 + -f : 포맷을 풀로 표시함
 + -p [PID] : 특정 PID의 프로세스를 표시함
 + -u [사용자] : 특정 사용자의 프로세스를 표시함
   ex ) ps aux : 모든 프로세스를 상세하게 표시
        ps -ef : 풀 포맷으로 모든 프로세스를 표시

---
# job 명령어

 + 현재 쉘 세션에서 백그라운드로 실행 중인 작업 목록을 보여줌
 + 백그라운드 작업 상태를 관리할 때 사용 함
   
**사용법**
 + 터미널에 'jobs'를 입력하고 엔터

**출력형식**
 + '+' : 가장 최근에 정지되거나 백그라운드에서 실행된 작업
 + '-' : 두번째로 최근 작업

**주요옵션**
 + -l : 각 작업의 PID를 함께 표시
 + -p : 각 직업의 PID만 표시
---
# kill 명령어

 + 지정한 프로세스를 종료할 때 사용
 + 프로세스 ID(PID)를 기반으로 종료 명령

**사용법**
 + 'kill [옵션][PID]'

**주요옵션**
 +  -9 : 강제 종료 시그널(SIGNAL9, SIGKILL) ex)'kill -9 1234'
 +  -15 : 기본 종료 시그널(SIGNAL 15, SIGTERM) ex)'kill -15 1234'
 +  -s [시그널 번호][PID] : 특정 시그널을 지정하여 보냄
 +  -l : 시그널 목록 표시

**기타**
 + killall[프로세스 이름] : 해당 이름의 모든 프로세스를 종료

ex )
 + 'kill 1234' : PID가 1234인 프로세스 종료
 + 'kill -9 1234' : PID가 123인 프로세스 강제종료
 + 'killall firefox' : 실행 중인 모든 'firefox' 프로세스를 종료 
  
